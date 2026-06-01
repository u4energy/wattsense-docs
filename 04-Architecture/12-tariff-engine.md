# Tariff Engine Architecture

## Overview

Tariff Engine merupakan komponen yang bertanggungjawab mengira kos elektrik berdasarkan penggunaan tenaga dan struktur tarif yang berbeza mengikut negara.

---

## Objectives

Tariff Engine perlu:

* Menyokong pelbagai negara.
* Menyokong perubahan tarif tanpa perubahan kod aplikasi.
* Menyokong pelbagai struktur caj utiliti.
* Menyediakan cost estimation yang konsisten.

---

## Design Principles

### Configurable

Semua kadar tarif perlu disimpan dalam database.

### Country-Aware

Setiap negara mempunyai konfigurasi tersendiri.

### Versioned

Perubahan tarif perlu direkodkan mengikut tarikh berkuat kuasa.

---

## Example Structure

```text
Tariff Configuration
│
├── Country
├── Effective Date
├── Generation Rate
├── Capacity Rate
├── Network Rate
├── Retail Charge
└── Adjustment Rate
```

---

## Benefits

Pendekatan ini membolehkan Wattsense berkembang ke:

* Malaysia
* Singapore
* Brunei
* Thailand
* Indonesia

tanpa perlu mengubah business logic utama.

---

## Long-Term Direction

Tariff Engine perlu menjadi komponen teras platform dan digunakan oleh:

* Dashboard
* Billing Module
* Reporting Module
* Analytics Module
* AI Recommendation Engine
