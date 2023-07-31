# Simple Notes App
This is a simple notes app built with React and Django.

## Requirements
1. Python 3.9
2. Node.js
3. React

## Installation
1. Clone the repository
```
git clone https://github.com/LondheShubham153/django-notes-app.git
```

2. Build the app
```
docker build -t notes-app .
```

3. Run the app
```
docker run -d -p 8000:8000 notes-app:latest
```

## Nginx

Install Nginx reverse proxy to make this application available

`sudo apt-get update`
`sudo apt install nginx`






For enabling reversy proxy through nginx in the nginx config file you'll need to edit a path
The path of the file is /etc/nginx/sites-enabled
The file name is default and under the server section make sure you edit the location section
proxy_pass http://127.0.0.1:8000

Also add the line if it isnt present
        location /api {
                proxy_pass http://127.0.0.01:8000;
        }

