# ECHO Case Report: *The Signal That Was Never Sent*

**Team:** `<TEAM NAME>` · **Members:** `<NAMES>` · **Stretch modules:** 04 (The Erased Measurement) and 06 (The Impossible Claim)
**Notebook:** `ECHO_Notebook.ipynb` (runs top to bottom in Google Colab)

---

## 1. Final Theory / Verdict

**Zara Mahmud did not send a message faster than light. ECHO produced a real but useless correlation: she mistook an echo for a voice.**

- Her twin detectors always agreed. That is genuinely what an entangled pair does, but it is *also* exactly what a boring pre-agreed secret does (Module 03).
- Even if her pair was truly entangled, entanglement cannot carry a message: the receiver's results look 50/50 whatever the sender does (Module 03, no-signalling test). The correlation only appears when both sides compare results over an ordinary classical channel.
- Her "teleportation" claim fails the same way: teleportation works only when two ordinary classical bits are sent as well. Without them the receiver gets a coin flip (Module 06).

**Confidence:** about **95 %** that ECHO was not faster-than-light signalling (this follows from physics we reproduced). Our confidence in *who* (if anyone) helped her believe it is **low**: our modules did not produce evidence strong enough to name a culprit, and we do not claim one (see Open Questions).

## 2. Evidence and Clues

1. **Module 01:** we can speak the machine's language (X, H, measure). Interference (H·H) shows quantum behaviour that a classical coin cannot mimic. Machine name and final-run time revealed on success: `<FILL FROM ORGANISERS' NOTEBOOK>`.
2. **Module 03:** the Bell pair gives only 00/11 (0 mismatches in 2000 shots), but a pre-agreed classical secret gives the same table. CHSH test gives **S ≈ 2.8 > 2** (classical limit 2), proving true entanglement. Bob's statistics stay 50/50 whatever Alice does.
3. **Module 05:** majority vote over the damaged stream recovers **"ECHO"**, and 20 of 32 triples were corrupted (one flip each). Note left beneath it: `<FILL FROM ORGANISERS' NOTEBOOK>`.
4. **Module 06:** teleportation succeeds 100 % with the two classical bits applied, but with no correction Bob's qubit matches the secret only ≈ 50 % of the time, and his raw measurement statistics are ≈ 0.50 whatever secret was sent. Nothing useful crosses without the classical channel.
5. **Module 04:** an unmeasured qubit's "changes" are exactly predictable (HH = I, HXH = Z); only a *measurement* destroys information. This bears on ARIA's claim that the log "changed when observed".

## 3. Evidence Board

| FACT (directly observed) | CLAIM (stated by a suspect/log) | INFERENCE (our interpretation) | OPEN QUESTION |
|---|---|---|---|
| Bell pair gave 00/11 only, 0 mismatches in 2000 shots | Zara: always-agreeing detectors prove a link across space | Agreement alone is insufficient evidence; a shared secret fits equally well | Was Zara's original pair ever tested at different angles (CHSH)? |
| A classical shared secret reproduces the same 00/11 table | Zara: ECHO sent a message faster than light | Correlation was misread as communication | Did anyone steer her toward that reading? |
| CHSH S ≈ 2.8 (> 2) for a Bell pair; classical max = 2 | ARIA: "No unauthorised command was issued" | A genuine entangled pair can exist, yet still cannot signal | Who configured ARIA's schedule? |
| Bob's marginal is ≈50/50 for every Alice action | Sana: "I only deleted a corrupted log" | No receiver could read a message from Alice's choices alone | What exactly was in the deleted log, and when? |
| Majority vote decodes the stream to "ECHO" (20/32 triples hit) | ARIA: log "changed when observed" | A *quantum state* can change when measured; a classical log file should not | Was the log a quantum record or an ordinary file? |
| H·H → always 0; H·measure·H → 50/50 | Bilal: "I warned her" (report now missing) | His report may be the only independent check on the discrepancy | Why is Bilal's report missing, and who had access? |
| Teleportation: 100 % with the 2 classical bits, ≈ 50 % without; Bob's raw statistics ≈ 0.50 for every secret | Zara: "teleported a message, no qubit crossing the gap" | Her message could only arrive with a classical channel, so it was not faster-than-light | Did her setup contain a classical link she overlooked? |

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

Module 03 is the crux. Perfect agreement is what Zara saw and what she called proof of a link. Our experiments show that (a) a classical secret gives the same agreement, (b) a CHSH test is what actually distinguishes the two, and (c) even a *real* entangled link gives Bob uniformly random results regardless of Alice's choice. So a message cannot be sent through it. Module 05 shows that a damaged *classical* message can be repaired by redundancy, whereas copying cannot protect a *quantum* state (no-cloning), which matches the theme: classical information needs classical channels. Module 06 is the climax: even the strongest use of entanglement, teleportation, needs a classical channel, and without it Bob's results are independent of the message, so ECHO cannot have been faster-than-light. Module 04 shows that a quantum state really can "change when observed", but only because of measurement, which we can predict; this supports ARIA's claim only if the log was a quantum record, which is not established.

## 6. Alternative Explanation

**Competing theory:** ECHO really was a groundbreaking, working faster-than-light channel, and someone suppressed it (Vance, the rival, or the system staff). We prefer our theory because it needs no new physics: it follows from established results (entanglement correlations cannot signal, and the no-signalling property reproduced in our test). The competing theory also cannot explain why Bob's results would show nothing unless the two sides compare notes. If ECHO were a real channel, Bob's statistics alone would change with Alice's action, and in every setup we can build they do not.

## 7. Next Experiment

Re-run Zara's original detector data with **different measurement angles** (a CHSH-style test), and test **signalling directly**: have Alice randomly pick her setting and check whether Bob's statistics depend on it, with the settings recorded by an independent party (not ARIA or Sana). If S ≤ 2 → her link was classical; if S > 2 but no signalling → entanglement without a message (our verdict). Also recover the missing report from Bilal and the original ARIA schedule configuration to settle the human question.

## 8. Limitations

- We worked on a **simulator** with a mathematically ideal Bell pair; a real lab detector has noise and loopholes (detection and locality) that we did not model.
- Module 04 shows quantum states change when measured; it **does not** prove the log was quantum, nor that ARIA, Sana or anyone tampered with it.
- None of our modules identifies who (if anyone) manipulated the experiment; we make no accusation.
- The ≈95 % confidence is a judgment about the physics, not a statistical result.

## 9. References and AI / External Assistance

- ECHO Participant Manual and the organisers' notebook (Qubits Qrew, NED University).
- Qiskit and Qiskit Aer documentation (IBM).
- Nielsen & Chuang, *Quantum Computation and Quantum Information* (repetition code, no-cloning, CHSH).
- Clauser, Horne, Shimony, Holt (1969), CHSH inequality.
- **AI assistance:** Claude (Anthropic) helped draft the notebook code and report text and explained the concepts. The team reviewed, ran and understands the results.
