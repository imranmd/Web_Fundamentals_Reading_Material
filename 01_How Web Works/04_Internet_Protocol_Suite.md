**Simplified Overview of the Internet Protocol Suite**

The Internet Protocol Suite, is a set of rules and protocols that enable devices to communicate on the internet. These protocols are organized into layers, with each layer building on top of the one below it. Let's take a closer look at the layers and their contributions:

![URL](../Assets/LayerOfProtocols.svg)

**1. Link Layer:**
At the bottom layer, devices need a way to physically send and receive digital data over wired or wireless connections. This layer handles the transmission of signals as bits and deals with issues related to the physical connection.

**2. Network Layer:**
To communicate beyond two directly connected devices, we need addressing protocols to identify the sender and receiver of data. The IP (Internet Protocol) addresses are used for this purpose, uniquely identifying each device on the internet.

**3. Transport Layer:**
Data on the internet is divided into small packets for efficient transmission. The Transport Layer manages the reliable and orderly delivery of these packets. TCP (Transmission Control Protocol) ensures data is delivered accurately, while UDP (User Datagram Protocol) provides faster but less reliable communication.

**4. Application Layer:**
At the top layer, we find various protocols that cater to specific services and applications on the internet. Some examples include:

- HTTP (Hypertext Transfer Protocol): Used for accessing web pages and browsing the World Wide Web.
- DNS (Domain Name System): Translates human-readable domain names (like www.example.com) into IP addresses.
- TLS (Transport Layer Security): Encrypts data for secure transmission, ensuring privacy and security for sensitive information.

**Protocol Stacks:**
When data travels through the internet, it passes through multiple layers of protocols, each responsible for a specific task. For example:

- When you access a new website, your browser may need to make a DNS request:
  - Application Layer: DNS
  - Transport Layer: UDP
  - Network Layer: IP (v4)
  - Link Layer: Ethernet or Wireless LAN

- If the website uses HTTPS, the protocol stack includes multiple layers at the application level (both HTTP and TLS):
  - Application Layer: HTTP and TLS
  - Transport Layer: TCP
  - Network Layer: IP (v4)
  - Link Layer: Ethernet or Wireless LAN

**Summary:**
The Internet Protocol Suite, represented by TCP/IP, is the backbone of communication on the internet. It works as a layered structure, with each layer playing a vital role in enabling smooth and reliable data transmission between devices. From physical connections to secure data encryption and everything in between, the Internet Protocol Suite makes the internet the interconnected and dynamic digital space we know today.