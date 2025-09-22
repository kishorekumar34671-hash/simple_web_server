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
content ='''

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Simple Web Server</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f6f9;
      text-align: center;
      padding: 50px;
    }
    h1 {
      color: #2c3e50;
      font-size: 2.5rem;
    }
    p {
      color: #555;
      font-size: 1.2rem;
    }
    .box {
      background: #fff;
      display: inline-block;
      padding: 20px 40px;
      margin-top: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
  </style>
</head>
<body>
  <div class="box">
    <h1>🚀 Welcome to My Web Server</h1>
    <p>This page is being served from <b>http://localhost:8000/</b></p>
  </div>
</body>
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
```
        
# OUTPUT:
![alt text](<../Screenshot 2025-09-22 091731.png>) 
![alt text](<../Screenshot 2025-09-18 184441.png>)

# RESULT:
The program for implementing simple webserver is executed successfully.
