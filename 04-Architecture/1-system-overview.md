# System Overview

## Overview

Wattsense merupakan platform Smart Energy Monitoring yang membolehkan pengguna memantau penggunaan tenaga secara real-time, mengira kos elektrik berdasarkan penggunaan kWh, serta mendapatkan analytics dan insights untuk mengoptimumkan penggunaan tenaga.

Platform ini direka untuk menyokong pengguna residential, commercial dan SME dengan fokus kepada pemantauan tenaga yang mudah digunakan, scalable dan boleh diperluaskan ke pelbagai negara pada masa hadapan.

---

## High-Level Architecture

```text
Smart Device
    ↓
Cloud Provider
    ↓
Wattsense Backend
    ↓
Database
    ↓
Dashboard & Analytics
```

---

## Core Components

### Smart Energy Device (IoT)

Peranti yang digunakan untuk mengumpul data penggunaan tenaga daripada peralatan elektrik.

**Supported Devices**

- Smart Plug
- Smart Switch
- Energy Meter
- Future Industrial Devices

**Main Responsibilities**

- Membaca penggunaan tenaga (kWh)
- Mengukur voltan, arus dan kuasa
- Menghantar data ke Cloud Provider
- Menyokong integrasi dengan Tuya dan future custom devices

---

### Integration Layer

Layer ini bertanggungjawab menghubungkan Wattsense dengan platform atau peranti pihak ketiga.

**Supported Integrations**

- Tuya IoT Cloud
- Future OEM Devices
- Future Industrial Meters

**Main Responsibilities**

- Mengambil data tenaga daripada Cloud Provider
- Menyelaraskan format data daripada pelbagai vendor
- Menyediakan abstraction layer untuk integrasi baharu

---

### Backend Layer

Backend dibangunkan menggunakan Java Spring Boot dan bertindak sebagai pusat pemprosesan sistem.

**Main Responsibilities**

- User Management
- Device Management
- Energy Data Collection
- Cost Calculation
- Analytics Processing
- Automation Rules
- API Services

---

### Data Layer

Semua data tenaga dan maklumat pengguna disimpan untuk tujuan analisis dan pelaporan.

**Technologies**

- PostgreSQL
- Redis (optional caching)

**Stored Data**

- Historical Consumption
- Device Information
- User Information
- Cost Calculation Records
- Analytics Data

---

### Presentation Layer

Maklumat tenaga dipaparkan kepada pengguna melalui interface yang mudah digunakan.

**Available Channels**

- Web Dashboard
- Mobile Application
- Future Partner Portal

**Main Features**

- Real-Time Monitoring
- Energy Analytics
- Cost Tracking
- Historical Trends
- Device Control

---

## Platform Goals

Wattsense dibangunkan dengan objektif berikut:

- Menyediakan pemantauan tenaga secara real-time yang tepat
- Membantu pengguna memahami kos penggunaan elektrik
- Mengurangkan pembaziran tenaga melalui data-driven insights
- Menyediakan platform yang scalable untuk pelbagai negara
- Menyokong pengembangan kepada SME dan industrial market

---

## Future Direction

Dalam jangka panjang, platform akan berkembang untuk menyokong:

- Energy Intelligence
- AI Recommendations
- Automation Engine
- Multi-Site Monitoring
- SME Analytics
- ESG Reporting
- Carbon Monitoring
- White Label Platform

---

## Regional Scalability

Architecture Wattsense direka untuk menyokong deployment di pelbagai negara termasuk:

- Malaysia
- Singapore
- Brunei
- Thailand

Negara tambahan boleh ditambah pada masa hadapan dengan konfigurasi tariff dan localisation yang minimum.