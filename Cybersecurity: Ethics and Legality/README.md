### 1) What are the main contributions of this paper (”Conducting Cybersecurity Research Legally and Ethically”)?

The paper focuses mainly on the laws associated with the stages commonly followed when
conducting cybersecurity research. Later, it explores the ambiguities researchers have when
appraising a research problem regarding legal and ethical implications. In addition, the author
notes that while some activities may be legal, they may not be ethical, which further restricts
researchers. The author concludes by highlighting the importance of a researcher’s organization
in analyzing concerns during such research activities.

### 2) What parts of the paper (”Conducting Cybersecurity Research Legally and Ethically”) do you find unclear?

The author mentions several laws; however, I didn’t understand what questions a researcher
should ask themselves while framing a research problem. I understand it is a complex issue, but
I am curious to know the steps a researcher must follows broadly.

### 3) What parts of the paper (”Conducting Cybersecurity Research Legally and Ethically”) are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)

The paper pointed out an organization’s vital role in cybersecurity research. However, it doesn’t
mention how organizations can abuse their rights and some examples where such cases have hap-
pened in the past (e.g., Uber, Cambridge Analytica, etc.) to better understand organization
capabilities.

### 4) Frame two security issues relating to wireless or device security. These don’t have to relate to the privacy discussion in the paper. It’s fine to interpret ”wireless” broadly. If you discuss a device issue(s), there should be some component of communication/networking. Sketch an approach or solution for each issue and describe its strengths and weaknesses. If you use external resources, provide citations.
- Wiretapping over wireless transmission channels is much easier than wired, making it
more vulnerable to eavesdropping attacks. The solution is to use encryption/obfuscation
techniques; however, most wireless devices have resource constraints (computation, com-
munication, etc.) that might affect the quality of service in another way.
- The attacker can set up a fake public network access point, impersonating the actual
Wifi-hotspot, inviting victims by transmitting more stronger signals. The potential so-
lution could be careful authentication. However, some public networks don’t require any
authentication; therefore, we should ensure that all our outgoing traffic is encrypted with
proper SSL certificate verification.

### 5) Apply the principles from the first paper (”Conducting Cybersecurity Research
Legally and Ethically”) to the second paper (”Encore: Lightweight Measurement of
Web Censorship with Cross-Origin Requests”). Do you think the work was legal?
Ethical? What is the set of sites you think the authors could use this technique to
measure before it crosses a legal or ethical line (if it did not already).


I don’t think the methodology adopted in the secondary paper to deliver the measurement
tasks is legal/ethical. Most Ad networks pack several things together, delivering unsolicited
executables to the user machine, as we saw in the last class secondary paper. I believe the
authors should have used websites that take the user’s consent before delivering the payload.


Additionally, the users interested in gaining financial benefits following a pay-per-install policy
could behave as potential vantage points.
