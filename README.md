# Intro to tcpdump

<h2>Description</h2>
In this network security task I was introduced to tcpdump, listened in on plaintext communication between a local host server and client, created an http 80 server using python 3 and captured the ASCII and header response from a curl request for a nonexistent file. 


<h2>Languages and Utilities Used</h2>

- <b>tcpdump</b>
- <b>python3</b>
- <b>linux CLI</b>


<h2>Environments Used </h2>

- <b>Unbuntu</b> 

<br />
<br />
Ran tcpdump with -D to list all available network interfaces before capturing. I decided to capture on loopback with a server and client terminal set up. 

![1) tcpdump -i to listen on lopback instances](https://github.com/user-attachments/assets/8515c623-cf8d-42e9-bc61-2a9412ad78b0)

<br />
<br />
On my seond terminal, I used netcat to set up a listening server on port 4321. 

![2) netcat to listen on port 4321 in 2nd terminal](https://github.com/user-attachments/assets/f8844d69-d6d3-42d4-9686-a3878ed3ffc3)

<br />
<br />  
I used netcat to establish a connect to the localhost server on port 4321. Connection was successful.  

![3) netcat connection to local host server on port 4321 success](https://github.com/user-attachments/assets/5e7585a7-7e5e-4d67-9744-15b39103e5fe)

<br />
<br />
On my tcpdump instance, I captured the tcp 3 wayhandshake connection from my local client to local host. 

![4) tcp 3 way handshake captured from local client to client server](https://github.com/user-attachments/assets/819c81eb-c309-40bd-9870-c3b6c34ef9db)

<br />
<br />
On my client isntance, I sent a message "HELLO" to my local server. 

![5) client sending HELLO to server](https://github.com/user-attachments/assets/3b83d6a6-cb1a-4931-8d22-b83ccccfc01a)

<br />
<br />
Tcpdump shows the message pushed through with a P. (push acknowledge) flag with a packet length of 6. 

![6) hello packet captured](https://github.com/user-attachments/assets/bbc1a3ef-4dca-4f14-a327-8a9d9768d3af)

<br />
<br />
I ran tcpdump to capture and display the data packet in hexidemcial & ASCII format with -x and ran "Hello again" from my local client. 

![7) -X shows ascii format of packet received](https://github.com/user-attachments/assets/a535e355-78d5-4af8-a7de-5350f9d34eaa)

<br />
<br />
I then created an http 80 server using python on my server instance. 

![8) creating an http port 80 server with python 3](https://github.com/user-attachments/assets/2263ba16-1a8b-4e87-b3a6-0952958f78d7)

<br />
<br />
On my client instance, I used curl to get a file that did not exist on my server instance to observe the response.  

![9) curl request for nonexistent file from port 80 http server](https://github.com/user-attachments/assets/51f94165-a930-4af9-87db-803087212e1c)

<br />
<br />
In my tcpdump terminal I observed the get headers from my curl request on my client instance, as well as the curl response from the server to my client when no file was found. 

![10) tcpdump shows full ascii response from webserver and http response headers](https://github.com/user-attachments/assets/693f9a44-7b14-4b4f-81b4-9741814a6aaa)

<br />
<br />
