## What IP address appears most frequently in the Source or Destination columns? What device is it?

From scrolling around the packet list, I found that the IP address 10.****** appears in the Destination column most frequently, and for the Source column it’s between quite a few addresses. 10.****** is the IP address for my device I am using to complete this lab, and the source IP addresses are from the servers I’m connecting to when I access my.utsa.edu and click on various links on the website.
 <img width="780" height="227" alt="Picture1" src="https://github.com/user-attachments/assets/60748a56-5f83-40e0-8d4e-86da45dea13e" /><br>
### Figure 1: The packet list pane displaying frequently appearing IP addresses.


## Which protocol appears most frequently in the Protocol column? What is the purpose of this protocol?

I found that the TCP appears the most when looking at network traffic protocols within the column. TCP assures that data that’s being delivered between a host and end user is properly delivered, with information readily available if an issue with the transfer of data over a network protocol was to exist.
 
### Figure 2: The packet list with TCP appearing most frequently.


## Identify the OSI model layers corresponding to rows 2, 3, and 4 in the Packet Details pane.

After selecting a packet and viewing the packet details pane I found that row 2 is the data link layer, row 3 is the network layer, and row 4 is the transport layer. Row 2 shows “Ethernet II” the method of data linking, row 3 shows I’m connected to the network through IPv6, and row 4 shows TCP as the protocol used to transport data.
 
### Figure 3: Wireshark showing packet details for a DNS response.


## Locate a DNS query. What domain name was being resolved, and what IP address was returned?

To locate a DNS query, I clicked the Protocol column title to filter all the traffic by protocols. I found a DNS query packet that contained the my.utsa.edu domain and expanded the fields in the packet detail pane to learn more. I found that the domain www.utsa.edu and 129.****** were being returned. I found this under the Domain Name System (response) section, and the Queries and Answer subsection allowed me to obtain this information.
 
### Figure 4: A selected packet that's a DNS query.



## What is the MAC address of your local machine as shown in the Ethernet frame? Why is this important at OSI Layer 2?

To find my MAC address, I decided to use the same DNS query from step 4 and decided to expand the frame that says “Ethernet II”. Once I did, I saw my MAC address in the Source field contained in the Ethernet frame. The importance of the MAC address is that it provides an identifier for an individual device and another device that handles networking of devices to identify it correctly when data is sent. The MAC addresses allow for when components of the data link layer allow devices to interact, the identification of individual devices making connections is done properly.

### Figure 5: The packet details pane displaying MAC addresses for a DNS query.

Apply a display filter (e.g., http, dns). What did you observe about the traffic for that protocol?

Using the documentation provided in the hyperlink, I added a DNS displayed filter. This resulted in being able to see a clearer list of DNS responses, which allows me to see quite a lot of domains and IP addresses as I scrolled down. Some were known domains such as my.utsa and others were DNS services like CloudFlare. Some of these requests were routing these domains to specific IP addresses, which is the purpose of DNS. Through WireShark I was able to capture a moment of network traffic and see different protocols and information that show how data is transmitted and how it can be recorded and analyzed.
 
### Figure 6: Viewing the packet list with a DNS display filter.
