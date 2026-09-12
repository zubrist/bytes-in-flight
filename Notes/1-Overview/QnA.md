## 1. ```[2021 General - Q1(c)]``` Write the differences between half duplex and duplex transmission?
> **Half-Duplex Mode:** In this mode, each station can both transmit and receive, but not at the same time. The entire capacity of the channel is taken over by whichever of the two devices is transmitting at that instant . A common example is a walkie-talkie

> **Full-Duplex (Duplex) Mode:** In this mode, both stations can transmit and receive simultaneously. Signals going in opposite directions share the capacity of the link, which can occur by having two physically separate transmission paths or by dividing the overall capacity of the channel. A common example is the telephone network

---
## 2. ```[2022 Honours - Q3(e)] / [2018 General - Q1(a)]```  For $n$ devices in a network, what is the number of cable links required for a mesh topology?
- In a fully connected mesh topology, every device has a dedicated point-to-point link to every other device5.
- For $n$ devices (nodes), the total number of physical duplex-mode links required is calculated using the formula: $$\text{Total Links} = \frac{n(n - 1)}{2}$$
- Additionally, each device on this network must have $(n - 1)$ input/output (I/O) ports
---
## 3. ```[2021 Honours - Q6(b)]``` What are the advantages and disadvantages of STAR topology?
> Advantages:
- Lower Cost & Less Cabling: It is less expensive than a mesh topology because each device requires only one link and one I/O port to connect to the central hub.
- Easy Installation & Reconfiguration: It is easy to install and reconfigure since moves, additions, or deletions of devices involve only a single connection between that device and the hub.
- Robustness: If one link fails, only that specific link is affected. All other devices remain fully operational.
- Easy Fault Isolation: Centralization makes it easy to identify and isolate faults.
> Disadvantages:
- Single Point of Failure: The entire network is completely dependent on the central controller (hub). If the central hub fails, the entire network drops and all systems go down.
---

## ```[2022 General - Q1(g)]``` Mention two advantages of Star topology.
1. **Robustness:** If a single link between a node and the central controller fails, only that node is disconnected; the rest of the network continues to function.
2. **Ease of Reconfiguration:** Adding, moving, or deleting network devices only requires changing a single connection to the central hub, avoiding disruptions to other nodes.
---

## ```[2022 General SEC-A-X-I - Q1(j)] / [2021 General - Q7(b)]``` What do you mean by multipoint communication / What are the differences between point to point and multipoint connections?

- Point-to-Point Connection: Provides a dedicated link between exactly two devices . The entire capacity of the link is reserved exclusively for transmission between those two devices .
- Multipoint (Multidrop) Connection: A single physical link is shared spatially or temporally by three or more specific devices . If devices use the link simultaneously, it is spatially shared; if they must take turns, it is *timeshared*.

---

## ```[2021 Honours - Q1(a)] / [2022 General SEC-A-X-I - Q3(a)]``` Highlight the main differences between LAN and WAN.

**Geographic Coverage:** A Local Area Network (LAN) normally covers a highly limited area of less than 2 miles, such as a single room, building, or campus . A Wide Area Network (WAN) spans a vast geographic area, such as a country, continent, or the entire world

**Ownership:** LANs are typically privately owned by the organization that owns the attached devices. WANs are normally leased from or run by common carriers or public multi-carrier infrastructures. 

**Data Rates:** LANs have extremely high internal data rates, normally operating at speeds of 100 Mbps or 1000 Mbps . WANs traditionally have lower data rates relative to the distances covered .

**Media and Topology:** LANs use a single type of transmission medium and follow structured topologies (primarily star, bus, or ring). WANs use complex switching nodes (routers) interconnected by circuit-switched or packet-switched technologies .
---
## ```[2022 General SEC-A-X-I - Q5(c)]``` What is ARPANET?
- ARPANET was developed in 1969 by the Advanced Research Projects Agency (ARPA) of the U.S. Department of Defense.
- It was the first operational packet-switching network.
- Initially, it connected host computers across four original locations (UCLA, UCSB, SRI, and the University of Utah) using specialized communication devices called Interface Message Processors (IMPs).
- It served as the direct predecessor and foundation of the modern global Internet.
---
## ```[2021 Honours - Q1(b)]``` Name the different layers of TCP/IP protocol.

