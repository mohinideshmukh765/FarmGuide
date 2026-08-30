```mermaid
flowchart LR
  subgraph ARCH[" "]
    direction LR

    A["(1) Data Acquisition<br/>Online Datasets & APIs"]
    B["(2) Data Preprocessing<br/>Cleaning & Preparation"]
    C["(3) Model Training<br/>AI / ML Models"]
    D["(4) Backend Layer<br/>Model Integration"]
    E["(5) Database<br/>Persistent Storage"]
    F["(6) Frontend Layer<br/>User Interface"]
    G["(7) End Users<br/>Farmers · Experts · Admin"]

    A --> B --> C --> D
    D <--> E
    D <--> F
    F --> G
  end

  classDef stage fill:#EAF1F5,color:#111827,stroke:#37474F,stroke-width:1px,rx:2,ry:2;
  classDef core fill:#DCE7DC,color:#111827,stroke:#37474F,stroke-width:1px,rx:2,ry:2;
  classDef user fill:#E5E7EB,color:#111827,stroke:#37474F,stroke-width:1px,rx:2,ry:2;

  class A,B,C stage;
  class D,E core;
  class F,G user;
```

**Fig. 1.** Proposed system architecture. Raw agricultural data is acquired from online datasets and APIs (1), preprocessed (2), and used to train the AI/ML models (3). The backend layer (4) integrates the trained models and maintains bidirectional communication with the database (5) for persistent storage and the frontend layer (6), which serves the end users (7).
