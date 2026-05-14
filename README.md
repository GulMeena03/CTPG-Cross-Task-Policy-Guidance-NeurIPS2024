# CTPG – Cross-Task Policy Guidance (NeurIPS 2024)

Official implementation of **Cross-Task Policy Guidance** for multi-task continuous control (HalfCheetah-MT5).  
The method explicitly implements:

1. **Policy-Filter Gate** (§4.2) – masks out control policies whose comparable guide Q-value < V-value.
2. **Guide-Block Gate** (§4.3) – blocks guidance for already mastered tasks (log αᵢ > mean log αⱼ).
3. **Hindsight Off-Policy Correction** (§4.1) – relabels guide actions using maximum likelihood over stored actions.
