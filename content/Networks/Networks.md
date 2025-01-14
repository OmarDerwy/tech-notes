---
lecturer: mabosehly
number: "01222387651"
---

# 1	into
why this network?

I am a programmer/developer. Why network?

- Data will transfer along a network. You need to understand how a network works
- for personal use also.
- sometimes interviews incorporate networks
cybersecurity
- not luxery or nonrelevant
- attacks are too common
- too much leaks in databases
distributed system
- 1 server for something like server? no multiple/farms of servers. This is called distribution
- what is cloud
- what is virtualization

extra resources
- maharateck: implementation of network fundamentals

9 hours

exam later 15 questions mcq. Simple

# 2	network

it has a card called NIC. every device has it. it connects to other devices through a medium

in old times we used a device called **hub**

it had a problem. when someone used a device in the network. Other users in the network cannot use it.
- We got rid of the hub and got a switch.
- got rid of the problem of collision.

phones. works using wifi in networks. how do they connect?
- access point
- it connects to devices using wireless interface

How do devices know which devices to send to and which devices should recieve?
- every device should have an IP

we have **mac address** comes with network card. **unique internationally**

when I send a message through to an IP. Send the mac addresses as well in it.

we have HTTP and HTTPS

if we use HTTP in sensitive operations. anyone could sniff the data being sent. HTTPS is encrypted and is decided to use between  the two devices

yahoo.com is external not internal in the networl

router has a device inside that transfers you from internal network to external network

has two NIC, **internal** and **external**

how does the router know the IP of Yahoo.com? **DNS server**


Network
	Collection of computers, other deices and preipherals connected together through connecting media to perform certain task
resources
- file sharing
- devices sharing
- software sharing / multi-user license
- voice and video calls
- shared internet access

## 2.1	topology
### 2.1.1	star topology
most relevant
switch in the middle
![[Pasted image 20241112093728.png]]
not the fastest
### 2.1.2	ring
faster
![[Pasted image 20241112093748.png]]
if a device falls or more than 60 then critical

### 2.1.3	mesh
![[Pasted image 20241112093826.png]]
any device can be reached directly
high cost
used in back

### 2.1.4	hybrid
![[Pasted image 20241112093901.png]]

## 2.2	covered area
### 2.2.1	PAN

personal network between his devices like:
- phone and bluetooth device
- phone and laptop
### 2.2.2	LAN
local area network
connected with a switch in a small geographical area

**Domain controller** controls peripherals people use
reduce cost, how?
- updates for example. update 500 MB. if each device downloads it then it multiplies. we could make a server get the update and then copies it to the devices
so:
- high speed
### 2.2.3	WAN
if the network expands to other geographical areas then we are using WAN
wide area network

very slow speed

ISP gives you the service or not?
internet is network of networks
global mesh of connected networks

![[Pasted image 20241112094656.png]]

world is connected in internet using submarine cables of fiber optics. 

Egypt is the connecting hub that has a lot of submarine cables that connect the east and the west.

submarine cabes could get severed because of fishing lines, terrorist attacks, earchquakes, etc.

satallite internet could be intercepted or distorted.

if one company becomes ISP (like starlink wants to do) then **one controls internet**

## 2.3	network model
### 2.3.1	peer to peer
everyone is standalone and no central control on the network
not used in corporations
### 2.3.2	client to server
server applies service to clients all over the organization, this requires:
- more powerful hardware
- server os like windows server

## 2.4	protocols
### 2.4.1	why we need them
to communicate efficiently
ISO came in 1983 introduced the OSI model protocol that defines how data is transfered in a network

based on it we created a protocol called
### 2.4.2	TCP protocol
standard and not controlled by anyone
- TCP/IP v4
- TCP/IP v6
![[Pasted image 20241112100551.png]]
int he application layer in TCP opens session presents the data and applicates the data.

presentation layer could compress data to send it

transport layer cuts the data into different packets to send it.

when we send it we use the internet layer to determine source ip to destination ip

datalink layer and physical source mac and destination mac

physical was introduced again into TCP because there are not multiple forms of physical representation of data like wifi, ethernet, fiber, and others

mac address first half second half #iti/inquire/network 
You could randomize mac address that could bypass mac blocking

you could do a white list of mac addresses you own and register them on router so that nobody uses your network.

### 2.4.3	IP Internet Protocol
![[Pasted image 20241112102140.png]]

255 is reserved for broadcast
0 is reserved for network

![[Pasted image 20241112102527.png]]

ip was seperated into multiple public IP classes. 
A 16 million devices
B 60 thousand
C ???
private IP addresses that are local
A 10.0.0.0 to 10.255.255.255
B 172.16.0.0 to 172.31.255.255
C 192.168.0.0 to 192.168.255.255

ISP gives you real ip

ISP changes IP address periodically for security

IP v4 works with all people even though it is limited because ips are private and public
DHCP server is the one that serves addresses to devices in a network

