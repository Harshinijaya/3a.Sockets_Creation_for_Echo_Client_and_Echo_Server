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
```
SERVER
import socket

server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

host = '127.0.0.1'
port = 5000

server_socket.bind((host, port))

server_socket.listen(1)
print("Server is waiting for connection...")

conn, addr = server_socket.accept()
print("Connected with:", addr)

data = conn.recv(1024).decode()
print("Received from client:", data)

conn.send(data.encode())

conn.close()
server_socket.close()

CLIENT

import socket

client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

host = '127.0.0.1'
port = 5000

client_socket.connect((host, port))

message = input("Enter message: ")
client_socket.send(message.encode())

data = client_socket.recv(1024).decode()
print("Echo from server:", data)

client_socket.close()
```
## OUPUT##
<img width="1917" height="1078" alt="Screenshot 2026-05-20 105735" src="https://github.com/user-attachments/assets/b511129d-408a-4aa1-82dc-8c2b4091bb21" />
<img width="1918" height="1078" alt="Screenshot 2026-05-20 105748" src="https://github.com/user-attachments/assets/62c2ad39-c949-4645-a23f-e0408f2b9684" />


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
