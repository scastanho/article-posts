# article-posts

# 7Rs Framework + Practical Examples (PT / EN) — Enhanced with Migration Patterns

---

## ☁️ 7Rs Framework — Summary

| Português                                                                                           | English                                                                                       |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| **Rehost (Lift & Shift):** Migrar workloads como estão (VM on-prem → VM cloud), com mínima mudança. | **Rehost (Lift & Shift):** Move workloads as-is (on-prem VM → cloud VM) with minimal changes. |
| **Replatform:** Pequenas otimizações (ex: VM → container, DB gerenciado).                           | **Replatform:** Minor optimizations (e.g., VM → containers, managed DB).                      |
| **Refactor / Re-architect:** Redesenho para cloud-native (APIs, microservices, event-driven).       | **Refactor / Re-architect:** Redesign into cloud-native (APIs, microservices, event-driven).  |
| **Repurchase:** Substituir por SaaS.                                                                | **Repurchase:** Replace with SaaS.                                                            |
| **Retire:** Desativar sistemas sem valor.                                                           | **Retire:** Decommission unused systems.                                                      |
| **Retain:** Manter on-prem ou híbrido.                                                              | **Retain:** Keep on-prem or hybrid.                                                           |
| **Relocate:** Migrar sem alteração (ex: VMware → VMware Cloud).                                     | **Relocate:** Move without changes (e.g., VMware to VMware Cloud).                            |

---

## 🧠 Migration Approach

| Português                      | English                      |
| ------------------------------ | ---------------------------- |
| Avaliar workloads e contexto   | Assess workloads and context |
| Mapear dependências            | Map dependencies             |
| Classificar (7Rs)              | Classify (7Rs)               |
| Definir plano                  | Define migration plan        |
| Executar com controle de risco | Execute with risk control    |

---

## 🚗 Auto & Home Insurance

| Português                                                                   | English                                                        |
| --------------------------------------------------------------------------- | -------------------------------------------------------------- |
| Rehost: migração de aplicações WebSphere/MQ on-prem para VMs em cloud       | Rehost: migrated WebSphere/MQ apps from on-prem to cloud VMs   |
| Refactor: APIs de cotação em tempo real desacoplando sistemas legados       | Refactor: real-time quoting APIs decoupling legacy systems     |
| Refactor: introdução de mensageria (MQ/Kafka) para processamento assíncrono | Refactor: introduced messaging (MQ/Kafka) for async processing |
| Retain: sistemas críticos de underwriting mantidos on-prem                  | Retain: critical underwriting systems kept on-prem             |

---

## 🛍️ Retail & Omnichannel

| Português                                                        | English                                                       |
| ---------------------------------------------------------------- | ------------------------------------------------------------- |
| Rehost: workloads legados migrados para cloud via VM             | Rehost: legacy workloads migrated to cloud via VMs            |
| Refactor: desacoplamento do mainframe via APIs e eventos         | Refactor: decoupled mainframe via APIs and event-driven flows |
| Refactor: uso de Kafka para integração omnichannel em tempo real | Refactor: Kafka used for real-time omnichannel integration    |
| Retain: core COBOL mantido por estabilidade                      | Retain: COBOL core retained for stability                     |

---

## 🏥 Healthcare (HL7 / FHIR)

| Português                                                  | English                                                |
| ---------------------------------------------------------- | ------------------------------------------------------ |
| Rehost: sistemas hospitalares migrados para cloud via VM   | Rehost: hospital systems migrated to cloud via VMs     |
| Refactor: EMR cloud-native com APIs FHIR                   | Refactor: cloud-native EMR using FHIR APIs             |
| Refactor: mensageria para troca segura de eventos clínicos | Refactor: messaging for secure clinical event exchange |
| Retain: sistemas legados hospitalares integrados           | Retain: legacy hospital systems integrated             |

---

## 🏦 Banking & Payments

