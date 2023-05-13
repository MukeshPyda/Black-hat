## Network tools

- The network is and always will be the sexiest arena for a hacker. With simple network access, hacker can scan for hosts, inject packets, sniff data, and remotely exploit hosts.
- After you get in, there are no network tools, No netcat. No Wireshark. No compiler, and no means to install one. But in many cases, you’ll have a Python installed.
- There are lot of networking tools in python, but all of them at core use SOCKET. We'll use socket module and we’ll also build clients, servers, and a TCP proxy.

## Create a TCP Client

go to /tcp_client_1/ \
create a venv `python -m venv tcp_client_1` \
activate it `source tcp_client_1/bin/activate` \
create code in tcp_client_1.py  (Socket is an inbuilt module, there is no need for pip install) \
run using the python tcp_client_1/tcp_client_1.py

### Serious Assumptions
- The first assumption is that our connectionwill always succeed
- The second is that the server expects us to send data first (some servers expect to send data to you first and await your response). 
- Our third assumption is that the server will always return data to us in a timely fashion.

## Create a UDP Client

go to /udp_client_1/ \
create a venv `python -m venv udp_client_1` \
activate it `source udp_client_1/bin/activate` \
create code in udp_client_1.py  (Socket is an inbuilt module, there is no need for pip install) \
run using the python udp_client_1/udp_client_1.py

### Assumptions

- There is a server listening `nc -nlvup 9997`     (Netcat listerer)
- Close the connection only when you get some data. (Type something and press enter in netcat)

Again, we’re not looking to be superior network programmers; we want it to be quick, easy, and reliable enough to handle our day-to-day hacking tasks.


## TCP Server

go to /tcp_server_1/ \
create a venv `python -m venv tcp_server_1` \
activate it `source tcp_server_1/bin/activate` \
create code in tcp_server_1.py  (Socket is an inbuilt module, there is no need for pip install) \
run using the python tcp_server_1/tcp_server_1.py


## Netcat.py

go to /netcat/ \
create netcat.py \
some commands: \
python netcat.py -t 192.168.1.203 -p 5555 -l -c        (as a server) \
python netcat.py -t 192.168.1.203 -p 5555               (as a client press Ctrl+D and send message/commands) \

python netcat.py -t 192.168.1.203 -p 5555 -l -e="cat /etc/passwd"  (in server) \
python netcat.py -t 192.168.1.203 -p 5555                           (in client press Ctrl+D)
nc 192.168.1.203 5555                                              (also works)

echo -ne "GET / HTTP/1.1\r\nHost: reachtim.com\r\n\r\n" |python ./netcat.py -t reachtim.com -p 80 (As a client) \


## Proxy
sudo python proxy.py 192.168.1.203 21 ftp.sun.ac.za 21 True


## SSH is awesome.
ssh_cmd is just a demo, doesn't include the keys inside the py file.
It is used for a single command to test the connection.

## Reverse SSH is totally agnificent-may.
send ssh_rcmd.py to windows when first connected.
start ssh_server.py in your pc.
Then start ssh_rcmd.py in windows.
Once the connection is made, then send windows commands FROM LINUX. Not from windows.