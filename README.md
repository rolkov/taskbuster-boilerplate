# Overview
This is an implementation of the [TaskBuster Django Tutorial](http://www.marinamele.com/taskbuster-django-tutorial)

# Configuration Management
- Python 3.6
- Other packages see in [requirements.txt](./requirements.txt)

# Accounts & Links
- Git & GitHub
  - user: ...
  - primary email (private): ...+git@gmail.com
  - password: _Közepes_ 1
- GitHub
  - repository: https://github.com/rolkov/garnetcal.git
- Django superuser
  - username: ...
  - email: ...@gmail.com
  - password: _Közepes_ 1
- Google OAuth client
  - Name: GarNetCal client 1
  - ID: 758573345906-2mf2fgu1o0ml888416dci56n4u88gp9h.apps.googleusercontent.com
  - Secret:  PdihV7B0LaX1gYnicw35eK_s
- PythonAnywhere
  - username: garnetcal
  - email: ...+garnetcal@gmail.com
  - password: _Közepes_ 1
  - web: http://garnetcal.pythonanywhere.com/
- PythonAnywhere superuser
  - username: ...
  - email:  ...+garnetcal@gmail.com
  - password: _Közepes_ 1
  - web: http://garnetcal.pythonanywhere.com/admin

# Environment Initialization Step
Install geckodriver
```shell
[local machine command-line]
$ mkvirtualenv --python=python3.6 taskbuster_dev
(taskbuster_dev) $ pip install django
(taskbuster_dev) $ pip install flake8
(taskbuster_dev) $ pip install flake8-docstrings
(taskbuster_dev) $ pip install hacking
(taskbuster_dev) $ deactivate
$ mkvirtualenv --python=python3.6 taskbuster_test
(taskbuster_test) $ pip install django
(taskbuster_test) $ pip install --upgrade selenium
(taskbuster_test) $ deactivate
$ workon taskbuster_dev
(taskbuster_dev) $ django-admin.py startproject taskbuster .

```

- [ ] venv CL: `pip freeze >> requirements.txt`
- [ ] CL: `git init`
- [ ] CL: `git config --global user.name `_`default`_
- [ ] CL: `git config --global user.email `_`default`_`+git@gmail.com`
  Create .gitignore:
    *.pyc
    *~
    __pycache__
    myvenv
    db.sqlite3EADME.
    /static
  Create empty new repo garnetcal on GitHub and use repo's https clone URL
  CL: git remote add origin https://github.com/rolkov/garnetcal.git
  CL: git push -u origin master

Django Project Setup
  venv CL: django-admin startproject calsite .
  Add to calsite/settings.py after STATIC_URL: STATIC_ROOT = os.path.join(BASE_DIR, 'static')
