# ArmRL — RL + Robotics: From Reach to Pick-and-Place

Reinforcement learning on a simulated Fetch arm: reaching, pushing, pick-and-place.

**Status:** Phase 1 — infrastructure setup

## Stack
MuJoCo · Gymnasium-Robotics · Stable-Baselines3 · PyTorch · Weights & Biases

## Setup
**Requirements:** [Python 3.11.9](https://www.python.org/downloads/release/python-3119/) · (Optional: CUDA 12.4+ GPU for faster training)

```bash
git clone https://github.com/MatiasPF1/ArmRL.git
cd ArmRL
py -3.11 -m venv venv        # Windows (ensures Python 3.11)
# python3.11 -m venv venv    # macOS/Linux

venv\Scripts\activate        # Windows
# source venv/bin/activate   # macOS/Linux

pip install -r requirements.txt
```

