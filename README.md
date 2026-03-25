# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
server.py
~~~
import socket
s=socket.socket()
s.bind(('localhost',9999))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMsg=c.recv(1024).decode()
    c.send(ClientMsg.encode())
~~~
client.py
~~~
import socket
s=socket.socket()
s.connect(('localhost',9999))
while True:
    msg=input("Client> ")
    s.send(msg.encode())
    print("Server> ",s.recv(1024).decode())
~~~
## OUPUT
server

<img width="971" height="470" alt="Screenshot 2026-03-25 114144" src="https://github.com/user-attachments/assets/77d00e72-654f-42c0-bde4-6a19a41589ab" />

client

<img width="916" height="375" alt="Screenshot 2026-03-25 114158" src="https://github.com/user-attachments/assets/18c3d2af-3e6d-4f62-8eec-ee0b37ab7233" />


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
