# DFA Minimizer

A browser-based tool for minimizing Deterministic Finite Automata (DFA) using the **Table-Filling (Myhill–Nerode) Algorithm**, with step-by-step visualization and an interactive string simulator.

Built as part of a **Theory of Computation (TOC)** assignment.

---

## Live Demo

👉 [https://dfa-minimizer-git-main-rithwikjoshis-projects.vercel.app/](https://dfa-minimizer-git-main-rithwikjoshis-projects.vercel.app/)

---

## Repository

👉 [https://github.com/rithwikjoshi/dfa-minimizor](https://github.com/rithwikjoshi/dfa-minimizor)

---

## Features

- Real-time DFA minimization via the Table-Filling algorithm
- Step-by-step visualization of each iteration
- Distinguishability table rendered after minimization
- Equivalent state groups with union-find merging
- Minimized DFA transition table with start/accept state labels
- SVG state diagram with directed edges and color-coded states
- String simulator — test any input and trace the full execution path
- Responsive UI — works on desktop and mobile

---

## Algorithm Overview

Implements the **Myhill–Nerode Theorem** via Table-Filling:

1. Remove all unreachable states
2. Mark pairs `(p, q)` where exactly one state is an accept state
3. Iteratively mark pairs whose transitions lead to an already-marked pair
4. Repeat until no new pairs are marked
5. Merge all unmarked (equivalent) pairs
6. Construct the minimized DFA

---

## Getting Started

No build tools or dependencies required.

```bash
git clone https://github.com/rithwikjoshi/dfa-minimizor.git
cd dfa-minimizor
open index.html
```

Or just double-click `index.html` — it runs entirely in the browser.

---

## Project Structure

```
dfa-minimizor/
├── index.html   # Full application (HTML + CSS + JS in one file)
└── README.md
```

---

## Usage

1. **Enter DFA details** — states, alphabet, start state, accept states
2. **Fill the transition table** — auto-generated from your input (use **Load Example** to try a sample)
3. **Click Minimize** — see the full step-by-step breakdown, distinguishability table, and state diagram
4. **Simulate strings** — test inputs against the minimized DFA

---

## Example

```
States:        q0, q1, q2, q3, q4, q5
Alphabet:      a, b
Start state:   q0
Accept states: q2, q4
```

After minimization, equivalent states are merged and the DFA is reduced to 3 states.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 |
| Logic | Vanilla JavaScript |
| Visualization | Inline SVG |
| Deployment | Vercel |

Zero external dependencies.
