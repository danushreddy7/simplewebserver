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
<html>
     
     <title> Software Companies Revenue </title>
     <body>
           <table border = "2" cellspacing = "10" cellpading = "6">
              <caption>TOP SIX REVENUE SOFTWARE COMPANIES </caption>
              <tr>
                  <th>S.NO</th>
                  <th>COMPANY</th>			
                  <th>REVENUE</th>
              </tr>
              <tr>
                  <td>1</td>
                  <td>Microsoft</td>
                  <td>65 Billion</td>
             </tr>
             <tr>
                  <td>2</td>
                  <td>Oracle</td>
                  <td>29.6 Billion</td>
             </tr>
             <tr>
                  <td>3</td>
                  <td>IBM</td>
                  <td>29.1Billion</td>
            </tr>
            <tr>
                  <td>4</td>
                  <td>SAP</td>
                  <td>6.4 Billion</td>
            </tr>
            <tr>
                  <td>5</td>
                  <td>Symantic</td>
                  <td>5.6 Billion</td>
            </tr>
            <tr>
                <td>6</td>
                <td>Adobe Inc</td>
                <td>19.8 Billion</td>
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



## OUTPUT:
![image](https://github.com/user-attachments/assets/6d01ddfd-c7d8-44ed-b8dd-5f7fe1d31781)



## RESULT:
The program for implementing simple webserver is executed successfully.
