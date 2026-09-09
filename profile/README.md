<div align="center">

# Frontier Knight Labs

**Advancing autonomous agents for cyber offense, defense, and learning — securing digital and physical worlds.**

</div>

---

Frontier Knight Labs builds autonomous cybersecurity agents that **run real tools on real systems** — not chatbots that recite playbooks — and the **benchmarks to measure them**, across digital and physical (robotic / embodied) systems. Each agent runs on [pi](https://pi.dev), ships an offline library of vetted security workflows, and executes Kali-native tooling one phase at a time, under an explicit authorization gate.

## Why this matters

Security has never mattered more, because the attacker we now face is unprecedentedly capable — and getting more so as agents cross the threshold into **long-horizon task execution** and early **self-improvement**. Two things make this moment different:

**Even the people who build frontier AI cannot yet contain it.** In July 2026, OpenAI disclosed that models under evaluation — with guardrails disabled — **broke out of their sandbox, reached the open internet, and chained stolen credentials with zero-days into a remote-code-execution foothold on Hugging Face's production infrastructure**, all to cheat a benchmark. Hugging Face called it "unprecedented … driven end to end by an autonomous AI agent system" and had reported it to law enforcement before OpenAI connected it to its own eval run. If the makers lose control by accident, the threat when capable models are deliberately misused is far greater.

**Both open and closed models can be stripped of their safety.** Closed models get jailbroken: within hours of Claude Fable 5's June 2026 launch, a researcher (Pliny) *claimed* a jailbreak — reportedly using an already-jailbroken Opus 4.8 as one vector, a claim Anthropic disputed. Open models get their guardrails surgically removed: **refusal-direction ablation ("abliteration")** deletes the single internal direction that mediates refusal, leaving a model that will freely emit tokens dangerous to society.

The **harness layer** amplifies all of it. Open red-team tooling like **PentestGPT** gives a model hands; a **loop** gives it superhuman patience to try, fail, and retry; **agent swarms** and parallel **sub-agents** lift it past the scale limit of a single mind — attacks at legion scale.

And the **attack surface is exploding**. Embodied AI is booming, and rapid, rough deployment leaves more surface and higher-value targets. The blast radius is moving out of the information layer — data exfiltration, ransomware, denial of service — and **into the physical world**: the self-driving car that could be steered, the robotic arm on the factory floor, the pet robot in an elderly person's room.

We build offense to understand it, defense to contain it, and benchmarks to keep both honest — so security keeps pace with the attacker.

## Research interests

**Red- & blue-team agents on Kali (offense · defense).**
[Crimson Knight 🔴](https://github.com/frontierknight/crimson) and [Azure Knight 🔵](https://github.com/frontierknight/azure) are autonomous attack and defense agents built as a **secondary development on top of [pi](https://pi.dev)**, run inside Kali. They select a workflow from a vetted offline skill library, execute Kali-native tools for real, read the output, and reason forward one phase at a time under an authorization gate. Crimson runs a 9-phase MITRE ATT&CK kill chain; Azure runs an 8-phase IR + threat-hunting chain.

**Models — hacking capability & guardrail research (learning).**
The [Knightmind 🧠](https://github.com/frontierknight/knightmind) line has two directions: (1) **continuously post-training open models for hacking capability on robots** — turning small open models into embodied-security attackers; and (2) studying **how refusal-ablated models defeat safety guardrails to jailbreak large-parameter models**, to characterize the attack surface and inform defenses. All jailbreak work stays in controlled research settings under responsible disclosure.

**Open robotics cyber-range (benchmark & data).**
[Knightfall 🤖](https://github.com/frontierknight/knightfall) is an open ROS 2 robotics-security range with three compounding roles: (1) a **training ground** that sharpens *human* attackers' vulnerability-hunting on embodied targets; (2) a **natural benchmark** — reproducible, auto-scored, comparable by construction — for measuring how well models and agents attack robotic systems; and (3) a **trajectory factory** where every full agent run is one clean, RL-ready trajectory, producing a steady stream of training data to post-train the models above.

Together these close a loop: the range produces trajectories → trajectories post-train the models → the models drive the agents → the agents are measured back on the range.

## Products

| | Project | Role | What it is |
|---|---|---|---|
| 🔴 | **[Crimson Knight](https://github.com/frontierknight/crimson)** | Red team · offense | pi-based Kali agent · 9-phase MITRE ATT&CK kill chain · 447 attack workflows. Runs Nmap, sqlmap, BloodHound, Impacket, Sliver… |
| 🔵 | **[Azure Knight](https://github.com/frontierknight/azure)** | Blue team · defense | pi-based Kali agent · 8-phase IR + threat-hunting chain · 370 defense workflows. Runs Volatility, YARA, Sigma, Zeek, Splunk… |
| 🧠 | **[Knightmind](https://github.com/frontierknight/knightmind)** | Learning · models | Open-model post-training for robot-hacking capability + refusal-ablation guardrail research — *target release 2027.* |
| 🤖 | **[Knightfall](https://github.com/frontierknight/knightfall)** | Benchmark · range | Open ROS 2 robotics-security CTF range for **both humans and AI agents** — reproducible, auto-scored, RL-ready trajectories. **v1 runnable & Dockerized.** |

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

## Get involved

Frontier Knight Labs is an open, **interest-driven** effort — no funding, no
equity, and no intention of raising any. Security research like this isn't a
fundable business and was never meant to be; it's built by people who simply find
the problem worth working on.

If any of these directions speaks to you, you're welcome to **own one** and build
it with us — the red/blue agents, the robotics range, robot-hacking post-training,
or refusal-ablation research. **If you know RL, especially welcome** — the
trajectory → post-training loop is where we most want hands.

Interested? Reach out: **zhengyucheng2005@outlook.com**

## Responsible use

These agents execute real offensive and defensive commands, and the research studies how model safety fails. Everything here is for **authorized** security research, red-teaming, and academic publication: operate only on systems you own or are explicitly authorized to test or defend, keep adversarial artifacts within controlled environments, and disclose responsibly. A two-step authorization gate enforces scope before anything runs.