| Português                                                      | English                                                   |
| -------------------------------------------------------------- | --------------------------------------------------------- |
| Rehost: workloads on-prem migrados para cloud (VM-based)       | Rehost: on-prem workloads migrated to cloud (VM-based)    |
| Refactor: arquitetura de APIs seguras para integração global   | Refactor: secure API architecture for global integrations |
| Refactor: pipelines de dados com streaming (Kafka) para fraude | Refactor: streaming pipelines (Kafka) for fraud detection |
| Retain: core banking mantido por compliance                    | Retain: core banking retained due to compliance           |

---

## 🏢 Property Management

| Português                                                          | English                                                          |
| ------------------------------------------------------------------ | ---------------------------------------------------------------- |
| Refactor: plataforma cloud-native com APIs e serviços desacoplados | Refactor: cloud-native platform with APIs and decoupled services |
| Repurchase: integração com serviços externos de pagamento          | Repurchase: integrated external payment services                 |
| Replatform: digitalização de processos operacionais                | Replatform: digitized operational processes                      |

---

## ⛏️ Mining (IoT)

| Português                                                 | English                                                     |
| --------------------------------------------------------- | ----------------------------------------------------------- |
| Refactor: arquitetura orientada a eventos para telemetria | Refactor: event-driven architecture for telemetry           |
| Refactor: streaming de dados via Kafka para Data Lake     | Refactor: Kafka streaming to Data Lake                      |
| Retain: sistemas industriais locais (edge/on-prem)        | Retain: industrial edge/on-prem systems                     |
| Relocate: integração edge → cloud sem alterar hardware    | Relocate: edge to cloud integration without hardware change |

---

## 🚚 Logistics & Transportation

| Português                                              | English                                                      |
| ------------------------------------------------------ | ------------------------------------------------------------ |
| Rehost: sistemas logísticos migrados para cloud via VM | Rehost: logistics systems migrated to cloud via VMs          |
| Refactor: APIs e eventos para otimização de rotas      | Refactor: APIs and event-driven flows for route optimization |
| Refactor: mensageria para integração ERP/WMS           | Refactor: messaging for ERP/WMS integration                  |
| Retain: sistemas legados operacionais                  | Retain: legacy operational systems                           |

---

## 🤖 AI & Machine Learning

| Português                                          | English                                       |
| -------------------------------------------------- | --------------------------------------------- |
| Refactor: pipelines MLOps cloud-native             | Refactor: cloud-native MLOps pipelines        |
| Replatform: dados preparados para analytics/ML     | Replatform: data prepared for analytics/ML    |
| Repurchase: uso de serviços cognitivos gerenciados | Repurchase: use of managed cognitive services |

---

## 🔐 Cybersecurity

| Português                                                  | English                                            |
| ---------------------------------------------------------- | -------------------------------------------------- |
| Retain: controles críticos (IAM, SIEM, compliance)         | Retain: critical controls (IAM, SIEM, compliance)  |
| Replatform: adaptação de segurança para cloud (Zero Trust) | Replatform: cloud security adaptation (Zero Trust) |

---

## 🔗 Enterprise Integrations

| Português                                                      | English                                                   |
| -------------------------------------------------------------- | --------------------------------------------------------- |
| Rehost: middleware on-prem migrado para cloud (VM/brokers)     | Rehost: on-prem middleware migrated to cloud (VM/brokers) |
| Refactor: evolução para APIs e arquitetura orientada a eventos | Refactor: evolved into APIs and event-driven architecture |
| Refactor: uso de Kafka/MQ para integração assíncrona escalável | Refactor: Kafka/MQ for scalable async integration         |
| Retain: sistemas legados integrados via ESB                    | Retain: legacy systems integrated via ESB                 |

---

## 🎯 Key Insight

| Português                                                      | English                                                      |
| -------------------------------------------------------------- | ------------------------------------------------------------ |
| Na prática, múltiplos Rs são combinados no mesmo sistema.      | In practice, multiple Rs are combined in the same system.    |
| Migração pode começar com VM (Rehost) e evoluir para Refactor. | Migration may start with VM (Rehost) and evolve to Refactor. |
| Arquiteturas modernas usam APIs, mensageria e eventos.         | Modern architectures use APIs, messaging, and events.        |
| Decisão depende de risco, custo, dependências e negócio.       | Decisions depend on risk, cost, dependencies, and business.  |
