#### ChatDev: Communicative Agents for Software Development
ChatDev is a communicative framework for software development that utilizes multiple agents powered by large language models (LLMs)
. These agents, assigned specialized social roles (such as CEO, Programmer, and Tester), collaborate through multi-turn dialogues to autonomously complete the software development lifecycle—from design to testing
. The paper demonstrates that natural language can serve as a unifying bridge to connect fragmented development phases into a cohesive, automated process
.

#### The Problem Found
The authors identified two primary challenges in current AI-driven software development:
Fragmentation and Inconsistency: Existing deep learning models are often designed for specific, isolated phases (e.g., just coding or just testing), leading to technical inconsistencies and an ineffective overall development process
.
* Coding Hallucinations: LLMs frequently generate source code that is incomplete, unexecutable, or inaccurate
. 
* These "hallucinations" often stem from vague instructions, requiring manual intervention and reducing the reliability of the software
.
#### How They Solve It and Their Idea
The core idea is to establish language as a unifying bridge for multi-agent collaboration
. 
* They solve the identified problems through:
Chat Chain: A structure that breaks down the development process into sequential phases and manageable subtasks, guiding agents on what to communicate
.
* Communicative Dehallucination: A mechanism where agents proactively request specific details from one another before providing responses, which significantly reduces coding errors
.

#### Methodology
The ChatDev framework is built on four technical pillars:
* Agentization: LLMs are "hypnotized" via inception prompting to take on specific roles like CEO, CTO, Programmer, and Reviewer
.
* Chat Chain Structure: The lifecycle is divided into three main phases: Design, Coding, and Testing
. 
* Coding is further split into writing and completion, while testing includes code review (static) and system testing (dynamic)
.
* Dual-Agent Communication: Each subtask involves an Instructor and an Assistant reaching a consensus through dialogue, simplifying complex multi-agent interactions
.
* Memory Management: The system uses short-term memory for intra-phase dialogue continuity and long-term memory to transmit completed solutions across different phases
.
#### Experimentation and Evaluation Results
The authors evaluated ChatDev using a new dataset called SRDD (1,200 software requirement prompts) and compared it against baselines like GPT-Engineer and MetaGPT
.
* Superior Quality: ChatDev outperformed all baselines across every metric, achieving an overall Quality score of 0.3953 compared to MetaGPT's 0.1523
.
* High Executability: The framework reached an executability rate of 88%, demonstrating the effectiveness of the testing and dehallucination phases
.
* User Preference: In pairwise comparisons, human evaluators preferred ChatDev-generated solutions over 90% of the time against GPT-Engineer
.
* Ablation Insights: Removing agent roles or the dehallucination mechanism led to significant performance drops, proving that specialized roles and active communication are critical for success
.
#### Future Works
The authors suggest several directions for future research:
* Complex Real-World Applications: While effective for prototypes, the current technology needs to be adapted for larger, high-density information systems
.
* Enhanced Evaluation: Future work should consider factors beyond executability, such as robustness, safety, and user-friendliness
.
* Efficiency Optimization: Multiple agents consume more tokens and time; therefore, researchers should aim to enhance agent capabilities with fewer interactions and lower computational costs
.
