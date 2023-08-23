### 1) What are the main contributions of this paper?)?

The authors investigate the spyware ecosystem linked with intimate partner surveillance (IPS).

The authors discover that it is effortless for abusers to acquire spyware software on the Internet,
including in off-store, and on-store locations(the Google Play Store, and Apple Apps). 

Later,
the authors created a method for identifying all spyware applications and found that existing
anti-virus and anti-spyware programs fail to detect all the spying applications as many legitimate
applications can be repurposed for espionage. In conclusion, the authors assert that the found
apps pose urgent and severe dangers to victims.

### 2) What parts of the paper do you find unclear?

- How did the spyware get into the Play Store in the first place, given that Google claims
to perform code reviews prior to publishing an app?

- In general, Why does IRB not interfere in such issues as using these covert applications,
humans can be monitored?

### 3) What parts of the paper are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)

- I believe the Logistic-Regression based Machine Learning classification system can be
easily fooled by carefully crafting the app description, summary, genre, etc. Thus, I
believe it would have be better if the authors had done done the static/dynamic analysis
on the app executables.
- I wonder how feasible the detection methodology would be in detecting web-based spy-
ware agents.

### 4) This paper outlines an attack that is technically not particularly novel, but has significant real world impact and consequences. Identify another current real world attack whose severity comes from the impact/consequences, rather than the technical novelty.

**SEXUAL ASSAULT/COERCION REPORTING IN ORGANISATIONS:** I believe that many
survivors in academic settings, politics, etc., do not report abusers since doing so could have
severe repercussions. Consequently, a ”powerful” individual could be a serial offender without
being apprehended. However, I feel that overcoming this issue without giving information about
the survivors and assisting the concerned authorities in taking legal action against the ”powerful”
perpetrator could be an interesting problem for security researchers.
