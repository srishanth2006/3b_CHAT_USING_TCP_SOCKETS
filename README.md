# 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME: SRISHANTH J
## REG.NO:212223240160
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server
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
## OUPUT
## Client:
<img width="436" alt="image" src="https://github.com/user-attachments/assets/85b5ef0e-9de8-41ab-b03c-fe03368a75e9">

## Server:
<img width="435" alt="image" src="https://github.com/user-attachments/assets/a503a9e1-cff9-45b0-9522-ffe2740003ec">



## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
