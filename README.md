# EX01 Developing a Simple Webserver

# Date:
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
httpd.serve_forever
```
        
# OUTPUT:
# RESULT:
The program for implementing simple webserver is executed successfully.
