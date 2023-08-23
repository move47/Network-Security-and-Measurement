## Spamalytics: An Empirical Analysis of Spam Marketing Conversion
### 1) What are the main contributions of this paper (”Spamalytics: An Empirical Analysis of Spam Marketing Conversion”)?
The paper broadly studies spam behavior and presents an approach to measure spam’s suc-
cess rate. The measurements are carried out using the Storm botnet and its spamming agents.

The authors emulate the spammer’s actions, infiltrate the command and control infrastructure
parasitically, and modify a subset of addresses to redirect any interested recipients to servers
under their control. Apart from redirecting prospective spam hosts, the authors do not harm
any external hosts.

### 2) What parts of the paper (”Spamalytics: An Empirical Analysis of Spam Marketing Conversion”) do you find unclear?

- From the networking view, I want to know more about how the author’s proxies became
part of the Storm Botnet.
- The authors mention that the conversion rate for binary installations can be inferred
from the HTTP POST signal. How does it actually work? Isn’t it a privacy violation if
the vendor can know whether the user has installed the software from the executable or
not?

### 3) What parts of the paper (”Spamalytics: An Empirical Analysis of Spam Marketing Conversion”) are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)

- Why didn’t the botnet block the author’s proxies after seeing the success reports from
the worker nodes that reported directly to the master servers? It might happen that the
worker node dropped out from the current round of communication but later turned up
and reported directly without going via the author’s proxies, OR the worker nodes get
connected to different proxies controlled by Master servers.
- How the attack would take place if the ongoing communication in botnet infrastructure
is encrypted in some form.

### 4) The Spamalytics study allowed us to measure for the first time, the conversion rate of spam. To achieve this goal, the authors inserted themselves into the botnet hierarchy, and rewrote spam urls sent to real users, to point to their servers. The authors claim this is ethical as it strictly reduces harm. Do you agree? Defend your position.

**Yes**, I believe the author’s adopted approach to be ethical. In fact, I think the authors reduced
the impact of spam as the users who were re-directed to a controlled address were saved from
being spammed. Additionally, the authors are not sending spam by themselves, they have just
modified the destination address contained inside the spam email, and this email would have
reached the potential host eventually had it not been changed by the authors.

### 5) Compare the results of Spamalytics to ”Understanding the Network-Level Behavior of Spammers”. Do the results conflict, or compliment each other? How?

- Both the papers almost converge to the same conclusion when we talk about listing spam
IP addresses on one of the known Blacklists.
- However, In terms of botnet worker’s persistence timings, both have somewhat different
views.
Spamalytics: “On average, worker bots remained connected for 40 minutes, although over
40% of workers connected for less than a minute. The longest connection lasted almost
81 hours.”
**Other Paper:** *“although roughly 75% of Bobax drones persist for less than two minutes,
the remainder persist for a day or longer, about 50 persist for about six months, and 10
persist for the entire length of the trace.”*

### 6) What is the result you found most interesting or unexpected from either of the papers?

- In Spamalytic’s paper, I like the result showing that hosts located in the US have been
mostly targeted with spam, but those hosts are actually among the least who actually
visited the links mentioned in the spam emails. However, the case is different with
countries like India, France, etc. I believe such results show the importance of Internet
Education.
- In the other paper, I found the BGP short-lived attack more exciting and even more
surprising fact about it that IP blacklists don’t list most of such invalid prefixes in their
list.

## Click Trajectories: End-to-End Analysis of the Spam Value Chain
### 1) What are the main contributions of this paper (”Click Trajectories: End-to-End Analysis of the Spam Value Chain”)?

In this study, the authors’ primary objective was to understand the resource requirements be-
hind the successful end-to-end operation of the Spam value chain. The author examines three
months of real-time source data, such as captive botnets, raw spam feeds, and feeds of spam-
advertised URLs, to identify possible bottleneck resources. 

Finally, the authors determined that
the payment infrastructure may be exploited to thwart spamming activities due to limited pay-
ment choices spammers have.

### 2) What parts of the paper (”Click Trajectories: End-to-End Analysis of the Spam Value Chain”) do you find unclear?

- I could not understand the difference between Fig. 3 and Fig. 4. I believe the information
conveyed in Fig. 4 can be understand from Fig. 3 itself, so I consider the information in
Fig.4 is redundant.
- I wonder, why doesn’t the authors investigate the logistics infrastructure involved in the
spam value chain, such as the delivery partners and return address for packages?

### 3) What parts of the paper (”Click Trajectories: End-to-End Analysis of the Spam Value Chain) are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)

- When the authors were performing the DNS and web crawling, the spam adversary
might control several URLs and thus can block such crawling form happening, I guess it
is possible with the proposed methodology as well.
- Fig. 5 highlights the effectiveness of resources (DNS, web hosting), etc., takedown on
the spamming chain. After taking values directly from the already collected data, I
assume the authors plotted the curves. However, I believe that the results might vary
in the case of actual takedowns of services as then spammers might have an alternative
infrastructure in place, which is not getting captured in these figures.

### 4). Frame an aspect of Internet cybercrime/the underground economy that interests you. Discuss the research issues it presents in terms of what you would like to understand about it, how you might go about investigating (and validating) it, and what difficulties (technical, logistical, ethical, legal) the undertaking might present.

I want to study the working of how major players like Google, Meta, and TikTok steal user data
for better advertisements.
The underlying economy is vast; consequently, web advertisements have become the cheap-
est product advertisement mode for most companies.
I think it is criminal activity as users’ browsing sessions get monitored without alerting them.

The technical challenge would be understanding the techniques used to steal user activities
(pixel embedding, javascript code injections, in-app browsing, etc. ). Later, some websites can
be randomly visited in sandboxing mode to know the type of third-party calls it makes. The
logistical challenge in this process would be the difficulty of doing this for large-scale websites.

Moreover, I believe this could results into several false positives/negatives. But the careful de-
sign of empirical methodologies can alleviate such issues. Finally, we can analyze the coverage
distribution of such companies, amount a company takes to sell its data to product owners, etc.
