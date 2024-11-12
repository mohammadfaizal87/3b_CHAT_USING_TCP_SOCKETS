# 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME : MOHAMMAD FAIZAL SK
## REGISTER NUMBER : 212223240092
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### CLIENT
```py
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### SERVER 
```py
import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())

```
## OUTPUT
### CLIENT OUTPUT
![Screenshot 2024-04-21 153822](https://github.com/c-sanjay/3b_CHAT_USING_TCP_SOCKETS/assets/147139405/e633ef4b-b7ba-4ae9-916f-9631cde4962d)

### SERVER OUTPUT
![Screenshot 2024-04-21 153836](https://github.com/c-sanjay/3b_CHAT_USING_TCP_SOCKETS/assets/147139405/7496b6c8-fd07-46c6-b855-6b408cf8ff46)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
