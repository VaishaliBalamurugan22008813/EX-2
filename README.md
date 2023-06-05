# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

DATE:15.03.2023

AIM :
To write a python program to perform stop and wait protocol 
```
ALGORITHM :
1.Start the program.
2.Get the frame size from the user
3.To create the frame based on the user request.
4.To send frames to server from the client side.
5.If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client.
6.Stop the program
```
PROGRAM :
```
CLIENT :
Developed by : VAISHALI BALAMURUGAN
Register Number : 212222230164
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
 print(ack)
 continue
 else:
 c.close()
 break
```
```
SERVER:
Developed by : VAISHALI BALAMURUGAN
Register Number : 212222230164
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Received".encode())
```
OUTPUT :
CLIENT:
![image](https://github.com/VaishaliBalamurugan22008813/EX-2/assets/119390134/15acdf69-b3f1-41ed-8bf9-6e0f27606828)

SERVER:
![image](https://github.com/VaishaliBalamurugan22008813/EX-2/assets/119390134/04338258-573c-43d0-96e7-a583b46664d9)


```
RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.
```

