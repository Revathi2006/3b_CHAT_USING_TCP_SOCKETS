# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## server.py
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```
## client.py
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## OUPUT
## server.py
<img width="619" height="242" alt="image" src="https://github.com/user-attachments/assets/3ecf721f-2f69-489d-8c0f-bd57ba0d0dc7" />

## client.py
<img width="628" height="273" alt="image" src="https://github.com/user-attachments/assets/6dd62960-2a56-4f8f-92c7-d7d9e6e746bf" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
