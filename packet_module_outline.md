
# Basic Packet Inspection : Ben K
* LO: Students will learn the framework of data packets, how to interpret fields and headers within a data packet and how to identify potentially malicious activity via packet inspection. 
* one week , two sessions => 4 hours "live" synchronous contact

1. _bridge protocols and applications into packets and network analysis (from NFA and NSM)_
2. network analysis basics and pcap introduction
3. Wireshark, the canonical protocol analyser
4. Learning about protocols with Wireshark
5. Answering infosec questions with packets and Wireshark
6. References / Do You Want to Know More?


## 1 [bridge in: connect with previous module LOs]
* Packets: tiny messages in pieces, each piece has layers
 * ( Ethernet frames, segments, datagrams )
* Sockets ... Internet network "tubes" with numbers on both ends
  * source IP: source port -> destination IP, destination port
* Protocols: languages used for communication, defined (mostly) by standards

* Layers -> Encapsulation 
* each layer serves a purpose and tells you about the next layer
* have to examine multiple layers to understand the traffic and answer questions 
* EG Web traffic is commonly: Ethernet : IP : TCP : HTTP
  * but DNS might be Ethernet : IP : UDP : DNS

```
Ethernet : Source and destination network "card" MAC addresses and protocol number
IP: Source and Destination IP, Hop Count, checksums ...
TCP: source and destination ports, handshake synchronisation numbers, checksum, flags
HTTP: application layer data like ```GET / HTTP 1.1 host:forensicswiki.xyz```
```

## 2 network analysis basics and pcap introduction
* Packet captures : recording of network activity : files full of packets recorded from a network
    * (uses network forensics tools and techniques)
    * Ideally a complete recording of the network communications between two or more systems
    * In binary ( 0s and 1s ) so we use analysis tools to interpret the data
      * Learn the binary / hex to trust/check your tools and understand evidence fully
* (how to get packets, the really simple version)
  * taps: hardware or software
    * really simple version in Wireshark **<-- in class**
    * more sophisticated: Stenographer, Moloch, Security Onion 
  * pcap files : libpcap & PCAP NG <- in class
  * inspect live traffic with network intusion detection systems (IDS) like Snort, Suricata, and Zeek
* used in IT and network operations
  * Network troubleshooting , application traffic verification
    * after "can you ping it?"
    * "what answer do you get?"
  * Learning about network traffic
    * What protocols is this new device using?
    * Is this login really encrypted? **<-- in class**

## 3 Wireshark
   * Wireshark basics and safety rules

## 4 Learning about protocols with Wireshark

## 5
* used in security analysis (red, blue, purple, etc): troubleshooting++
  * blue: intrusion analysis and incident response
    * Is this system compromised, did they steal private data?
    * What does this attack technique look like "on the wire"?
  * red: vulnerability analysis and exploit development, testing
    * Did I send enough As to the open port? 
    * Do I have a shell yet?
  * purple (red + blue working together):  
    * Blue team, can you see when I do this (attack)? *click* How about now?

## 6 : Outlinks
* Wireshark.org (Riverbed)
  * libpcap , snort, suricata, zeek
* Laura Chappel books and Chris Sanders (& Jason?) PPA
* Infosec books: PNSM, ANSM
* Malware Traffic Analysis (MTA) and other challenges (honeynet archive)
* OST.info: (network flow analysis)
* SANS SEC503, SEC511, FOR572

