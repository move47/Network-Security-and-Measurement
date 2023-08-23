### 1) What are the main contributions of this paper (“Comprehensive Experimental Analyses of Automotive Attack Surfaces”)?
The authors discuss practical vulnerabilities in modern automobiles having severe consequences.
The paper is a follow-up study from the same authors. In a previous study, the authors assumed
to have direct access to the target vehicle; however, the current research show that prior attacks
can also be carried out without requiring direct physical access. 

The authors follow the common
vulnerabilities discovery mechanisms and found exploits similar to traditional system vulnerabil-
ities, such as buffer overflows, inconsistent predicate checks, integration of two separate vendors’
software, etc. Finally, the authors also propose some defense mechanisms but realize that it is
not trivial for manufacturers to adopt all of them.

### 2) What parts of the paper(“Comprehensive Experimental Analyses of Automotive Attack Surfaces”) do you find unclear?

- I didn’t understand the working of the remote attack carries using the cellular networks
wherein the malicious payload was delivered via the crafted song.

### 3) What parts of the paper (“Comprehensive Experimental Analyses of Automotive Attack Surfaces”) are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)

The authors mention repeatedly about the heterogeneity in the software/hardware com-
ponents used by automobile manufactures, and they validate their proposed attacks on
on one sedan model. Therefore, I am curious to know whether the attacks are transferable
across either different models or different manufactures.
