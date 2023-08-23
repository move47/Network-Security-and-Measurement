### 1) What are the main contributions of this paper (”Your Botnet is My Botnet: Analysis of a Botnet Takeover”)?
The paper broadly studies botnet behavior. The measurements are carried out by actively
infiltrating the Torpig botnet for approximately 10 days. The authors leveraged information
about the domain generation algorithm and Torpig’s C&C protocol to register domains that
the infected hosts would contact. 

Later, when the infected hosts visited the C&C servers under
authors control, they stored all the data to analyse amount of information stolen by Torpig.

### 2) What parts of the paper (”Your Botnet is My Botnet: Analysis of a Botnet Takeover”) do you find unclear?
- I did quite understand the difference between Fig. 5 & 7, and Fig. 6 & 8. I think each
pair represents the same information.
- Fig. 5 and Fig. 9 depict a static pattern. I wonder in real-world whether such pattern
exists or not, especially while dealing with network measurements.

### 3) What parts of the paper (”Your Botnet is My Botnet: Analysis of a Botnet Takeover”) are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)

- In Section 5.2.3, the authors briefly talk about the exclusion of False positives using nid
value as distinction metric. However, I believe both bot and non-bot hosts can have
same nid as well; as this value is computed over hardware specifications.
- The authors didn’t provide any potential defenses to prevent from such botnet attacks.
For long term, I think having certain defense mechanisms are better compared to man-
ually asking government organisation (like FBI) to seize such malicious behaviour.

### 4) Do you agree with the actions of the researchers? Defend your position with specific examples.
I entirely disagree with the authors’ approach of doing this empirical analysis. The data col-
lected over ten days contains all sorts of information, from personal mail accounts to banking
credentials. 

I believe storing such data passively without the owners’ consent is a direct breach
of privacy. I would have preferred to have authors storing only minimal information in terms of
aggregate statistics rather than storing the raw data.

### 5) This paper appeared exactly one year after Spamalytics. How has the landscape changed, both in terms of botnets and results, and in terms of researcher activity?

- I think the goal of both the papers is different as this paper tries to figure out what sort
of private data the botnet steals; however, the earlier paper attempted to calculate the
spam conversion rate.
- I believe the Torpig botnet is quite complicated in its technical operations compared to
the Storm botnet.
- The authors in the Spamalytics work were able to redirect the victim traffic to their
controlled servers for around 26 days, and however, in this case, the controlled C&C
servers were thrown out of the measurement in just ten days. It shows that the botnet
advances its working principles overtime to hide its presence.
