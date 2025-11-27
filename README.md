
<h1 align="center">
  👋 Hey There, I'm <strong>Maniram</strong> <img src="https://media.giphy.com/media/12oufCB0MyZ1Go/giphy.gif" width="35">
</h1>


<div align="center">
  <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/colored.png" width="500">
</div>

<p align="center">
  <img 
    src="https://readme-typing-svg.herokuapp.com?font=Merriweather&size=15&duration=3000&pause=1000&color=000000&center=true&vCenter=true&width=500&lines=DevOps+Engineer+•+Cloud+•+Kubernetes+•+Observability+•+CI/CD" 
  />
</p>


<img align="right" src="https://gifdb.com/images/high/animated-man-computer-coding-nae6mec378lsg1i3.gif" width="230">

## 🧑‍💻 Professional Summary  
DevOps & SRE Engineer with 3+ years of experience in designing, automating, and optimizing large-scale cloud-native infrastructure. Skilled in Kubernetes, AWS, Terraform, Jenkins, observability platforms, and distributed systems. Passionate about reliability, scalability, and building well-architected cloud platforms.


## 🔧 Key Tools & Technologies
<p align="center">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" />
  <img src="https://img.shields.io/badge/GCP-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white" />
  <img src="https://img.shields.io/badge/Terraform-623CE4?style=for-the-badge&logo=terraform&logoColor=white" />
  <img src="https://img.shields.io/badge/Jenkins-D33833?style=for-the-badge&logo=jenkins&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" />
  <img src="https://img.shields.io/badge/Elasticsearch-005571?style=for-the-badge&logo=elasticsearch&logoColor=white" />
</p>

- **Cloud Platforms:** AWS, GCP, Linux  
- **Containers & Orchestration:** Docker, Kubernetes, Helm, Rancher  
- **Infrastructure as Code:** Terraform, Ansible  
- **CI/CD & Automation:** Jenkins, GitLab CI/CD, GitHub Actions, Shell Scripting  
- **Observability & Monitoring:** Prometheus, Grafana, OpenTelemetry, Elasticsearch, OpenSearch, EFK Stack, Fluentd, Datadog  
- **Platforms & Reverse Proxy:** NGINX, HAProxy  
- **Databases & Streaming:** PostgreSQL, Redis, Kafka, Flink, Trino, Superset  
- **Programming & Scripting:** Python, Bash  
- **Version Control & Tools:** Git, Nexus, SonarQube  

## 📂 Key Projects  

### 🔹 Enterprise Observability Platform  

- Full-stack telemetry: metrics, logs, tracing  
- Victoria Metrics + Grafana dashboards, alerts, SLO monitoring  
- Distributed tracing using OTEL Collector  

<pre>
    Applications / Microservices
              │
              ▼
        OTEL SDK → OTEL Collector
              │
   ┌──────────┼────────────┐
   ▼          ▼             ▼
Victoria     Fluentd      Tracing Backend
(Metrics)    (Logs)     (Tempo / Jaeger)
   │          │              │
   ▼          ▼              ▼
Grafana   Elasticsearch   Grafana (Traces)
(Dashboards) / OpenSearch  + Alerting
</pre>
 
 
### 🔹 CI/CD Automation Framework

- Multi-service deployment pipelines  
- Blue/Green, Canary rollout strategies  
- Infrastructure-as-code driven release orchestration  

<pre>
          Git (Source)
                │
                ▼
     CI Pipeline (Jenkins/GitLab)
                │
                ▼
          Docker Build
                │
                ▼
         Nexus / Registry
                │
                ▼
       CD Pipeline (Helm / Argo)
                │
                ▼
      Kubernetes Cluster (Deployments)
                │
                ▼
   Observability Stack (Prometheus/Grafana)
</pre>


### 🔹 Streaming Analytics

- Kafka → Flink → Trino → Superset  
- Real-time insights for analytics workloads  

<pre>
  Producers / Applications
              │
              ▼
            Kafka
           (Topics)
              │
              ▼
      Flink Stream Jobs
              │
              ▼
     Data Lake / Warehouse
              │
              ▼
           Trino Engine
              │
              ▼
       Superset Dashboards
</pre>
### 🔹 Automated Disaster Recovery (DR) Orchestration System  
Built an end-to-end DR automation workflow using **Jenkins, Terraform, Ansible, and DNS automation** to enable seamless failover between primary and secondary sites.

#### 🔧 Key Highlights  
- Automated failover for multiple microservices running across distributed servers  
- Intelligent traffic draining mechanism to safely disconnect client DB connections  
- Automated service bring-up sequence in DR site  
- Database role-switching with safe promotion of DR write node  
- Automated public DNS cutover to reroute production traffic  
- End-to-end validation, health checks, and service readiness gates  
- Reduced DR execution time to **under 10 minutes**

flowchart LR

    A[Jenkins Orchestrator] --> B[Traffic Drain<br>Per Microservice]
    B --> C[Primary Site<br>Service Shutdown]
    C --> D[Freeze DB Writes]

    D --> E[Start Services<br>in DR Site]
    E --> F[Promote DR DB<br>as Primary]

    F --> G[DNS / Public IP Switch]
    G --> H[Client Traffic Moves<br>to DR Site]

    H --> I[Post-Failover<br>Health Checks]



## 📊 GitHub Stats

![Maniram's GitHub Stats](https://github-readme-stats.vercel.app/api?username=ManiramGudla&show_icons=true&theme=dracula)
---

## 📫 Contact  
📧 Email: **maniramofficial@gmail.com**  
🔗 LinkedIn: **https://linkedin.com/in/maniramgudla**  
🐙 GitHub: **github.com/ManiramGudla**

---

<p align="center">
  <sub>“Infrastructure is code. Delivery is automation. Observability is clarity.”</sub>
</p>




