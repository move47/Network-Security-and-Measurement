## The Million Dollar Dissident 
### [Article Link](https://citizenlab.ca/2016/08/million-dollar-dissident-iphone-zero-day-nso-group-uae/)

### 1) What are the main contributions of this paper (“The Million Dollar Dissident:Zero day Apple vulnerability”)?

The article focuses mainly on the operational aspects of the spyware used to track a human
rights activist stationed in the UAE. The malware writers primarily exploited an iPhone zero-
day vulnerability, which allowed them to execute applications with elevated privileges. Later,
investigators ascribed this malware to NSO Group, based in Harzelia, Israel, and simultaneously
emphasized the government’s active participation.

### 2) What parts of the paper(“The Million Dollar Dissident: Zero day Apple vulnerability”) do you find unclear?

- The report is well documented.
- How do we define ethics/morality while discussing offensive and defensive research?
- As we discussed in the last class, some legitimate apps can also be re-purposed to track
someone’s location, e.g., Google can follow an individual through a device tracking fea-
ture provided for lost and found cases. How do we consider these cases in this context?

### 3) What parts of the paper (“The Million Dollar Dissident: Zero day Apple vulnerability”) are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)

- How is the allocation of alike domains like googleplay-store.com, whatsapp-app.com pos-
sible? I believe a parent organisation reserves some domains with sufficient edit distance
with them.
- I believe an ISP can blacklist the c2c domains/IPs; however, it might not be possible if
the government participates in this. So, what is the best approach in such circumstances
apart from the device organization (Apple in this case) releasing a security patch?
- Moreover, it is believed that the malware (e.g., Mirai Botnet) disappears when the device
reboots. However, in this case, the spyware persisted and started its intended activities
after reboot, so what makes such malware different from the die-on-reboot malware?
