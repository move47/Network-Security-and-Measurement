### 1. What are the main contributions of this paper (”Bro: A System for Detecting Network Intruders in Real-Time”)? 

The work proposed an open-source real-time Network Intrusion Detection tool known as Bro. Bro passively monitors the network and provides notification in case of suspicious activity (host connecting to a non-allowed port, TCP RST without having a prior connection, etc.). 

Bro mainly works by first parsing network traffic using libpcap to get its application-level meaning and then running event-oriented analyzers that compare the activity with patterns that are thought to be anomalous.

### 2. What parts of the paper do you find unclear?

(1) Bro provides intrusion notifications in real-time. However, looking at the workflow, it seems that a decent amount of post-processing is required before flagging suspicious events. I believe I couldn’t figure out how much is this time duration.

(2) I quite didn’t understand how Bro can protect itself from subterfuge attacks. The ex-
ample provided in the text seems trivial to defend against.

### 3. What parts of the paper are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)

(1) The author mentions that for better monitoring, Bro tries to store the full packet content
except for TCP SYN/RST/FIN. I was wondering how much space we really need in case of heavy traffic link monitoring, and the link is also facing overload attacks simultaneously?


(2) The Bro language doesn’t support loop constructs. However, I believe we need loops if we want to do brute-force scans when indexed search is not possible to do.

(3) How effectively Bro performs in case of Encrypted network traffic?

(4) Snort was also introduced around the same time frame, however authors don’t compare Bro against Snort to highlight its pros and cons.

### 4. The most popular open source NIDS today are Snort and Suricata. What can you determine about their overall architecture and its model of how to detect attacks? What do you see as its strength and weaknesses?

(1) They monitor traffic in the network, compare the received packets against signatures, log attacks, and later present the attack statistics. Their architecture is not decoupled like Bro’s architecture: event generation engine and policy script interpreter.

(2) Bro is an IDS system, however Snort and Suricata are both IDS and IPS engines.

(3) Bro operates on single-thread, however these both work on multi-threaded design to provide multiple detection engines.

(4) Bro takes both signature and anomaly based approaches for detection, however Snort and Suricata only uses signature or rule-based approaches.

### 5. Investigate (say a half hour’s worth) a modern commercial intrusion detection/prevention system. What you can determine about its technical underpinnings? How does its approach compare to those of Bro and Suricata? Provide URL(s) to the information you used in your assessment.

I studied about CISCO IDS [1]. Its architecture is somewhat similar to Suricata; however different from Zeek(Bro). Cisco’s overall architecture can be split into two entities, i.e., the Sensor
platform (SP) and the Director platform (DP). SP captures the network traffic, performs the monitoring based on its signature database, and later alarms the suspicious activity via com-
mand and control to DP. 

DP is a management GUI for end-users and configures sensors and the
actions corresponding to the sensor alarms. The same is not the case with Zeek, whose architecture is highly modular, does deep packet inspection, and takes both signature and anomaly-based
detection approaches. Users on [2] reports that the installation process is easier and cheaper for open-source IDSes due to the presence of active community, however Cisco IDS is better in
terms re-programmability and accountability. Additionally, Cisco IDS does great job with both IP fragment and TCP session reassembly.

### References
[1] https://www.ciscopress.com/articles/article.asp?p=24696

[2] https://community.cisco.com/t5/network-security/cisco-ids-vs-snort/td-p/317493

[3] https://www.gartner.com/reviews/market/intrusion-prevention-systems/compare/cisco-vs-snort
