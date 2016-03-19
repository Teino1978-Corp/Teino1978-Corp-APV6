The National Institute of Standards and Technology (NIST) 800-10 divides firewalls into three basic types:

**Packet filters:**

On the Internet, packet filtering is the process of passing or blocking packets at a network interface based on source and destination addresses, ports, or protocols. The process is used in conjunction with packet manglingand Network Address Translation (NAT). Packet filtering is often part of a firewallprogram for protecting a local network from unwanted intrusion.
n a software firewall, packet filtering is done by a program called a packet filter. The packet filter examines the header of each packet based on a specific set of rules, and on that basis, decides to prevent it from passing (called DROP) or allow it to pass (called ACCEPT).

There are three ways in which a packet filter can be configured, once the set of filtering rules has been defined. In the first method, the filter accepts only those packets that it is certain are safe, dropping all others. This is the most secure mode, but it can cause inconvenience if legitimate packets are inadvertently dropped. In the second method, the filter drops only the packets that it is certain are unsafe, accepting all others. This mode is the least secure, but is causes less inconvenience, particularly in casual Web browsing. In the third method, if the filter encounters a packet for which its rules do not provide instructions, that packet can be quarantined, or the user can be specifically queried concerning what should be done with it. This can be inconvenient if it causes numerous dialog boxes to appear, for example, during Web browsing.


**Stateful inspection:**

Stateful inspection has largely replaced an older technology, static packet filtering. In static packet filtering, only the headers of packets are checked -- which means that an attacker can sometimes get information through the firewallsimply by indicating "reply" in the header. Stateful inspection, on the other hand, analyzes packets down to the application layer. By recording session information such as IP addresses and port numbers, a dynamic packet filter can implement a much tighter security posture than a static packet filter can.
Stateful inspection monitors communications packets over a period of time and examines both incoming and outgoing packets. Outgoing packets that request specific types of incoming packets are tracked and only those incoming packets constituting a proper response are allowed through the firewall.

In a firewall that uses stateful inspection, the network administrator can set the parameters to meet specific needs. In a typical network, ports are closed unless an incoming packet requests connection to a specific port and then only that port is opened. This practice prevents port scanning, a well-known hacking technique.



**Proxy:**

That's an important distinction and it requires a little insight into the history of these devices. Proxy firewalls, or application gateway firewalls, are a fairly recent addition to mainstream security environments. Until a few years ago, the stateful inspection firewall was the most advanced firewall protection. While stateful firewalls can monitor open connections, they cannot inspect application layer traffic. Therefore, if you were to allow HTTP traffic through your firewall, a stateful inspection firewall would not prevent an HTTP-based attack. Proxy firewalls, on the other hand, combine stateful inspection technology with the ability to perform deep application inspections. They also analyze layer 7 protocols, such as HTTP and FTP and monitor traffic for additional signs of attack. To make this work, the firewall must act as a proxy; that is, the client opens a connection with the firewall (usually unbeknownst to the client) and the firewall opens a separate connection to the server on the client's behalf.

Proxy servers, however, don't provide the benefits of a firewall. Like proxy firewalls, they act as a middleman for connections, but they don't provide stateful inspection or other firewall technology. They're generally used to provide content filtering and performance enhancements (such as caching) for local user's Web traffic. Since most proxy firewalls can provide all of the benefits of a proxy server, administrators typically use dedicated proxy servers where they wish to remove the performance load from the firewall.

NIST Guidelines for Firewall Policy:[NIST FireWall Guidelines](http://csrc.nist.gov/publications/nistpubs/800-41-Rev1/sp800-41-rev1.pdf)