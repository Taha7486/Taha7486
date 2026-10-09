# Taha Essamit

**Final-year Computer Engineering student @ ENSA Tétouan — DevOps, DevSecOps & Platform Engineering**

I build Kubernetes platforms with GitOps delivery and security built into the pipeline: no secrets in Git, default-deny networking, and vulnerability scans that block a deploy.

🔎 Looking for a **6-month PFE internship starting January 2027** (DevOps / DevSecOps / Platform, or backend with real infra exposure).

---

## Stack

**Containers, Orchestration & IaC**

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)

**CI/CD & GitOps**

![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?style=flat-square&logo=argo&logoColor=white)

**Security**

![Vault](https://img.shields.io/badge/HashiCorp_Vault-000000?style=flat-square&logo=vault&logoColor=white)
![Trivy](https://img.shields.io/badge/Trivy-1904DA?style=flat-square)
![gitleaks](https://img.shields.io/badge/gitleaks-555555?style=flat-square)
![Calico](https://img.shields.io/badge/Calico_NetworkPolicies-FB8C00?style=flat-square)

**Observability**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)

**Languages & Frameworks**

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![C#](https://img.shields.io/badge/C%23-.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)

---

## Featured project

### [CodeReview — Kubernetes platform, GitOps and security hardening](https://github.com/Taha7486/Review_Code)

Solo project: a code review platform running as 7 services on Kubernetes (React, .NET 9 API calling a PHP 8.2 analysis service, MySQL and its exporter, Prometheus, Grafana).

- **GitOps**: GitHub Actions (tests → Trivy → build/push) → ArgoCD syncs a dedicated deploy branch. No manual `kubectl apply`.
- **Secrets**: HashiCorp Vault + Vault Secrets Operator inject secrets at runtime. No secret values in files or Git history.
- **Network isolation**: 12 Calico NetworkPolicies on a default-deny baseline, each service limited to the flows it needs.
- **Supply chain**: Trivy in CI blocks any CRITICAL CVE before images reach the cluster.
- **Clear ownership**: Terraform manages the platform and security layer (namespaces, RBAC, Vault, NetworkPolicies), ArgoCD manages the runtime, so they never fight over sync.
- **Observability**: Prometheus + Grafana, metrics instrumented in code, dashboard provisioned as a ConfigMap.
- **Resilience**: rolling updates, self-healing, and git-revert recovery verified in practice.

---

## Experience

**HB Développement — PFA internship, Full-Stack & secured CI** (June – August 2026, pair project)

Co-developed an internal HR application (10 modules, replacing Excel-based management).

- Two-repo CI: lint, tests, and a Trivy scan that blocks on CRITICAL/HIGH CVEs, then an automated GitOps handoff to the company's Kubernetes cluster. gitleaks run on the full Git history.
- Write-protected audit log: PostgreSQL rules reject direct `UPDATE`/`DELETE`, verified by an integration test that attempts the write and asserts it fails.
- Integration tests on a real PostgreSQL via Testcontainers.

---

## Other projects

- **SGITU — analytics microservice** (team of 4): co-developed with Spring Boot, Kafka and MongoDB. Resilience4j circuit breaker, dead-letter queue, GitHub Actions CI, Kubernetes deployment with Prometheus + Grafana.
- **ChriOnline — application security architecture** (team): TLS, RSA-2048 + AES-256, BCrypt, RBAC with 4 roles, layered anti-bruteforce and anti-replay in a Java client-server app.

---

## In progress

**Forge: software supply-chain trust chain** (solo, early stage). Open-source apps are rebuilt in CI, scanned, given an SBOM, signed keyless with Cosign and attested. Kyverno admission control then refuses any pod whose image was not signed by the exact build workflow. The integration risks (signature and attestation verification, admission latency and failure behaviour) were tested and measured locally on a kind cluster. AWS (EKS, ECR, Terraform) is the planned target; nothing is deployed on a cloud yet.

---

## Certifications

- IBM — Docker Essentials: A Developer Introduction
- IBM — Introduction to Containers, Kubernetes, and OpenShift
- KodeKloud — Terraform Basics Training Course

---

## Contact

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/taha-essamit-05316b349)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:tahaessamit@gmail.com)
