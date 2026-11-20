# ClassroomHub

Educational Django site backed by MySQL/MariaDB. It has a public catalog of learning resources, account signup, login and logout, a private dashboard, and a catalog review page restricted to a group by permission.

## Versions

- Python 3.15 (tested on Windows)
- Django 6.1.3
- MariaDB (tested with 13.0.2 and 13.1.1). Django 6.1 requires MariaDB 10.11+ or MySQL 8.4+.

## Setup

1. Create and activate a virtual environment, then install dependencies:

   ```
   py -m venv .venv
   .venv\Scripts\activate
   py -m pip install -r requirements.txt
   ```

2. Create the database and a SQL account (replace `CHANGE_ME`):

   ```sql
   CREATE DATABASE classroom_hub CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
   CREATE USER 'classroomhub_user'@'localhost' IDENTIFIED BY 'CHANGE_ME';
   CREATE USER 'classroomhub_user'@'127.0.0.1' IDENTIFIED BY 'CHANGE_ME';
   GRANT ALL PRIVILEGES ON classroom_hub.* TO 'classroomhub_user'@'localhost';
   GRANT ALL PRIVILEGES ON classroom_hub.* TO 'classroomhub_user'@'127.0.0.1';
   GRANT ALL PRIVILEGES ON test_classroom_hub.* TO 'classroomhub_user'@'localhost';
   GRANT ALL PRIVILEGES ON test_classroom_hub.* TO 'classroomhub_user'@'127.0.0.1';
   ```

3. Copy `.env.example` to `.env` and set the same password. Never commit `.env`.

4. Apply migrations and create an administrator:

   ```
   python manage.py migrate
   python manage.py createsuperuser
   ```

## Run

```
python manage.py check
python manage.py runserver
```

## Routes

| Route | Access |
| --- | --- |
| `/` | Public home page |
| `/resources/` | Public catalog |
| `/about/` | Public |
| `/accounts/signup/` | Public signup (regular accounts only) |
| `/accounts/login/` | Public login |
| `/accounts/logout/` | POST only; GET returns 405 |
| `/dashboard/` | Requires login |
| `/resources/review/` | Requires login and `pages.view_resource` (403 otherwise) |
| `/admin/` | Staff only |

## Reviewer group

In Django Admin, open Groups and create `Catalog reviewers` with the permission `pages | resource | Can view resource`. Then open a user and add it to the group. Reviewers do not become staff.

## Tests

```
python manage.py test pages
```

Tests run against a separate database, `test_classroom_hub`, so the SQL account needs privileges on it.

## Not included

- Public create, edit and delete for resources.
- Password reset by email, OAuth, multi-factor authentication.
- Production settings.