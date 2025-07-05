#### Introduction

How does the internet work? The understanding of how the internet works has always seem like magic to most of us, Or some of us just don't care, and that's alright for a non technical person, but as a developer understanding how the internet works is really crucial in creating applications that communicate over networks and ensuring data are transmitted securely.

We won't be going that much in depth in this essay,
But you will know enough to try impress and get a follow back from some 40yo man anime waifu pfp for no reason on [twitter](https://x.com/HassanAmiriiii).

#### Short history of the internet

Come with me to America durig the [cold war](https://www.historyonthenet.com/cold-war) in the 1950s, The launch of [Sputnik](https://www.havefunwithhistory.com/facts-about-sputnik/) by the Soviet Union in 1957 spurred the U.S. to invest heavily in scientific and technological research, The idea was that the U.S only relied on a centralized telephone network, Which is really a big problem at the time because If a central hub was destroyed, communication could be completely cut off.

So the idea of a distributed network was born based on a concept known as packet switching; What this means is that, instead of transmitting data or packets to another computer with only one possible route, we could distribute the packets over many route

If one route is destroyed, The packets can just easily re-route to get to their specific destination. for more in-depth history you can check [history of the internet](https://historycooperative.org/who-invented-the-internet/).

#### network

- It'd be easier if you visualize network as links or connections

- standardized protocols :
  these are two words right;
  standardized: somethings we all agree on,
  protocol: rules

so we could say standardized protocols are set of instructions agreed upon so computers can communicate effectively.

TCP ensures that data packets are sent and received in the correct order.

switch device
a device for that allows communication btw computers within the same Lan

Lan
local area network

https ensures communication between a website and a server are secure basically encrypted from hackers or tamperes, also verifies the identity of the receiver using ssl/tls certificate

router
delivers packets from a computer to the internet

isp
internet service provider: basically takes your packets from the router and sends it to the final destination where the data requested are stored or to be posted and these process involve both wireless and wired connection --responsible for the transmission of packets from one location to the other

fiber optics cable
fastest data transmission device are

router table
the algorithm that decides the most efficient path btw interconnected routers a router should transfer packets to

streaming
when packets are sent in little by little and depends heavily on your internet speed

servers
an organization dB storage

load balancing
a way to manage heavy request to a single point from multiple computers

Wan (wide area network)
connection of multiple lans
the internet is made of wans cuz it is network of network
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
