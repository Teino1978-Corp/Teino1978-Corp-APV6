### Countermeasures

* Administratively shut down a switch port interface associated with a system from which
attacks are being launched.

* Look for the nop opcode other than Ox90 to defend against the polymorphic shellcode
problem.

* Perform "bifurcating analysis," in which the monitor deals with ambiguous traffic
streams by instantiating separate analysis threads for each possible interpretation
of the ambiguous traffic.

* Maintain security vulnerability awareness, patch vulnerabilities as soon as possible, and
wisely choose the IDS based on t he network topology and network traffic received.

* Generate TCP RST packets to tear down malicious TCP sessions, any issues of several
available ICMP error code packets in response to malicious UDP traffic.

* Interact with the external firewall or router to add a general rule to block all
communication from individual IP addresses or entire networks.


* Implement a "traffic normalizer": a network forwarding element that attempts to
eliminate ambiguous network traffic and reduce the amount of connection state that
the monitor must maintain.

* Ensure that IDSs normalize fragmented packets and allow t hose packets to be
reassembled in t he proper order, which enables the IDS to look at the information just
as the end host can see it.

* Keep updating the IDS system and firewall software regularly.

* Maintain security vulnerability awareness, patch vulnerabilities as soon as possible, and
wisely choose the IDS based on the network topology and network traffic received.

* Change the TIL field to a large value, ensuring that the end host always receives the
packets. In such case, attackers cannot slip information to the IDS. As a result, that data
never reaches the end host, leaving the end host with the malicious payload.