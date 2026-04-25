# SpamGaurd - Automata Bases Spam Filter
**An rule-based spam detection system** that combines two classical computer science concepts.
 -> Finite State Automata (FSA) - for decision making logic
 -> Regular Expressions (Regex) - for pattern matching
to classify emails as HAM, Suspicious or SPAMS without any machine-learning dependencies**

--Overview-- 
This project implements classical automata theory and pattern matching techniques from Natural Language Processing (NLP). Instead of relying on machine learning, the system uses:
-> A weighted keyword dictionary (45 keywords across 6 categories)
-> A Regex Pattern Engine with leet-speak normalization and flexible spacing
-> A Finite State Automaton to make the final classification decision

The result is a fully interpretable, auditable spam detector — you can see exactly why every email was flagged.

**Features**
-> Keyword Matching - 45 weighted words across 6 catagories
-> FSA Classification - rule-based machine with 4 states
-> Leet Speak Normalization - catches obfuscated texts
-> Flexible Regex - handles keyword patters
-> Spam Amplifiers - detects texts which are suspicious even without keyword hit
-> False Positive Reducer - protects legit emails
-> Detailed-Metrics - per email breakdown with score, state trace and matched
-> Testing - test any custom email

**Installation**
No external libraries required beyond python standard library

# Clone or download the project
git clone https://github.com/your-username/spam-filter.git
cd spam-filter

Launch Jupyter Notebook
jupyter notebook spam_filter.ipynb

Requirements:
Python 3.7+
Jupyter Notebook or JupyterLab

Limitations:
No learning — new spam patterns must be added manually to the keyword dictionary
Language — currently supports English only
Context-blind — does not understand sentence meaning, only surface patterns
Determined thresholds — score thresholds (3 and 7) are manually set and may need tuning for different datasets
