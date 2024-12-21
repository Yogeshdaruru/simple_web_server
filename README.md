# EX01 Developing a Simple Webserver

<<<<<<< HEAD
# Date:13-11-2024
=======
# Date:12/09/2024
>>>>>>> d88a0a97edd20306211eef12a66471f02e92cd1a
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

content='''
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
    <table border="5">
        <tr>
            <th>Configuration</th>
            <th>Description</th>
        </tr>
        <tr>
            <td>Processor</td>
            <td>13th intel(R) core(TM) i5-1335U, 1300Mhz, 10 Core(s), 12 Logical Processor</td>
        </tr>
        <tr><td>Storage(HDD/SSD)</td><td>SAMSUNG MZAL4512HBLU-00BL1</td></tr>
        <tr>
            <td>Memory</td><td>8.5 GB</td>
        </tr>
        <tr>
            <td>Graphics Card</td>
            <td>
                Intel(R) Iris(R) Xe Graphics , 
                NVIDIA GeForce MX550
            </td>
        </tr>
        <tr>
            <td>Operating System</td><td>Edition:Windows , Version:22H2 , OS build:22621.4169</td>
        </tr>
        <tr>
            <td>RAM</td><td>16.0 GB</td></tr>
        
    </table>
</body>
</html>
'''

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()

```

# OUTPUT:
<<<<<<< HEAD
![alt text](<Screenshot 2024-12-07 215614.png>)
![alt text](<Screenshot (26).png>)
=======
![Screenshot 2024-12-07 222408](https://github.com/user-attachments/assets/3bb35581-c36a-44df-ac82-a9833c7eb272)

![Screenshot 2024-12-07 222512](https://github.com/user-attachments/assets/498b1eda-f400-4011-aa5c-8a43fcb2784e)

>>>>>>> d88a0a97edd20306211eef12a66471f02e92cd1a
# RESULT:
The program for implementing simple webserver is executed successfully.
