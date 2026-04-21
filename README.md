# U4 Energy - Documentation Repository

This repository contains all the notes, architecture diagrams, product information, and technical guidelines for the U4 WattSense project.

## Structure
- **architecture/** - System, frontend, backend, and API architecture.
- **backlog/** - Roadmap, feature list, and backlog items.
- **product/** - Product vision, MVP scope, pricing, and user personas.
- **diagrams/** - Diagrams: components, sequence, data flow.
- **guides/** - Guides such as kWh to RM calculation, installation, and API usage.
- **meeting-notes/** - Notes from discussions and meetings.

## Purpose
To have a centralized knowledge base for the U4 Energy project for both technical and business teams.

# ⚡ U4 Wattsense

Smart Energy Monitoring & Cost Intelligence Platform

---

## 🚀 Overview

U4 Wattsense helps users monitor electricity usage (kWh) and convert it into real cost (RM) in real-time.

---

## 🎯 Problem

Most users only see electricity usage after receiving their bill. There is no real-time visibility or control.

---

## 💡 Solution

* Real-time energy monitoring
* kWh → RM conversion (TNB-based logic)
* Smart alerts for abnormal usage
* Device-level control (on/off)

---

## 🏗️ System Architecture

See full details 👉 [Architecture](docs/architecture.md)

---

## ⚙️ Features

* Live dashboard
* Device monitoring
* Monthly bill estimation
* Alerts & automation

---

## 📦 Tech Stack

* Frontend: Angular / React
* Backend: Spring Boot
* Database: PostgreSQL
* IoT: Tuya / MQTT

---

## 🚀 Getting Started

### Backend

```bash
cd backend
./mvnw spring-boot:run
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

---

## 📊 Core Logic

See 👉 [Calculation](docs/calculation.md)

---

## 🧪 Roadmap

See 👉 [Roadmap](docs/roadmap.md)

---

## 📄 License

Private (for now)
