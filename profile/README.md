<div align="center">

![Cruise Hospitality Technology Banner](https://raw.githubusercontent.com/Cruise-JavaCLass/.github/main/profile/assets/hero-banner.svg)

<br />

**Cruise Maritime Operations & Hospitality Platform:** An open enterprise ecosystem engineered for luxury cruise fleets. Seamlessly unifying high-concurrency itinerary navigation, excursion bookings, maritime safety protocols, and offline-first cashless POS.

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

### Architecture & Repositories

<table>
  <thead>
    <tr>
      <th width="30%">Repository</th>
      <th width="35%">Technology Stack</th>
      <th width="35%">Domain & Scope</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <a href="https://github.com/Cruise-JavaCLass/Cruise-api">
          <b>Cruise-api</b>
        </a><br />
        <sub>Backend Engine & Gateway</sub>
      </td>
      <td>
        <code>Java 21</code> &bull; <code>Spring Boot 4.x</code><br />
        <code>Spring Security</code> &bull; <code>MySQL</code> &bull; <code>Redis</code>
      </td>
      <td>
        High-throughput API Gateway, daily itinerary navigation, excursion booking engine, and folio billing ledger.
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://github.com/Cruise-JavaCLass/Cruise-web">
          <b>Cruise-web</b>
        </a><br />
        <sub>Operations Deck & Guest Experience</sub>
      </td>
      <td>
        <code>React 19</code> &bull; <code>TypeScript</code> &bull; <code>Vite</code><br />
        <code>Tailwind CSS 4</code> &bull; <code>Three.js</code> &bull; <code>TanStack Query</code>
      </td>
      <td>
        Fleet command dashboard, interactive 3D vessel digital twin, guest mobile-first portal, and real-time muster.
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://github.com/Cruise-JavaCLass/Cruise-pos">
          <b>Cruise-pos</b>
        </a><br />
        <sub>Mobile Edge Point of Sale</sub>
      </td>
      <td>
        <code>Android</code> &bull; <code>Kotlin</code> &bull; <code>Jetpack Compose</code><br />
        <code>Room DB</code> &bull; <code>NFC / RFID</code> &bull; <code>Coroutines</code>
      </td>
      <td>
        Offline-first handheld POS for onboard lounges and dining, with satellite-adaptive batch synchronization.
      </td>
    </tr>
  </tbody>
</table>

---

### System Architecture & Sync Flow

```mermaid
graph LR
    classDef client fill:#0B1F33,stroke:#C5A572,stroke-width:1.5px,color:#fff;
    classDef gateway fill:#102A43,stroke:#397C80,stroke-width:2px,color:#fff;
    classDef service fill:#071727,stroke:#64B5F6,stroke-width:1.5px,color:#fff;

    WEB["🖥️ Cruise-web<br/>(Command Deck & Guest Portal)"]:::client
    POS["📱 Cruise-pos<br/>(Mobile Edge Terminal)"]:::client

    GW["🚪 API Gateway<br/>(:8080)"]:::gateway

    WEB -->|JWT / REST API| GW
    POS -->|Offline Batch Sync| GW

    subgraph Core ["Enterprise Maritime Services"]
        GW --> ITIN["🚢 Itinerary Service"]:::service
        GW --> ACT["🎟️ Excursion & Activity"]:::service
        GW --> POSS["💳 POS & Guest Ledger"]:::service
        GW --> AUTH["🔐 Auth & Access Control"]:::service
    end
```

---

### Resources & Governance

<table>
  <tr>
    <td width="33%" align="center">
      <b>📖 Documentation & APIs</b><br />
      Explore microservices contracts and API schemas in <a href="https://github.com/Cruise-JavaCLass/Cruise-api">Cruise-api</a>.
    </td>
    <td width="33%" align="center">
      <b>🤝 Contributing</b><br />
      Read our standards and branching strategy in <a href="CONTRIBUTING.md">CONTRIBUTING.md</a>.
    </td>
    <td width="33%" align="center">
      <b>🛡️ Security & Compliance</b><br />
      Report vulnerabilities and review muster policies in <a href="SECURITY.md">SECURITY.md</a>.
    </td>
  </tr>
</table>

<br />

<div align="center">

**[Cruise Hospitality Technology](https://github.com/Cruise-JavaCLass)** &bull; Engineered for Luxury Maritime Operations  
<sub>Cruise Management System &copy; 2026. Distributed under the MIT License.</sub>

</div>
