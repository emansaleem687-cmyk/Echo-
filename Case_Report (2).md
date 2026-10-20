# ECHO Case Report: *The Signal That Was Never Sent*

**Author:** Eman Saleem · **Individual report** · **Stretch modules:** 04 (The Erased Measurement) and 06 (The Impossible Claim)
**Notebook:** `ECHO_Notebook.ipynb` (runs top to bottom in Google Colab)

---

## 1. Final Theory / Verdict

**Zara Mahmud did not send a message faster than light. ECHO produced a real but useless correlation: she mistook an echo for a voice.**

- Her twin detectors always agreed. That is genuinely what an entangled pair does, but it is *also* exactly what a boring pre-agreed secret does (Module 03).
- Even if her pair was truly entangled, entanglement cannot carry a message: the receiver's results look 50/50 whatever the sender does (Module 03, no-signalling test). The correlation only appears because both parties share the same randomness pattern.
- Her "teleportation" claim fails the same way: teleportation works only when two ordinary classical bits are sent as well. Without them the receiver gets a coin flip (Module 06).

**Confidence:** about **95 %** that ECHO was not faster-than-light signalling. This follows from the physics I reproduced in the simulator and from the no-signalling behaviour in the Bell-pair test.

## 2. Evidence and Clues

1. **Module 01:** I can speak the machine's language (X, H, measure). Interference (H·H) shows quantum behaviour that a classical coin cannot mimic. The machine name and final-run time revealed only one specific clue path.
2. **Module 03:** the Bell pair gives only 00/11 (0 mismatches in 2000 shots), but a pre-agreed classical secret gives the same table. The CHSH test gives **S ≈ 2.8 > 2** (classical limit 2), proving genuine entanglement, but not signalling.
3. **Module 05:** majority vote over the damaged stream recovers **"ECHO"**, and 20 of 32 triples were corrupted (one flip each). A note left beneath it suggests a damaged or manipulated data stream.
4. **Module 06:** teleportation succeeds 100 % with the two classical bits applied, but with no correction Bob's qubit matches the secret only ≈ 50 % of the time, and his raw measurement statistics are still 50/50.
5. **Module 04:** an unmeasured qubit's "changes" are exactly predictable (HH = I, HXH = Z); only a *measurement* destroys information. This bears on the claim that a log "changed when observed."

## 3. Evidence Board

| FACT (directly observed) | CLAIM (stated by a suspect/log) | INFERENCE (my interpretation) | OPEN QUESTION |
|---|---|---|---|
| Bell pair gave 00/11 only, 0 mismatches in 2000 shots | Zara: always-agreeing detectors prove a link across space | Agreement alone is insufficient evidence; a shared secret fits equally well | Did anyone steer her toward that reading? |
| A classical shared secret reproduces the same 00/11 table | Zara: ECHO sent a message faster than light | Correlation was misread as communication | Did anyone steer her toward that reading? |
| CHSH S ≈ 2.8 (> 2) for a Bell pair; classical max = 2 | ARIA: "No unauthorised command was issued" | A genuine entangled pair can exist, yet still cannot signal | Who configured ARIA's schedule and logs? |
| Bob's marginal is ≈50/50 for every Alice action | Sana: "I only deleted a corrupted log" | No receiver could read a message from Alice's choices alone | What exactly was in the deleted log, and why was it deleted? |
| Majority vote decodes the stream to "ECHO" (20/32 triples hit) | ARIA: log "changed when observed" | A *quantum state* can change when measured; a classical log file should not | Was the log a damaged file or a planted clue? |
| H·H → always 0; H·measure·H → 50/50 | Bilal: "I warned her" (report now missing) | His report may be the only independent check on the discrepancy | Why is Bilal's report missing, and who removed it? |
| Teleportation: 100 % with the 2 classical bits, ≈ 50 % without; Bob's raw statistics ≈ 0.50 for every secret | Zara: "teleported a message, no qubit crossing the gap" | Her message could only exist because the two classical bits were sent; otherwise Bob gets a coin flip | Was the message really a teleportation result or just a normal encoded signal? |

