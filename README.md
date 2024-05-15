# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
```
Developed by : SUDHIR KUMAR .R
Register number : 212223230221
```
## CLIENT.PY:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER.PY:
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
## OUPUT:
## CLIENT.PY:

![321229317-6340ccc8-50de-45f2-811a-b628716bc6e8](https://github.com/Sudhirr5/3b_CHAT_USING_TCP_SOCKETS/assets/139332214/7c514722-e80a-447a-b791-baf708cf5a50)

## SERVER.PY:

![321229419-2a62d972-8df1-4b99-a7e2-fc17daef4930](https://github.com/Sudhirr5/3b_CHAT_USING_TCP_SOCKETS/assets/139332214/28c43735-6c53-4e27-a722-1aca1f61e7c0)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
