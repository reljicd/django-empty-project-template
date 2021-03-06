# Django Template

## About

This is a demo project for practicing Django.

It was made using **Python 3.6** + **Django** and database is **SQLite**.
**Bootstrap** was used for styling.
Testing is done using **untitest** module.

There is a login and registration functionality included.

App is covered with tests.

## Prerequisites

\[Optional\] Install virtual environment:

```bash
$ python -m virtualenv env
```

\[Optional\] Activate virtual environment:

On macOS and Linux:
```bash
$ source env/bin/activate
```

On Windows:
```bash
$ .\env\Scripts\activate
```

Install dependencies:
```bash
$ pip install -r requirements.txt
```

## How to run

### Default

You can run the application from the command line with manage.py.
Go to the root folder of the application.

Run migrations:
```bash
$ python manage.py migrate
```

Initialize data:
```bash
$ python manage.py loaddata users
```

Run server on port 8000:
```bash
$ python manage.py runserver 8000
```

#### Helper script

It is possible to run all of the above with helper script:

```bash
$ chmod +x scripts/run.sh
$ scripts/run.sh
```

### Docker

It is also possible to run the myapp app using docker:

Build the Docker image:
```bash
$ docker build -t reljicd/django-myapp -f docker\Dockerfile .
```

Run the Docker container:
```bash
$ docker run --rm -i -p 8000:8000 reljicd/django-myapp
```

#### Helper script

It is possible to run all of the above with helper script:

```bash
$ chmod +x scripts/run_docker.sh
$ scripts/run_docker.sh
```

## Post Installation

Go to the web browser and visit `http://localhost:8000/home`

Admin username: **admin**

Admin password: **adminpassword**

User username: **dusan**

User password: **dusanpassword**

## Helper Tools

### Django Admin

It is possible to add additional admin user who can login to the admin site. Run the following command:
```bash
$ python manage.py createsuperuser
```
Enter your desired username and press enter.
```bash
Username: admin_username
```
You will then be prompted for your desired email address:
```bash
Email address: admin@example.com
```
The final step is to enter your password. You will be asked to enter your password twice, the second time as a confirmation of the first.
```
Password: **********
Password (again): *********
Superuser created successfully.
```

Go to the web browser and visit `http://localhost:8000/admin`

### Tests

Running tests:
```bash
$ python manage.py test myapp
```