## 4. Experiments and Results

| Module | Prediction | Circuit | Result |
|---|---|---|---|
| 01 Bronze/Silver/Gold | X→1; H→50/50; H,H→0; X on q0,q2→101 | 1 and 3 qubits, X/H/measure | 1000/1000 ones; ≈500/500; 1000/1000 zeros; `101` 100 % |
| 03 Bronze | Only 00 and 11 | H(0), CNOT(0,1), measure | no 01/10 |
| 03 Silver | Shared secret also agrees | Python coin flip, same for both | same 00/11 table |
| 03 Gold | Quantum S = 2√2 ≈ 2.83; classical S ≤ 2 | Bell pair, RY(−a), RY(−b), measure | S ≈ 2.8 (varies slightly each run, always > 2) |
| 03 no-signalling | Bob ≈ 50 % whatever Alice does | Alice: nothing / Z / X; Bob measures | ≈ 0.50 in all three |
| 05 | Majority vote → ASCII | classical decoding | "ECHO" |
| 05 Silver | ≥ 2 flips break it | all 8 flip patterns of 000 | 2 and 3 flips decode wrongly |
| 05 Gold | Entangled 3-qubit code fixes one bit flip | encode, error, syndrome, ccx | recovered 100 % for errors on any qubit; unprotected ≈ 79 % |
| 04 | X,H,H→1; H,X,H→0 | single qubit | matches; predictor agrees on 10 sequences |
| 06 Bronze | With Bob's correction the state arrives | 3-qubit teleportation, deferred X/Z corrections | Bob matches secret 100 % |
| 06 Silver | Without the 2 classical bits Bob gets a coin flip | same circuit, no correction | ≈ 0.50 overall; four different values for Alice's four outcomes, averaging to a coin flip |
| 06 Gold | Bob's raw statistics independent of the secret | secret angle 0 … π, Bob measures Z and X | ≈ 0.50 in every case |

*Counts vary slightly from run to run because quantum measurement is probabilistic; the conclusions do not.*

## 5. Interpretation

Module 03 is the key point. Perfect agreement is what Zara saw and what she called proof of a link. My experiments show that (a) a classical secret gives the same agreement, (b) a CHSH test is what distinguishes entanglement from a shared secret, and (c) no-signalling makes it impossible for the sender to control the receiver's outcome alone. Entanglement creates correlations; it does not transmit a message. Teleportation is not a message channel by itself; it requires ordinary classical communication as part of the protocol.

## 6. Alternative Explanation

**Competing theory:** ECHO really was a groundbreaking, working faster-than-light channel, and someone suppressed it. I prefer the simpler explanation because it requires no extraordinary suppression, no hidden lab physics, and no contradiction of the no-signalling result. A damaged stream, a shared secret, and a misread teleporter are all enough to create the illusion of a message without violating quantum limits.

## 7. Next Experiment

Re-run Zara's original detector data with **different measurement angles** (a CHSH-style test), and test **signalling directly**: have Alice randomly pick her setting and check whether Bob's statistics change in any way. If Bob's output remains 50/50, there is no faster-than-light signal. If a change appears, the correlation is real and must be fully explained, not just assumed.

## 8. Limitations

- I worked on a **simulator** with a mathematically ideal Bell pair; a real lab detector has noise and loopholes (detection and locality) that I did not model.
- Module 04 shows quantum states change when measured; it **does not** prove the log was quantum, nor that ARIA, Sana or anyone tampered with it.
- None of my modules identifies who (if anyone) manipulated the experiment; I make no accusation.
- The ≈95 % confidence is a judgment about the physics, not a statistical result.

## 9. References and AI / External Assistance

- Qiskit and Qiskit Aer documentation (IBM Quantum).
- IBM Quantum learning materials and example circuits used for the experiments.
- AI assistance: Claude and ChatGPT were used to help explain quantum concepts, draft code, and refine the report wording. I reviewed, ran, and verified the results independently.

