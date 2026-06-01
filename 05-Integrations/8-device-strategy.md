# Device Strategy

## Overview

Wattsense dibangunkan untuk membantu pengguna memahami penggunaan tenaga dan mengurangkan kos elektrik tanpa memerlukan pemasangan yang kompleks atau kos permulaan yang tinggi.

Tiada satu teknologi yang mampu memberikan penyelesaian yang murah, mudah dipasang dan 100% tepat pada masa yang sama. Oleh itu, Wattsense menggunakan pendekatan berperingkat yang menggabungkan beberapa teknologi mengikut keperluan produk dan kematangan platform.

---

## Device Monitoring Approaches

### Smart Plug

Smart Plug memberikan bacaan penggunaan tenaga yang paling tepat pada peringkat peranti.

#### Advantages

* Ketepatan hampir 100% untuk peranti yang dipantau.
* Mudah mengira penggunaan kWh dan kos bagi setiap peranti.
* Sesuai untuk peranti seperti:

  * TV
  * Peti sejuk
  * Penapis air
  * Mesin basuh

#### Limitations

* Setiap peranti memerlukan Smart Plug tersendiri.
* Kos meningkat apabila bilangan peranti bertambah.
* Kurang sesuai untuk pengguna yang mempunyai banyak peralatan elektrik.

---

### CT Clamp

CT Clamp dipasang pada Distribution Board (DB) dan mengukur penggunaan tenaga keseluruhan atau mengikut litar.

#### Advantages

* Hanya memerlukan satu pemasangan.
* Sesuai untuk rumah dan premis SME.
* Memberikan bacaan penggunaan tenaga keseluruhan yang tepat.
* Kos pemasangan lebih rendah berbanding memasang Smart Plug pada semua peranti.

#### Limitations

* Tidak dapat mengenal pasti penggunaan tenaga bagi setiap peranti secara langsung.
* Hanya dapat memaparkan penggunaan tenaga mengikut litar atau zon.

---

### AI-Based Device Detection (NILM)

Non-Intrusive Load Monitoring (NILM) menggunakan Machine Learning untuk menganggarkan penggunaan tenaga setiap peranti berdasarkan corak penggunaan elektrik.

#### Advantages

* Hanya memerlukan sensor pada DB.
* Pengguna tidak perlu memasang Smart Plug pada setiap peranti.
* Berpotensi memberikan device-level insights secara automatik.

#### Limitations

* Tidak mencapai ketepatan 100%.
* Memerlukan data latihan yang banyak.
* Kompleks untuk dibangunkan dan diselenggara.
* Tidak sesuai untuk MVP.

---

## Recommended Strategy

### Phase 1 - MVP

Wattsense menggunakan pendekatan hybrid:

* CT Clamp untuk pemantauan keseluruhan rumah atau premis.
* Smart Plug untuk beberapa peranti penting.

Contoh:

* Aircond
* Water Heater
* Water Filter
* Refrigerator

Pendekatan ini memberikan keseimbangan terbaik antara kos, ketepatan dan pengalaman pengguna.

---

### Phase 2 - Enhanced Insights

Platform mula menggabungkan data daripada:

* CT Clamp
* Smart Plug
* Historical Usage Data

untuk menghasilkan anggaran penggunaan tenaga yang lebih pintar.

---

### Phase 3 - AI Energy Intelligence

Wattsense akan membangunkan kemampuan NILM sendiri bagi menganggarkan penggunaan tenaga setiap peranti tanpa memerlukan pemasangan Smart Plug yang banyak.

Ini akan menjadi salah satu kelebihan kompetitif utama platform.

---

## Long-Term Vision

Matlamat jangka panjang Wattsense adalah membolehkan pengguna:

* Memasang satu atau beberapa sensor sahaja.
* Mendapatkan gambaran penuh penggunaan tenaga rumah atau premis.
* Mengenal pasti peranti yang menyumbang kepada bil elektrik yang tinggi.
* Mengambil tindakan untuk mengurangkan kos elektrik.

---

## Strategic Principle

Wattsense tidak mengejar ketepatan 100% pada peringkat awal.

Keutamaan utama adalah memberikan maklumat yang mencukupi kepada pengguna untuk membantu mereka membuat keputusan yang boleh mengurangkan bil elektrik dan meningkatkan kecekapan tenaga.
