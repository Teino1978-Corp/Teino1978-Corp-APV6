### Step 1: Disable a trusted host

You should try to find and disable the trusted host so that the targeted host thinks that the
traffic that the attacker will generate emanates from there.

### Step 2: Perform an insertion attack

### Step 3: Implement the evasion technique

### Step 4: Perform a denial-of-service attack

### Step 5: Obfuscate or encode the attack payload

You should implement the obfuscating technique to encode attack packets that the IDS would
not detect but an liS web server would decode and be attacked.

### Step 6: Perform the false positive generation technique

You should use the false positive generation technique to create a great deal of log "noise" in
an attempt to blend real attacks with the false.

### Step 7: Perform the Session Splicing Technique 

You should implement the session splicing technique to stop the IDS by keeping the session
active longer than IDS will spend on reassembling it.

### Step 8 : Perform the Unicode evasion technique

You should implement the Unicode evasion technique to evade IDSes as it is possible to have
multiple representations of a single character.

### Step 9: Perform a fragmentation attack

### Step10: Perform the overlapping fragments technique

You should use overlapping fragments technique to craft a series of packets with TCP
sequence numbers configured to overlap.

### Step 11: Perform a Time-To-live attack

### Step 12: Perform the invalid RST packets technique

You should use the invalid RST packets technique to evade detection by sending RST packets
with an invalid checksum that causes the IDS to stop processing the stream.

### Step 13: Perform the urgency flag technique

You should use the urgency flag technique to evade IDSrd as some IDSrds do not consider the
TCP protocol's urgency feature.

### Step 14 : Perform the polymorphic shellcode technique

You should use the polymorphic shellcode technique to hide the shellcode by encrypting it in a
simplistic form that is difficult for IDS to identify that data as a shellcode.

### Step 15: Perform the ASCII shellcode technique

You should perform the ASCII shellcode technique to bypass IDS pattern matching signatures
because strings are hidden within the shellcode as in a polymorphic shellcode.

### Step 16: Perform an Application-layer attacks

You should try to perform Application-level attacks as many lOSes will have no way to check the
compressed file format for signatures.

### Step 17: Perform encryption and flooding techniques

You should try encryption and flooding attacks with the victim or send loads of unnecessary
traffic to produce noise that can't be analyzed by the IDS.

### Step 18: Perform a post-connection SYN attack

### Step 19: Perform a pre-connection SYN attack

### Step 20: Document all the results obtained from this test

You should perform a fragmentation attack with IDS fragmentation reassembly timeout less
and more than t hat of the victim.