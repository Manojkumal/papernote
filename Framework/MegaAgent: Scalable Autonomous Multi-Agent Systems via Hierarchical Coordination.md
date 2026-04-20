#### MegaAgent: Scalable Autonomous Multi-Agent Systems via Hierarchical Coordination

MegaAgent is a large-scale autonomous LLM-based multi-agent system (MAS) designed to handle complex tasks without relying on human-predefined Standard Operating Procedures (SOPs)
. Inspired by operating system (OS) design, it manages agents through a hierarchical structure that enables dynamic task decomposition, parallel execution, and systematic monitoring
.
#### Problem Identified
The authors identified several critical limitations in existing multi-agent systems:
* Limited Scalability and Coordination: Existing systems fail to achieve adaptive coordination when tasks require hundreds of agents, such as in social simulations
.
* Reliance on Predefined SOPs: Most MAS depend heavily on user-defined configurations, including specific agent roles, static communication graphs, and manual SOPs, which limits flexibility and requires excessive human effort
.
* Communication Inefficiencies: Managing communication becomes difficult as tasks grow in scale, particularly when coordinating multiple agents across parallel processes
.
* Reliability Issues: LLM agents often generate hallucinated outputs or fail to complete tasks correctly in a single round; without robust monitoring, these errors propagate through the system
.
#### Solution and Core Idea
The authors propose MegaAgent, which treats agents as processes or threads within an OS-like framework
. 
* The core idea is to eliminate the need for manual SOPs by assigning LLM agents to autonomously split tasks and generate their own procedures
.
* Boss Agent: A central controller that receives a meta-prompt and autonomously initiates the task
.
* Dynamic Hierarchical Structure: The system recursively decomposes large tasks into hierarchical subtasks, with "Admin Agents" recruiting "Ordinary Agents" as needed based on task complexity
.
* Parallelism: Unlike sequential baseline systems, MegaAgent allows different agent groups to operate in parallel, significantly reducing completion time
.
#### Methodology
MegaAgent’s architecture is built on two primary pillars:
Hierarchical Task Management:
* Task Splitting: The Boss Agent divides the main task into subtasks for Admin Agents, who can further recruit subordinates to form recursive, dynamic groups
.
* Message Queue: Uses a producer-consumer paradigm where agents cycle through "Idle," "Processing," and "Response" states to manage asynchronous communications efficiently
.
* File and Memory Management: Implements Git-based version control to prevent conflicts during concurrent file edits and utilizes a vector database for long-term memory retrieval
.
* Hierarchical Monitoring:
Agent-Level: Each agent tracks progress via a self-generated checklist
.
* Group-Level: Admin Agents supervise their groups, flagging errors and prompting retries
.
* System-Level: The Boss Agent reviews final outputs from all groups to ensure overall accuracy and format consistency
.
#### Experimentation and Evaluation Results
MegaAgent was evaluated across three main domains, consistently outperforming baselines like MetaGPT and AutoGen:
* Standard Benchmarks: It achieved superior accuracy on reasoning and coding tasks, scoring 92.2% on MBPP, 93.3% on HumanEval, and 93.0% on GSM-8K
.
* Software Development (Gobang Game): MegaAgent was the only system to successfully develop a fully functional Gobang game (including AI logic and UI) within 800 seconds
. Baselines either failed to produce executable code or became stuck in loops
.
* Social Simulation (National Policy Generation): The system successfully coordinated 590 agents to generate multi-domain policies in roughly 3,000 seconds
. In contrast, baselines typically managed fewer than 10 agents and failed to produce comprehensive outcomes
.
* Efficiency: MegaAgent demonstrated a linear-to-logarithmic communication cost reduction (O(logn) for n agents), with an average processing time of just 5 seconds per agent in large-scale simulations
.
#### Future Works
The authors highlight several areas for future improvement:
* Token Optimization: Reducing high input-output token consumption by exploring advanced summarization, semantic compression, and more efficient dialogue storage methods
.
* Robust Hallucination Mitigation: Addressing persistent errors by incorporating external expert knowledge bases during the verification process
.
* Integration and Cost: Integrating specialized, domain-specific LLMs to reduce the high API costs associated with using models like GPT-4o for all tasks
.