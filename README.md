# capstone-projects-news-app
Breaking News App:


What goal will your website be designed to achieve? 

This is a simple news app with a variety of categories and topics. Also adding weather data on site. Users can view the latest news across different places, different topics like sports, entertainment, worldwide news, politics, finance, covid-data, etc.



What kind of users will visit your site? In other words, what is the demographic of your users? 

In general all the users can visit the site. Users who wants to check the latest and trending news



What data do you plan on using? You may have not picked your actual API yet, which is fine, just outline what kind of data you would like it to contain.

I am using news api-https://newsapi.org/ For weather data api-http://api.openweathermap.org Also adding covid data with api: https://covid-19-statistics.p.rapidapi.com



What kinds of issues might you run into with your API? 

Using just a simple and free api, for news I am getting data of title, image, content, date created at, etc.


Is there any sensitive information you need to secure? 

Each user can create an account or can check in as a guest. To sign up, users need to add name, username and password.


What functionality will your app include? 

Simple app, navbar at the top with sign up and login button. Also users can login as guests if they don't want to sign up. App will be using javascript, axios, flask, python, prosql database, api, bootstrap, etc.



What features make your site more than CRUD? Do you have any stretch goals?

Adding with signup/login/logout features with adding comments, like and share button for news content.


What will be the user flow looks like?

-Landing Page
  -Top News story/search news
  -Register
  -Login
    -Views News with different catogories/search news
    -Post new News/delete post
    -Comments on different News/delete comments
     
## Getting Started

This is a Capstone Projects for News App using Python, Flask, News Api, SQLAlchemy, WTForms, Postgres Database, Javascript, Bootstrap, Ajax, etc.

### Installing Dependencies

#### Python 3.7+

Follow instructions to install the latest version of python for your platform in the [python docs](https://docs.python.org/3/using/unix.html#getting-and-installing-the-latest-version-of-python)

#### Virtual Enviornment

Instructions for setting up a virual enviornment for your platform can be found in the [python docs](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/)

> Create virtual environment by running `python3 -m venv venv`

> - Then activate it by running `source venv/bin/activate`
> - Install all your dependencies on this env using `pip freeze > requirements.txt`
> - To deactivate the env run `deactivate`

#### PIP Dependencies

Once your virtual environment setup and running, install dependencies by naviging to the `/backend` directory and running:

```bash
pip3 install -r requirements.txt
```

This will install all of the required packages within the `requirements.txt` file.

##### Key Dependencies

- [Flask](http://flask.pocoo.org/)  is a backend framework. Flask is required to handle requests and responses.

- [SQLAlchemy](https://www.sqlalchemy.org/) and [Flask-SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/en/2.x/) are libraries to handle the sqlite database. We can view in  `./src/database/models.py`. 


## Running the server

First make sure you are working using your created virtual environment.

Each time you open a new terminal session, run:

```bash
export FLASK_APP=app.py;
```

On windows you should run this command instead:

```bash
set FLASK_APP=app.py;
```

To run the server, execute:

```bash
flask run 
```



## Deploy the application on heroku

To depoloy your application follow this document => [Deploy an application on Heroku](https://github.com/DinaTaklit/HerokuSample/blob/master/README.md).

1. `hroku login`to loggin into heroku
2. Update requirements.txt each time you add dependency `pip freeze > requirements.txt`
4. Install **Gunicorn**  => `pip install gunicorn`
5. Create `Procfile`:  `web: gunicorn app:app` 
6. Your file structure should contains those files
  
  ```bash
  .gitignore
  app.py
  models.py
  forms.py
  Procfile
  requirements.text
 
  ```
  
7. Crete heroku app => `heroku create name_of_your_app`
8. Add git remote for heroku to local repo.  => `git remote add heroku heroku_git_url` 
9. Add postgresql add on for your database => `heroku addons:create heroku-postgresql:hobby-dev --app name_of_your_application`
10. Push from git to heroku => `git push heroku main`

And that is it all. Congratulation, now we have a live app 


###Base URL
Base URL: We can be run locally and it is hosted also as a base URL using heroku (http://sanam-breaking-news-app.herokuapp.com/). The backend app is hosted at the default, `http://127.0.0.1:5000/`, 

### Endpoints

- GET '/news'
- GET '/covid'
- GET '/business'
- GET '/health'
- GET '/technology'
- GET '/science'
- GET '/jobs'
- GET '/military'
- GET '/stocks'
- GET '/pets'
- GET '/travel'
- GET '/fitness'
- GET '/bitcoin'
- GET '/entertainment'
- GET '/sports'
- GET '/animals'
- GET '/tech'
- GET '/weather'
- GET '/beauty'
- GET '/search'
- GET '/post-news'
- GET '/post-news/{post_id}'
- POST '/search'
- POST '/post-news/add'
- POST '/post-news/{post_id}/comment'
- PATCH '/post-news/{post_id}'
- PATCH '/post-news/{comment_id}'
- DELETE '/post-news/{post_id}'
- DELETE '/post-news/{comment_id}'

