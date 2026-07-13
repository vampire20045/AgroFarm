# AgroConnect

> AI-Powered Digital Contract Farming & Agricultural Leasing Platform

AgroConnect (within the AgroFarm repository) is a target architecture for a secure, transparent, and AI-assisted platform that connects **farmers**, **contractors** (MNCs/food processing companies), and **government authorities**.

This project is designed to modernize contract farming through digital workflows, document verification, multilingual AI assistance, and event-driven system design.

---

## Table of Contents

- [Overview](#overview)
- [System Architecture](#system-architecture)
- [Key Personas](#key-personas)
- [Core Capabilities](#core-capabilities)
- [AI Capabilities](#ai-capabilities)
- [Target Architecture](#target-architecture)
- [Tech Stack](#tech-stack)
- [Security](#security)
- [Deployment](#deployment)
- [Documentation](#documentation)
- [Roadmap](#roadmap)
- [Resume-Friendly Summary](#resume-friendly-summary)

---

## Overview

AgroConnect enables end-to-end digital contract farming:

- Farmers register and onboard farms with documentation.
- Contractors discover, evaluate, and lease farms.
- Government officials verify records and approve contracts.
- AI services provide multilingual communication, recommendations, and risk insights.

> **Note:** This repository documentation reflects a **production target architecture** and implementation direction. Some features may be planned/in-progress.

---

## System Architecture

![AgroConnect Platform Architecture](docs/argoconnect.png)

---

## Key Personas

### 1) Farmer

- Aadhaar-based registration and verification
- Farmer profile and farm registration
- Upload ownership documents, soil reports, and farm images
- Provide details: area, crop history, lease expectation, irrigation, water source, soil type
- Accept/reject contractor proposals
- Track contract lifecycle
- Chat and receive AI recommendations in regional languages

### 2) Contractor (MNC / Food Processing Company)

Examples: ITC, PepsiCo, Nestlé, Britannia, local food industries

- Company verification and onboarding
- Search farms with filters (location, area, soil type, crop, water availability, lease cost)
- Review farm history and farmer ratings
- Send proposals and upload contract PDFs
- Track approval pipeline
- AI-assisted risk analysis and contract insights

### 3) Government Employee

- Verify Aadhaar and land ownership documents
- Approve/reject farmer registrations and contracts
- Flag disputes or fraudulent submissions
- Manage complaints and pending approvals
- Access reports, dashboards, and audit logs

---

## Core Capabilities

- **Authentication & Access Control**: OTP, JWT, RBAC
- **Farm Lifecycle Management**: farm onboarding, document workflows
- **Proposal & Contract Management**: proposal issuance, acceptance, approvals
- **Government Approval Workflows**: verification and compliance checks
- **Notification System**: email/SMS/push events
- **Analytics Dashboards**: operational and decision dashboards

---

## AI Capabilities

### AI Assistant (Gemini API)

Multilingual support (target):

- English
- Hindi
- Kannada
- Tamil
- Telugu
- Marathi
- Bengali

### Recommendations & Insights

- Crop and fertilizer suggestions
- Water usage guidance
- Profit estimation and best-offer matching
- Government scheme suggestions
- Productivity and soil quality scoring
- Weather risk and yield projections
- Fraud/anomaly detection for suspicious activity

---

## Target Architecture

High-level flow:

- **Frontend**: React + TypeScript
- **API Gateway**: Node.js
- **Core services**: Authentication, Farm Service, Contract Service
- **Data layer**: Prisma ORM + PostgreSQL + MongoDB
- **Performance**: Redis caching/session support
- **Event-driven**: Kafka + background workers
- **Storage**: Amazon S3 for images and documents

See: [docs/architecture.md](docs/architecture.md)

---

## Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React, TypeScript |
| Backend/API | Node.js, API Gateway pattern |
| ORM | Prisma |
| Relational DB | PostgreSQL |
| Document/Log DB | MongoDB (Atlas) |
| Cache | Redis |
| Event Streaming | Kafka |
| File Storage | AWS S3 |
| Containerization | Docker |
| Orchestration | Kubernetes |
| Deployment | Vercel (frontend), Render (backend) |

See: [docs/tech-stack.md](docs/tech-stack.md)

---

## Security

- Aadhaar verification workflows
- JWT authentication + Role-Based Access Control (RBAC)
- Password hashing with bcrypt
- HTTPS and secure transport
- Input validation and request sanitization
- SQL injection mitigation through Prisma patterns
- Rate limiting on sensitive endpoints
- Signed S3 URLs for controlled document access
- Encryption for sensitive documents
- Immutable audit trails for approvals and actions

---

## Deployment

- **Frontend**: Vercel
- **Backend Services**: Render
- **Databases**: PostgreSQL + MongoDB Atlas
- **Storage**: AWS S3
- **Infra**: Docker containers orchestrated via Kubernetes

---

## Documentation

- [Architecture](docs/architecture.md)
- [Tech Stack](docs/tech-stack.md)
- [Roadmap](docs/roadmap.md)

---

## Roadmap

A phased delivery plan is available in [docs/roadmap.md](docs/roadmap.md), covering:

1. Foundation & Platform Setup
2. Core Contract Farming Workflows
3. AI Assistant & Insights
4. Scale, Reliability & Observability
5. Compliance & Enterprise Readiness

---

## Resume-Friendly Summary

**AgroConnect – AI-Powered Contract Farming Platform**

- Designed a scalable platform connecting farmers, contractors, and government authorities for secure digital contract farming.
- Planned/implemented a React + TypeScript frontend and Node.js service architecture with Prisma, PostgreSQL, MongoDB, Redis, Kafka, Docker, and Kubernetes.
- Integrated multilingual AI assistance and recommendation workflows powered by Gemini API.
- Built secure document flows using Amazon S3, signed URLs, and auditable approval workflows.
