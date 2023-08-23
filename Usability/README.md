### 1) What are the main contributions of this paper (“Alice in Warningland: A Large-Scale Field Study of Browser Security Warning Effectiveness”)?
The authors refute the claims made in previous research studies that end-users don’t care about
web security; therefore, security should not be delegated to users. The paper primarily focuses
on clickthrough rate to see how users in the real-world perceive security warnings corresponding
to malware/phishing web pages or SSL warnings. 

The proposed approach has been tested using
the in-browser telemetry feature of Google Chrome and Mozilla Firefox. It is a comprehensive
measurement study analogous to prior studies conducted in controlled environments. Further-
more, the authors realize that users do pay attention to warnings and make cognitive decisions
before ignoring them. Finally, some recommendations are proposed for making security warnings
better.

### 2) What parts of the paper(“Alice in Warningland: A Large-Scale Field Study of Browser Security Warning Effectiveness”) do you find unclear?

- The paper is well written and is explained with proper illustrations. Several technical
terms are also expanded during further occurrences.
- I partially understood certificate pinning(Sec 5.2) as one of the causes behind the higher
clickthrough rate in Chrome than Firefox for SSL warnings, but I would like to know
more about it. The author’s suggestion of allowing Chrome users to ignore the warning
for HSTS (HTTP Strict Transport Security) websites might reduce the clickthrough rate
but it might also increase security risks.

### 3) What parts of the paper (“Alice in Warningland: A Large-Scale Field Study of Browser Security Warning Effectiveness”) are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)

- The authors mention that they could not collect demographic data apart from browser
versions and the user operating system. However, I believe the authors can also geo-
locate the user requests through their IP locations and categorize them better.
- Moreover, In this study, the authors discuss less about bot behavior. It may be due to
the non-prevalence of bots while this article was written. However, I wonder how do I
account for bots if I try to carry out similar study now.
