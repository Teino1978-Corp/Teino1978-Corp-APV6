

**Insertion Attack**

The IDS does not know that the end-system would reject that packet. Then the attacker can for example insert blinders within a malicious string (sent byte by byte).
The IDS would accept all bytes and recognizes the string as harmless
The host only accepts those bytes that belong to the malicious
sequence

When UDP is used, the blinders could be data-grams with wrong checksum (which are only dropped by the destination host). Widespread vulnerability! Therefore also the IDS must check the checksum of each packet, etc. . .
Insertion---The IDS gets more packets than the destination.



**Evasion**

If the IDS is more strict, then this could lead to evasion attacks:
For example, if the malicious sequence is sent byte-by-byte, and one byte is rejected by the IDS, the IDS cannot detect the attack. Generally, the IDS rejects packets, the victim does not.
Evasion: The IDS gets less packets than the destination.


**Denial-of-Service**

An adversary can evade detection by disabling or overwhelming the IDS. This can be accomplished by exploiting a bug in the IDS, using up computational resources on the IDS, or deliberately triggering a large number of alerts to disguise the actual attack. The tools 'stick' and 'snot' were designed to generate a large number of IDS alerts by sending attack signatures across the network, but will not trigger alerts in IDSs that maintain application protocol context.



**Obfuscation**

An IDS can be evaded by obfuscating or encoding the attack payload in a way that the target computer will reverse but the IDS will not. In the past, an adversary using the Unicode character could encode attack packets that an IDS would not recognize but that an IIS web server would decode and become attacked.
subsequent avoidance of such can lead to a successful intrusion

**False Positive Generation**

This mode does not actually attack the target. This is to deliberately trigger a false  IDSs alarm. This will cause the IDS to generate a large number of false detection reports. This is aimed at creating network "noise" in order to disguise malicious network activity.

**Session Splicing**

Session splicing is an IDS evasion technique that exploits how some IDSes do not reconstruct sessions before performing pattern matching on the data. This is a network-level evasion tactic that divides the string across several packets. The data in the packet is divided into small portions of bytes in order to evade signature detection. Many IDSes reassemble communication streams, so if a packet is not received within a reasonable amount of time, many IDSes stop reassembling and handling that particular stream. 

**Unicode Evasion Technique**

Unicode is a character representation that gives each character a unique identifier for each written language to facilitate the uniform computer representation of each language. This is an issue for IDS technology because it is possible to have multiple representation of a single character.

**Fragmentation Attack**

Attackers break the single Internet protocol data-gram into multiple packets of small size. IDS fragmentation reassembly timeout is less than fragmentation reassembly timeout of the victim.

**Overlapping Fragments**

An IDS evasion technique is to craft a series of packets with TCP sequence numbers configured to overlap. In an Overlapping fragment attack the packet start in the middle of another packet.

**Time-to-live attacks**

Each IP packet has a field called Time to Live(TTL), which indicates how many more hopes the packet should be allowed to make before being discarded or returned. Each router along a data path decrements this value, by one. When a router decrements this value to zero, it drops the packet and send an ICMP alert notification. The attacker breaks into this fragment and reassemble will remaining undetected by the IDS.

**Invalid RST packets**

The TCP protocol use checksum to ensure that communication is reliable. A checksum is added to every transmitted segment and it is checked at the receiving end. When a checksum differs from the checksum expected by the receiving host the packet is dropped at the receiver's end. Attackers can use this feature to elude detection by sending 
RST packets with an invalid checksum, which causes the IDS to stop processing the stream because the IDS thinks the communication session has ended.

**Polymorphic Shell code**

Most IDSes contain signatures for commonly used strings within malicious shellcode. This is easily bypassed by using encoded shellcode containing a stub that decodes the shellcode that follows. This hides the actual shellcode, making signature detection almost useless.


**ASSCI Shell code**

ASSCI shellcode contains only characters contained within the ASCII standard. This form of shelcode allows attackers to bypass commonly enforced restrictions within string input code. It also helps attackers bypass IDS pattern matching signatures because strings are hidden within the shellcode in a similar fashion to polymorphic shellcode.


### Additional Types of Evasion

**Encryption**

When the attacker has already established an encrypted session within the victim, it results in the most effect evasion attack.

**Flooding**

The attackers send loads of unnecessary traffic to produce noise, and if the IDS does not analyze the traffic properly, it may slip by undetected.