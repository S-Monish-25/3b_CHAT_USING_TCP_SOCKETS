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
Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
Server:
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

Client:

![Screenshot 2025-04-29 100239](https://github.com/user-attachments/assets/a1d454e3-657d-430f-bc80-50004c6fa053)


Server:

![Screenshot 2025-04-29 100250](https://github.com/user-attachments/assets/f496db3e-683e-449c-935b-b94df7b135be)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
