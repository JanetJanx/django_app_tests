[![Coverage Status](https://coveralls.io/repos/github/JanetJanx/django_app_tests/badge.svg?branch=master)](https://coveralls.io/github/JanetJanx/django_app_tests?branch=master)

## Documentation

We shall install using the following commands:

python3 -m pip install -r requirements.ini

<!-- Start django project -->

python3 -m django startproject mytest

<!-- creates django application -->

python3 -m django startapp users
python3 manage.py makemigrations
python3 manage.py migrate
python3 -m coverage run --source=mytest --omit='_tests_,_migrations_,_admin_,_mytest_' -m py.test -v --tb=native
