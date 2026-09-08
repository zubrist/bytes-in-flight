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