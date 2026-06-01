# Frontend Architecture

## Overview

Wattsense menggunakan React dan Next.js sebagai teknologi frontend utama.

Architecture frontend direka untuk menyokong pembangunan jangka panjang, scalability dan maintainability apabila bilangan feature dan ahli pasukan bertambah.

---

## Design Principles

### Feature-Based Structure

Kod aplikasi perlu disusun mengikut domain atau feature dan bukannya mengikut jenis fail semata-mata.

Contoh:

```text
dashboard
billing
devices
analytics
settings
```

Pendekatan ini memudahkan pembangunan dan penyelenggaraan apabila sistem semakin besar.

---

### Separation of Concerns

Setiap lapisan aplikasi mempunyai tanggungjawab yang jelas:

* UI Components
* Business Logic
* API Communication
* State Management
* Shared Utilities

---

### Reusability

Komponen yang boleh digunakan semula perlu ditempatkan dalam shared components library.

Contoh:

* Buttons
* Tables
* Charts
* Forms
* Modals

---

### Scalability

Architecture perlu menyokong:

* Multi-country support
* Multi-site monitoring
* SME dashboard
* Future enterprise features

tanpa perubahan struktur yang besar.

---

## Recommended Project Structure

```text
app/
features/
components/
services/
hooks/
contexts/
types/
utils/
config/
public/
```

---

## Future Considerations

Frontend architecture perlu bersedia untuk menyokong:

* Role-Based Access Control (RBAC)
* Multi-tenancy
* Internationalisation (i18n)
* Offline Support
* Progressive Web App (PWA)

---

## Architecture Principle

Frontend perlu dibina untuk jangka panjang dan bukannya hanya untuk mempercepatkan pembangunan MVP.


## Professional Next.js Project Structure (Production-Ready) Sample

wattsense-frontend/
├── app/                            # Next.js App Router (Next 13+)
│   ├── layout.tsx                  # Root layout, header/footer, providers
│   ├── page.tsx                    # Home page / Dashboard entry
│   ├── loading.tsx                 # Global loading indicator
│   ├── error.tsx                   # Global error boundary
│   ├── api/                        # API routes (Next.js route handlers)
│   │   ├── readings/
│   │   │   ├── route.ts
│   │   │   └── service.ts          # encapsulate API logic
│   │   └── billing/
│   │       └── route.ts
│   ├── features/                   # Feature-based grouping
│   │   ├── dashboard/
│   │   │   ├── page.tsx
│   │   │   ├── components/         # dashboard-specific components
│   │   │   └── hooks/
│   │   │       └── useDashboardData.ts
│   │   └── billing/
│   │       ├── page.tsx
│   │       ├── components/
│   │       └── hooks/
│   └── components/                 # Shared / reusable UI components
│       ├── charts/
│       ├── tables/
│       └── ui/                     # Buttons, inputs, modals, etc.
├── contexts/                       # React contexts / global state
│   └── KwhContext.tsx
├── hooks/                           # Shared custom hooks
├── libs/                            # External libs / helpers / utils
│   ├── apiClient.ts                 # axios/fetch wrapper
│   ├── kwhToRM.ts
│   └── logger.ts
├── types/                           # TypeScript types / interfaces
│   └── kwh.ts
├── services/                        # Business logic layer (optional)
│   ├── kwhService.ts
│   └── billingService.ts
├── middlewares/                     # Middlewares for API or auth
├── public/                          # Static assets (images, icons)
├── styles/                          # Tailwind, SCSS, CSS modules
├── config/                          # Env configs, constants
│   └── index.ts
├── utils/                           # General helpers
├── .env.local                       # Local environment variables
├── next.config.js
├── tsconfig.json
└── package.json