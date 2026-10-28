<div align="center">

![Cruise Hospitality Technology Banner](https://raw.githubusercontent.com/Cruise-JavaCLass/.github/main/profile/assets/hero-banner.svg)

<br />

### Enterprise Maritime Cloud & Edge Operations

Cruise Hospitality Technology delivers an open-standard software infrastructure for passenger cruise liners. Engineered with strict fault tolerance, offline-first edge reliability, and sub-second maritime communications.

<br />

<p align="center">
  <a href="https://github.com/Cruise-JavaCLass/Cruise-api"><img src="https://img.shields.io/badge/API_Core-Java_21_%7C_Spring_Boot_4-007396?style=flat-square&logo=openjdk&logoColor=white" alt="API" /></a>
  &nbsp;
  <a href="https://github.com/Cruise-JavaCLass/Cruise-web"><img src="https://img.shields.io/badge/Web_Suite-React_19_%7C_TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="Web" /></a>
  &nbsp;
  <a href="https://github.com/Cruise-JavaCLass/Cruise-pos"><img src="https://img.shields.io/badge/Edge_POS-Android_%7C_Jetpack_Compose-3DDC84?style=flat-square&logo=android&logoColor=white" alt="POS" /></a>
  &nbsp;
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-D4AF37?style=flat-square" alt="License" /></a>
</p>

</div>

---

### Core Repositories & Subsystems

<table>
  <thead>
    <tr style="border-bottom: 2px solid #30363d;">
      <th align="left" width="28%">Repository</th>
      <th align="left" width="32%">Key Capabilities</th>
      <th align="left" width="40%">Technology Stack</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="left">
        <a href="https://github.com/Cruise-JavaCLass/Cruise-api">
          <b>Cruise-api</b>
        </a>
        <br />
        <small style="color: #8b949e;">Central Maritime Engine</small>
      </td>
      <td align="left">
        Itinerary navigation engine, cabin ledger reconciliation, excursion roster, and gateway security.
      </td>
      <td align="left">
        <code>Java 21</code> &bull; <code>Spring Boot 4.x</code> &bull; <code>MySQL</code> &bull; <code>Redis</code> &bull; <code>Docker</code>
      </td>
    </tr>
    <tr>
      <td align="left">
        <a href="https://github.com/Cruise-JavaCLass/Cruise-web">
          <b>Cruise-web</b>
        </a>
        <br />
        <small style="color: #8b949e;">Operations & Guest Experience</small>
      </td>
      <td align="left">
        Fleet operations deck, 3D interactive vessel deck plans, passenger booking hub, and emergency muster.
      </td>
      <td align="left">
        <code>React 19</code> &bull; <code>TypeScript</code> &bull; <code>Vite</code> &bull; <code>Tailwind 4</code> &bull; <code>Three.js</code>
      </td>
    </tr>
    <tr>
      <td align="left">
        <a href="https://github.com/Cruise-JavaCLass/Cruise-pos">
          <b>Cruise-pos</b>
        </a>
        <br />
        <small style="color: #8b949e;">Edge Handheld POS</small>
      </td>
      <td align="left">
        High-availability cashless checkout, RFID wristband tap, offline transaction spooling, and satellite batch sync.
      </td>
      <td align="left">
        <code>Kotlin</code> &bull; <code>Jetpack Compose</code> &bull; <code>Room DB</code> &bull; <code>Coroutines</code> &bull; <code>NFC</code>
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

    WEB["Cruise-web<br/>Operations & Guest Portal"]:::client
    POS["Cruise-pos<br/>Edge Offline Terminal"]:::client

    GW["API Gateway<br/>Port :8080"]:::gateway

    WEB -->|JWT / HTTPS| GW
    POS -->|Encrypted Batch Sync| GW

    subgraph Cluster ["Core Maritime Services"]
        GW --> ITIN["Itinerary Service"]:::service
        GW --> ACT["Excursion & Activities"]:::service
        GW --> POSS["POS & Cabin Ledger"]:::service
        GW --> AUTH["Auth & Security"]:::service
    end
```

---

### Developer & Governance Resources

<table>
  <tr>
    <td width="33%" align="left">
      <h4>Documentation</h4>
      <p>Microservice contracts, schema definitions, and OpenAPI documentation.</p>
      <a href="https://github.com/Cruise-JavaCLass/Cruise-api">View Architecture &rarr;</a>
    </td>
    <td width="33%" align="left">
      <h4>Contributing</h4>
      <p>Engineering workflows, PR templates, and Git branching guidelines.</p>
      <a href="CONTRIBUTING.md">Read Guidelines &rarr;</a>
    </td>
    <td width="33%" align="left">
      <h4>Security & SOLAS</h4>
      <p>Responsible disclosure policies and maritime safety compliance standards.</p>
      <a href="SECURITY.md">Review Protocols &rarr;</a>
    </td>
  </tr>
</table>

<br />

<div align="center">

**[Cruise Hospitality Technology](https://github.com/Cruise-JavaCLass)** &bull; Enterprise Maritime Systems  
<sub>Cruise Management System &copy; 2026. Distributed under the MIT License.</sub>

</div>
