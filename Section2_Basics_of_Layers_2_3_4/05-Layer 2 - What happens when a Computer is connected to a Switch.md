- Let's assume we have a computer with a network interface card or a NIC, and that NIC has a MAC address hardcoded to it.
- And so this MAC address is always going to be associated with this network interface card. 
- And now, we wanna connect this computer to an Ethernet switch.
- And the Ethernet switch has a bunch of physical ports. I have numbered them 1 through 8,
- We're going to take our network interface card and connect it with the cable to one of the ports on this Ethernet switch.
- And when this computer generates any type of traffic, that traffic is now going to be received by the Ethernet switch.
- And the Ethernet switch will then create an entry in its MAC address table, and the entry in the MAC table
will look something like this. It'll contain the MAC address of this computer, and it will assign the necessary port number to it.
- So this computer is connected to port 1, and this computer has this MAC address.
- Therefore, the MAC table now associates that MAC address with that port.
- And if the Ethernet switch receives traffic that is destined for that MAC address on some other port, it'll refer to its MAC table and it'll send that traffic out the appropriate port.
- And the entries in the MAC table, these are temporary in nature.
- They're going to have an aging timer where typically the entry will only remain for a few minutes if no frames are received on that port.
- So if this computer gets shut down for an extended period of time, there's not gonna be any traffic on that port, and the entry will be removed from the MAC table.
- But as soon as this computer starts sending traffic again, the entry will be rebuilt.
- And by the way, there could potentially be multiple MAC addresses for one particular port.
- So for example, let's imagine that another Ethernet switch is connected to port 8 on this Ethernet switch,
while all of the MAC addresses that are connected to the second switch are going to be reachable from the first switch through port 8.
- So the MAC address table in this switch will reflect that. It'll show all of the MAC addresses that it learns.
- So as traffic, let's say, comes from port 4 and ends up going to this other switch, now the switch on top is going to learn, "Hey, "I just got traffic from a specific MAC address "on port 8. "Let me add that address to the MAC table "and build out the contents of the MAC table."
- So a single switch port can map to multiple MAC addresses if it's connected to another network device, like a hub or another switch.
- And so by learning the MAC addresses on each port and forwarding frames only to the correct port, the switch will reduce unnecessary traffic and make a network more efficient than it would be if we used something like a hub.
# Summary
- Every switch has a MAC address table, and the MAC table is going to associate or map a MAC address to a port. 
- So when a switch receives traffic on a specific port, it will notice the MAC address and it will map that MAC address to that port, so it knows how to send traffic to that MAC address.
- And we have situations where multiple MAC addresses could be associated with a single switch port. This happens if you connect another network device, like a switch or a hub to a switch port.
- We also learned that entries in a MAC table are temporary. So for example, if I remove a computer or disconnect it from a switch, eventually, that entry in the MAC table will time out and be automatically removed.