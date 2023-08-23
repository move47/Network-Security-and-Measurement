### 1) What are the main contributions of this paper (”Timing Analysis of Keystrokes and Timing Attacks on SSH”)?
The paper highlights two design flaws in the SSH protocol and shows how an eavesdropper
can exploit these weaknesses to figure out victim-user passwords by passively observing the time
between packets. 

The central idea behind this password recovery attack was that every keystroke
in the interactive mode of SSH is sent to the remote machine as a separate IP packet. Later, the
authors compare their proposed method to statistical bounds as well. 

Lastly, a proof-of-concept
system called Herbivore was developed to test whether an attack could work in a multi-user
environment.

### 2) What parts of the paper do you find unclear?
- I think the paper is well-written, and the authors did an excellent job of maintaining a
flow for the readers. However, I would have preferred if there had been an algorithm
showing the steps involved in **N-Viterbi** Algorithm.

### 3) What parts of the paper are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)
- I think the assumption of having inter-state independency while modeling the Hidden
Markov Model doesn’t hold in practice, especially when dealing with text/words.
- I believe authors also don’t consider the impact of the network itself while determining
the inter-keystroke timing. I think Network delay gets induced in practice, making the
proposed attack infeasible.
- Moreover, the proposed attack is validated with touch-typing users; however, the scenario
might change if the attack is mounted against naive users.
### 4) Propose some form of inferring activity (it needn’t rely upon timing) by which you might plausibly be able to infer a specific property of network activity that is not directly manifest. Sketch how you might acquire data to test your approach, including the issue of obtaining or approximating/bootstrapping ground truth. 
I just thought about an attack that might not have much relevance. But still, let me explain it
here. I guess this attack can be used to target systems/machines that use mechanical parts for
their operation, e.g., Hard Disks, ATMs, digital locks, etc. For instance, in the case of ATMs,
an adversary can keep a sound sensor to correlate the duration of sound the mechanical parts
produced with the number of bills the victim withdrew from the ATM. 

Later, based on the
received sound signal, the adversary can decide who is ”rich.” To train such a detector, the
attacker can do several types of personal transactions. Moreover, in the case of HDD, the sound
produced by the mechanical movement of the pivot can be used to recover some cryptographic
keys[1].

### References
[1] Genkin, D., Shamir, A. & Tromer, E. Acoustic cryptanalysis. Journal Of Cryptology. 30, 392-443 (2017)
