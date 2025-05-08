# 3b.CREATION FOR CHAT USING TCP SOCKETS
# NAME: MADHUPRIYA R
# REG NO:212224040177
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
```
CLIENT

import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 
SERVER

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
![image](https://github.com/user-attachments/assets/7f7b38dd-23ae-4faf-b5cd-d7da4765949c)
![image](https://github.com/user-attachments/assets/b81475a9-f18e-4dd2-a0ca-c3c886e68b92)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
