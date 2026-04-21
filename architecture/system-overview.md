# System Overview

U4 WattSense is a smart energy monitoring system designed to measure electricity consumption in real-time, calculate costs, and optimize energy usage.

## Key Components
1. **Smart Energy Device (IoT)**
   - Reads energy consumption (kWh)
   - Communicates with backend via MQTT or REST API
   - Supports Tuya and future custom devices

2. **Backend (Java Spring Boot)**
   - API for device data ingestion
   - Stores historical consumption in database
   - Provides endpoints for analytics and billing

3. **Frontend (React + Vite)**
   - Dashboard for real-time monitoring
   - Graphs consumption trends
   - Displays cost calculation based on kWh → RM

4. **Cloud / Database**
   - PostgreSQL for structured data
   - Optional Redis for caching
   - Supports multi-country deployment (Malaysia, Singapore, Brunei, Thailand)

## Goals
- Accurate real-time energy monitoring
- User-friendly dashboard and analytics
- Scalable backend for multiple regions