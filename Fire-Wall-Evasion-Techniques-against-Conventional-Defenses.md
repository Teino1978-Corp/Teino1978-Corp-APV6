## Bypassing a Firewall through the ACK Tunneling Method

ACK tunneling allows tunneling a backdoor application with TCP packets with the ACK bit set.
The ACK bit is used to acknowledge receipt of a packet. Some firewalls do not check packets
with the ACK bit set because ACK bits are supposed to be used in response to legitimate traffic
that is already being allowed through. Attackers use this as an advantage to perform ACK
tunneling. Tools such as AckCmd (http://ntsecurity.nu) can be used to implement ACK
tunneling.


## IP Address Spoofing

IP address spoofing or IP spoofing is one of the ways that an attacker tries to evade
firewall restrictions. IP spoofing is a technique where the attacker creates Internet protocol
packets by using a forged IP address and gains access over the system or network without any
authorization. The attacker spoofs the messages and they appear to be sent from a reliable
source. Thus, the attacker succeeds in impersonating others' identities with help of IP spoofing.

This technique is used to hide their true attack.

## Source Routing

Using this technique, the sender of the packet designates the route that a packet
should take through the network in such a way that the designated route should bypass the
firewall node. Using this technique the attacker can evade the firewall restrictions.
When these packets travel through the nodes in the network, each router will check the IP
address of the destination and choose the next node to forward them.

## Tiny Fragments

The attacker uses the IP fragmentation technique to create extremely small
fragments and force the TCP header information into the next fragment. This may result in a
case whereby the TCP flags field is forced into the second fragment, and filters will be unable to
check these flags in the first octet thus ignoring them in subsequent fragments.
Attackers hope that only the first fragment is examined by the filtering router (firewall) and the
remaining fragments are passed through. This attack is used to avoid user defined filtering rules
and works when the firewall checks only for the TCP header information.

## Bypass Blocked Sites Using IP Address in Place of URL

You can also evade firewall restrictions by typing the IP address of t he blocked site instead of
its domain names. This allows you to access the restricted or blocked sites. You need to use
some tools to convert the target domain name into its IP address.

## Bypass Blocked Sites Using Anonymous Website Surfing Sites.

Anonymous website surfing sites help you to surf the Internet anonymously and to unblock
blocked sites. i.e., evade firewall restrictions. By using these sites, you can surf restricted sites
anonymously, i.e., without using your IP address on the Internet. There are a number of
anonymous website surfing sites available on the Internet. Some websites provide options to
encrypt the URLs of websites.

http://proxify.com

http://anonymouse.org

http://hiemyass.com

## Bypassing a Firewall through the ICMP Tunneling Method

**By using a proxy server, you can also bypass the firewall restriction imposed by a**
**particular organization. To evade t he firewall restrict ions using a proxy server, follow these**
**steps:**

1. Find an appropriate proxy server.

2. On the Tools menu of any Internet browser, go to LAN of Network Connections tab, and
then click LAN/Network Settings.

3. Under Proxy server settings, select t he use a proxy server for the LAN.

4. In the Address text box, type the IP address of the proxy server.

5. In the Port text box, type t he port number t hat is used by the proxy server for client
connections (by default, 8080).

6. Click to select the bypass proxy server for local addresses check box if you do not want
the proxy server computer to be used when connected to a computer on the local
network.

7. Click OK to close the LAN Settings dialog box.

8. Click OK again to close the Internet Options dialog box.

## Bypassing a Firewall through the ACK Tunneling Method

ICMP tunneling allows tunneling a backdoor shell in the data portion of ICMP Echo packets. RFC
792, which delineates ICMP operation, does not define what should go in the data portion . The
payload portion is arbitrary and is not examined by most of the firewalls, thus any data can be
inserted in the payload portion of the ICMP packet, including a backdoor application. Some
administrators keep ICMP open on their firewall because it is useful for tools like ping and
traceroute.

## Bypassing a Firewall through the HTTP Tunneling Method

This method can be implemented if the target company has a public web server with port 80
used for HTTP traffic, that is unfiltered on its firewall. Many firewalls do not examine the
payload of an HTTP packet to confirm that it is legitimate HTTP traffic, thus it is possible to
tunnel traffic inside TCP port 80 because it is already allowed.

## Bypassing a Firewall through a MITM Attack

**The following steps illustrate an example scenario of how an attacker bypasses a firewall through an MITM attack:**

1. Attacker performs DNS server poisoning.

2. User A requests WWW.juggyboy.com to the corporate DNS server.

3. Corporate DNS server sends the IP address (127.22.16.64) of the attacker.

4. User A accesses the attacker's malicious server.

5. Attacker connects with t he real host and tunnels the user's HTTP traffic.

6. Attacker inserts malicious payload into t he requested web page (Java applet), and thus
the attacker's code is executed on the user's machine.

## Bypassing a Firewall through External Systems

**Attackers can bypass firewall restrictions through external systems **

1. Legitimate user works with some external system to access the corporate network.

2. Attacker sniffs the user traffic, and steals the session ID and cookies.

3. Attacker accesses t he corporate network bypassing the firewall and gets Windows ID of
the running Netscape 4.x/ Mozilla process on user's system.

4. Attacker then issues an openURL() command to the found window.

5. User's web browser connects with the attacker's WWW server.

6. Attacker inserts malicious payload into the requested web page (Java applet) and thus
the attacker's code gets executed on t he user's machine.