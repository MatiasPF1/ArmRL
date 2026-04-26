# ArmRL --> RL + Robotics: From Reach to Pick-and-Place

An iterative reinforcement learning study on robotic manipulation,
training a simulated Fetch arm through tasks of increasing difficulty:
reaching, pushing, and pick-and-place.

**Status:** in progress — Phase 1 (infrastructure setup).

## Stack
- MuJoCo physics simulator
- Gymnasium + Gymnasium-Robotics
- Stable-Baselines3 (SAC, PPO, HER)
- imitation library (behavior cloning)
- PyTorch, Weights & Biases

## Setup

**Requirements:** Python 3.11.9 · CUDA 12.4 (for GPU support)

```bash
# Clone the repo
git clone https://github.com/MatiasPF1/ArmRL.git

# Create and activate virtual environment
python -m venv venv

# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate

# Install PyTorch with CUDA 12.4 support
pip install torch --index-url https://download.pytorch.org/whl/cu124

# Install remaining dependencies
pip install -r requirements.txt
```

> To keep `requirements.txt` up to date after installing new packages:
> ```bash
> pip freeze > requirements.txt
> ```

