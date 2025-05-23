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
client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
server:
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
## OUTPUT
client:
![Screenshot 2025-05-23 045744](https://github.com/user-attachments/assets/8ca4bfd3-a8b8-4eca-9079-55e386d4b923)

server:
![Screenshot 2025-05-23 045757](https://github.com/user-attachments/assets/a8e5e715-1017-4479-9cdb-3a7cb56712e0)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
