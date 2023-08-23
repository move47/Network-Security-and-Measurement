### 1) What are the main contributions of this paper (“Imperfect Forward Secrecy: How Diffie-Hellman Fails in Practice”)?
The paper discusses an inherent flaw in the TLS protocol and further exploits it to show how
an active attacker can take control of an ongoing HTTPS session. 

In particular, the authors
pre-compute 512-bit discrete logs and later use it to downgrade a regular DHE connection to
use a DHE EXPORT group in real-time. It results in the violation of both the confidentiality
and integrity of application data.

### 2) What parts of the paper(“Imperfect Forward Secrecy: How Diffie-Hellman Fails in Practice”) do you find unclear?
- I didn’t understand the idea behind using the same prime group by many servers. Is it
because it comes default with applications, or are the admins lazy enough to change it?
- I didn’t understand the need of solving the discrete logs in real-time. I believe it can be
done passively as well, as our goal is to solve either ga or gb to get either a or b. Later, gab
can be obtained using it, and then all the previous encrypted traffic can be decrypted.

### 3) What parts of the paper (“Imperfect Forward Secrecy: How Diffie-Hellman Fails in Practice”) are questionable? (That is, you think a conclusion may be wrong, an approach or evaluation technically flawed, or data ill-presented.)

- The paper presents a serious attack similar to FREAK (RSA factoring), and is well
presented.
- I believe the authors could have highlighted the cost/energy consumption required to
perform the pre-compuations related to discrete logs.
- Towards the end, the authors mention that state-level actors like NSA have the potential
to even break the security of large prime groups (768-bit, 1024-bit) by setting up the
required computation infrastructure. I wonder what stops such organisations from not
using Quantum computers as it can solve the desired computations in polynomial time.
