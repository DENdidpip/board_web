# Flask Blog Application

A simple blog web application built with **Flask**, **SQLAlchemy**, and **SQLite**. The project allows users to register, create articles, edit them, view posts, and delete articles.

## Features

* User registration with unique username and email validation
* Create new blog articles
* View all articles on the homepage
* Read individual articles
* Edit existing articles
* Delete articles
* SQLite database integration using SQLAlchemy
* Simple HTML templates rendering with Jinja2

## Technologies Used

* Python 3
* Flask
* Flask-SQLAlchemy
* SQLite
* SQLAlchemy ORM
* HTML/CSS (Templates)

## Database

The application uses SQLite as the database engine.

The database file:

```text
dtbs.db
```

Tables are created automatically on the first application launch:

```python
with app.app_context():
    db.create_all()
```

## Routes

| Route                  | Description                 |
| ---------------------- | --------------------------- |
| `/`                    | Login page                  |
| `/sign_up`             | User registration           |
| `/home`                | Main page with all articles |
| `/about`               | About page                  |
| `/create-article`      | Create a new article        |
| `/posts/<id>`          | View article details        |
| `/change-article/<id>` | Edit article                |
| `/delete-article/<id>` | Delete article              |

## Models

### User

```python
class User(db.Model):
    id
    nick
    email
    password
```

### Article

```python
class Article(db.Model):
    id
    title
    intro
    text
    date
```

