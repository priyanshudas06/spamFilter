# SpamGuard — Automata-Based Spam Filter

> A rule-based spam detection system that combines two classical computer science concepts:
>
> - **Finite State Automaton (FSA)** — for decision-making logic
> - **Regular Expressions (Regex)** — for pattern matching
>
> Classifies emails as **HAM**, **Suspicious**, or **SPAM** — with zero machine-learning dependencies.

---

## Overview

SpamGuard implements classical automata theory and pattern matching techniques from **Natural Language Processing (NLP)**. Instead of relying on machine learning, the system uses:

- A **weighted keyword dictionary** — 45 keywords across 6 categories
- A **Regex Pattern Engine** — with leet-speak normalization and flexible spacing
- A **Finite State Automaton** — to make the final classification decision

The result is a fully **interpretable, auditable** spam detector — you can see exactly _why_ every email was flagged.

---

## Features

| Feature                  | Description                                              |
| ------------------------ | -------------------------------------------------------- |
| Keyword Matching         | 45 weighted keywords across 6 spam categories            |
| FSA Classification       | Rule-based state machine with 4 states                   |
| Leet-Speak Normalization | Catches obfuscated text like `fr33`, `m0ney`             |
| Flexible Regex           | Handles varied keyword patterns (`f.r.e.e`, `f-r-e-e`)   |
| Spam Amplifiers          | Detects suspicious signals even without keyword hits     |
| False Positive Reducer   | Protects legitimate emails from being wrongly flagged    |
| etailed Metrics          | Per-email breakdown with score, state trace, and matches |
| Custom Testing           | Test any email with a single cell                        |

---

## Installation

No external libraries are required beyond the Python standard library.

**1. Clone or download the project**

```bash
git clone https://github.com/your-username/spam-filter.git
cd spam-filter
```

**2. Launch Jupyter Notebook**

```bash
jupyter notebook spam_filter.ipynb
```

**Requirements**

- Python 3.7+
- Jupyter Notebook or JupyterLab

---

## Limitations

- **No learning** — new spam patterns must be added manually to the keyword dictionary
- **Language** — currently supports English only
- **Context-blind** — does not understand sentence meaning, only surface patterns
- **Fixed thresholds** — score thresholds (3 and 7) are manually set and may need tuning for different datasets
