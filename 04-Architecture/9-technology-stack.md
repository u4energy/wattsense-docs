# Technology Stack

## Overview

Dokumen ini menerangkan technology stack rasmi yang digunakan oleh platform Wattsense.

Technology stack dipilih berdasarkan keperluan scalability, maintainability dan pembangunan produk jangka panjang.

---

## Frontend

### Framework

Next.js (React + TypeScript)

Digunakan untuk:

* Web Dashboard
* Admin Portal
* Future Partner Portal

### Language

TypeScript

### State Management

Zustand atau Context API

Digunakan untuk:

* Authentication State
* User Preferences
* Global UI State
* Device Selection State

### Server State Management

TanStack Query

Digunakan untuk:

* API Data Fetching
* Caching
* Background Refetching
* Optimistic Updates

### UI Framework

shadcn/ui

Digunakan untuk:

* Reusable UI Components
* Form Components
* Dialogs
* Tables
* Dashboard Widgets

### Styling

Tailwind CSS

Digunakan untuk:

* Responsive Layout
* Design System
* Utility-First Styling

### Form Management

React Hook Form

Digunakan untuk:

* Device Configuration Forms
* User Management Forms
* Settings Forms

### Validation

Zod

Digunakan untuk:

* Form Validation
* API Schema Validation
* Runtime Type Validation

### Data Visualization

Recharts

Digunakan untuk:

* Energy Consumption Charts
* Cost Analysis Charts
* Dashboard Analytics

### Future Enhancement

Apache ECharts

Digunakan apabila analytics menjadi lebih kompleks seperti:

* Multi-Series Charts
* Heatmaps
* Advanced Energy Analytics
* Industrial Monitoring Dashboards

---

## Backend

### Framework

Java Spring Boot

### Security

Spring Security

### Authentication

JWT

### ORM

Spring Data JPA

### API Style

REST API

### Future Enhancement

GraphQL

Boleh dipertimbangkan untuk dashboard yang memerlukan flexible data querying dan complex reporting.

---

## Database

### Primary Database

PostgreSQL

Digunakan untuk:

* Users
* Devices
* Billing
* Configuration
* Business Data

### Future Enhancement

TimescaleDB

Digunakan untuk:

* Energy Consumption Data
* Time-Series Analytics
* High-Volume Meter Readings

---

## Caching

### Redis

Digunakan untuk:

* Session Management
* Device State Cache
* Frequently Accessed Data
* Rate Limiting
* API Response Cache

---

## Messaging

### Initial Phase

Spring Events

Digunakan untuk komunikasi dalaman antara module dalam Modular Monolith.

### Future Phase

Apache Kafka

Digunakan apabila jumlah peranti dan data meningkat secara signifikan.

Contoh penggunaan:

* Device Events
* Billing Events
* Notification Events
* Analytics Processing

---

## IoT Integration

### Current Provider

Tuya IoT Cloud

### Communication Method

REST API

Digunakan untuk:

* Device Discovery
* Device Control
* Energy Data Retrieval

### Future Direction

Platform perlu menyokong pelbagai penyedia peranti dan tidak bergantung kepada satu vendor sahaja.

Contoh:

* OEM Smart Devices
* Industrial Energy Meters
* Modbus Gateways
* Custom IoT Devices

---

## Infrastructure

### Container Platform

Docker

### Cloud Platform

AWS atau GCP

### Services

* Compute Services
* Managed PostgreSQL
* Redis Services
* Object Storage
* Monitoring Services
* Container Registry

### Future Enhancement

Kubernetes

Digunakan apabila platform memerlukan:

* High Availability
* Auto Scaling
* Multi-Service Deployment
* Multi-Region Infrastructure

---

## Monitoring & Observability

### Application Monitoring

Spring Boot Actuator

### Metrics Collection

Prometheus

### Dashboard & Monitoring

Grafana

### Logging

ELK Stack atau OpenSearch

Digunakan untuk:

* Centralized Logging
* Error Analysis
* System Monitoring

---

## Mobile Application

### Future Options

Flutter

Digunakan untuk:

* iOS Application
* Android Application

Flutter dipilih kerana satu codebase boleh digunakan untuk kedua-dua platform dan sesuai untuk dashboard serta device management application.

---

## Architecture Principle

Technology stack dipilih berdasarkan:

* Long-Term Scalability
* Maintainability
* Developer Productivity
* System Reliability
* Future Extensibility
* Product Growth Requirements

dan bukannya semata-mata kelajuan pembangunan MVP.
