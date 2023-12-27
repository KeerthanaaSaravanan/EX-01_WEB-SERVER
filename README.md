# EX-01: Developing a Simple Webserver
'''
# Developed by: KEERTHANA S
# Register no: 23013398
'''
# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver
# PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler

content="""

<html>
<head>
</head>
<body>
<h1>Welcome</h1>
</body>
</html>
"""

class MyHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html')
        self.end_headers()
        self.wfile.write(content.encode())


server_address=('',80)
httpd=HTTPServer(server_address,HelloHandler)
httpd.serve_forever()

```

# OUTPUT:
![output](https://github.com/KeerthanaaSaravanan/Web_server/assets/145742596/08c66f22-c9f7-4c62-ac9b-b8840e1da3ec)

# RESULT:

The program is executed succesfully
