## Network tools

- The network is and always will be the sexiest arena for a hacker. With simple network access, hacker can scan for hosts, inject packets, sniff data, and remotely exploit hosts.
- After you get in, there are no network tools, No netcat. No Wireshark. No compiler, and no means to install one. But in many cases, you’ll have a Python installed.
- There are lot of networking tools in python, but all of them at core use SOCKET. We'll use socket module and we’ll also build clients, servers, and a TCP proxy.

## Create a TCP Client

go to /tcp_client_1/ \
create a venv `python -m venv tcp_client_1` \
activate it `source tcp_client_1/bin/activate` \
create code in tcp_client_1.py  (Socket is an inbuilt module, there is no need for pip install) \
run using the play button.

### Serious Assumptions
- The first assumption is that our connectionwill always succeed
- The second is that the server expects us to send data first (some servers expect to send data to you first and await your response). 
- Our third assumption is that the server will always return data to us in a timely fashion.

## Create a UDP Client

go to /udp_client_1/ \
create a venv `python -m venv udp_client_1` \
activate it `source udp_client_1/bin/activate` \
create code in udp_client_1.py  (Socket is an inbuilt module, there is no need for pip install) \
run using the play button.

### Assumptions

- There is a server listening `nc -nlvup 9997`     (Netcat listerer)
- Close the connection only when you get some data. (Type something and press enter in netcat)

Again, we’re not looking to be superior network programmers; we want it to be quick, easy, and reliable enough to handle our day-to-day hacking tasks.