# 🛰️ adminctl.co.uk

**The Unified Fleet Orchestration & Real-Time Observability Stack.**

Adminctl is a high-performance ecosystem designed to bridge the gap between distributed edge infrastructure and actionable central command. Built with the memory safety of **Rust** and the reactive power of **Angular**, we provide the tools to monitor, manage, and command thousands of nodes with sub-second latency.

---

### 🏗️ Enterprise Architecture
Our system is engineered for scale, supporting multi-node clustering and deep custom observability:

* **[client](https://github.com/getadminctl/client) (The Edge Agent):** A lightweight Rust binary. Capable of acting as a "Gateway/Proxy," sending real-time telemetry, and executing remote commands like `dnf update -y`.
* **[ingestion](https://github.com/getadminctl/ingestion) (The Backbone):** A high-speed Rust ingestion server. Designed for **High-Availability Clustering**, it can be deployed in a distributed mesh to handle massive telemetry loads.
* **[dashboard](https://github.com/getadminctl/dashboard) (The Command Center):** A TypeScript & Angular interface for visualizing fleet health and dispatching global orchestration commands.
* **[misc](https://github.com/getadminctl/misc) (Misc stuff):** Misc scripts etc

---

### ⚡ Key Capabilities

| Feature | Description |
| :--- | :--- |
| **High-Availability Clustering** | Horizontal scaling of Ingestion servers to support massive node counts without bottlenecks. |
| **Custom Metric Commands** | Define your own metrics via CLI or config; the agent executes them and pipes the output directly to the TSDB. |
| **Real-time Ingestion** | Optimized Rust pipelines handling **1400+ active packets** per second with ease. |
| **Remote Orchestration** | Dispatch commands from the UI directly to the edge. Invoke CLI updates and monitor logs live. |
| **Edge Proxying** | Use agents as secure gateways/proxies for isolated subnets and restricted environments. |
| **SSE Updates** | Real-time reactive dashboard updates (Receiver → Dash) for instant incident response. |

---

### 🛠️ Technical Stack
* **Languages:** Rust (Performance/Edge), TypeScript (Frontend/API).
* **Frameworks:** Angular (Dashboard).
* **Data:** Time-Series Database (TSDB) for historical metrics.
* **Protocols:** Server-Sent Events (SSE) for metrics, Secure RPC for Command Dispatch.

---

### 📊 System Status (Concept Preview)
Our architecture is designed to handle high-velocity traffic and elastic scaling. 
* **Current Mode:** `INGESTION` (Cluster-aware)
* **Packet Throughput:** `1459/sec`
* **Simulation Speed:** `1.5x`

> **Pro Tip:** Use the `adminctl-client --custom-metric "sh /opt/scripts/temp.sh"` command to pipe bespoke hardware data directly into your central dashboard in real-time.

---

### 🤝 Connect with us
Visit [adminctl.co.uk](https://adminctl.co.uk) for documentation and enterprise support.
