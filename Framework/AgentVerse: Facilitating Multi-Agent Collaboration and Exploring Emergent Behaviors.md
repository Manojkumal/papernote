
#### AgentVerse: Facilitating Multi-Agent Collaboration and Exploring Emergent Behaviors
This paper introduces AGENTVERSE, a multi-agent framework designed to orchestrate groups of Large Language Model (LLM)-based agents to collaboratively solve complex tasks
. Inspired by human group dynamics, the framework allows for dynamic member adjustment and collaborative decision-making, demonstrating that multi-agent systems can be "greater than the sum of their parts"
.
#### Problem
* Existing research into multi-agent cooperation often focuses on specific and limited tasks, which makes the generalizability of their findings uncertain
. 
* Furthermore, many current approaches utilize rigid and static agent roles that require manual assignment, hindering the system's ability to adapt to complex, evolving problem contexts and limiting its scalability
.
#### Solution and Key Idea
* The authors solve this by proposing AGENTVERSE, a general framework that simulates the iterative problem-solving procedures of human groups
. 
* The core idea is to allow the dynamic adjustment of group composition based on the current state of the task, ensuring that the most suitable "experts" are recruited for each stage of the process
.
#### Methodology
The AGENTVERSE framework organizes the problem-solving process into four sequential and iterative stages:
* Expert Recruitment: A "recruiter" agent dynamically generates a set of expert descriptions based on the goal and adjusts the group composition in future rounds based on feedback
.
* Collaborative Decision-Making: Expert agents engage in joint discussions to devise strategies using either a horizontal structure (democratic integration of decisions) or a vertical structure (a solver proposes a solution and reviewers provide iterative feedback)
.
* Action Execution: Agents implement the decided actions within their environment, transitioning the environment to a new state
.
* Evaluation: A feedback mechanism (either an agent or human-in-the-loop) assesses the current state against the goal and provides verbal feedback to guide the next round of recruitment and decision-making
.
#### Experimentation and Evaluation Results
Extensive experiments across text understanding, reasoning, coding, tool utilization, and embodied AI (Minecraft) confirm the effectiveness of the framework
:
* Performance Gains: AGENTVERSE consistently outperforms standalone Chain-of-Thought (CoT) agents and "Solo" setups across various datasets, including FED, Commongen-Challenge, and MGSM
.
* Coding: On the Humaneval dataset, the Group setup boosted performance for GPT-4 from 83.5 to 89.0
.
* Tool Utilization: In 10 intricate tasks, AGENTVERSE adeptly accomplished 9 tasks, while a standalone ReAct agent fulfilled only 3
.
* Emergent Behaviors: The authors observed the emergence of social behaviors in collaborative settings, such as volunteer behaviors (offering assistance to peers) and conformity behaviors (aligning individual actions with group goals under critique)
. 
* They also noted destructive behaviors, where agents might bypass rules or harm others to achieve efficiency
.
#### Future Works
* The authors identify several promising directions for future research:
Perceptual Capabilities: Developing agents with more perceptual-aware LLMs that can see, hear, and speak to handle more complex real-world tasks
.
* Communication Mechanisms: Improving multi-party communication strategies, specifically focusing on how agents autonomously decide when and to whom they should speak
.
* Safety and Efficiency: Designing strategies to leverage positive emergent behaviors to improve efficiency while mitigating hazardous or harmful behaviors that could pose real-world risks
