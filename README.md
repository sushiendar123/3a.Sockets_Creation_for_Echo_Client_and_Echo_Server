# Name: M.Sushiendar
# Register Number: 212223040217
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
# cilent
```
import socket

HOST = '127.0.0.1'  
PORT = 65432       

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
  s.bind((HOST, PORT))
  s.listen()
  conn, addr = s.accept()
  with conn:
    print('Connected by', addr)
    while True:
      data = conn.recv(1024)
      if not data:
        break
      conn.sendall(data)

```
# server
```
import socket

HOST = '127.0.0.1'  
PORT = 65432        

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
   s.connect((HOST, PORT))
   while True:
      message = input("Enter message to send to server: ")
      s.sendall(message.encode())
      data = s.recv(1024)
      print('Received', repr(data.decode()))
```

## OUTPUT
![image](https://github.com/sushiendar123/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/169825800/22cbd48c-73eb-4542-b516-e99b636a20f2)
![image](https://github.com/sushiendar123/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/169825800/89e9448e-4594-43c7-9aac-b82a6b1b609d)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
