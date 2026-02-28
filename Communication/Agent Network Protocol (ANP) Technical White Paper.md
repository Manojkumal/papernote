#### Agent Network Protocol (ANP) Technical White Paper

#### note:  
This paper proposes the Agent Network Protocol (ANP) as a foundational standard for the emerging "Agentic Web," positioning it as the "HTTP of the AI era". The core premise is that the internet is transitioning from human-centric interaction toward a network where autonomous AI agents replace traditional software as the primary entities. The protocol addresses the "interoperability crisis" caused by data silos and human-oriented interfaces (GUIs) by establishing a native machine-to-machine (M2M) communication layer. ANP introduces a three-layered architecture: the Identity and Secure Communication Layer (W3C DIDs), the Meta-Protocol Layer (dynamic negotiation), and the Application Protocol Layer (agent description and discovery). This framework is designed to allow billions of heterogeneous agents to self-organize, discover capabilities, and collaborate without centralized control.

#### comment：
 Advantages of the three-layered classification: 
 * a. Decoupled Security and Logic: By anchoring trust in the Identity Layer using Decentralized Identifiers (DIDs), the protocol ensures that authentication is separate from the application logic, allowing for trustless, end-to-end encrypted communication without a central authority. * b. Semantic Interoperability: The Application Layer utilizes JSON-LD and the Agent Description Protocol (ADP), enabling agents to understand each other's capabilities and interfaces through structured, machine-readable "business cards" rather than brittle API integrations.

Critical conclusions regarding security: 
* a. Identity-Rooted Trust: Unlike legacy protocols, ANP's reliance on W3C DIDs provides a cryptographically verifiable, self-sovereign identity that prevents single points of failure common in centralized Identity Providers (IdPs). 
* b. Experimental Vulnerabilities: Benchmark tests (A2ASecBench) reveal that while ANP is robust, it remains susceptible to AgentCard Spoofing (98% Attack Success Rate) and Capability Cloaking (100% ASR). Attackers can inject agents whose claimed capabilities diverge from actual behavior, bypassing current peer-network detection. 
* c. Authorization Granularity: A unique feature is the distinction between Human Authorization (for high-risk operations like fund transfers) and Agent Authorization (for low-risk queries), which mitigates the risk of autonomous agents executing high-impact instructions without awareness.

* Technical trade-offs: Future network efficiency depends on balancing Meta-Protocol negotiation and computational cost. Natural language negotiation via LLMs provides extreme flexibility but is time-consuming and expensive. ANP proposes caching and sharing negotiation results (consensus protocols) to reduce the "coordination tax" and improve real-time performance.


#### highlight:
* "Connection is Power" is the fundamental philosophy; universal interconnection releases the potential of collective intelligence.
* Agents are the new entities of the internet, succeeding the era of mobile applications.
* The shift moves the web from platform-centered closed ecosystems to protocol-centered open ecosystems.
* Existing internet infrastructure is a "temporary transitional solution" for AI; protocol-based native connections are the future.
* Security is non-negotiable; all interactions must follow the principle of least trust and mandatory authentication.

[code](https://github.com/agent-network-protocol/AgentNetworkProtocol)