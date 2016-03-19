**Signature Recognition(misuse detection)**

It tries to identify events that indicate an abuse of a system. It is achieved by creating models of intrusions. Incoming events are compared with intrusion models to make a detection decision. While creating signatures, the model must detect an attack without disturbing the normal traffic on the system. Attacks, and only attacks, should match the model or else false alarms can be Generated

* The simplest form of signature recognition uses simple pattern matching to compare
the network packets against binary signatures of known attacks. A binary signature may
be defined for a specific portion of the packet, such as the TCP flags.

*  Signature recognition can detect known attacks. However, t here is a possibility that
other packets that match might represent the signature, triggering bogus signals.
Signatures can be customized so that even well-informed users can create them.

* Signatures that are formed improperly may trigger bogus signals. In order to detect
misuse, the number of signatures required is huge. The more t he signatures, the more
attacks can be detected, though traffic may incorrectly match with the signatures,
reducing the performance of the system.

* The bandwidth of the network is consumed with the increase in the signature database.
As the signatures are compared against those in the database, there is a probability that
the maximum number of comparisons cannot be made, resulting in certain packets
being dropped.

* New virus attacks such as ADMutate and Nimda create the need for multiple signatures
for a single attack. Changing a single bit in some attack strings can invalidate a signature
and create the need for an entirely new signature.

* Despite problems with signature-based intrusion detection, such systems are popular
and work well when configured correctly and monitored closely

**Anomaly Detection(not-use detection)**

The model consists of a database of anomalies. Any event that is identified with the database in considered an anomaly. Any deviation from normal use is labeled an attack. Creating a model of normal use is the most difficult task in creating an anomaly detector.

* In the traditional method of anomaly detection, important data is kept for checking
variations in network traffic for the model. However, in reality, there is less variation in
network traffic and too many statistical variations making these models imprecise;
some events labeled as anomalies might only be irregularities in network usage.

* In this type of approach, the inability to instruct a model thoroughly on the normal
network is of grave concern. These models should be trained on the specific network
that is to be policed.

**Protocol Anomaly Detection**

Protocol anomaly detection is based on the anomalies specific to a protocol. This
model is integrated into the IDS model recently. It identifies the TCP/IP protocol specific flaws
in the network. Protocols are created with specifications, known as RFCs, for dictating proper
use and communication. The protocol anomaly detector can identify new attacks.
Protocol anomaly detection systems are easier to use because they require no signature
updates

* There are new attack methods and exploits that violate protocol standards being
discovered frequently.

* The pace at which t he malicious signature attacker is growing is incredibly fast. But the
network protocol, in comparison, is well defined and changing slowly. Therefore, the
signature database must be updated frequently to detect attacks.

* Protocol anomaly detection systems are easier to use because they require no signature
updates

* Protocol anomaly detectors are different from the traditional IDS in how they present
alarms.

* The best way to present alarms is to explain which part of the state system was
compromised. For this, the IDS operators have to have a thorough knowledge of the
protocol design; the best way is the documentation provided by the IDS.