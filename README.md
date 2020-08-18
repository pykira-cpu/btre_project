# Real Estate Website
### This is a website for the fictional real estate company BT Real Estate. Check here for **[website](http://64.227.23.221/)**.

Created using:

* *Python*
* *Django*
* *HTML*
* *CSS*
* *Bootstrap*
* *PostgreSQL*
* *Gunicorn*
* *Nginx*

### Functionalities of the website

- The website uses Python's Django framework combined with PostgreSQL to allow users to admin the content of the website. Admin users can add, delete and edit details of property listings and the realtors associated with the listings. Property enquiries can also be viewed.


- Website visitors can view, search and inquire for a property. Registered users have their inquired properties saved in the database (which they can view on their dashboard) and cannot inquire for a property more than once. Once a user inquires about a property, the company and the realtor associated with the property are informed via email.

### Deploying it on DigitalOcean Ubuntu 18.04 droplet

- The project's development environment was enclosed in a 'virtual environment' to isolate project files and library dependencies ensuring there would be no clashes with the libraries contained on the local machine. All requirements were tested locally including a local instance of the database before deploying the website on a Digital Ocean Linux Ubuntu droplet. The droplet was protected by SSH authentication and was accessed using PuTTy.

- Gunicorn was used in combination with Nginx to replace Django's local deployment functionality and instead deploy the website globally. The website can be accessed using the IP address of the Linux droplet. 

### Run it in your local machine
            
        git clone https://github.com/nsnakhil/btre_project.git

**Make sure you have installed Django and postgres in the environment(virtual or local) your working!**

Before running migrations, make changes to:
 
- SECRET_KEY : ' 
- ALLOWED_HOSTS : []
- DATABASES : 'change usernmae, password and dbname to the ones you create on postgresDB'
- DEBUG : True
- EMAIL_* : 'To yours'

### Run Migrations

        python manage.py makemigrations
        python manage.py migrate

### Create super user
        python manage.py createsuperuser

### Create static files
        python manage.py collectstatic

### Run server
        python manage.py runserver
