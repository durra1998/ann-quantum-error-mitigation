# Artificial Neural Network(ANN)-Based Quantum Error Mitigation

This repository presents a simulation-based investigation of machine learning–driven quantum error mitigation using artificial neural networks (ANNs). The work investigates how classical neural models can learn and reduce noise-induced distortions in quantum measurement outcomes on near-term (NISQ) quantum devices, without relying on quantum error correction.

The project focuses on modeling depolarizing gate noise using Qiskit Aer and evaluating the effectiveness of **ordinary versus concatenated ANN architectures** for mitigating errors across increasing system sizes. The implementation emphasizes reproducibility, scalability analysis, and clear performance baselines.

---

## Motivation
Near-term quantum computers are inherently noisy, and full quantum error correction remains impractical due to high qubit and resource overhead. As a result, **quantum error mitigation (QEM)** techniques have emerged as a promising alternative. Among these, **machine learning–based approaches** offer flexibility in learning complex, hardware-dependent noise patterns from data. This work explores ANN-based QEM as a hybrid quantum–classical strategy to reduce noise effects in simulated quantum circuits.

---

## Methodology
- Random entangling quantum circuits are generated using a universal gate set.
- Circuits are simulated using Qiskit Aer under single-qubit depolarizing gate noise.
- Measurement outcomes are converted into probability distributions.
- Noise-induced error is defined as the deviation between noisy and ideal distributions.
- Two neural architectures are trained and compared:
  - **Ordinary feedforward ANN**
  - **Concatenated (deeper) ANN**
- Performance is evaluated using **Root Mean Square Error (RMSE)** and analyzed as a function of qubit number.

---

## Key Results
- Noisy (unmitigated) quantum circuits exhibit increasing RMSE as the number of qubits grows, reflecting accumulated noise effects.
- ANN-based models consistently reduce RMSE compared to unmitigated baselines across all tested system sizes.
- The **concatenated ANN architecture** demonstrates improved robustness for larger qubit numbers, suggesting that deeper hierarchical models better capture complex noise behavior.
- Results indicate that learning-based error mitigation can partially counteract noise growth in multi-qubit quantum circuits.

---


