# EX01 Developing a Simple Webserver

# Date:19.09.2025
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
```from django.shortcuts import render
from http.server import HTTPserver,BaseHTTPRequestHandler
content ='''<html>
                <h1>Hello</h1>
            </html>'''


class Myserver(BaseHTTPRequestHandler):
    def do_GET(self):
        print("GET request received...")
        self.send_response(200)
        self.send_header("content-type","text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address =('',8000)
httpd =HTTPserver(server_address,Myserver)
httpd.serve_forever()
 HEAD

```
 4120ae8f6bc92b2ac33f1da32da44ffaca29957c
        
# OUTPUT:
![alt text](<Screenshot 2025-09-18 184340.png>)
![alt text](<Screenshot 2025-09-18 184441.png>)

# RESULT:
The program for implementing simple webserver is executed successfully.