The standard TCP/IP protocol suite used in modern networks is organized into five layers:
1. Physical Layer
2. Data Link Layer (or Network Access/Data Link Layer)
3. Network Layer (or Internet Layer)
4. Transport Layer (or Host-to-Host Layer)
5. Application Layer (or Process Layer)
---
##  ```[2021 Honours - Q5(a)]``` Name the layers of the OSI model. Briefly state their functions.
The OSI model is a layered theoretical framework containing **seven distinct layers**:
1. **Physical Layer (Layer 1):** Coordinates the mechanical, electrical, and functional specifications to transmit raw bit streams over a physical transmission medium .
2. **Data Link Layer (Layer 2):** Packages raw bits into manageable units called frames and ensures error-free hop-to-hop (node-to-node) delivery using physical addressing (MAC).
3. **Network Layer (Layer 3):** Manages source-to-destination packet delivery, logical addressing (IP), and routing across independent networks.
4. **Transport Layer (Layer 4):** Guarantees reliable process-to-process (end-to-end) delivery of the entire message, managing flow control and error control at the source-to-destination level.
5. **Session Layer (Layer 5):** Establishes, maintains, synchronizes, and terminates communication sessions and dialogue controls between processes.
6. **Presentation Layer (Layer 6):** Standardizes data syntax and semantics by handling translation between differing data representations, encryption/decryption, and data compression.
7. **Application Layer (Layer 7):** Provides direct user interfaces and software support for distributed services like e-mail, file transfer, and web browsing.
---

## ```[2021 General - Q4] / [2023 General - Q3(e)]``` Write down the differences between OSI and TCP/IP models.
- **Development Order:** The OSI reference model was devised before its corresponding protocols were written. The TCP/IP model was written as a description of an already existing protocol suite.
- **Layer Count:** The OSI model defines 7 layers , whereas the TCP/IP model defines 4 or 5 layers.
- **Presentation & Session Services:** OSI has independent, explicitly defined Presentation and Session layers. In TCP/IP, these functionalities are integrated directly into a single Application layer.
- **Practical Usage:** The OSI model is used primarily as a reference and teaching tool. The TCP/IP suite is the dominant practical protocol suite deployed worldwide across the global Internet
---

## ```[2022 General SEC-A-X-I - Q1(k)]``` Differentiate between logical address and physical address of a device.
- **Physical Address (Link Address):**
    - Defined by the local network (LAN or WAN) to identify a node within its local jurisdiction .
    - Imprinted on the Network Interface Card (NIC).
    - Its format and size depend on the network technology (e.g., Ethernet uses a 48-bit/6-byte address).
- **Logical Address (IP Address):**
    - Uniquely and universally defines the connection of a device to the global Internet.
    - Used by the network layer to route packets across multiple network boundaries.
    - It is universally unique  and is currently 32 bits (IPv4) or 128 bits (IPv6) in length
    ---

## ```[2021 Honours - Q7(b)]``` What is process to process delivery? Explain with suitable example.   
- Process-to-process delivery is the transport layer responsibility of ensuring that an entire message is delivered from a specific running program (process) on the source host to the correct running program (process) on the destination host.
- While the network layer delivers packets from host to host, it treats them independently. The transport layer recognizes the relationship between those packets and ensures they arrive intact and in order.
- Example: When a user runs a web browser client process to access a website, the transport layer delivers the data specifically to the web server process running on the host machine. This is achieved using port addresses (e.g., port 80 for HTTP, port 25 for SMTP e-mail, and port 53 for DNS).
