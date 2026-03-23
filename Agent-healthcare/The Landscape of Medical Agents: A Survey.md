#### The Landscape of Medical Agents: A Survey

#### note
The research paper "The Landscape of Medical Agents: A Survey," published on November 30th, 2025, provides a comprehensive overview of the transition from static, task-specific medical artificial intelligence (MedAI) to dynamic, workflow-integrated Medical Agents
. These agents are characterized by their ability to operate over multimodal data, maintain an internal state, and plan sequences of actions within clinical information systems under strict governance constraints
.
Here is a detailed summary of the paper's core components:

#### 1. Definition and Developmental Roadmap
The authors define Medical Agents through a three-level evolutionary roadmap to help stakeholders categorize emerging technologies
:
* Level 1: Knowledge-Centric Assistance: Reactive agents that act as interactive medical encyclopedias, using techniques like Retrieval-Augmented Generation (RAG) to synthesize information from medical literature
.
* Level 2: Workflow-Integrated Decision Support: Proactive "co-pilots" that are deeply embedded in the Electronic Health Record (EHR) and reason over live patient data to provide real-time recommendations.

* Level 3: Semi-Autonomous Workflow Execution: Transformative systems that can independently plan and execute complex administrative and clinical tasks, such as end-to-end prior authorizations or care pathway orchestration.

#### 2. Core Agentic Capabilities
The paper identifies six primary capabilities that distinguish agents from traditional models:

* Planning: Moving from fixed pipelines (static workflows) to dynamic task graphs where agents decompose complex medical goals into executable sub-tasks.

* Tool Use: Agents treat external resources—such as clinical calculators, imaging backends, and EHR APIs—as "first-class actions" they can call as needed.

* Memory: Systems maintain episodic memory of specific encounters and longitudinal memory of patient histories, allowing for continuity of care across visits.

* Self-Improvement: Agents utilize reflection, multi-agent peer review, and reinforcement learning in simulated environments to update their policies over time.

* Reasoning: Structured reasoning modes are used to suppress hallucinations and manage uncertainty during complex clinical judgment.

* Perception: Transitioning from static image analysis to "active perception," where agents can selectively view, zoom, or query specific modalities to support their reasoning.

#### 3. Multi-Agent Systems (MAS)
A major focus of the paper is Collective Intelligence, where specialized agents work together to solve complex problems.

* Architectures: The paper analyzes Static Topologies (fixed connectivity like hierarchical or centralized structures) and Dynamic Topologies (which adjust inter-agent connections in real-time).

* Collaboration Paradigms: MAS can be Consensus-oriented (simulating Multidisciplinary Teams or MDTs), Collaborative Learning (mutual enrichment of internal models), or Task-oriented (focused on workflow automation).

#### 4. Applications Across the Care Pathway
Medical agents are mapped to the entire patient journey and specific hospital departments:

* Front-line Consultation: Optimizing diagnostic questioning and outpatient reception workflows.

* Clinical Core: Virtual MDT-style teams for complex diagnosis and "radiologist-like" multimodal reasoning.

* Procedures: Surgical robots and planners that use imaging to guide interventions.

* Back-office Operations: Automating documentation, ICD coding, medical research, and regulatory compliance.

#### 5. Safety, Governance, and Evaluation
* The authors argue that the value of Medical Agents is measured by their reliable restructuring of workflows rather than just benchmark accuracy.

* Safety Challenges: The paper addresses critical risks, including medical hallucinations, privacy leakage of sensitive patient data, bias in decision-making, and vulnerability to adversarial attacks.

* Evaluation Framework: They propose moving beyond static medical tasks to Sequential Clinical Simulations (e.g., AgentClinic) and system-level benchmarks that measure clinical impact, workload reduction, and equity.

#### 6. Future Directions
The paper concludes by identifying several open challenges, such as the need for operational realism in simulators, the development of cross-departmental architectures, and the creation of multidisciplinary governance structures that include clinicians, informaticians, and patients.