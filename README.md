# Multi-Agent Pacman — Adversarial Search

## Overview
This project implements **multi-agent adversarial search algorithms** in a game environment using Pacman as a testbed.

The focus is on **decision-making under competition and uncertainty**, where Pacman must reason about multiple adversarial agents (ghosts) that act either optimally or probabilistically.

> ⚠️ This repository contains **only my implemented AI logic**.  
> The original UC Berkeley CS188 Pacman framework is **not included**.

---

## Implemented Algorithms

### Reflex-Based Agent
- Reflex agent using a custom evaluation function
- Considers food distance, ghost proximity, and terminal states

### Adversarial Search
- **Minimax**
  - Supports multiple ghost agents
  - Depth-limited search
  - Worst-case decision modeling

- **Alpha-Beta Pruning**
  - Optimized minimax search
  - Prunes unnecessary branches
  - Same minimax values with fewer explored states

### Stochastic Search
- **Expectimax**
  - Models ghosts as probabilistic agents
  - Uses expected utility instead of worst-case assumptions
  - More realistic behavior against non-optimal opponents

---

## Evaluation Function
- Custom state evaluation function
- Balances:
  - Remaining food
  - Distance to food
  - Ghost distance & scared timers
  - Game score
- Optimized for both performance and computational efficiency

---

## Project Structure
multiagent/
└── multiAgents.py # All implemented agents & algorithms
