# Location Strategy

## Overview

Wattsense merancang untuk menyediakan visualisasi lokasi pengguna dan peranti melalui dashboard berasaskan peta bagi menyokong analitik global dan multi-country monitoring.

---

## Important Limitation

Peranti Tuya standard seperti Smart Plug dan Smart Switch tidak menyediakan GPS coordinates.

Maklumat yang biasanya tersedia:

* Device ID
* Device Status
* Energy Usage
* Timezone

Latitude dan longitude tidak disediakan secara langsung oleh peranti.

---

## Recommended Approach

### Phase 1 - User Location

Lokasi diperoleh semasa proses pendaftaran pengguna.

Maklumat yang dikumpulkan:

* Country
* State
* City
* Optional Address

Maklumat ini akan ditukarkan kepada latitude dan longitude menggunakan geocoding service.

---

### Phase 2 - Mobile App GPS

Aplikasi mobile boleh mendapatkan lokasi sebenar pengguna dengan kebenaran pengguna.

Maklumat lokasi akan dipautkan kepada premis atau kumpulan peranti yang berkaitan.

---

### Phase 3 - Multi-Site Management

Pengguna boleh mendaftarkan beberapa lokasi secara manual.

Contoh:

* Rumah
* Kedai
* Pejabat
* Cawangan

---

## Future Dashboard

### Global View

Paparan dunia yang menunjukkan:

* Jumlah pengguna mengikut negara
* Jumlah peranti aktif
* Penggunaan tenaga keseluruhan

### Country View

Paparan terperinci mengikut negara:

* Penggunaan tenaga
* Bilangan pengguna
* Bilangan peranti
* Trend penggunaan

---

## Strategic Value

Location intelligence membolehkan Wattsense menyediakan analitik yang lebih bernilai serta menyokong pengembangan ke pasaran antarabangsa.
