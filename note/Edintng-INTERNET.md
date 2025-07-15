## Introduction

How does the internet work? The understanding of how the internet works has always seem like magic to most of us, Or some of us just don't care, and that's alright for a non technical person, but as a developer understanding how the internet works is really crucial in creating applications that communicate over networks and ensuring data are transmitted securely.

We won't be going that much in depth in this essay,
But you will know enough to try impress and get a follow back from some 40yo man anime waifu pfp for no reason on [twitter](https://x.com/HassanAmiriiii).

## Short history of the internet

Come with me to America during the [cold war](https://www.historyonthenet.com/cold-war) in the 1950s, The launch of [Sputnik](https://www.havefunwithhistory.com/facts-about-sputnik/) by the Soviet Union in 1957 spurred the U.S. to invest heavily in scientific and technological research, The idea was that the U.S only relied on a centralized telephone network, Which is really a big problem at the time because If a central hub was destroyed, communication could be completely cut off.

So the idea of a distributed network was born based on a concept known as packet switching; What this means is that, instead of transmitting data or packets to another computer with only one possible route, we could distribute the packets over many route

If one route is destroyed, The packets can just easily re-route to get to their specific destination. for more in-depth history you can check [history of the internet](https://historycooperative.org/who-invented-the-internet/).

# What is the internet

The internet is a network of interconnnected computers that communicate with each other using standardized protocols.

### understanding network:

network is simply the connection of multiple devices, for instance; you might have a network of computer and devices, your neighbors, your friends might do too, so this connection together as one forms the internet.

### understanding standardized protocol:

these are two words right;
standardized: Things we all agree on,
protocol: rules of how we do those things,
so we could say standardized protocols are set of rules we all agreed upon so computers can communicate effectively.

# Basic concepts and terminology

understanding these basic concepts would really help you digest the flow of how the internet works.

- **packets:** These are the data you and i send and receive from one computer to the other, but in terms of _internet_ we call it packets

- **Ip (Internet protocol):** This is a set of rules that governs how data/packets are transmitted.

- **TCP (Transmission control protocol):** This is another set of rules that ensures packets are sent and received in the correct order.

- **Ip address:** We all need this to connect to the internet in the first place, It's in charge of allocating the destination of packets we send and receive, represented as four sets of numbers, separated by periods, For example: 192.168.1.1 or 172.20.10.4

  - If you're interested in checking your computer's IP address, you could go to your terminal and input:

    Windows: ipconfig

    Linux: ip a or ifconfig

    macOS: ifconfig

- **Isp (Internet service provider):**
  responsible for the transmission of packets from one location to the other.

- **Lan:** Local area network, it is the connection of computers within a small area, eg a school or campus.

- **Wan (wide area network):**
  connection of multiple lans,
  The internet is made of wans because it is network of network(wans of wans). The inetrnet is made of wans but not all wans makes up the internet.

- **switch device:**
  a device that allows communication between computers within the same Lan.

- **router:**
  delivers packets from your computer to the internet.

- **router table:**
  the algorithm that decides the most efficient path to transfer packets between interconnected routers.

- **servers:**
  an organization data-base storage

- **streaming:**
  This refers to when packets are sent in chunks and depends heavily on your internet speed, for instance; when you are watching a youtube video, youtube server does not wait till it serves you the whole video at once, instead the packets are sent in chunks, and if you noticed, you'd see some white lines showing the available video to watch.

## introduction to HTTP and HTTPS

- **HTTP (Hypertext Transfer Protocol):** It's a foundational protocol responsible for communication between a web browser (client) and a web server, enabling the exchange of web pages and other web content. However, HTTP itself does not provide any security, meaning data transmitted over it is unencrypted and vulnerable.

- **HTTPS (Hypertext Transfer Protocol Secure):** This is the secure version of HTTP. It uses SSL/TLS (Secure Sockets Layer/Transport Layer Security) to encrypt the communication between a web browser and a server. This encryption protects data packets from being intercepted or read by unauthorized parties ("hackers"). Additionally, HTTPS uses SSL/TLS certificates to verify the identity of the server (the website you are connecting to), ensuring the authenticity and trustworthiness of the connection.

load balancing
a way to manage heavy request to a single point from multiple computers

but not all wans makes up the internet cuz private organizations could set up their own private wan by connecting their lans

vpn - virtual private network
vpn tunnel link create privacy, anonymity, security trust over a public network
it encrypt your data sent over a publk network eeping your data secure from unautorized access

encryption: putting data in a way unauthorized person cannt read
encapsulation : tunnel link iz a form of encapsulation , wrapping data packets in another packets

add to add encryption

lan for switches -- more secure

wan for routers -- less secure

public wans

- linking up lans through the internet; which is unsecure
  -could also utilize vpn to create a tunnel link -- which provides better security but still over the public internet

private wans - through isp wan network - can be costly
these are dedicated infastructure; created through the isp, to provide a fully secured private connction to authorized hooman- basically creating a private internet

router -- connect different network to the internet

local isps-- a small isp serving small community

regional isps -- sevring large city in a country

global isps -- serving internarionally

pop -- point of presence : basically connects the routers of difernt isps ; TO improve connection, data exchange and all

peering-- large companies linking a server to multiples isps for faster connections

networks of different global isps -- is called INternet backbone

ixp -- internet exchange point: are like pop but for global isps aka internet backbone to enable peering btw global isps
