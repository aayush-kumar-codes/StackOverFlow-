## StackOver Flow - Clone

<a href="https://github.com/Yawan-1/StackOverFlow--Clone/stargazers"><img alt="GitHub stars" src="https://img.shields.io/github/stars/Yawan-1/StackOverFlow--Clone"></a>
<a href="https://github.com/Yawan-1/StackOverFlow--Clone/blob/master/LICENSE"><img alt="GitHub license" src="https://img.shields.io/github/license/Yawan-1/StackOverFlow--Clone"></a>
<img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/Yawan-1/StackOverFlow--Clone">
![python3.x](https://img.shields.io/badge/python-3.x-brightgreen.svg)

Clone of Stack Overflow where I implemented nearly all of its functionalities. My intention was to provide insight and demonstration to developers on the inner workings of Stack Overflow - including how tasks are performed <b style="color:lightgreen">behind the scenes</b> and how queries are executed..

> Note: Please have a look at the Blog explaining <a href="https://yawan-1.github.io/">What I learned from this Project?</a>

## Demo

Here is a working live demo : <a href="https://stonkoverflow.herokuapp.com/">Demo</a> <b>(Removed from heroku because usage of so's production LOGO</b>)</b>

## Technology Stack

* [Python 3.7.x](https://www.python.org/)
* [Django Web Framework 3.2.x](https://www.djangoproject.com/)
* [Redis 5.x](https://pypi.org/project/django-redis/)
* [BootStrap 4](https://getbootstrap.com/)
* [Jquery 3](https://api.jquery.com/)
* [Postgresql 14](https://www.postgresql.org/)


## Functionalities


* 50+ Badges are implemented to award
* 20 Privileges to Earn
* Track Badges
* Reputation Awarding
* Privilege and Activity Notifications
* Live Q&A MarkDown Preview
* User @mentioning in comments
* Create and award Bounties
* <code>Threading</code> to keep track of the remaining days of Bounty.
* Reviewing Tasks :
  * First Question Review
  * First Answer Review
  * Late Answer Review
  * Review Flag Posts
  * Review Flag Comments
  * Review Close Votes
  * Review ReOpen Votes
  * Review Low-Quality Posts
  * Review Suggested Edits


* And much more. You can find list of all functionalities <a href="https://github.com/Yawan-1/StackOverFlow--Clone/blob/759157fc68f59398d9352ddd705eee396336bb81/Functionalities.md">Here</a>


## Setup Commands

Clone this repository

1. Clone this project using
````
$ git clone https://github.com/Yawan-1/StackOverFlow--Clone
````

For Postgresql usage*, you will need to download and install it.

1. Download Postgresql from [this Link](https://www.postgresql.org/download/)
2. After installation, create Database in postgresql shell using these commands
   1. `CREATE DATABASE so_clone;`
   2. `CREATE USER so_clone_user WITH PASSWORD 'password';`
   3. `GRANT ALL PRIVILEGES ON DATABASE so_clone TO so_clone_user;`
3. and fill **database name** , **database password** and **user** in `settings.py` like

  ````
  DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'so_clone',
        'USER': 'so_clone_user',
        'PASSWORD': 'password',
        'HOST': 'localhost',
        'PORT': '',
    }
}
  ````

_*Note: If you are setting up this project using sqlite, you have the option to bypass the postgresql installation step. To do so, please consider commenting out the postgresql configuration and uncommenting the sqlite configuration._



Now run make <code>migrations</code> command, running make migrations command will perform Data Migrations to save the "Badges" in the database.
then migrate to load the operations of Data Migrations in database.
````
$ python manage.py makemigrations
$ python manage.py migrate
````
> [Migration Operations](https://docs.djangoproject.com/en/3.2/ref/migration-operations/) will be automatically created on migration creation to save Tags and Tag Badges.

Then, simply run the server using this command.
````
$ python manage.py runserver
````

## Deployment

The following details and steps on how to deploy this application

#### Heroku

See detailed [Deploying django app on Heroku](https://devcenter.heroku.com/articles/django-app-configuration)


## Contributing

If you have any question or issues, It may have bugs that i may have missed. You can create <a href="https://github.com/Yawan-1/StackOverFlow--Clone/pulls">Pull request</a>.

Note: <small>Frontend and complete design is also inside this project's repo (html, css).</small>

