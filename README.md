# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM:
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python.
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server.
4. Send and receive the message using the send function in socket.

## PROGRAM:
## Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## Server:
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

## OUTPUT:
## Client:
![Screenshot 2024-04-03 111815](https://github.com/HEMAKESHG/3b_CHAT_USING_TCP_SOCKETS/assets/144870552/ecfab044-a2cb-4612-b046-e67d00b9ac5f)
## Server:
![Screenshot 2024-04-03 111822](https://github.com/HEMAKESHG/3b_CHAT_USING_TCP_SOCKETS/assets/144870552/e02addf1-9ce0-4f8b-95a0-65595bc75d86)


## RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
