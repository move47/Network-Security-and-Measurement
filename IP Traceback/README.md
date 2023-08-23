### 1) What are the main contributions of this paper (”Practical Network Support for IP Traceback”)?
    The work provides an ‘efficient’ approach for tracing an approximate route from the attacker to the victim. 
    It begins by highlighting several reasons why the existing solutions do not work. 
    Later, it proposes a probabilistic packet marking mechanism and discusses how the scheme can be compressed and encoded in the IP Identification field for better performance. 
    The proposed idea is tested in a simulation setting and finally finishes by highlighting the limitations of the proposed scheme.

### 2) What parts of the paper do you find unclear?
    (1) I quite didn’t understand how can an route would be constructed in case of multiple attackers?

    (2) On page 10 first para, authors say, ”The analytic bounds we described earlier are conservative, 
    but in our experience they are no more than 30% higher than our experimental results”, 
    the authors highlight results in a specific probability setting and that too in simulation, so wondering whether the presented theoretical bounds are really conservative or not. 
    If yes, why didn’t better bounds be presented?

### 3) What parts of the paper are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)
    (1) The paper doesn’t validate the correctness of the proposed idea in real-world settings.

    (2) Several performance-related metrics, such as computation time, convergence time, 
    route reconstruction time, False-positive rate, etc., were not reported as part of the evaluation.
    
    (3) Moreover, the authors mention that some of the routers may be compromised 
    but don’t discuss how the presence of intermediate malicious routers impacts the scheme’s feasibility.

### 4) The paper is somewhat fast-and-loose in its discussion of one of the scheme’s significant limitations. State what you think it is, explain why the explanation is not satisfactory, and discuss how to reasonably extend the scheme to deal with the limitation (if you think that’s viable), or why the limitation appears quite difficult to address.

The explanation provided under the path validation subsection raises doubts for me. 
The authors mention that the attacker can only add the ”fake” edges at the end of the actual attack path. 
However, I believe that the attacker can still add fake edges with the fake distance that branches out from the true path, given that downstream routers do not update it. 
In this case, the victim will lead to an utterly non-existent path during reconstruction.

### 5) Discuss another form of spoofed identity that occurs in the Internet and sketch a mechanism to either prevent it or trace it back. Briefly discuss your proposed approach in terms of what it costs, its limitations, and how an attacker might subvert it.
<div align="left">
        ARP spoofing: In it, an active/passive adversary would intentionally send a forged 
        MAC address corresponding to a legitimate ARP request and gain covert access to the following requests/replies. Following, I am highlighting a mechanism that can help track an ARP attacker operating in promiscuous mode. The proposed idea works in two steps: fake ARP request flooding and TCP Syn flooding. The first step doesn’t incur any overhead, as it is a standard ARP request. However, the second step requires one extra network broadcast. The notable drawback of this scheme is the restriction on the adversary’s mode of operation.
</div> <br>

### 6) Bonus (optional) there is a large body of work on traceback, launched (in part) as a followup to this work. Do a brief literature search (protip: pivot on papers that cite this paper) and identify a follow-on study you find interesting. Why is it interesting? Do you think it improves significantly over the original? Other thoughts?

<div align="left">
    I found the study by Song. et al. [1](#references) interesting. The study proposes an optimization and highlights the limitations in this work along the way. I particularly liked their idea of using simple hashing operations for compression. 
    It reduces the reconstruction overhead as hashing is deterministic, unlike the random search required for getting the right combinations for the re-fragamation of XORed segments in the current work. This study also provides a study that covers most of the performance metrics that are not in current work. However, they also validate the efficacy in a simulation setting only. They also discuss an authentication mechanism to avoid relaying any fake marked packet.
</div>

### References

[1] Dawn Xiaodong Song and Adrian Perrig. *“Advanced and authenticated marking schemes for IP traceback”*. In: Proceedings IEEE INFOCOM 2001. Conference on Computer Commu-
nications. Twentieth Annual Joint Conference of the IEEE Computer and Communications
Society (Cat. No. 01CH37213). Vol. 2. IEEE. 2001, pp. 878–886.