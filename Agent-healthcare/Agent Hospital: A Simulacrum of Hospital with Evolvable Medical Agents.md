#### Agent Hospital: A Simulacrum of Hospital with Evolvable Medical Agents

#### Summary 
The goal of this paper is to replicate the entire medical treatment process: from symptom onset to diagnosis, treatment, recovery, and follow-up and to let AI doctors learn by doing inside the simulation.

#### Comments
Unlike conventional training that needs humans to label data, this approach enables doctor agents to evolve by practicing on many simulated patients without hand-annotated datasets.The system automatically simulates disease emergence and progression based on knowledge bases and LLM output.

The paper introduces MedAgent-Zero, a strategy that allows AI doctor agents to accumulate knowledge from thousands of simulated patient encounters.Learn from mistakes and successes to refine their decision-making similar to practical experience for human doctors.Use a medical record library and an experience base to improve.

Achieved state-of-the-art accuracy on medical examination and decision-making tasks.When tested on a subset of the MedQA medical benchmark (based on USMLE questions), these doctor agents scored around 93.06%, broadly outperforming existing medical agent methods.

[medical_agent](medical_agent.png)