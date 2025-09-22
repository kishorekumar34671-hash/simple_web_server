# EX01 Developing a Simple Webserver

# Date:22\09\2025
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
            <title>TCP/IP Protocol Suite</title>
            <style>
                body { font-family: Arial, sans-serif; background: #f9f9f9; padding: 40px; }
                h1 { color: #2c3e50; text-align: center; }
                .layer { margin: 20px 0; padding: 15px; background: #fff; border-radius: 8px;
                         box-shadow: 0 4px 8px rgba(0,0,0,0.1); }
                h2 { color: #2980b9; }
                ul { line-height: 1.8; }
            </style>
        </head>
        <body>
            <h1>🌐 TCP/IP Protocol Suite</h1>

            <div class="layer">
                <h2>1. Application Layer</h2>
                <ul>
                    <li>HTTP / HTTPS</li>
                    <li>FTP</li>
                    <li>SMTP</li>
                    <li>DNS</li>
                    <li>Telnet</li>
                </ul>
            </div>

            <div class="layer">
                <h2>2. Transport Layer</h2>
                <ul>
                    <li>TCP (Transmission Control Protocol)</li>
                    <li>UDP (User Datagram Protocol)</li>
                </ul>
            </div>

            <div class="layer">
                <h2>3. Internet Layer</h2>
                <ul>
                    <li>IP (IPv4 / IPv6)</li>
                    <li>ICMP</li>
                    <li>ARP</li>
                    <li>IGMP</li>
                </ul>
            </div>

            <div class="layer">
                <h2>4. Network Access Layer</h2>
                <ul>
                    <li>Ethernet</li>
                    <li>Wi-Fi (IEEE 802.11)</li>
                    <li>PPP</li>
                    <li>Frame Relay</li>
                </ul>
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

![alt text](<Screenshot 2025-09-18 184441.png>)
![alt text](<Screenshot 2025-09-22 103611.png>)
![alt text](<Screenshot 2025-09-22 103702.png>)




# RESULT:
The program for implementing simple webserver is executed successfully.
