# CUSTOMERVIDEOSERVICEDJANGO by soufiane radouni

$ git clone https://github.com/soufiane-radouni/DJANGO-VIDEO-APP-SERVICE.git

$ cd DJANGO-VIDEO-APP-SERVICE

# Create a virtualenv (Optional but reccomended)
$ python3 -m venv myvirtualenv

# Activate the virtualenv
$ source myvirtualenv/bin/activate (Linux)

# Install all dependencies
$ pip install -r requirements.txt

#Set environment variables. Make sure to replace the values with your own environment settings.

 export DEBUG=True
 export SECRET_KEY='super secret key'
 export DATABASE_URL='postgresql://user:passwd@localhost/videodjango'
 export TWILIO_ACCOUNT_SID='ACxxxxxxxxxxxxxxxxxxxx'
 export TWILIO_AUTH_TOKEN='ACxxxxxxxxxxxxxxxxxxxx'

#Create database and schema.

 createdb videodjango
 python manage.py syncdb

#Run the app.

 python manage.py runserver

Open web browser and head to http://localhost:8000/ to see your local app running.

             # DEPLOYING TO HEROKU 

    heroku create
    heroku addons:add heroku-postgresql

    heroku config:set SECRET_KEY='something super secret'
    heroku config:set TWILIO_ACCOUNT_SID='ACxxxxxxxxxxxxxxxx'
    heroku config:set TWILIO_AUTH_TOKEN='xxxxxxxxxxxxxxxxxxx'
    heroku config:set DATABASE_URL='postgresql://user:passwd@localhost/videodjango'
    
   

    git push heroku master

    heroku run python manage.py syncdb



