#### MetaGPT: Standardized Operating Procedures for Multi-Agent Software Engineering

MetaGPT is an innovative meta-programming framework designed for multi-agent collaboration based on Large Language Models (LLMs)
. By simulating a professional software company, it incorporates human Standardized Operating Procedures (SOPs) into prompt sequences to streamline workflows and improve the coherence of solutions
. It effectively decomposes complex tasks into subtasks assigned to specialized agents with roles such as Product Manager, Architect, and Engineer
.
#### Problem Identified
* The authors found that while existing LLM-based multi-agent systems can handle simple dialogue tasks, they struggle with complex software engineering problems
. 
* These systems often oversimplify tasks and suffer from logic inconsistencies caused by cascading hallucinations when LLMs are naively chained together
.
*  Additionally, existing frameworks frequently lack effective workflows and structured output formats, leading to communication errors like the "telephone game" effect, where original information becomes distorted through multiple rounds of interaction
.
#### The MetaGPT Solution 
* The core idea behind MetaGPT is to bridge the gap between LLM agents and real-world problem-solving by encoding human SOPs into the framework
. 
* Unlike previous models that rely on unconstrained natural language dialogue, MetaGPT requires agents to generate structured outputs, such as Product Requirements Documents (PRDs), system designs, and flowcharts
. 
* This approach minimizes ambiguities, reduces "idle chatter" between agents, and allows for human-like domain expertise to verify intermediate results
.

#### Methodology
The framework's methodology is built on three main pillars:
* Role Specialization: It defines specific roles—Product Manager, Architect, Project Manager, Engineer, and QA Engineer—each with its own goals, constraints, and specialized tools
.
* Communication Protocol: MetaGPT uses a shared message pool and a publish-subscribe mechanism
. 
* Agents subscribe to information relevant to their role and publish structured messages, preventing information overload and ensuring efficient data dissemination
.
* Iterative Programming with Executable Feedback: The framework includes a self-correction mechanism where the Engineer agent generates code, runs unit tests, and uses the runtime feedback and error logs to debug and improve the code iteratively
.

#### Experimentation and Evaluation Results
* MetaGPT was evaluated using HumanEval, MBPP, and a challenging new dataset called SoftwareDev
. 
* The results include:
State-of-the-Art Performance: MetaGPT achieved a Pass@1 score of 85.9% on HumanEval and 87.7% on MBPP, outperforming all previous approaches
.
* Robustness in Complex Tasks: In the SoftwareDev benchmark, MetaGPT achieved a 100% task completion rate and an executability score of 3.75 out of 4, significantly higher than competitors like ChatDev (2.25)
.
* Efficiency: It demonstrated higher productivity by using fewer tokens per line of code generated (124.3 tokens/line) compared to ChatDev (248.9 tokens/line)
.
* Ablation Success: Adding more specialized roles and the executable feedback mechanism consistently improved both code executability and reduced the cost of manual human revisions
.
#### Future Works
The authors outline several directions for future development:
* Recursive Self-Improvement: Developing mechanisms where agents learn from the experience of past projects to adjust their own constraint prompts and become more effective over time
.
* Multi-Agent Economies: Exploring "Economies of Mind" where agents use market principles like supply and demand to assign credit and self-organize their collaborations
.
* Expanded Capabilities: Incorporating multimodal tools and specialized agents to better handle UI and front-end development, which the current system does not fully cater to