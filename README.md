## Network tools

- The network is and always will be the sexiest arena for a hacker. With simple network access, hacker can scan for hosts, inject packets, sniff data, and remotely exploit hosts.
- After you get in, there are no network tools, No netcat. No Wireshark. No compiler, and no means to install one. But in many cases, you’ll have a Python installed.
- There are lot of networking tools in python, but all of them at core use SOCKET. We'll use socket module and we’ll also build clients, servers, and a TCP proxy.

## Create a TCP Client

go to /tcp_client_1/
create a venv `python -m venv tcp_client_1`
activate it `source tcp_client_1/bin/activate`
create code in tcp_client_1.py  (Socket is an inbuilt module, there is no need for pip install)
run using the play button.