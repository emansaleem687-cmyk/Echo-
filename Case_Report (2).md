1| # ECHO Case Report: *The Signal That Was Never Sent*
2| 
3| **Author:** Eman Saleem · **Individual report** · **Stretch modules:** 04 (The Erased Measurement) and 06 (The Impossible Claim)
4| **Notebook:** `ECHO_Notebook.ipynb` (runs top to bottom in Google Colab)
5| 
6| ---
7| 
8| ## 1. Final Theory / Verdict
9| 
10| **Zara Mahmud did not send a message faster than light. ECHO produced a real but useless correlation: she mistook an echo for a voice.**
11| 
12| - Her twin detectors always agreed. That is genuinely what an entangled pair does, but it is *also* exactly what a boring pre-agreed secret does (Module 03).
13| - Even if her pair was truly entangled, entanglement cannot carry a message: the receiver's results look 50/50 whatever the sender does (Module 03, no-signalling test). The correlation only appear[...]
14| - Her "teleportation" claim fails the same way: teleportation works only when two ordinary classical bits are sent as well. Without them the receiver gets a coin flip (Module 06).
15| 
16| **Confidence:** about **95 %** that ECHO was not faster-than-light signalling. This follows from the physics I reproduced in the simulator and from the no-signalling behaviour in the Bell-pair tes[...]
17| 
18| ## 2. Evidence and Clues
19| 
20| 1. **Module 01:** I can speak the machine's language (X, H, measure). Interference (H·H) shows quantum behaviour that a classical coin cannot mimic. The machine name and final-run time revealed o[...]
21| 2. **Module 03:** the Bell pair gives only 00/11 (0 mismatches in 2000 shots), but a pre-agreed classical secret gives the same table. The CHSH test gives **S ≈ 2.8 > 2** (classical limit 2), pr[...]
22| 3. **Module 05:** majority vote over the damaged stream recovers **"ECHO"**, and 20 of 32 triples were corrupted (one flip each). A note left beneath it suggests a damaged or manipulated data stre[...]
23| 4. **Module 06:** teleportation succeeds 100 % with the two classical bits applied, but with no correction Bob's qubit matches the secret only ≈ 50 % of the time, and his raw measurement statist[...]
24| 5. **Module 04:** an unmeasured qubit's "changes" are exactly predictable (HH = I, HXH = Z); only a *measurement* destroys information. This bears on the claim that a log "changed when observed."
25| 
26| ## 3. Evidence Board
27| 
28| | FACT (directly observed) | CLAIM (stated by a suspect/log) | INFERENCE (my interpretation) | OPEN QUESTION |
29| |---|---|---|---|
30| | Bell pair gave 00/11 only, 0 mismatches in 2000 shots | Zara: always-agreeing detectors prove a link across space | Agreement alone is insufficient evidence; a shared secret fits equally well | [...]
31| | A classical shared secret reproduces the same 00/11 table | Zara: ECHO sent a message faster than light | Correlation was misread as communication | Did anyone steer her toward that reading? |
32| | CHSH S ≈ 2.8 (> 2) for a Bell pair; classical max = 2 | ARIA: "No unauthorised command was issued" | A genuine entangled pair can exist, yet still cannot signal | Who configured ARIA's schedul[...]
33| | Bob's marginal is ≈50/50 for every Alice action | Sana: "I only deleted a corrupted log" | No receiver could read a message from Alice's choices alone | What exactly was in the deleted log, an[...]
34| | Majority vote decodes the stream to "ECHO" (20/32 triples hit) | ARIA: log "changed when observed" | A *quantum state* can change when measured; a classical log file should not | Was the log a q[...]
35| | H·H → always 0; H·measure·H → 50/50 | Bilal: "I warned her" (report now missing) | His report may be the only independent check on the discrepancy | Why is Bilal's report missing, and who[...]
36| | Teleportation: 100 % with the 2 classical bits, ≈ 50 % without; Bob's raw statistics ≈ 0.50 for every secret | Zara: "teleported a message, no qubit crossing the gap" | Her message could onl[...]
37| 
38| ## 4. Experiments and Results
39| 
40| | Module | Prediction | Circuit | Result |
41| |---|---|---|---|
42| | 01 Bronze/Silver/Gold | X→1; H→50/50; H,H→0; X on q0,q2→101 | 1 and 3 qubits, X/H/measure | 1000/1000 ones; ≈500/500; 1000/1000 zeros; `101` 100 % |
43| | 03 Bronze | Only 00 and 11 | H(0), CNOT(0,1), measure | no 01/10 |
44| | 03 Silver | Shared secret also agrees | Python coin flip, same for both | same 00/11 table |
45| | 03 Gold | Quantum S = 2√2 ≈ 2.83; classical S ≤ 2 | Bell pair, RY(−a), RY(−b), measure | S ≈ 2.8 (varies slightly each run, always > 2) |
46| | 03 no-signalling | Bob ≈ 50 % whatever Alice does | Alice: nothing / Z / X; Bob measures | ≈ 0.50 in all three |
47| | 05 | Majority vote → ASCII | classical decoding | "ECHO" |
48| | 05 Silver | ≥ 2 flips break it | all 8 flip patterns of 000 | 2 and 3 flips decode wrongly |
49| | 05 Gold | Entangled 3-qubit code fixes one bit flip | encode, error, syndrome, ccx | recovered 100 % for errors on any qubit; unprotected ≈ 79 % |
50| | 04 | X,H,H→1; H,X,H→0 | single qubit | matches; predictor agrees on 10 sequences |
51| | 06 Bronze | With Bob's correction the state arrives | 3-qubit teleportation, deferred X/Z corrections | Bob matches secret 100 % |
52| | 06 Silver | Without the 2 classical bits Bob gets a coin flip | same circuit, no correction | ≈ 0.50 overall; four different values for Alice's four outcomes, averaging to a coin flip |
53| | 06 Gold | Bob's raw statistics independent of the secret | secret angle 0 … π, Bob measures Z and X | ≈ 0.50 in every case |
54| 
55| *Counts vary slightly from run to run because quantum measurement is probabilistic; the conclusions do not.*
56| 
57| ## 5. Interpretation
58| 
59| Module 03 is the key point. Perfect agreement is what Zara saw and what she called proof of a link. My experiments show that (a) a classical secret gives the same agreement, (b) a CHSH test is wha[...]
60| 
61| ## 6. Alternative Explanation
62| 
63| **Competing theory:** ECHO really was a groundbreaking, working faster-than-light channel, and someone suppressed it. I prefer the simpler explanation because it requires no extraordinary suppress[...]
64| 
65| ## 7. Next Experiment
66| 
67| Re-run Zara's original detector data with **different measurement angles** (a CHSH-style test), and test **signalling directly**: have Alice randomly pick her setting and check whether Bob's stati[...]
68| 
69| ## 8. Limitations
70| 
71| - I worked on a **simulator** with a mathematically ideal Bell pair; a real lab detector has noise and loopholes (detection and locality) that I did not model.
72| - Module 04 shows quantum states change when measured; it **does not** prove the log was quantum, nor that ARIA, Sana or anyone tampered with it.
73| - None of my modules identifies who (if anyone) manipulated the experiment; I make no accusation.
74| - The ≈95 % confidence is a judgment about the physics, not a statistical result.
75| 
76| ## 9. References and AI / External Assistance
77| 
78| - Qiskit and Qiskit Aer documentation (IBM Quantum).
79| - IBM Quantum learning materials and example circuits used for the experiments.
80| - AI assistance: Claude and ChatGPT were used to help explain quantum concepts, draft code, and refine the report wording. I reviewed, ran, and verified the results independently.
81| 
82| 
