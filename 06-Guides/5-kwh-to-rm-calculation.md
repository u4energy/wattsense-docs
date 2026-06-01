# kWh to RM Calculation

## Overview

Wattsense menyediakan fungsi penukaran penggunaan tenaga kepada kos elektrik berdasarkan struktur tarif yang dikonfigurasikan.

---

## Basic Formula (V1)

### Formula

```text
Cost (RM) = Energy Usage (kWh) × Tariff Rate
```

### Example

```text
Energy Usage = 150 kWh
Tariff Rate = RM0.454

Cost = RM68.10
```

---

## Purpose

Formula ini digunakan untuk:

* Real-time dashboard
* Device-level monitoring
* Quick cost estimation

---

## Limitations

Formula ini tidak mengambil kira:

* Tariff tiers
* Capacity charges
* Network charges
* Monthly adjustments
* Regulatory charges

Oleh itu ia hanya sesuai untuk anggaran pantas.

---

## Advanced Formula (V2)

Untuk mendapatkan anggaran yang lebih hampir kepada bil utiliti sebenar, Wattsense akan menggunakan Tariff Engine.

Komponen yang boleh disokong:

* Generation Charge
* Capacity Charge
* Network Charge
* Retail Charge
* Regulatory Adjustment
* Country-specific Charges

---

## Design Principle

Formula tidak boleh di-hardcode.

Semua kadar tarif perlu dikonfigurasi melalui sistem konfigurasi bagi menyokong:

* Malaysia
* Singapore
* Brunei
* Thailand
* Indonesia
* Future Markets

---

## Strategic Principle

Ketepatan bil adalah penting.

Namun nilai sebenar Wattsense adalah:

* Device Cost Visibility
* Energy Insights
* Cost Optimisation

dan bukannya menggantikan bil rasmi utiliti.
