### 1. What are the main contributions of this paper (”Understanding the Mirai Bot-
net”)?

    The research explains the Mirai-IoT botnet phenomena and how low-power devices with pre-
    dictable passwords get attacked. Later, it employs multiple measures to track Mirai’s spread,
    targets/attacks, ownership remapping, and evolution. Finally, it discusses defense techniques to
    prevent IoT/Embedded devices from being part of such DDoS attacks.

### 2. What parts of the paper do you find unclear?

    (1) I didn’t understand the rationale behind using Network Telescope and Active Scanning
    simultaneously.

    (2) In Figure 3, why some ports (22, 2222, 37777) have very minimal scans compared to
    other ports (23, 5555).

### 3. What parts of the paper are questionable? (That is, you think a conclusion may
be wrong, an approach or evaluation technically flawed, or data ill-presented.)

    (1) On Page 1, the second paragraph talks about how ”efficient spreading based on Internet-
    wide scanning” was one reason behind Mirai’s success. On Page 3, though, it says that
    ”Mirai’s probes were based on stateless scanning” under Network Telescope section. I
    wonder if it is stateless, then how come it is efficient spreading?

    (2) Most of the attack targets are run by well-known network operators, so most of them
    would be using firewalls, intrusion detection systems, etc. I doubt that the authors
    measure how well these defenses worked to keep the attacks out.

### 4. You’ve now read 2 papers on DoS, 16 years apart. From these two works (”Infer-
ring Internet Denial-of-Service Activity”, and ”Understanding the Mirai Botnet”),
how has the landscape of DoS changed both technically and non-technically? Iden-
tify specifics.

    The first paper used the backscatter theory to analyze attack patterns, whereas the second
    adopted a holistic approach and analyzed data for an extended duration. Both papers have
    different threat models because the IoT world wasn’t observed in the first. Moreover, in the
    former, the attack pattern seemed static; however, in the latter, the malware was dynamic and
    adaptable to new exploits, making the defender’s job harder. On the non-technical side, the
    companies became much more concerned about the security of their customers. For instance, in
    Figure 3, the peak of infections didn’t last long because the patches were deployed immediately
    against the vulnerabilities.

### 5. Identify a specific methodological contribution you found interesting in this
paper, and describe it briefly. What is another kind of attack or study that could
make use of this method?

    I found the idea of IoT Honeypots interesting. The authors collected binaries out of honeypots,
    and then extracted default passwords dictionary, IP blacklists, C2C server domains, and how
    the malware was changing with time.
    I believe honeypots can also aid in determining the IP addresses of infected devices and DDoS
    targets. This IP information can be used to alert ISPs and network administrators about ongoing
    malicious activities. This data is more detailed than simply collecting scanning behavior.

### 6. Bonus (optional) both works make use of network telescopes. Do you find one
description or approach to be more clear, compelling, or ”correct”? Justify your
answer.

    I believe the former is more compelling because it clearly states all the assumptions. The second
    one, on the other hand, might have some ”hidden” presumptions that the authors don’t talk
    about. Also, the latter relies on several other techniques apart from Network Telescopes, and
    the authors don’t highlight how much telescopes have actually helped them.
