# ArmRL — RL + Robotics
Reinforcement learning on a simulated Fetch arm: reaching, pushing, pick-and-place. An iterative study, documented progression through the core challenges of manipulation RL.

**Status:** infrastructure setup ✅

## Stack
MuJoCo · Gymnasium-Robotics · Stable-Baselines3 · PyTorch (CUDA 12.4) · Weights & Biases

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

### Weights & Biases
Experiment tracking uses W&B. Copy `.env.example` to `.env` and fill in your API key:

```bash
cp .env.example .env
# then edit .env and replace the placeholder with your key from https://wandb.ai/authorize
```

### Verify the install

```bash
python -c "import gymnasium as gym; import gymnasium_robotics; from stable_baselines3 import SAC; gym.register_envs(gymnasium_robotics); env = gym.make('FetchReach-v4'); model = SAC('MultiInputPolicy', env, verbose=0); print('OK')"
```
You should see `OK` printed. If so, the full stack is working.


## Repository structure
```
ArmRL/
├── README.md           # this file
├── requirements.txt    # exact pinned dependencies
├── .env.example        # template for API keys
└── .gitignore
```

Training scripts and writeups will be added as the project grows.

