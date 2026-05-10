# SecurityAnalyst: AI-Driven Cloud-Native Python Security Assessment Platform

## Overview

SecurityAnalyst is a cloud-native AI-powered security analysis platform designed to perform automated vulnerability assessment, static code analysis, and intelligent security reasoning for Python codes at scale. The platform integrates modern DevSecOps principles with Large Language Models (LLMs), static analysis engines, and Google Cloud Platform (GCP) infrastructure to provide real-time security insights for software systems.

The system combines:
- Static Application Security Testing (SAST)
- AI-assisted vulnerability reasoning
- Cloud-native scalable deployment
- Automated DevSecOps workflows
- Infrastructure-as-Code (IaC) using Terraform
- Containerized microservices deployment using Cloud Run

This project demonstrates a production-grade cybersecurity and AI engineering workflow suitable for:
- AI Security Research
- DevSecOps Engineering
- Cloud Security Engineering
- Secure Software Development
- Applied AI Infrastructure

---

# Key Features

- AI-driven Python security assessment
- Static code analysis using Semgrep
- Vulnerability classification and reasoning using OpenAI LLMs
- Cloud-native deployment on Google Cloud Platform (GCP)
- Fully containerized architecture using Docker
- Infrastructure provisioning using Terraform
- Automated scalable deployment with Cloud Run
- Artifact Registry integration for container management
- REST API architecture using FastAPI
- Security-focused DevSecOps workflow
- Scalable serverless architecture

---

# System Architecture

## High-Level GCP Architecture

```text
                    ┌────────────────────┐
                    │    Client/User     │
                    └─────────┬──────────┘
                              │ HTTPS
                              ▼
                   ┌─────────────────────┐
                   │   Google Cloud Run  │
                   │  FastAPI Backend    │
                   └─────────┬───────────┘
                             │
         ┌───────────────────┼────────────────────┐
         │                   │                    │
         ▼                   ▼                    ▼
┌────────────────┐  ┌─────────────────┐  ┌─────────────────┐
│ OpenAI API     │  │ Semgrep Engine  │  │ Cloud Logging   │
│ Vulnerability  │  │ Static Analysis │  │ Monitoring      │
│ Reasoning      │  │ Security Rules  │  │ Observability   │
└────────────────┘  └─────────────────┘  └─────────────────┘
                             │
                             ▼
                 ┌─────────────────────┐
                 │ Artifact Registry   │
                 │ Docker Image Store  │
                 └─────────────────────┘
                             │
                             ▼
                 ┌─────────────────────┐
                 │ Terraform IaC       │
                 │ Infrastructure Mgmt │
                 └─────────────────────┘
```

---

# Technology Stack

## Backend
- Python 3.12
- FastAPI
- Uvicorn

## Security Analysis
- Semgrep
- Static Application Security Testing (SAST)
- AI-assisted vulnerability reasoning

## AI/LLM
- OpenAI API
- GPT-based security reasoning

## Cloud Infrastructure
- Google Cloud Platform (GCP)
- Cloud Run
- Artifact Registry
- Cloud Logging
- IAM

## DevOps / Infrastructure
- Docker
- Terraform
- GitHub
- Git

---

# Security Analysis Workflow

## Step 1 — Code Submission
Python source code is submitted through the API interface.

## Step 2 — Static Security Analysis
Semgrep scans the codebase for:
- Hardcoded credentials
- Injection vulnerabilities
- Insecure deserialization
- Weak cryptographic practices
- Misconfigured authentication flows
- Dangerous subprocess execution
- Command injection patterns

## Step 3 — AI-Based Security Reasoning
The detected findings are sent to an LLM pipeline to:
- Explain vulnerabilities
- Estimate severity
- Provide remediation guidance
- Generate contextual security insights

## Step 4 — Cloud-Native Deployment
The platform is deployed using:
- Docker containers
- Artifact Registry
- Cloud Run serverless services
- Terraform-managed infrastructure

---

# Infrastructure-as-Code (IaC)

Terraform provisions:
- Cloud Run services
- Artifact Registry repositories
- Required Google APIs
- IAM permissions
- Public service endpoints

This enables:
- Reproducible deployments
- Scalable cloud infrastructure
- Automated environment provisioning
- DevSecOps automation

---

# Deployment Pipeline

## Local Development

```bash
uvicorn server:app --host 0.0.0.0 --port 8000
```

## Docker Build

```bash
docker build -t securescope .
```

## Terraform Deployment

```bash
terraform init

terraform plan \
  -var="openai_api_key=$OPENAI_API_KEY" \
  -var="semgrep_app_token=$SEMGREP_APP_TOKEN"

terraform apply
```

---

# Example Security Findings

The platform can detect:
- Command Injection
- Arbitrary Code Execution
- Hardcoded Secrets
- SQL Injection
- Insecure File Handling
- Unsafe Deserialization
- Weak Authentication Patterns

---

# Cloud-Native Engineering Highlights

This project demonstrates:
- Serverless AI deployment
- AI-assisted cybersecurity analysis
- Cloud-native DevSecOps workflows
- Infrastructure automation
- Container orchestration concepts
- Production-ready API engineering
- Secure CI/CD principles

---

# Research and Industry Relevance

This project aligns with:
- AI Security Engineering
- Cloud Security Research
- DevSecOps
- Software Supply Chain Security
- Intelligent Vulnerability Detection
- Explainable AI for Cybersecurity
- Secure AI Infrastructure

Potential applications include:
- Enterprise DevSecOps platforms
- Secure code review systems
- AI-assisted security auditing
- Educational cybersecurity labs
- Secure software engineering pipelines

---

# Future Enhancements

- Multi-language security analysis
- Kubernetes deployment
- CI/CD pipeline integration
- Real-time GitHub scanning
- Reinforcement learning for vulnerability prioritization
- Explainable AI dashboards
- Vector database integration for secure RAG pipelines
- Security telemetry analytics

---

# Author

## Faria Jaheen

PhD in Electrical and Computer Engineering (AI)  
University of Ottawa

### Research Interests
- AI Systems Engineering
- Cloud-Native AI
- Cybersecurity AI
- Robotics and Intelligent Systems
- Explainable AI
- Machine Learning Infrastructure

### Links
- GitHub: https://github.com/FariaJaheen
- LinkedIn: https://www.linkedin.com/in/fariajaheen
- Google Scholar: https://scholar.google.ca/citations?user=w92696kAAAAJ&hl=en
