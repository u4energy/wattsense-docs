# Backend Architecture

## Overview

Wattsense menggunakan Java Spring Boot sebagai backend framework utama untuk mengendalikan pengurusan pengguna, pengurusan peranti, pemprosesan data tenaga, analytics dan pengiraan kos elektrik.

Backend direka untuk menyokong pertumbuhan produk daripada platform Smart Energy Monitoring kepada platform Energy Intelligence dan SME Energy Management pada masa hadapan.

---

## Architecture Decision

### Decision

Java Spring Boot dipilih sebagai teknologi backend utama.

Node.js atau NestJS tidak digunakan sebagai backend utama bagi memastikan platform mempunyai asas yang lebih kukuh untuk pertumbuhan jangka panjang dan business logic yang semakin kompleks.

---

## Rationale

### Long-Term Product Vision

Wattsense dibangunkan sebagai produk jangka panjang dan bukan sekadar MVP.

Platform dijangka berkembang kepada:

* Energy Monitoring Platform
* Energy Intelligence Platform
* SME Energy Management Platform
* ESG Reporting Platform
* Carbon Monitoring Platform

---

### Complex Business Logic

Backend perlu menyokong pelbagai business logic yang semakin kompleks seperti:

* Billing Engine
* Cost Calculation
* Energy Analytics
* Automation Rules
* Notification Processing
* Multi-Tenant Management
* Future AI Services

Java Spring Boot memberikan struktur yang lebih sesuai untuk mengendalikan keperluan ini secara maintainable dan scalable.

---

### Scalability

Spring Boot menyediakan laluan yang jelas untuk pertumbuhan architecture tanpa perlu melakukan perubahan besar pada sistem.

Architecture boleh berkembang daripada:

* Modular Monolith

kepada:

* Event-Driven Architecture
* Microservices Architecture
* Enterprise Integration Architecture

mengikut keperluan perniagaan pada masa hadapan.

---

### Technical Growth

Pemilihan Spring Boot juga membantu membangunkan kepakaran pasukan dalam membina sistem enterprise yang lebih matang, stabil dan mudah diselenggara.

---

## Technology Stack

### Core Technologies

* Java 17
* Spring Boot
* PostgreSQL
* Docker

### Optional Components

* Redis (Caching)
* MQTT Broker (IoT Communication)

---

## Initial Architecture

Pada fasa awal pembangunan, backend akan menggunakan pendekatan Modular Monolith.

### Proposed Module Structure

```text
auth
user
device
energy
billing
notification
common
```

### Module Responsibilities

#### auth

Mengurus:

* Authentication
* Authorization
* JWT Management
* Security Configuration

#### user

Mengurus:

* User Profile
* Account Settings
* User Preferences

#### device

Mengurus:

* Device Registration
* Device Management
* Device Status Monitoring
* Device Integration

#### energy

Mengurus:

* Energy Data Collection
* Data Processing
* Consumption Calculation
* Historical Data

#### billing

Mengurus:

* Tariff Configuration
* Cost Calculation
* Billing Records
* Usage Summary

#### notification

Mengurus:

* Alerts
* Notifications
* Automation Events

#### common

Mengandungi:

* Shared Utilities
* Common DTOs
* Shared Configurations
* Helper Components

---

## Core Backend Modules

Backend Wattsense terdiri daripada beberapa domain utama:

### Device Management

Bertanggungjawab mengurus semua operasi berkaitan peranti termasuk pendaftaran, konfigurasi dan pemantauan status.

### Energy Data Ingestion

Mengumpulkan data tenaga daripada pelbagai sumber seperti Tuya IoT Cloud dan future device integrations.

### Billing & Pricing

Mengira kos elektrik berdasarkan penggunaan tenaga dan struktur tariff yang ditetapkan.

### User Management

Mengurus pengguna, peranan, akses dan konfigurasi akaun.

### Analytics & Reports

Menjana analytics, insights dan laporan penggunaan tenaga.

---

## Future Architecture

Apabila platform berkembang, modul tertentu boleh dipisahkan kepada service yang berasingan tanpa memerlukan rewrite secara besar-besaran.

Contoh service yang berpotensi dipisahkan:

* Device Service
* Energy Service
* Billing Service
* Analytics Service
* Notification Service

Pendekatan ini membolehkan sistem berkembang secara berperingkat mengikut pertumbuhan pengguna dan keperluan perniagaan.

---

## Design Principles

Backend Wattsense dibina berdasarkan prinsip berikut:

* Maintainability
* Scalability
* Modularity
* Security
* Performance
* Future Extensibility

Semua keputusan architecture perlu menyokong objektif jangka panjang platform dan mengurangkan keperluan untuk melakukan major rewrite pada masa hadapan.

---

## Conclusion

Java Spring Boot dipilih sebagai platform backend utama kerana ia menawarkan keseimbangan terbaik antara maintainability, scalability dan keperluan jangka panjang produk.

Pendekatan Modular Monolith digunakan pada peringkat awal untuk mempercepatkan pembangunan sambil menyediakan laluan yang jelas ke arah architecture yang lebih besar apabila platform berkembang.
