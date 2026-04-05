#### MASCA: LLM based-Multi Agents System for Credit Assessment

#### note

#### Problem

Traditional credit scoring systems (like rule-based or statistical models):
* Don’t use all available data effectively
* Are hard to interpret (not transparent)
* Are not flexible when situations change
Even basic LLM approaches (like simple prompting) struggle with:
* Complex reasoning
* Error buildup in long decision chains

#### Their Idea to Solve the Problem

The researchers propose MASCA, a system that:

* Uses multiple AI agents (powered by LLMs) instead of one model
* Mimics how real organizations make decisions (different teams handling different tasks)
* Breaks a complex decision (credit approval) into smaller, specialized steps

#### How They Solve It

They design a 3-layer system:

1. Layer 1: Understand the data

* Clean and prepare applicant data
* Build a profile (behavior, financial habits)
* Compute key metrics (like debt-to-income ratio)

2. Layer 2: Evaluate from two perspectives

* Risk team → looks for problems (debt, unstable income)
* Reward team → looks for benefits (profit potential, good history)

3. Layer 3: Final decision

* Balance risk vs reward
* Make the final approval/rejection decision

They also use Signaling Game Theory:

* Borrowers send signals (income, history)
* The system interprets these signals to make smarter decisions
#### Experimentation and Results
Tested on the German Credit Dataset using models like GPT-4o and o3-mini

#### Results:

* 60% accuracy and 73.33% F1 score
* This is ~20% better than traditional methods

Key findings:

* Multi-agent system > single model
* Hierarchical structure > flat structure
* Simple prompting methods performed worse
* Chain-of-thought failed due to error accumulation

#### Future Work / Limitations
* Currently depends on specific models (like GPT-4o)
Needs testing on:
* Open-source models (e.g., LLaMA)
* More diverse datasets

Bias still exists:
* Lower accuracy for female applicants
* Differences across ethnic groups

Future work will likely focus on:

* Reducing bias
* Improving fairness
* Making the system more generalizable