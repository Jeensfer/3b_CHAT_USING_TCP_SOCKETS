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
### Server
```python
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
### Client 
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## OUPUT
### Server
<img width="703" height="91" alt="image" src="https://github.com/user-attachments/assets/0d7a27b3-259e-443d-9c53-7906739ce5ae" />

### Client 
<img width="747" height="109" alt="image" src="https://github.com/user-attachments/assets/61ec98c6-cd05-42fc-9749-e2e07a9d7e09" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
