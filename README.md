# Microblog
This project, as the name sugest, its a little blog. 
I developed it folowing an <a href="https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world" target="_blank">tutorial</a> to learn Flask.

:point_right: <a href="https://microblog-byshimun.herokuapp.com/"> See this application working </a> on Heroku. :point_left:   

## :scroll: Microblog has:
* Users subsystem that allows users login and logout
* Users Registration
* Password recovery
* Posts writing functionality
* Profile page
* Followers functionality
* Explore page (to see all the blog posts)
* Posts translations
* Search posts by its content
* Private messages between users (With notifications)


## :hammer: Instalation steps

* Clone the repository
```bash
  git clone https://github.com/IgorShimun/microblog.git
  cd microblog
```

<br>

* Initialize the virtual environment
##### Linux
```bash
  python3 -m venv venv
  . venv/bin/activate
```
##### Windows
```bash
  python -m venv venv
  venv\Scripts\activate.bat
```
<br>

* Install dependecies
```bash
  pip install -r requirements.txt
```

<br>

* Start a updated database 
```bash
  flask db upgrade 
```

<br>

* Turn on the translations
```bash
  flask translate compile
```

<br>

* Run the aplication
```bash
  flask run
```

<br>
<br>

## Optional
If you want to see the reset password e-mail without configure a smtp server, 
run this command in a separate terminal: 
```bash
python -m smtpd -n -c DebuggingServer localhost:8025
```
In this terminal you will can read the e-mail with the reset link

<br>

## About environment variables
* Im Using a Third-Party Translation Service from <a href="https://azure.microsoft.com/" target="_blank">Azure</a>
```MS_TRANSLATOR_KEY=<your-key-of-azure-translation-service>```

* URL for the Search Engine <a href="https://www.elastic.co/" target="_blank">Elasticsearch</a>
```ELASTICSEARCH_URL=<your-elasticsearch-url>```

* I'm using my google account to send e-mails (You will have to enable <a href="https://myaccount.google.com/lesssecureapps" target="_blank">less secure apps</a>)
```
MAIL_SERVER=smtp.googlemail.com                          
MAIL_PORT=587                                             
MAIL_USE_TLS=1
MAIL_USERNAME=<your-gmail-username>
MAIL_PASSWORD=<your-gmail-password>
```
