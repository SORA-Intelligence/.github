<p align="center">
  <img src="./assets/SL1.png" alt="SORA-Intelligence Banner" width="100%" />
</p>

```mermaid
graph TD
    Kenzo["**Kenzo Shenel N. Vidal**<br/>Project Manager<br/>DevOps Lead • Solutions Architect"]
    Andrea["**Andrea R. Andres**<br/>QA Specialist<br/>Research Lead • Documentations Lead"]
    
    Sandra["**Sandra C. Agustin**<br/>UI/UX Designer<br/>Technical Illustrator"]
    Jhonwell["**Jhonwell A. Española**<br/>Software Engineer<br/>Backend Lead"]
    Timothy["**Timothy James A. Herrera**<br/>Software Engineer<br/>Frontend Lead"]
    John["**John Michael S. Tuba**<br/>IoT Engineer<br/>Firmware Lead • ML Lead"]
    Ferkeem["**Ferkeem F. Mamayson**<br/>IoT Engineer<br/>Systems & Integration Lead"]
    Antonio["**Antonio O. Tenegra Jr.**<br/>IoT Engineer<br/>Product Design Lead"]

    Kenzo --> Andrea
    Andrea --> Sandra
    Andrea --> Jhonwell
    Andrea --> John
    Andrea --> Ferkeem
    Jhonwell --> Timothy
    Ferkeem --> Antonio
```


# **SORA**

This document serves as the operational guide and engineering pipeline specification for the SORA-Intelligence team. It outlines the repository architecture, project board governance, and development workflows for the ALAMOK ecosystem.

**ALAMOK** (Autonomous Larvicidal AI-Driven Mosquito Ovitrap and Killer) is an off-grid, solar-powered IoT mosquito control system. It integrates edge-AI computer vision (Raspberry Pi co-processor) for automated larvae detection, low-power microcontrollers (ESP32) for fluid management and power orchestration, point-to-point LoRa/BLE telemetry, and dedicated desktop/mobile client applications to monitor and automate larvicide dispatch.

---

## Repository Architecture

The system employs a Domain-Driven Isolation strategy across five dedicated repositories to maintain clear boundaries between hardware, AI, software, documentation, and system deployment components:

| Repository | Focus Area | Primary Technology Stack |
| :--- | :--- | :--- |
| **`ALAMOK-Hardware`** | Field hardware, sensors, actuators, power management | ESP32, SX1278 LoRa, C++, PlatformIO |
| **`ALAMOK-Software`** | Ingestion server, REST/WebSocket API, dashboard, mobile app | FastAPI, NestJS, React, Electron, Expo |
| **`ALAMOK-ML`** | Computer vision pipeline & edge inference models | TensorFlow Lite, YOLO, Python |
| **`ALAMOK-Documentation`** | Thesis manuscript, BOM, UAT protocols, field logs | System Architecture Diagrams, Markdown |
| **`ALAMOK-System-Release`** | System orchestration, submodule sync, release manifests | Git Submodules, SemVer, GitHub Actions |

---

## Project Management & Governance

To maintain operational clarity and prevent status clutter, software engineering tasks are separated from academic writing processes using two dedicated project boards.

```text
SORA-Intelligence Organization
 ├── ALAMOK Engineering Board  (ALAMOK-Hardware, Software, ML, System-Release)
 └── ALAMOK Thesis Track Board (ALAMOK-Documentation)
```

### 1. ALAMOK Engineering Board
Tracks all technical execution across hardware, edge AI, software, and system releases. 

*Note: Task statuses are fully automated via GitHub Workflows to minimize manual toggling.*

**Automated Lifecycle Stages:**
`To Do` → `In Review` *(PR Opened)* → `Staging` *(PR Merged)* → `Production` *(Merged to Main)*

### 2. ALAMOK Thesis Track Board
Tracks academic compliance, chapter revisions, field testing data, and adviser feedback.

**Lifecycle Stages:**
`To Do` → `In Progress` → `Done`


---

## Team Roles & Maintainers

| Name | Role | GitHub Account |
| :--- | :--- | :--- |
| **Vidal, Kenzo Shenel N.** | Project Manager / Lead DevOps & Systems Architect | [@kzc0des](https://github.com/kzc0des) |
| **Española, Jhonwell A.** | Backend & Core Systems Engineer | [@ryu-zaki](https://github.com/ryu-zaki) |
| **Herrera, Timothy James** | Frontend Engineer | [@JujuDecoder](https://github.com/JujuDecoder) |
| **Agustin, Sandra C.** | UI/UX Designer & Technical Illustrator | [@sandytrtl](https://github.com/sandytrtl) |
| **Andres, Andrea C.** | Research & Documentation Lead / Quality Assurance (QA) | [@wippiiee](https://github.com/wippiiee) |
| **Mamayson, Ferkeem F.** | IoT Systems & Electronics Engineer | [@Ysokii](https://github.com/Ysokii) |
| **Tenegra, Antonio** | Hardware Product Designer | [@Ji-stacks](https://github.com/Ji-stacks) |
| **Tuba, Michael John S.** | Firmware Engineer | [@jeyem07](https://github.com/jeyem07) |