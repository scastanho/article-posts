# 7Rs Framework — Best Practices (PT / EN)

---

## ☁️ 7Rs Framework — Best Practices Summary

| Português                                                                                                                     | English                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **Comece pelo negócio, não pela tecnologia:** priorize valor, impacto e criticidade antes da decisão técnica.                 | **Start with business, not technology:** prioritize value, impact, and criticality before technical decisions.        |
| **Faça assessment por workload, não por sistema inteiro:** componentes diferentes podem ter estratégias diferentes (multi-R). | **Assess per workload, not entire system:** different components may require different strategies (multi-R).          |
| **Mapeie dependências profundamente:** identifique integrações, dados, latência e acoplamentos antes de migrar.               | **Map dependencies thoroughly:** identify integrations, data flows, latency, and coupling before migrating.           |
| **Use Rehost como estratégia inicial, não final:** acelera a migração, mas não entrega modernização completa.                 | **Use Rehost as a starting strategy, not final state:** accelerates migration but doesn’t deliver full modernization. |
| **Planeje evolução incremental (Rehost → Refactor):** adote abordagem faseada para reduzir risco.                             | **Plan incremental evolution (Rehost → Refactor):** use phased approach to reduce risk.                               |
| **Evite refatorar tudo de uma vez:** escolha sistemas críticos ou de alto valor para modernização profunda.                   | **Avoid refactoring everything at once:** prioritize high-value or critical systems.                                  |
| **Considere custo total (TCO), não só migração:** inclua operação, manutenção e licenciamento.                                | **Consider total cost (TCO), not just migration:** include operations, maintenance, and licensing.                    |
| **Inclua segurança desde o início:** IAM, criptografia, compliance e arquitetura Zero Trust.                                  | **Embed security from the start:** IAM, encryption, compliance, and Zero Trust architecture.                          |
| **Garanta readiness de infraestrutura:** networking, identidade, storage e governança devem estar preparados.                 | **Ensure infrastructure readiness:** networking, identity, storage, and governance must be ready.                     |
| **Defina estratégia de rollback:** sempre tenha plano de reversão para mitigar riscos.                                        | **Define rollback strategy:** always have a fallback plan to mitigate risks.                                          |
| **Use automação sempre que possível:** IaC, pipelines CI/CD e scripts reduzem erro humano.                                    | **Use automation whenever possible:** IaC, CI/CD pipelines, and scripts reduce human error.                           |
| **Adote arquitetura desacoplada:** APIs e mensageria (ex: Kafka, MQ) facilitam evolução e escalabilidade.                     | **Adopt decoupled architecture:** APIs and messaging (e.g., Kafka, MQ) enable scalability and evolution.              |
| **Prefira processamento assíncrono quando possível:** melhora resiliência e throughput.                                       | **Prefer asynchronous processing when possible:** improves resilience and throughput.                                 |
| **Planeje cutover com cuidado:** minimize downtime e impacto ao negócio.                                                      | **Plan cutover carefully:** minimize downtime and business impact.                                                    |
| **Engaje stakeholders desde o início:** alinhe times técnicos e de negócio continuamente.                                     | **Engage stakeholders early:** align technical and business teams continuously.                                       |
| **Documente decisões (ADR):** registre trade-offs e justificativas técnicas.                                                  | **Document decisions (ADR):** capture trade-offs and technical rationale.                                             |
| **Monitore e valide após migração:** observabilidade, métricas e logs são essenciais.                                         | **Monitor and validate post-migration:** observability, metrics, and logs are critical.                               |
| **Não ignore sistemas para Retire:** elimine redundâncias para reduzir custo e complexidade.                                  | **Do not ignore Retire candidates:** remove redundancy to reduce cost and complexity.                                 |
| **Use Retain de forma consciente:** manter legado deve ser decisão estratégica, não inércia.                                  | **Use Retain consciously:** keeping legacy should be strategic, not inertia.                                          |
| **Avalie SaaS (Repurchase) quando fizer sentido:** acelera time-to-market e reduz manutenção.                                 | **Evaluate SaaS (Repurchase) when appropriate:** accelerates time-to-market and reduces maintenance.                  |
| **Considere latência e localização de dados:** especialmente para sistemas críticos ou regulados.                             | **Consider latency and data locality:** especially for critical or regulated systems.                                 |
| **Prepare times operacionais:** suporte, monitoramento e operação devem evoluir junto com a arquitetura.                      | **Prepare operational teams:** support, monitoring, and operations must evolve with architecture.                     |

---

## 🎯 Key Insight

| Português                                                                           | English                                                                             |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| O 7Rs não é uma decisão única — é um processo contínuo e evolutivo.                 | 7Rs is not a one-time decision — it is a continuous and evolving process.           |
| A melhor estratégia geralmente combina múltiplos Rs ao longo do tempo.              | The best strategy often combines multiple Rs over time.                             |
| O sucesso depende mais de execução e alinhamento do que da escolha técnica isolada. | Success depends more on execution and alignment than on isolated technical choices. |




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
