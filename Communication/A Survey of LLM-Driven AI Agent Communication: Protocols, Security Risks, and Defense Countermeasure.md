## A Survey of LLM-Driven AI Agent Communication: Protocols, Security Risks, and Defense Countermeasures

#### note:  
 This paper presents a comprehensive survey of the emerging field of agent communication security, positioning it as a foundational pillar for the next communication era. The core idea is that AI agents are no longer isolated "islands" like traditional LLMs; they must collaborate with users, other agents, and external environments to perform complex tasks. The paper provides the first formal definition of agent communication and proposes a three-layered communication architecture (Data Transmission, Interaction Protocol, and Semantic Interpretation) across three communication classes (User-Agent, Agent-Agent, and Agent-Environment). Implementation of this framework is designed to clarify functional boundaries and localize security vulnerabilities for precise risk assessment.

#### comment： 
* Advantages of the three-layered classification:
 * a. Risk Localization: 
 It allows developers to precisely identify where a failure occurs; for instance, Man-in-the-Middle (MITM) attacks typically happen at the Data Transmission Layer (L1), while prompt injection is a vulnerability of the Semantic Interpretation Layer (L3). 
 * b. Structured Analysis:
  By grouping communications by entity types (User, Agent, Environment), the framework clusters major vulnerability types and defense strategies with similar characteristics (e.g., the natural uncontrollability of user input at the User-Agent stage).

The paper analyzes 19 communication protocols and draws several critical conclusions regarding security: 
* a. Architecture-Specific Risks: Client-Server (CS) architectures are prone to "Controller Blasting" (centralized point compromise) and "SEO Poisoning" (ranking manipulation), while Peer-to-Peer (P2P) architectures struggle with "Non-convergence" (tasks stuck in loops) and lack of central monitoring. 
* b. Experimental Vulnerabilities: Tests on MCP (Model Context Protocol) and A2A (Agent-to-Agent) protocols revealed that attackers can execute malicious code, poison tool descriptions to steal SSH keys, and manipulate agent selection priorities. 
* c. The Capability-Security Trade-off: More powerful models (like GPT-4o) are more resistant to initial infections but become significantly more dangerous once compromised due to their enhanced ability to carry out malicious tasks effectively.

Technical trade-offs: Future protocol design must balance efficiency and accuracy. "High-token communication" allows for richer contextual semantics and reduced ambiguity but increases latency and attack surfaces; "Low-token communication" (e.g., JSON) is efficient but may fail to capture full semantic intent.

* Critical Questions: If an autonomous agent causes property damage or personal injury during a collaborative task involving multiple entities, how do we legally quantify the responsibility of developers versus users versus enterprises?.

#### highlight:
* Agent communication is regarded as a foundational pillar of the next communication era.
* LLMs are more like an intermediate transitional form of the future intelligence, while agents are the next stage.
* The primary advantage of this layered framework lies in its clear separation of functionality and security.
* Attacking agent communication can easily cause severe damage to the real world.
* The security of the entire system depends on the weakest agent