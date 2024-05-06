# 2b IMPLEMENTATION OF SLIDING WINDOW PROTOCOL
## AIM
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
CLIENT
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c, addr=s. accept()
size=int(input ("Enter number of frames to send"))
l=list(range(size))
s=int(input("Enter Window Size : "))
st=0
i=0
while True:
  while(i<len(l)):
   st+=s
   c.send(str(l[i:st]).encode())
   ack=c.recv(1024).decode()
   if ack:
    print(ack)
    i+=s
SERVER
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("acknowledgement recived from the server".encode())
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("acknowledgement recived from the server".encode())
 
OUTPUT

CLIENT OUTPUT:
![image](https://github.com/mdgj2005/2b_SLIDING_WINDOW_PROTOCOL/assets/145533936/8fa72bab-9d8d-42f5-b4df-da82a20e7789)

SERVER OUTPUT:
![image](https://github.com/mdgj2005/2b_SLIDING_WINDOW_PROTOCOL/assets/145533936/0791ee96-7945-4286-a9f3-6234a453490e)


## OUPUT
## RESULT
Thus, python program to perform stop and wait protocol was successfully executed
