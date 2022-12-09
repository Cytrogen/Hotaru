<div align="center">
  <img src="/static/icons/Hotaru.png" width=30%>
</div>

<br>

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10.7-orange">
  <img src="https://img.shields.io/badge/Flask-2.2.2-black">
</div>

<div align="center">
  <a href="/docs/cn.md">中文</a> | <a href="README.md">ENG</a>
</div>

# Hotaru

<details>
  <summary>Directory</summary>
  
- [Hotaru](#hotaru)
      - [Video Demo:](#video-demo)
  - [Description](#description)
    - [Guide](#guide)
  - [Design](#design)
</details>

#### Video Demo: NOT YET

## Description

Hotaru is a web-based ~~instant messaging~~ social platform, using Flask framework and SQLite.
> **Hotaru has NOT YET used Socket.IO to implement instant messaging.**

This is the Final Project for CS50.

## Guide

1. Configure your Email address:
   ``` Python
   # app.py
   # This Email address will be used to send Emails to the users
   # Such as sending verification link
   app.config['MAIL_SERVER'] = ''
   app.config['MAIL_PORT'] = ''
   app.config['MAIL_USERNAME'] = ''
   app.config['MAIL_PASSWORD'] = ''
   app.config['MAIL_USE_TLS'] = ''
   app.config['MAIL_USE_SSL'] = ''
   mail = Mail(app)

   # This Email address will be used to receive the user reports
   # Such as receiving bug reports, comments, etc.
   MyEmailAddress = ''
   ```
2. To run the project: `python app.py`

## Project Structure

<details>
  <summary>Details</summary>

1. `static` directory contains:
   - `Hotaru.ico`, website's icon
   - `scripts.js`
   - `styles.css`
   - `icons` directory
     - contains the default user avatar `Hotaru.png`, and all custom avatars that will be uploaded by the user
2. `templates` directory contains all the HTML files
3. `app.py`, the main entrance of the project
4. `config.py` contains functions for `app.py`
5. `hotaru.db` is the database of the project
   - contains user information, chat logs, and channels
</details>