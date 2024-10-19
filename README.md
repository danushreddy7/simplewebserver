# EX01 Developing a Simple Webserver
## NAME:T.DANUSH REDDY
# REGISTER NO:212223040029
# Date:25-09-2024

## AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
....
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>Software Companies</title>
</head>
<body bgcolor="cyan">
<table border="4" cellspacing="1" cellpadling="1" height="300" width="700" bgcolor="white">
<caption>TOP SOFTWARE COMPANIES WITH REVENUE</caption>
		<tr>
			<th>COMPANY</th>
			<th>REVENUE</th>
			<th>PERCENTAGE</th>
		</tr>
		<tr>
			<td>Google</td>
			<td>4541397</td>
			<td>1</td>
		</tr>

		<tr>
			<td>Meta</td>
			<td>3216464</td>
			<td>2</td>
		</tr>

		<tr>
			<td>SAMSUNG</td>
			<td>1649465</td>
			<td>3</td>
		</tr>
                 <tr>
			<td>TCS</td>
			<td>51918518</td>
			<td>4</td>
		</tr>

                 <tr>
			<td>Infosys</td>
			<td>5191587</td>
			<td>5</td>
		</tr>



	</table>
</body>
</html>

"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
.....



## OUTPUT:
![image](https://github.com/user-attachments/assets/c750e445-65ba-4198-bf03-07fca2b02e52)




## RESULT:
The program for implementing simple webserver is executed successfully.
