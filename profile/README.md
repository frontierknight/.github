<div align="center">

# Frontier Knight Labs

**Advancing autonomous agents for cyber offense, defense, and learning — securing digital and physical worlds.**

</div>

---

Frontier Knight Labs builds autonomous cybersecurity agents that **run real tools on real systems** — not chatbots that recite playbooks. Each agent runs on [pi](https://pi.dev), ships an offline library of vetted security workflows, and executes Kali-native tooling one phase at a time, under an explicit authorization gate.

## Products

| | Agent | Role | What it does |
|---|---|---|---|
| 🔴 | **[Wraith](https://github.com/frontierknight/wraith)** | Red team · offense | 9-phase MITRE ATT&CK kill chain · 7 offensive tools · 447 attack workflows. Runs Nmap, sqlmap, BloodHound, Impacket, Sliver… |
| 🔵 | **[Aegis](https://github.com/frontierknight/aegis)** | Blue team · defense | 8-phase IR + threat-hunting chain · 8 defensive tools · 370 defense workflows. Runs Volatility, YARA, Sigma, Zeek, Splunk… |
| 🧠 | *Learning* | RL post-training | Reinforcement-learning post-trained security models — *in progress.* |

## Quick start (Kali)

```bash
# Red team
git clone https://github.com/frontierknight/wraith ~/wraith && cd ~/wraith && ./install.sh

# Blue team
git clone https://github.com/frontierknight/aegis ~/aegis && cd ~/aegis && ./install.sh

source ~/.zshrc
wraith   # 🔴     aegis   # 🔵
```

Needs [pi](https://pi.dev) (Node ≥ 22). Each agent installs in an isolated config and leaves plain `pi` untouched.

## Responsible use

These agents execute real offensive and defensive commands. Operate **only on systems you are authorized to test or defend** — authorized pentests, your own or lab systems, CTFs. A two-step authorization gate enforces this before anything runs.
