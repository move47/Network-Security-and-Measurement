### 1) What are the main contributions of this paper (”SoK: Towards Grounding Censorship Circumvention in Empiricism”)?

The survey paper highlights the disconnect between real-world sensors’ operating characteristics
and the circumvention techniques proposed in research. For instance, the authors assert that
real-world sensors focus on attacks during the link setup phase; however, research solutions fo-
cus on link usage attacks. Later, the paper expands on the existing research gaps and provides
recommendations on how better circumvention tools can be designed

### 2) What parts of the paper (”SoK: Towards Grounding Censorship Circumvention in Empiricism”) do you find unclear?

- I didn’t understand what the authors mean by point 3 on page 2, i.e., Censors favor
attacks that do not risk falsely blocking allowed connections due to packet loss, whereas
research considers many less robust attacks.
- I didn’t understand the cause of the disparity between the research and practice. I would
like to know more about why researchers proposed advanced/irrelevant approaches than
actual requirements. I feel there might be some caveats behind this disparity.

### 3) What parts of the paper (”SoK: Towards Grounding Censorship Circumvention in Empiricism”) are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)

- I wonder why the authors did not look at the Ethical considerations of circumvention
approaches.
- In Table II, the authors mention the vulnerabilities exploited by censors against TOR
till 2013(except one from 2014). However, the paper was presented in 2016. I believe
there might also be other censorship attacks against TOR during this missed time.
- The authors look at the circumvention tools that mostly fall into the category of Poly-
morphism and Steganography. However, I believe there could be networking-based cir-
cumvention approaches as well. e.g., Encrypted DNS, Dynamic CDNs, etc.

### 4) From the reading, identify a trend in either censorship or circumvention that you found interesting. Describe it and why it interested you.

**END-TO-END ENCRYPTION(E2E):** I think the adoption of E2E by popular services is making
governments job hard to perform active/passive analysis of user traffic. For instance, early this
year, the Indian government protested against Whatsapp when it claimed to deploy E2E for
Indian users.
DEPENDENCY ON LARGE PLATFORMS: Many smaller content producers(Spyware apps)
can use the more pervasive platforms(Google Playstore, Apple Appstore, etc.) to reach end
users, wherein if they go directly, they might get censored.
