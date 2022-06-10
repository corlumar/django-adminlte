# [AdminLTE](https://appseed.us/generator/adminlte/) Django

Open-source **Django Dashboard** generated by `AppSeed` op top of an iconic design. For newcomers, **[AdminLTE](https://appseed.us/generator/adminlte/)** is one of the best open-source admin dashboard & control panel theme. Built on top of Bootstrap, `AdminLTE` provides a range of responsive, reusable, and commonly used components. 

- 👉 [AdminLTE Django](https://appseed.us/product/adminlte/django/) - product page
- 👉 [AdminLTE Django](https://adminlte-django.appseed-srv1.com/) - LIVE deployment
- 👉 [Complete documentation](https://docs.appseed.us/products/django-dashboards/adminlte) - `Learn how to use and update the product`
  - ✅ [Set up the environment](https://docs.appseed.us/products/django-dashboards/adminlte#environment)
  - ✅ [Manage App users](https://docs.appseed.us/products/django-dashboards/adminlte#manage-app-users)
  - ✅ [Application Bootstrap Flow](https://docs.appseed.us/products/django-dashboards/adminlte#application-bootstrap-flow)
  - ✅ [App Routing](https://docs.appseed.us/products/django-dashboards/adminlte#project-routing)
  - ✅ [UI Assets and Templates](https://docs.appseed.us/products/django-dashboards/adminlte#ui-assets-and-templates)
  - ✅ [Set up the MySql Database](https://docs.appseed.us/products/django-dashboards/adminlte#set-up-the-mysql-database)
  - ✅ [Adding a new app](https://docs.appseed.us/products/django-dashboards/adminlte#adding-a-new-app)
  - ✅ [Static Assets for production](https://docs.appseed.us/products/django-dashboards/adminlte#static-assets-for-production)  
  
<br />

> Built with [AdminLTE Generator](https://appseed.us/generator/adminlte/)

- Timestamp: `2022-05-30 20:42`
- Build ID: `899eeced-3754-4f36-90b0-129d0982601d`
- **Free [Support](https://appseed.us/support/)** (registered users) via `Email` and `Discord`

<br />

> Features

- `Up-to-date dependencies`
- Database: `sqlite`
- UI-Ready app, Django Native ORM
- `Session-Based authentication`, Forms validation

<br />

![AdminLTE - Full-Stack Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/168842202-9b80a957-a375-4e6d-8247-2cc459267a86.png)

<br />


## ✨ Start the app in Docker

> **Step 1** - Download the code from the GH repository (using `GIT`) 

```bash
$ # Get the code
$ git clone https://github.com/app-generator/django-adminlte.git
$ cd django-adminlte
```

<br />

> **Step 2** - Edit `.env` and remove or comment all `DB_*` settings (`DB_ENGINE=...`). This will activate the `SQLite` persistance. 

```txt
DEBUG=True

# Deployment SERVER address
SERVER=.appseed.us

# For MySql Persistence
# DB_ENGINE=mysql            <-- REMOVE or comment for Docker
# DB_NAME=appseed_db         <-- REMOVE or comment for Docker  
# DB_HOST=localhost          <-- REMOVE or comment for Docker 
# DB_PORT=3306               <-- REMOVE or comment for Docker
# DB_USERNAME=appseed_db_usr <-- REMOVE or comment for Docker
# DB_PASS=<STRONG_PASS>      <-- REMOVE or comment for Docker

```

<br />

> **Step 3** - Start the APP in `Docker`

```bash
$ docker-compose up --build 
```

Visit `http://localhost:5085` in your browser. The app should be up & running.

<br />




## ✨ How to use it

> Download the code 

```bash
$ # Get the code
$ git clone https://github.com/app-generator/django-adminlte.git
$ cd django-adminlte
```

<br />

### 👉 Set Up for `Unix`, `MacOS` 

> Install modules via `VENV`  

```bash
$ virtualenv env
$ source env/bin/activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Database

```bash
$ python manage.py makemigrations
$ python manage.py migrate
```

<br />

> Start the app

```bash
$ python manage.py runserver
```

At this point, the app runs at `http://127.0.0.1:8000/`. 

<br />

### 👉 Set Up for `Windows` 

> Install modules via `VENV` (windows) 

```
$ virtualenv env
$ .\env\Scripts\activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Database

```bash
$ python manage.py makemigrations
$ python manage.py migrate
```

<br />

> Start the app

```bash
$ python manage.py runserver
```

At this point, the app runs at `http://127.0.0.1:8000/`. 

<br />

### 👉 Create Users

By default, the app redirects guest users to authenticate. In order to access the private pages, follow this set up: 

- Start the app via `flask run`
- Access the `registration` page and create a new user:
  - `http://127.0.0.1:8000/register/`
- Access the `sign in` page and authenticate
  - `http://127.0.0.1:8000/login/`

<br />

## ✨ Code-base structure

The project is coded using a simple and intuitive structure presented below:

```bash
< PROJECT ROOT >
   |
   |-- core/                               # Implements app configuration
   |    |-- settings.py                    # Defines Global Settings
   |    |-- wsgi.py                        # Start the app in production
   |    |-- urls.py                        # Define URLs served by all apps/nodes
   |
   |-- apps/
   |    |
   |    |-- home/                          # A simple app that serve HTML files
   |    |    |-- views.py                  # Serve HTML pages for authenticated users
   |    |    |-- urls.py                   # Define some super simple routes  
   |    |
   |    |-- authentication/                # Handles auth routes (login and register)
   |    |    |-- urls.py                   # Define authentication routes  
   |    |    |-- views.py                  # Handles login and registration  
   |    |    |-- forms.py                  # Define auth forms (login and register) 
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>         # CSS files, Javascripts files
   |    |
   |    |-- templates/                     # Templates used to render pages
   |         |-- includes/                 # HTML chunks and components
   |         |    |-- navigation.html      # Top menu component
   |         |    |-- sidebar.html         # Sidebar component
   |         |    |-- footer.html          # App Footer
   |         |    |-- scripts.html         # Scripts common to all pages
   |         |
   |         |-- layouts/                   # Master pages
   |         |    |-- base-fullscreen.html  # Used by Authentication pages
   |         |    |-- base.html             # Used by common pages
   |         |
   |         |-- accounts/                  # Authentication pages
   |         |    |-- login.html            # Login page
   |         |    |-- register.html         # Register page
   |         |
   |         |-- home/                      # UI Kit Pages
   |              |-- index.html            # Index page
   |              |-- 404-page.html         # 404 page
   |              |-- *.html                # All other pages
   |
   |-- requirements.txt                     # Development modules - SQLite storage
   |
   |-- .env                                 # Inject Configuration via Environment
   |-- manage.py                            # Start the app - Django default start script
   |
   |-- ************************************************************************
```

<br />

## ✨ PRO Version

> For more components, pages and priority on support, feel free to take a look at this amazing starter:

Soft UI Dashboard is a premium Bootstrap 5 Design now available for download in Django. Made of hundred of elements, designed blocks, and fully coded pages, Soft UI Dashboard PRO is ready to help you create stunning websites and web apps.

- 👉 [Soft UI Dashboard PRO Django](https://appseed.us/product/soft-ui-dashboard-pro/django/) - Product Page
- 👉 [Soft UI Dashboard PRO Django](https://django-soft-ui-dashboard-pro.appseed-srv1.com/) - LIVE Demo

<br >

![Soft UI Dashboard PRO - Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/170829870-8acde5af-849a-4878-b833-3be7e67cff2d.png)

<br />

---
[AdminLTE](https://appseed.us/generator/adminlte/) Django - Open-source starter generated by **[AppSeed Generator](https://appseed.us/generator/)**.
