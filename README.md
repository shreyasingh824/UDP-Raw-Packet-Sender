# UDP Raw Packet Sender

## Overview

This C program demonstrates a simple implementation of a UDP packet sender using raw sockets. It crafts a UDP packet with custom headers, sets up a raw socket, and sends the packet in a loop.

## Usage

1. **Compile the program:**
   ```bash
   gcc -o udp_sender udp_sender.c
Remember to replace "udp_sender.c" with the actual filename if it's different. Additionally, it's important to address the issues mentioned in the code before using it in a production environment.

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
in_cksum:

Description: Calculates the Internet checksum.
Parameters:
unsigned short *addr: Pointer to the data.
int len: Length of the data.
in_cksum_udp:

Description: Calculates UDP checksum using a pseudo-header.
Parameters:
int src: Source IP address.
int dst: Destination IP address.
unsigned short *addr: Pointer to the UDP data.
int len: Length of the UDP data.
Thread Function
run:
Description: Runs the UDP sender thread. Crafts UDP packets, sets up a raw socket, and sends packets in a loop.
Parameters:
void *arg: Argument (not currently used).
Main Function
main:
Description: Calls the run function to execute the UDP sender.
Parameters:
int argc: Number of command-line arguments.
char **argv: Array of command-line argument strings.


