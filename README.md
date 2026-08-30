```mermaid
flowchart LR
  subgraph ARCH[" "]
    direction LR

    A["<b>(1) Data Acquisition</b><br/>─────────────<br/>Online Datasets & APIs<br/><br/>• Weather Data<br/>• Soil & Crop Data<br/>• Historical Yield Records<br/>• Govt./Research Datasets<br/><br/><i>Sources: Public APIs,<br/>Agricultural Repositories</i>"]

    B["<b>(2) Data Preprocessing</b><br/>─────────────<br/>Cleaning & Preparation<br/><br/>• Data Validation<br/>• Missing-Value Handling<br/>• Noise Removal<br/>• Feature Engineering<br/>• Normalization<br/><br/><i>Ensures consistent,<br/>model-ready data</i>"]

    C["<b>(3) Model Training</b><br/>─────────────<br/>AI / ML Model Development<br/><br/>• Disease Prediction<br/>• Yield Estimation<br/>• Weather Forecasting<br/>• Fertilizer Recommendation<br/>• Crop Suitability<br/>• Advisory Chatbot (NLP)<br/><br/><i>Trained, validated &<br/>evaluated models</i>"]

    D["<b>(4) Backend Layer</b><br/>─────────────<br/>Model Integration<br/><br/>• REST APIs<br/>• Authentication & Access<br/>• Request Handling<br/>• Business Logic<br/>• Model Inference Calls<br/><br/><i>Central processing<br/>core of the system</i>"]

    E["<b>(5) Database</b><br/>─────────────<br/>Persistent Storage<br/><br/>• User Records<br/>• Crop & Soil Data<br/>• Prediction History<br/>• Model Metadata<br/><br/><i>Structured storage for<br/>all system data</i>"]

    F["<b>(6) Frontend Layer</b><br/>─────────────<br/>User Interface<br/><br/>• Web Dashboard<br/>• Mobile Application<br/>• Chatbot Interface<br/>• Alerts & Reports<br/><br/><i>Presents insights to<br/>the end user</i>"]

    G["<b>(7) End Users</b><br/>─────────────<br/><br/>• Farmers<br/>• Agricultural Experts<br/>• System Administrators<br/><br/><i>Consume predictions &<br/>system recommendations</i>"]

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

**Fig. 1.** Proposed system architecture. Raw agricultural data — weather, soil, crop, and historical yield records — is acquired from public APIs and research repositories (1), then validated, cleaned, and normalized during preprocessing (2). This data trains the core AI/ML models for disease prediction, yield estimation, weather forecasting, fertilizer recommendation, crop suitability, and the NLP-based advisory chatbot (3). The backend layer (4) exposes these models through authenticated REST APIs and handles all business logic and inference requests, maintaining bidirectional communication with the database (5), which persists user, crop, and prediction records, and with the frontend layer (6), comprising the web dashboard, mobile application, and chatbot interface. The frontend serves the end users (7) — farmers, agricultural experts, and system administrators — who consume the resulting predictions and recommendations.
