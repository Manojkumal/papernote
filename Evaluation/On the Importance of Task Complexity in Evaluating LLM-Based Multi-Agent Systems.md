#### On the Importance of Task Complexity in Evaluating LLM-Based Multi-Agent Systems

#### note:

#### Problem

Researchers didn’t clearly understand when and why multi-agent AI systems (LLM-MAS) perform better than single-agent systems (LLM-SAS).

Most past work only looked at final performance (accuracy/output quality), but didn’t explain:

What kind of tasks actually benefit from multiple agents
What makes a task “hard” in a meaningful way

#### Idea to Solve the Problem

They propose that the key is task complexity, and define it using two factors:

Depth (d) → How many steps of reasoning are needed (like a long chain of thinking)
Width (w) → How many different skills/knowledge types are needed at each step


#### How They Solve It



They 
1. Build a mathematical model
* A task = sequence of steps
* Each step has multiple smaller operations (width)
* Each operation has some chance of failure
2. Compare systems theoretically
* Single-agent: does everything alone → errors accumulate
* Multi-agent: multiple agents collaborate → can check and fix mistakes
3. Key theoretical insights
* As tasks get deeper, single-agent errors stack up quickly
* Multi-agent systems reduce this by cross-checking intermediate steps
* As tasks get wider, multiple agents help by splitting different skills

#### Experimentation and Results

They tested their ideas on two types of tasks:

A. Math Reasoning
Controlled difficulty using structured problems (graphs of operations)
B. Creative Writing (new benchmark: DW2)
Depth = number of sentences
Width = number of different topics/keywords to include

Results
* Both systems perform worse as tasks get harder (good validation of their complexity definition)
* Multi-agent systems improve more than single-agent systems as complexity increases
* Depth is the most important factor:
* Long reasoning chains hurt single agents a lot
* Multi-agents handle them better via collaboration
* In writing tasks Multi-agents were better at handling multiple constraints (like covering many topics)


### Future Work

* Building adaptive multi-agent systems that:
* Change number of agents based on task complexity
* Adjust how agents communicate
* Designing better benchmarks that:
* Reward collaboration, critique, and consensus-building
* Developing systems that analyze a task first and then decide:
