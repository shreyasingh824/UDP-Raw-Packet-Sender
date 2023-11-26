# UDP Raw Packet Sender

## Overview

This C program demonstrates a simple implementation of a UDP packet sender using raw sockets. It crafts a UDP packet with custom headers, sets up a raw socket, and sends the packet in a loop.

## Usage

1. Compile the program:
   ```bash
   gcc -o udp_sender udp_sender.c
Run the executable: ./udp_sender


plaintext
Copy code
# UDP Raw Packet Sender

## Overview

This C program demonstrates a simple implementation of a UDP packet sender using raw sockets. It crafts a UDP packet with custom headers, sets up a raw socket, and sends the packet in a loop.

## Usage

1. Compile the program:
   ```bash
   gcc -o udp_sender udp_sender.c
Run the executable:
bash
Copy code
./udp_sender
Code Structure
Header Files
netinet/in_systm.h
netinet/in.h
netinet/ip.h
netinet/udp.h
netinet/tcp.h
stdlib.h
arpa/inet.h
Struct Definition
struct psd_udp: Represents a pseudo-header for UDP checksum calculation.
Functions
unsigned short in_cksum(unsigned short *addr, int len): Calculates the Internet checksum.
unsigned short in_cksum_udp(int src, int dst, unsigned short *addr, int len): Calculates UDP checksum using a pseudo-header.
Thread Function
void *run(void *arg): Runs the UDP sender thread. Crafts UDP packet, sets up raw socket, and sends packets in a loop.
Main Function
int main(int argc, char **argv): Calls the run function to execute the UDP sender.


Remember to replace "udp_sender.c" with the actual filename if it's different. Additionally, it's important to address the issues mentioned in the code before using it in a production environment.



