# CTPG – Cross-Task Policy Guidance (NeurIPS 2024)

Official implementation of **Cross-Task Policy Guidance** for multi-task continuous control (HalfCheetah-MT5).  
The method explicitly implements:

1. **Policy-Filter Gate** (§4.2) – masks out control policies whose comparable guide Q-value < V-value.
2. **Guide-Block Gate** (§4.3) – blocks guidance for already mastered tasks (log αᵢ > mean log αⱼ).
3. **Hindsight Off-Policy Correction** (§4.1) – relabels guide actions using maximum likelihood over stored actions.

## Requirements

- Python 3.8+
- MuJoCo (free license, e.g., `mujoco==3.1.6`)
- Gymnasium 0.29.1
- PyTorch 2.0+
- See `requirements.txt`

## Installation

```bash
git clone https://github.com/yourusername/CTPG-NeurIPS2024.git
cd CTPG-NeurIPS2024
pip install -r requirements.txt
