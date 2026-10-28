<div align="center">

![Cruise Hospitality Technology Banner](https://raw.githubusercontent.com/Cruise-JavaCLass/.github/main/profile/assets/hero-banner.svg)

<br />

**Cruise, the maritime operations & hospitality cloud:** An open, multi-tier enterprise ecosystem engineered for luxury cruise liners and maritime services. Unifies itinerary navigation, shore excursions, SOLAS safety muster tracking, and offline-first cashless POS — optimized for ultra-low latency, mission-critical resilience, and editorial elegance.

<br />

<p align="center">
  <a href="https://github.com/Cruise-JavaCLass/Cruise-api">
    <img src="https://img.shields.io/badge/Java_21-007396?style=flat&logo=openjdk&logoColor=white" alt="Java 21" />
  </a>
  <a href="https://github.com/Cruise-JavaCLass/Cruise-api">
    <img src="https://img.shields.io/badge/Spring_Boot_4-6DB33F?style=flat&logo=springboot&logoColor=white" alt="Spring Boot" />
  </a>
  <a href="https://github.com/Cruise-JavaCLass/Cruise-web">
    <img src="https://img.shields.io/badge/React_19-20232A?style=flat&logo=react&logoColor=61DAFB" alt="React 19" />
  </a>
  <a href="https://github.com/Cruise-JavaCLass/Cruise-web">
    <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white" alt="TypeScript" />
  </a>
  <a href="https://github.com/Cruise-JavaCLass/Cruise-web">
    <img src="https://img.shields.io/badge/Three.js-000000?style=flat&logo=threedotjs&logoColor=white" alt="Three.js" />
  </a>
  <a href="https://github.com/Cruise-JavaCLass/Cruise-pos">
    <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white" alt="Kotlin" />
  </a>
  <a href="https://github.com/Cruise-JavaCLass/Cruise-pos">
    <img src="https://img.shields.io/badge/Jetpack_Compose-4285F4?style=flat&logo=android&logoColor=white" alt="Compose" />
  </a>
  <a href="LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-C5A572?style=flat&logo=open-source-initiative&logoColor=white" alt="License" />
  </a>
</p>

</div>

---

### 🚢 Learn About Cruise Ecosystem ⚓ 🎓

- 📖 **Understand Core Operations**: Explore backend microservices in [`Cruise-api`](https://github.com/Cruise-JavaCLass/Cruise-api)
- 🖥️ **Explore the Web Experience**: Tour the luxury editorial dashboard and 3D digital twin in [`Cruise-web`](https://github.com/Cruise-JavaCLass/Cruise-web)
- 📱 **Inspect Point of Sale (POS)**: Review mobile RFID/NFC offline syncing in [`Cruise-pos`](https://github.com/Cruise-JavaCLass/Cruise-pos)
- 🛡️ **Security & Safety Standards**: Read our [Security Policy](SECURITY.md) and SOLAS emergency muster protocol
- 🤝 **Contribute to the Fleet**: Check our [Contributing Guide](CONTRIBUTING.md) and [Code of Conduct](CODE_OF_CONDUCT.md)

---

### 🏛️ Core Repositories & Subsystems

| Subsystem | Stack | Primary Responsibilities |
| :--- | :--- | :--- |
| **[`Cruise-api`](https://github.com/Cruise-JavaCLass/Cruise-api)** | Java 21 • Spring Boot 4.x • MySQL | **Maritime Intelligence Core:** Daily itinerary scheduling, shore excursion rosters, cabin billing accounts, and API Gateway routing. |
| **[`Cruise-web`](https://github.com/Cruise-JavaCLass/Cruise-web)** | React 19 • TypeScript • Tailwind 4 • Three.js | **Command Deck & Guest Portal:** Fleet operations dashboard, 3D maritime globe, digital boarding pass, and real-time activity bookings. |
| **[`Cruise-pos`](https://github.com/Cruise-JavaCLass/Cruise-pos)** | Android • Kotlin • Jetpack Compose | **Mobile POS Terminal:** Outlets, bars, and dining orders with local cache and adaptive satellite sync when connectivity drops. |

---

### 🗺️ System Dataflow & Synchronization

```mermaid
graph LR
    classDef client fill:#0B1F33,stroke:#C5A572,stroke-width:1.5px,color:#fff;
    classDef gateway fill:#102A43,stroke:#397C80,stroke-width:2px,color:#fff;
    classDef service fill:#071727,stroke:#64B5F6,stroke-width:1.5px,color:#fff;

    WEB["🖥️ Cruise-web<br/>(Operations & Guest Portal)"]:::client
    POS["📱 Cruise-pos<br/>(Mobile Offline Terminal)"]:::client

    GW["🚪 API Gateway<br/>(:8080)"]:::gateway

    WEB -->|JWT / REST API| GW
    POS -->|Offline Sync / Batch Queue| GW

    subgraph Cluster ["⚙️ Enterprise Microservices Cluster"]
        GW --> ITIN["🚢 Itinerary Service"]:::service
        GW --> ACT["🎟️ Excursion & Activity"]:::service
        GW --> POSS["💳 POS & Cabin Ledger"]:::service
        GW --> AUTH["🔐 Auth & Security"]:::service
    end
```

---

<div align="center">

**[Cruise Hospitality Technology](https://github.com/Cruise-JavaCLass)** • Transforming Maritime Journeys Through Intelligent Engineering  
<sub>Cruise Management System © 2026. Licensed under MIT.</sub>

</div>
