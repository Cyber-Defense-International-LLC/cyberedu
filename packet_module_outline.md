## 3) Basic Packet Inspection (18) (V)
   * Students will learn the framework of data packets, how to interpret fields and headers within a data packet and how to identify potentially malicious activity via packet inspection. (3 nights per week)
   * one week , two sessions

## module outline
* Packet captures : recording of network activity
  * uses network forensics techniques
    * Ideally a complete recording of the network communications between two or more systems
    * In binary so we use analysis tools to interpret the data
  * used in IT and network operations
    * Network troubleshooting , application traffic verification
      * after "can you ping it?"
      * "what answer do you get?"
    * Learning about network traffic
      * What protocols is this new device using?
      * Is this login really encrypted?
  * used in security analysis (red, blue, purple, etc) and troubleshooting
    * blue: intrusion analysis and incident response
      * Is this system compromised, did they steal private data?
    * red: vulnerability analysis and exploit development, testing
      * Did I send enough As to the open port? Is it a shell yet?
    * purple (red + blue working together):  
      * Blue team, can you see when I do this (attack)? *click* How about now?

* (how to get packets, the really simple version)
  * taps: hardware or software

* sockets ... Internet network "tubes" with numbers on both ends
  * source IP: source port -> destination IP, destination port

* encapsulation and layers
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

* Wireshark for decoding of packets by layer and protocol
* Wireshark usage introduction, tips

## idea bin
Intrusion analysis -> investigation questions and worksheet ,ala Wireshark prez
  * http://dfirfiles.net/myslides/Event_Analysis_worksheet.pdf
  * stimulus and response

Forensics Science -> core principles: like evidence integrity, strong repeatable processes, and documentation