![[Pasted image 20241112105147.png]]
if a device connects without DHCP server present then APIPA gets assigned so that internal devices could communicate

```
ipconfig /release
ipconfig /renew
```

we use `ping` to test connictivity between devices

#iti/inquire/network review in recording the part about ttl in 2:30:00


we use ping to make sure our connection with every packet is successful 
`ping <site> -t` indefinite
`ping <site> -n <# of times>`

ping is one of the most dangerous attack a hacker can use

Denial of service could be used with ping
`ping <site> -l 5000`
max value is 65500

if i want to attack a site like yahoo you could use 20000 and -t
Denial of Service attack (DoS)
if we use multiple devices to do this then
Disctributed Denial of Service attack (DDoS)

ICMP

ARP protocol fills destination MAC address with FFFFFFF. when the destination device replies then the source device gets the MAC address from the destination device

arp table is temporary
sometimes hackers use arp poisoning

ARP broadcast 2:50:00 #iti/inquire/network 

V6

128 bit addresses 340 billion billion billion billion addresses

isn't endorsed by ICANN

MAC address is only shared **inside** networks

IoT

a big problem in IoT is cybersecurity

Transport layer

![[Pasted image 20241112113445.png]]

3:08:00 #iti/inquire/network UDP

![[Pasted image 20241112114722.png]]

Port num

65535 port in NIC to recieve service from

1023 known port number and registered protocol
80 http
443 https
shodan.io to know websites from IP address #iti/funfact/network 
close and open ports in firewalll

127.0.0.1 self IP
loopsback on self

goes out from a port and goes back on a different port

browser is URL
![[Pasted image 20241112114934.png]]

TLD
- com
- net
- org
- etc.
NTLD
- online
- art
- shop
- ink
- site
- co
- space

`netstat -n` to check ports
`nsloopup` to check DNS and lookup ip of websites

yahoo has multiple IPs and appears in nslookup

Google has multiple server but when you lookup server it only gives back one ip depending on which one is fastest to respond

### 2.4.4	FTP

4:47:00 and implementation of network fundamentals #iti/inquire/network 

why back up on local server instead of public cloud like google cloud?
why did the provider do it for free?
do they have you data privacy best interest in mind?

Datacenter
- physical security, not anybody can get in
- lights cannot go out. multiple lines and ups
- internet out? no wouldn't go out multiple ISP
- A/C no more than 16 degrees
- managed remotely with authentication
use protocol telnet to connect on the server using port 23, ==but isn't not encrypted== on the way to the server and username and password could be sniffed.
- use instead protocol SSH for encryption
if you want GUI windows has RDP protocol remote desktop protocol

why use protocols instead of teamviewer or anydesk?
### 2.4.5	mail protocols
#### 2.4.5.1	SMTP send mail transfer protocol
in a corporation you cannot use personal email. you use mail from local mail server
we use 

#### 2.4.5.2	IMAP
imap v4

read mail from the server
to read you have to be connected

#### 2.4.5.3	POP
POP v3

everytime you access mail it gets downloaded and server storage is reset when you download

# 3	cyber security
![[Pasted image 20241112134241.png]]

cybersecurity is a subset under information security

md5 checksum should be used to check integrity of files downloaded from sites

if we achieve CIA then we achieve cybersecurity

![[Pasted image 20241112134748.png]]

![[Pasted image 20241112135054.png]]
to avoid cookies then use incognito or VM

![[Pasted image 20241112135728.png]]
device backs up data in event viewer and hacker deletes this data to cover tracks. that's why cyber forensics need to backup event viewer

great explanation in social engineering 5:30:00 #iti/funfact/network also use virustotal.com

insider attacks are more dangerous than outsider attacks because insiders have more permissions than outsiders

![[Pasted image 20241112143859.png]]

registry files contact with memory (??)

virus doesn't spread on the network

worm spreads on the network

![[Pasted image 20241112145924.png]]
![[Pasted image 20241112150155.png]]

## 3.1	firewall
blocks traffic inbound or outbound based on rules that you set
### 3.1.1	static firewall
manual firewall that should be configured manually
### 3.1.2	dynamic firewall
nobody communicates with pc from the outside
state table revises if data that is coming is coming due to request from inbound or is coming on its own.

### 3.1.3	IDS / IPS
check in 7:45:00 #iti/inquire/network 
![[Pasted image 20241112164903.png]]
### 3.1.4	NGFW
FW + IPS
very expensive

### 3.1.5	DMZ

isolated place where server exists
## 3.2	Encryption
### 3.2.1	Asymmetric
creates two keys to for the cipher.  public key and private key which exists with only the user
# 4	distributed systems
![[Pasted image 20241112170956.png]]
![[Pasted image 20241112171028.png]] 

![[Pasted image 20241112172323.png]]
![[Pasted image 20241112172643.png]]