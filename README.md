# EXP : 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## Register no: 212223230239
## Name: Vignesh raaj s
## AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
### Server
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
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
## OUPUT:
![CN 3a op](https://github.com/22008837/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/120194155/382979fe-0d09-45d0-b7c3-96797da7548f)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
