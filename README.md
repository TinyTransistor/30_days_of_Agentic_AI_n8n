# 30 Days of Agentic AI & Workflow Automation (n8n)

Tracking my journey from absolute beginner to building autonomous AI agents using n8n orchestration and Docker.

## 🗓️ Day 1: Foundations & API Orchestration
Initialized my local developer environment and established a live data processing pipeline.

### Technical Implementation
* **Infrastructure**: Deployed a self-hosted n8n instance via **Docker Desktop** running over a WSL 2 Linux kernel architecture backend.
* **Network Protocol**: Configured an **HTTP Request** node executing a synchronous `GET` request.
* **Data Ingestion**: Parsed real-time spatial telemetry coordinates (latitude, longitude, velocity) from the International Space Station public API endpoint.
* **Data Inspection**: Evaluated raw payloads using both **JSON** code frameworks and structured **Table** data arrays.

### How to Run
Import `day1-iss-tracker.json` directly onto your n8n workspace grid and click **Execute workflow**.
## 🗓️ Day 2: JSON Parsing & Data Expression Mapping
Advanced from basic ingestion to structural data manipulation by extracting precise keys from a chaotic API payload.

### Technical Implementation
* **Data Transformation**: Integrated an **Edit Fields (Set)** node directly downstream from the HTTP layer.
* **JSON Target Mapping**: Utilized dot-notation expressions (`{{ $json.latitude }}`, `{{ $json.longitude }}`) to programmatically isolate target keys from a raw JSON nested object schema.
* **Payload Sanitation**: Formatted unstructured coordinate integer arrays into a single, human-readable data string, successfully stripping away redundant system metadata.

### How to Run
Import `day2-json-parsing.json` directly onto your n8n canvas, execute the workflow, and check the JSON/Table outputs inside the Edit Fields node.
