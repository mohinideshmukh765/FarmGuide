```mermaid
flowchart LR
  subgraph ARCH[" "]
    direction LR

    A["(1) Data Acquisition<br/>Online Datasets & APIs<br/><i>Weather · Soil · Crop ·<br/>Historical Yield Records</i>"]
    B["(2) Data Preprocessing<br/>Cleaning & Preparation<br/><i>Validation · Missing-Value<br/>Handling · Normalization</i>"]
    C["(3) Model Training<br/>AI / ML Models<br/><i>Disease · Yield · Weather ·<br/>Fertilizer · Crop · Chatbot</i>"]
    D["(4) Backend Layer<br/>Model Integration<br/><i>APIs · Authentication ·<br/>Request Handling</i>"]
    E["(5) Database<br/>Persistent Storage<br/><i>User, Crop & Prediction<br/>Records</i>"]
    F["(6) Frontend Layer<br/>User Interface<br/><i>Web Dashboard ·<br/>Mobile App</i>"]
    G["(7) End Users<br/><i>Farmers · Agricultural<br/>Experts · Administrators</i>"]

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

**Fig. 1.** Proposed system architecture. Raw agricultural data — weather, soil, crop, and historical yield records — is acquired from online datasets and APIs (1), then cleaned, validated, and normalized during preprocessing (2). This data trains the core AI/ML models for disease detection, yield estimation, weather forecasting, fertilizer recommendation, crop suitability, and the advisory chatbot (3). The backend layer (4) exposes these models through authenticated APIs, maintaining bidirectional communication with the database (5), which persists user, crop, and prediction records, and with the frontend layer (6), comprising the web dashboard and mobile application. The frontend serves the end users (7) — farmers, agricultural experts, and administrators.
