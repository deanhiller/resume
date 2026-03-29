# GitHub Open Source Projects

## Profile: [github.com/deanhiller](https://github.com/deanhiller)
## Location: Denver, CO
## 60+ Public Repositories

---

## Flagship Projects

### webpieces -- Java Web Framework
- **Repository:** [deanhiller/webpieces](https://github.com/deanhiller/webpieces)
- **Stars:** 34 | **Forks:** 10 | **Commits:** 1,936 | **Releases:** 342
- **Languages:** Java (80%), CSS, JavaScript, HTML, Shell
- Full-featured, modular Java web framework providing all components needed to build web servers
- Hot-recompiling dev server (no restarts needed)
- HTTP/1.1 and HTTP/2 support with backpressure
- **100,000 req/sec single-threaded; 24 Gbps NIO throughput**
- Built-in CSRF protection, cookie hashing, form auth tokens
- Server push, header compression, request multiplexing
- Guice-based dependency injection, JPA/Hibernate and NoSQL support
- 370+ customer-facing tests
- 11 modular components: channelmanager, asyncserver, HTTP parsers, HTTP clients, HTTP frontend, webserver, runtime compiler, etc.

### playorm -- NoSQL ORM with Scalable SQL
- **Repository:** [deanhiller/playorm](https://github.com/deanhiller/playorm)
- **Stars:** 78 | **Forks:** 17 | **Commits:** 1,041
- **Language:** Java
- ORM for NoSQL databases that provides SQL-like query capabilities ("S-SQL")
- Bridges the gap between NoSQL flexibility and SQL's structured query approach
- Targeted Apache Cassandra as primary backend
- Used as the data layer for NREL's DataBus project

### databus -- Time Series Database (NREL)
- **Repository:** [deanhiller/databus](https://github.com/deanhiller/databus)
- **Stars:** 53 | **Forks:** 21 | **Commits:** 943 | **Tags:** 1,803
- **Languages:** Python (53%), Java (24%), JavaScript (17%)
- Open-source time series data platform built on Cassandra with web-based visualization
- **Developed for NREL (National Renewable Energy Laboratory)**
- Dean Hiller served as **NREL architect** for this project
- Handles 100,000+ events per second, scales by adding data nodes
- Modbus protocol support for industrial data collection
- Solr full-text search integration
- Used for tracking and analyzing energy use on NREL's campus
- Featured in NREL press releases, ACM Communications, and Architect Magazine

### webpieces-ts -- TypeScript Microservice Framework
- **Repository:** [deanhiller/webpieces-ts](https://github.com/deanhiller/webpieces-ts)
- **Language:** TypeScript | **License:** Apache 2.0
- TypeScript port of the Java webpieces framework for Node.js
- Auto-wiring REST APIs via decorators
- Filter chain architecture for cross-cutting concerns
- Request-scoped context management (AsyncLocalStorage)
- No-HTTP testing (test APIs without HTTP overhead)
- Inversify-based dependency injection
- Active development (updated March 2026)

---

## Networking / Infrastructure Libraries

### channelmanager2
- **Repository:** [deanhiller/channelmanager2](https://github.com/deanhiller/channelmanager2)
- **Stars:** 3 | **Language:** Java
- Java NIO networking library -- "the only one with TRUE TCP flow control"
- Proper backpressure handling for network I/O
- Foundation networking layer used by webpieces

### tcpproxyrecorder
- **Repository:** [deanhiller/tcpproxyrecorder](https://github.com/deanhiller/tcpproxyrecorder)
- **Stars:** 5 | **Language:** Java
- TCP socket proxy that records all incoming/outgoing traffic
- Recorded data can be replayed for deterministic regression testing
- Eliminates need for actual downstream server during testing

---

## User Service Implementations (Polyglot)

Same service implemented in multiple languages to demonstrate cross-language proficiency:

| Repository | Language |
|---|---|
| [userService](https://github.com/deanhiller/userService) | Java |
| [userServiceTs](https://github.com/deanhiller/userServiceTs) | TypeScript |
| [userServiceJs](https://github.com/deanhiller/userServiceJs) | JavaScript |
| [pythonUserSvc](https://github.com/deanhiller/pythonUserSvc) | Python |

---

## NLP / Chinese Language Processing

### stanford-segmenter
- **Repository:** [deanhiller/stanford-segmenter](https://github.com/deanhiller/stanford-segmenter)
- **Stars:** 6 | **Language:** Java
- Chinese language word segmentation and parsing tool built on Stanford's algorithms

### corbit
- **Repository:** [deanhiller/corbit](https://github.com/deanhiller/corbit)
- **Language:** Java | **License:** BSD 3-Clause
- Chinese text analyzer

### CoreNLP (fork)
- Fork of stanfordnlp/CoreNLP -- Stanford's core NLP toolkit

---

## Web / Frontend Projects

| Repository | Description | Language |
|---|---|---|
| [webpieces-ts-example](https://github.com/deanhiller/webpieces-ts-example) | Example app for webpieces-ts | TypeScript |
| [webpiecesexample-all](https://github.com/deanhiller/webpiecesexample-all) | Example for Java webpieces | Java |
| [reactpatterns-all](https://github.com/deanhiller/reactpatterns-all) | React pattern testing | TypeScript |
| [firebase-auth](https://github.com/deanhiller/firebase-auth) | Firebase authentication | HTML |
| [codeignitercrud](https://github.com/deanhiller/codeignitercrud) | CRUD in CodeIgniter PHP | PHP |

---

## Android / Mobile

| Repository | Description | Language |
|---|---|---|
| [compositeAndroid](https://github.com/deanhiller/compositeAndroid) | Android composite builds with Gradle | Java |
| [androidStudio](https://github.com/deanhiller/androidStudio) | Android Studio project | Java |
| [codenameOneExamples](https://github.com/deanhiller/codenameOneExamples) | Cross-platform mobile (Codename One) | Java |

---

## Build / DevOps / Tooling

| Repository | Description | Language |
|---|---|---|
| [testMonorepoTemplate](https://github.com/deanhiller/testMonorepoTemplate) | Monorepo template | Java |
| [testMonorepo](https://github.com/deanhiller/testMonorepo) | Monorepo testing | TypeScript |
| [yarnworkspaces](https://github.com/deanhiller/yarnworkspaces) | Yarn workspaces testing | JS |
| [propertiesplugin](https://github.com/deanhiller/propertiesplugin) | Gradle properties plugin | Java |
| [databus-control](https://github.com/deanhiller/databus-control) | Databus operations scripts | Shell |

---

## Educational / Demonstration

| Repository | Description | Language |
|---|---|---|
| [catchall](https://github.com/deanhiller/catchall) | Response codes vs exceptions | Java |
| [guice-examples](https://github.com/deanhiller/guice-examples) | Power of Guice DI | Java |
| [salesserver-all](https://github.com/deanhiller/salesserver-all) | Sales server for gocode | Java |
| [stateMachine](https://github.com/deanhiller/stateMachine) | State machine implementation | Java |
| [feature-test-example](https://github.com/deanhiller/feature-test-example) | Feature testing patterns | Java |

---

## Notable Forks

| Repository | Original | Description |
|---|---|---|
| [fhir](https://github.com/deanhiller/fhir) | google/fhir | FHIR Protocol Buffers (healthcare) |
| [astyanax](https://github.com/deanhiller/astyanax) | Netflix/astyanax | Cassandra client library |
| [async-http-client](https://github.com/deanhiller/async-http-client) | -- | Async HTTP/WebSocket client |
| [play1](https://github.com/deanhiller/play1) | playframework/play1 | Play Framework 1.x |
| [gradle-nexus-staging-plugin](https://github.com/deanhiller/gradle-nexus-staging-plugin) | -- | Gradle Nexus staging |

---

## Other Projects

| Repository | Description | Language |
|---|---|---|
| [alipay](https://github.com/deanhiller/alipay) | Alipay (Chinese payment platform) library | Java |
| [timecardx](https://github.com/deanhiller/timecardx) | Timecard web software | Python |
| [playorm-server](https://github.com/deanhiller/playorm-server) | Web server for S-SQL interface | Python |
| [emptylog4j](https://github.com/deanhiller/emptylog4j) | Helper for logback migration | Shell |

---

## Key Technology Summary

| Technology | Depth |
|---|---|
| **Java** | Primary language across ~35 repos; frameworks, ORMs, NIO networking, Android, NLP |
| **TypeScript** | Growing focus; webpieces-ts, user services, React, monorepo tooling |
| **Python** | Databus (NREL), timecard apps, playorm-server |
| **HTTP/2** | Full implementation in webpieces |
| **Java NIO** | channelmanager2, webpieces async server -- true TCP flow control |
| **Apache Cassandra** | Backend for playorm, databus |
| **Guice / Inversify** | Dependency injection (Java / TypeScript) |
| **NLP** | Stanford segmenter, CoreNLP, Corbit (Chinese text) |
| **Android** | Composite builds, mobile examples |
| **Gradle** | Build system for nearly all Java projects |
