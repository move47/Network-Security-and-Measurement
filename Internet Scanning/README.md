### 1) What are the main contributions of this paper (”ZMap: Fast Internet-Wide Scanning and its Security Applications”)?
The paper introduces ZMap, an open-source network scanner that can perform IPv4 Internet-
wide scans under 45 minutes using an off-the-shelf machine. The authors compared their pro-
posed mechanism with an existing scanning methodology based on the most aggressive NMap
settings and found it to be 1300 times faster with equivalent accuracy. 

The authors got such
a significant boost in performance because they optimized probing and eliminated the need to
keep track of the connection state. Lastly, the author stops scanning a person or organization
if that person or group doesn’t want to be scanned.

### 2) What parts of the paper (”ZMap: Fast Internet-Wide Scanning and its Security Applications”) do you find unclear?

- On page 1, under optimised probing subsection, the authors mention, we attempt to
send probes as quickly as the source’s NIC can support, skipping the TCP/IP stack and
generating Ethernet frames directly, I didn’t understand how can we generate packets
without using the protocol stack?
- On page 2, the authors mention to discover unadverstised services using ZMap, I was
wondering how is this possible in case of NATs, Firewalls, etc.

### 3) What parts of the paper (”ZMap: Fast Internet-Wide Scanning and its Security Applications”)nare questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)

- Throughout the text, the authors mainly highlight that ZMap can scan the whole IPv4
space in 45 minutes. However, in Table 1, ZMap configured with one probe packet takes
over 1hr for just 1M scans. I didn’t understand the cause of the difference between these
two reported timings.
- I was wondering since there is no authentication between the responding host and the
scanning machine. It means that devices controlled by an attacker could send false
reports. Consequently, I think the scanning reports might not always reflect the actual
scenario.
- It would have been better had there been statistics about active/in-active IPv4 devices
found as a part of the scan. I believe there would be quite a few dormant devices among
such scanning results.

### 4) Sketch potential challenges (technical, social. ethical, or otherwise) with large scale Internet scanning?
Building such services always faces the four issues listed. The authors addressed them adequately
in ZMap. First, securing host organization consent is difficult. Public organizations don’t want
to be entangled in legal proceedings if something goes wrong. Private companies may invest
in such applications as it brings monetary benefits. 

Internet scanning involves humans, and
humans feel uneasy when being surveilled. The technological problem may also ensure that
the intended network/resources host (software/hardware) is always available. Moreover, such
challenges get compounded when the service is open to use for all through open-source.

### 5) Do you think scanning the Internet is ethical? Defend your position. What can be done to make it more ethical / safer? Are there specific scans that are and are not acceptable?
Yes, I feel that Internet scanning is moral. It has some favorable applications as well as some
negative ones. It does, however, present a means of gathering information previously considered
opaque— insight into vulnerable hosts, protocol modification tracking, and so forth. The gen-
eral public should be aware of the potential security risks associated with Internet citizenship. 

I
feel scans that differentiate a person based on race/gender should be prohibited and considered
a violation of customer privacy by ISPs. However, I believe that in the long term, it will be the
go-to technique for measuring the impact of the commercially developed product.

### 6) Describe how ZMap and Censys fit together. What are the main contributions of Censys, and how does ZMap play a roll in those contributions?
Censys itself is not a new Internet Scanner; instead, it builds upon ZMap to provide a high-level
interface to scan data. Censys can provide detailed information about the scans and can also
answer non-trivial questions such as *“What fraction of embedded devices prefer CBC ciphers?”*,
which would take significant time if done with just ZMap scans. Censys follows a highly engi-
neered modular structure and provides the scan results in “real-time”. 

It also allows users to
customize the search results to extract their desired information from scans. Overall, Censys
uses several ZMap worker nodes for its scanning activities