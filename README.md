# EX01 Developing a Simple Webserver

# Date:19/09/2025
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
```
from http.server import HTTPServer,BaseHTTPRequestHandler
content='''<!DOCTYPE html>
<html>
<head>
<title>Laptop Specification</title>
</head>
<body bgcolor ="orange">
<h1 align='center'><u>TCP/IP Model</u></h1>
<table align="center" width="800" cellspacing="5" cellpadding="6" border="5">
<caption style="font-size: larger;"><b>Layers and it's protocols</b></caption>

<tr>
<th style="background-color: red;color: white;">Application layer</th>
<td style="background-color: grey;color: white;">HTTP, FTP, TFTP, DNS, DHCP, SMPT, Telnet</td>
</tr>
<tr>
<th style="background-color: red;color: white;">Transport layer</th>
<td style="background-color: grey;color: white;">TCP and UDP</td>
</tr>
<tr>
<th style="background-color:  red;color: white;">Internet layer</th>
<td style="background-color: grey;color: white;">IP</td>
</tr>
<tr>
<th style="background-color:  red;color: white;">Network Interface layer</th>
<td style="background-color: grey;color: white;">Ethernet, TokenRing, FrameRelay and ATM</td>
</tr>
<tr>
<th style="background-color: red;color: white;">Product ID</th>
<td style="background-color: grey;color: white;">00330-53142-21373-AAOEM</td>
</tr>
<tr>
<th style="background-color: red;color: white;">System type</th>
<td style="background-color: grey;color: white;">64-bit operating system, x64-based processor</td>
</tr>
<tr>
<th style="background-color: red;color: white;">Pen and Touch</th>
<td style="background-color: grey;color: white;">No pen or touch input is available for this display</td>
</tr>
</table>
</body>
</html>
'''
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("content-type","text/html")
        self.end_headers()
        self.wfile.write(content,encode())
print("This is my webserver")
server_address=(' ',8000)
httpd =HTTPServer(server_address,MyServer)
httpd.serve_forever()
```
# OUTPUT:
<img width="1902" height="935" alt="image" src="https://github.com/user-attachments/assets/92d17116-a73b-461e-9ff5-f244581a60bc" />

![alt text](image-2.png)
# RESULT:
The program for implementing simple webserver is executed successfully.
