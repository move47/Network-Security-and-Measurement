### 1) What are the main contributions of this paper (”The Base-Rate Fallacy and the Difficulty of Intrusion Detection”)?

The research article tries to answer how can Intrusion Detection Systems suffer from the Base-rate fallacy phenomenon. The authors claim that it is not a good idea to measure the effectiveness of IDS only based on its ability to identify behavior correctly as intrusive. 

This sort of interpretation suffers from the Base-rate fallacy. Consequently, the authors suggest that for
measuring such systems’ effectiveness, an individual should also look at its ability to suppress
false alarms in conjunction to True detection rate.

### 2) What parts of the paper do you find unclear?
- I didn’t exactly understand section 5.2, i.e. *"Human-Machine Interaction in Intrusion
Detection”*.
- Moreover, I believe for Fig. 2 and 3, the authors could have done better in terms of
explanation. I realized some details are missing from it.

### 3) What parts of the paper are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)
- In Section 6.2, the authors talk about how detection rates dropped sharply when IDS
systems were used with attacks that had never been seen before. However, the false
alarm rate did not change in the same way. They make a conjecture about what’s going
on and say that, yes, the attack traffic changes, but the background traffic doesn’t. In my
opinion if the background traffic remains the same, then overall false alarm rate should
decrease as the attack traffic would be considered as Benign traffic.
- In conclusion, the authors mention that anomaly detection methods have higher false
alarm rates than Signature detection systems. However, I believe they don’t compare
both for true detection rates..
- I wondered how Bayesian Detection rate (mentioned in Section 5) change with respect
to threat model and type of IDS system, i.e., anomaly vs. signature-based changes.

### 4) Identify a research paper (preferably outside this course) that you think may suffer from base-rate problems. The proceedings of IEEE Security Privacy, ACM CCS, and USENIX Security are a good starting point. Sketch the work very briefly and outline your concern. Papers you’ve looked at in other courses are fair game.
I considered [1] for reading. The paper explores the question “Is it possible to mitigate more
amplification attacks and drop more attack traffic when distributed attack mitigation platforms
collaborate?”. The authors argue that if at network providers exchange information collected
at IXPs then they can collaboratively fight DDoS attacks and consequently drop up to 100%
of the attack traffic that is routed via these collaborating networks. 

I believe the authors don’t
study the Base-fallacy rate during the analysis of their proposed solution, and as this underlying
paper argues, it is practically impossible to build an ideal attack detection system having a 100%
attack detection rate. Therefore, the authors, I believe, focus only on the attack detection rate
while missing out on measuring the impact on false alarm rates.

### 5) Propose two steps the field of security research could take to strengthen the work that the discipline produces. For your discussion you can stay focused on intrusion detection if you wish, but you do not have to. You can instead address other areas of security research (needn’t be related to networking or the Internet), and it’s fine to look at specific, focused issues, or quite broadly at classes of problems, or something in between.
- I believe the research output would be better if solutions could be tailor-made for spe-
cific problems rather than achieving a generalized solution. For example, a solution for
securing traditional computers might not be considered an optimized solution for smart
meters communication. For instance, in the prior case, if some devices are compromised,
it won’t have the same consequences as a smart meter failure, wherein the household
losses access to power and might not be able to cook meals for that whole day.
- Controlled experiments (Simulatiopn/Lab-only evaluations) are a good way to look at
certain parts of an proposed approach, but whenever possible, it should be tested in a
real-world setting to show how well it works and what problems still need to be solved,
which will encourage more research.

### References
[1] Wagner, D., Kopp, D., Wichtlhuber, M., Dietzel, C., Hohlfeld, O., Smaragdakis, G. & Feldmann, A. United
We Stand: Collaborative Detection and Mitigation of Amplification DDoS Attacks at Scale. Proceedings Of
The 2021 ACM SIGSAC Conference On Computer And Communications Security. pp. 970-987 (2021