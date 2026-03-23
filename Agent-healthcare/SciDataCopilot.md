#### SciDataCopilot: An Agentic Data Preparation Framework for AGI-driven Scientific Discovery

#### note
#### 1. The "Scientific AI-Ready" Paradigm

The paper says that normal “AI-ready” data (data cleaned for AI use) isn’t enough for scientific work. Usually, this kind of data is just formatted nicely so AI can read it, but it doesn’t fully match what scientists actually need.

* Data is organized based on the specific scientific task
* It follows rules from that scientific field
* It keeps track of how the data was created in experiments

In simple terms, the data isn’t just clean — it’s prepared in a way that AI can directly use it for real scientific analysis.

#### 2. The SciDataCopilot Framework

SciDataCopilot is a system made of multiple AI “agents” (like specialized helpers) that automatically prepare scientific data.

It uses three main storage areas:

* Data Lake (D): where raw data is stored
* Tool Lake (T): where tools and functions are stored
* Case Lake (C): where past solutions and workflows are saved

There are four main agents:

* Data Access Agent

Finds and reads different types of files
Organizes messy data and metadata
Breaks data into small, usable pieces

* Intent Parsing Agent

Understands what the scientist is asking in plain language
Turns it into a structured task
Looks at past similar problems to help plan a solution

* Data Processing Agent

Turns the plan into step-by-step code
Runs the code automatically
Fixes errors by itself if something goes wrong

* Data Integration Agent

Combines all processed data
Makes sure everything fits together correctly
Builds a final dataset that works across different data types
#### 3. Key Findings and Case Studies

The system was tested in different scientific fields and showed big improvements:

* Life Sciences (Enzyme Catalysis)

Built a dataset with 214,000 reactions in about 5 hours
About 20× larger than previous manual datasets

* Neuroscience (EEG/MEG Analysis)

Performed as well as human experts
Was 3–5× faster from start to finish

* Earth Sciences (Meteorology)

Combined large and complex datasets efficiently
Was over 30× faster than manual spreadsheet methods