#                                      aria-native-learning-benchmark
An AI research experiment exploring native decision-making, consequence-based feedback, and persistent goal adaptation within ARIA's cognitive framework


##                                            Project Overview


This experiment is exploring how ARIA can make decisions on it's own, learn from failure, and it's behavioral adaptation through experience. The project
tests ARIA's native decision-making framework, focusing on how it's actions and their outcomes change future priorities without relying on a LLM to
do so.

The initial controlled tests demonstrate persistent, feedback driven goal adaptation. Ongoing tests aim to determine if these mechanisms produce measurable
improvements in autonomy, learning, & generalization.

**To put it simply, the goal is to measure genuine adaptive intelligence through evidence, not a simulation of intelligence through conversation.**


##                                              Architecture

W006 (current stage) demonstrates a controlled feedback pathway connecting native goal selection, action execution, verified synthetic consequences, and 
continuous priority adaptation.

```mermaid
[
flowchart TD
    A["Competing Goals<br/>Persistent Goal State"]
    B["Native Decision System<br/>Goal Selection"]
    C["Runtime Dispatch"]
    D["Plan Runner<br/>Action Execution"]
    E["Controlled Environment<br/>Synthetic Action Outcome"]
    F["Independent Feedback Verification"]
    G["Appraisal & Goal Priority Revision"]
    H[("SQLite<br/>Persistent Goal State")]
    I["Future Native Goal Selection"]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H
    H --> I

    I -. "Updated priorities inform<br/>later arbitration" .-> B

    classDef storage fill:#20334a,stroke:#7aa7d8,color:#ffffff
    classDef decision fill:#21473e,stroke:#67c5ab,color:#ffffff
    classDef action fill:#303a58,stroke:#9bade8,color:#ffffff
    classDef feedback fill:#51402a,stroke:#d7a85c,color:#ffffff

    class A,H storage
    class B,I decision
    class C,D action
    class E,F,G feedback
]
