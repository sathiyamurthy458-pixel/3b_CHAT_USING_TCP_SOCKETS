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
SERVER
```
import socket 
s=socket.socket() 
s.bind(('localhost',6000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    print("Client > ",ClientMessage) 
    msg=input("Server > ") 
    c.send(msg.encode())

```
CLIENT
```
import socket 
s=socket.socket() 
s.connect(('localhost',6000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 
    

```
## OUTPUT
client

<img width="907" height="390" alt="image" src="https://github.com/user-attachments/assets/8d127fad-9390-47de-ae6e-0ae747c163b2" />

server

<img width="966" height="411" alt="image" src="https://github.com/user-attachments/assets/6aa351f0-2ded-4444-9e0d-15e0a15cd219" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
