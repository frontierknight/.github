<div align="center">

# Frontier Knight Labs

**Advancing autonomous agents for cyber offense, defense, and learning — securing digital and physical worlds.**

</div>

---

Frontier Knight Labs builds autonomous cybersecurity agents that **run real tools on real systems** — not chatbots that recite playbooks — and the **benchmarks to measure them**, across digital and physical (robotic / embodied) systems. Each agent runs on [pi](https://pi.dev), ships an offline library of vetted security workflows, and executes Kali-native tooling one phase at a time, under an explicit authorization gate.

## Products

| | Agent | Role | What it does |
|---|---|---|---|
| 🔴 | **[Crimson Knight](https://github.com/frontierknight/crimson)** | Red team · offense | 9-phase MITRE ATT&CK kill chain · 7 offensive tools · 447 attack workflows. Runs Nmap, sqlmap, BloodHound, Impacket, Sliver… |
| 🔵 | **[Azure Knight](https://github.com/frontierknight/azure)** | Blue team · defense | 8-phase IR + threat-hunting chain · 8 defensive tools · 370 defense workflows. Runs Volatility, YARA, Sigma, Zeek, Splunk… |
| 🧠 | *Learning* | RL post-training | Reinforcement-learning post-trained security models — *in progress.* |
| 🤖 | **Knightfall** *(benchmark)* | ROS 2 security CTF range | A ROS 2 robotics-security CTF range for **both humans and AI agents** — reproducible, auto-scored scenarios that benchmark security agents against embodied systems. *In progress.* |

## Quick start (Kali)

```bash
# Red team — Crimson Knight
git clone https://github.com/frontierknight/crimson ~/crimson && cd ~/crimson && ./install.sh

# Blue team — Azure Knight
git clone https://github.com/frontierknight/azure ~/azure && cd ~/azure && ./install.sh

source ~/.zshrc
crimson  # 🔴     azure  # 🔵
```

Needs [pi](https://pi.dev) (Node ≥ 22). Each agent installs in an isolated config and leaves plain `pi` untouched.

## Responsible use

These agents execute real offensive and defensive commands. Operate **only on systems you are authorized to test or defend** — authorized pentests, your own or lab systems, CTFs. A two-step authorization gate enforces this before anything runs.
