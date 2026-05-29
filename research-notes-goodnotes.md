# 📓 PhD Research Notes
## Process Improvement × Software Engineering

**Program:** วศ.ด. วิศวกรรมคอมพิวเตอร์ · Chulalongkorn University
**Intake:** Semester 1/2569 · **Target Graduation:** Semester 2/2571
**Last Updated:** May 29, 2026

---

## 🗂️ How to Use This File

- Add ideas under the relevant section as you explore
- Use `[ ]` checkboxes to track follow-up actions
- Tag entries with `#hot` when something feels like a strong thesis angle
- Use the **Parking Lot** at the bottom for half-baked ideas you don't want to lose

---

# 💡 Research Topics & Angles

---

## Topic 1 — AI-Augmented Software Process Improvement `#hot`

> *How can LLMs and ML tools be embedded into the SPI lifecycle to predict, detect, and correct process degradation?*

**Key observations:**
- AI now writes 20%+ of code at Google/Microsoft (2025) — how does this change SPI metrics?
- Existing frameworks (DORA, SPACE, CMMI) were not designed for AI-generated code
- Gap: new measurement models needed for AI-augmented teams
- CMMI AI Working Group (IBM + CMMI Institute, 2025) integrating GenAI into CMMI practice areas

**Potential RQ:**
> *How should software process quality metrics be redefined when a significant portion of code is AI-generated?*

**Papers to read:**
- [ ] arXiv:2603.28592 — *Debt Behind the AI Boom: AI-Generated Code in the Wild*
- [ ] arXiv:2510.10165 — *AI-Assisted Programming Decreases Productivity of Experienced Developers*
- [ ] CMMI + IBM AI WG press release (ISACA, April 2025)

---

### 🔭 Deep Dive — AI-Augmented SPI

**Status:** Active exploration · `#hot` · Last updated: 2026-05-29

---

#### 1.1 What is AI-Augmented SPI?

The classical SPI loop — **measure → analyse → improve → control** — is being reshaped by AI at every stage. AI agents continuously monitor telemetry, surface patterns, and propose (or apply) corrections. SPI becomes near-real-time rather than periodic.

| Traditional SPI | AI-Augmented SPI |
|---|---|
| Plan improvement | Continuous telemetry ingestion |
| Collect process data | ML anomaly detection (always-on) |
| Human analysis | LLM-generated root cause hypotheses |
| Implement change | Automated refactoring / pipeline tuning |
| Evaluate result | Predictive outcome modelling |

**Key tension:** AI-augmented SPI can move faster than human understanding — trading visible process debt for invisible cognitive debt.

---

#### 1.2 Three Lenses on AI-Augmented SPI

| Lens | Description | Examples |
|---|---|---|
| **AI as Tool** | Using AI to improve SE processes | Predictive analytics, auto-refactoring, LLM code review |
| **AI as Subject** | Improving processes that *involve* AI | CMMI for AI, DevSecOps for AI pipelines, AI testing |
| **AI as Risk** | Managing new failure modes from AI | Cognitive debt, intent debt, code duplication, skill erosion |

> Most research sits in **AI as Tool**. The **AI as Subject** and **AI as Risk** lenses are underexplored — strong thesis territory.

---

#### 1.3 Where AI Plugs Into the SPI Stack

| SPI Stage | Traditional Method | AI-Augmented Method | Tools / Research |
|---|---|---|---|
| **Requirements** | Reviews, inspections | NLP ambiguity detection, defect prediction | LLM-based RE analysis (PROFES 2024) |
| **Design** | Architecture reviews | Architectural smell detection, coupling graphs | ML static analysers, SonarQube ML |
| **Development** | Code reviews, pair programming | SATD detection, auto-refactoring | GitHub Copilot, Refact.ai, OpenRewrite |
| **Testing** | Manual test design | LLM test generation, flaky test prediction | EvoSuite, CodamosaAI |
| **Deployment** | Post-deploy monitoring | CI/CD anomaly detection, lead-time prediction | DevSecOps AI, DORA dashboards |
| **Retrospectives** | Facilitated sessions | Sentiment analysis, pattern mining from retro notes | GenAI facilitation tools |
| **Measurement** | Manual metric collection | Automated DORA/SPACE, AI code quality metrics | BLEU-diff, LEMOD (Sun et al. 2025) |

---

#### 1.4 The Measurement Gap — Core Problem

> *"You can't improve what you can't measure — and existing measures weren't built for AI."*

| Framework | What It Measures | Limitation with AI Code |
|---|---|---|
| **DORA** (2014) | Deployment frequency, lead time, MTTR, change failure rate | Measures delivery speed, not code understanding or authorship quality |
| **SPACE** (2021) | Satisfaction, Performance, Activity, Communication, Efficiency | Developer-centric; ignores AI agent contributions |
| **CMMI levels** | Process capability maturity (1–5) | Assumes human-authored artefacts; no AI-actor model |
| **SonarQube** | Code smells, bugs, vulnerabilities, duplication | Rule-based; misses semantic/intent issues in AI-generated code |

**The gap:** No existing framework can answer:
> *"How healthy is a process where 30% of code is AI-generated, and developers have partial understanding of it?"*

This is a strong candidate for an **original contribution**.

---

#### 1.5 Research Directions

**Direction A — AI-Aware Metric Suite** `#hot` `#thesis-candidate`
Design and validate a new metric layer — or extension of DORA/SPACE — capturing process quality in AI-augmented teams. Possible new metrics: AI authorship ratio, human comprehension coverage, intent documentation coverage, AI-introduced defect rate.
- *Method:* Design Science Research (DSR) — propose artefact, validate with Thai case studies
- *Contribution:* Framework + empirical validation

**Direction B — Process Model with AI as Actor** `#hot`
Propose a formal process model where AI agents have defined roles, responsibilities, and handoff protocols — similar to how DevOps formalised Dev/Ops collaboration.
- *Method:* Design Science + SLR, then model construction + expert validation
- *Contribution:* Novel process model

**Direction C — Empirical Study: AI-SPI Adoption in ASEAN** `#feasible`
Survey how software teams in Thailand / Southeast Asia use AI for process improvement. Compare against global benchmarks (PEX 2025, DORA State of DevOps).
- *Method:* Online survey + follow-up interviews (Thai companies, startups, government IT)
- *Contribution:* Empirical evidence base + adoption model
- *Fit for:* CIMPS 2026, EuroSPI 2026

**Direction D — Governance Framework for AI-Driven SPI Decisions**
When an AI tool autonomously applies a process change, how is that decision auditable and explainable? Connects to ISO/IEC 42001 (AI management systems).
- *Method:* Framework from ISO 42001 + CMMI AI WG + DevSecOps literature
- *Contribution:* Governance framework

---

#### 1.6 Key Concepts to Understand Deeply

| Concept | Why It Matters | Where to Start |
|---|---|---|
| **SATD** (Self-Admitted Technical Debt) | AI can introduce and detect SATD via code comments | Sun et al. 2025; arXiv:2306.10194 |
| **Cognitive Debt** | Team doesn't understand AI-generated code they own | arXiv:2603.22106 |
| **Intent Debt** | Team doesn't know *why* AI wrote code a certain way | arXiv:2603.22106 |
| **Design Science Research (DSR)** | Dominant PhD method for framework/artefact contributions | Hevner et al. (2004), MIS Quarterly |
| **Systematic Literature Review (SLR)** | Standard method for establishing what is known | Kitchenham (2004) guidelines |
| **DORA metrics** | Benchmark for software delivery performance | Forsgren et al. (2018) *Accelerate* |
| **SPACE framework** | Multi-dimensional developer productivity model | Forsgren et al. (2021), ACM Queue |
| **ISO/IEC 42001** | AI management systems standard — governance | ISO.org (2023) |
| **CMMI V3** | Latest maturity model, being extended for AI | CMMI Institute (2023) |

---

#### 1.7 Thesis Framing Options

**Option 1 (Recommended):**
*"An AI-Aware Process Quality Measurement Framework for Software Teams Using Generative AI in the SDLC"*
- Highest novelty — no existing framework covers this
- Achievable in 3–5 years with DSR + 2–3 case studies
- Publication path: SLR paper → framework paper → validation paper

**Option 2:**
*"A Process Model for AI-Augmented Software Development: Defining AI as a Process Actor"*
- Strong conceptual contribution
- Needs expert validation (Delphi study or interviews)
- Good fit: JSS or EMSE

**Option 3:**
*"AI-Driven SPI Adoption in Southeast Asian Software Organisations: An Empirical Investigation"*
- Lower technical risk, strong regional relevance
- Publishable quickly as survey papers
- Best fit: CIMPS, EuroSPI, regional SE journals

---

#### 1.8 Reading Roadmap

**Phase 1 — Foundation (Months 1–3)**
- [ ] Kitchenham (2004) — *SLR guidelines*
- [ ] Hevner et al. (2004) — *Design Science in IS Research* (MIS Quarterly)
- [ ] Humphrey (1989) — *Managing the Software Process*
- [ ] Forsgren et al. (2018) — *Accelerate* (DORA foundations)
- [ ] CMMI Institute (2023) — *CMMI V3.0 Model Overview*

**Phase 2 — AI in SE (Months 3–6)**
- [ ] arXiv:2603.28592 — *Debt Behind the AI Boom* (2025, empirical)
- [ ] arXiv:2510.10165 — *AI-Assisted Programming Decreases Productivity* (2025)
- [ ] arXiv:2603.22106 — *Cognitive and Intent Debt* (2025)
- [ ] arXiv:2306.10194 — *AI for Technical Debt Management* (SLR, 15 papers)
- [ ] Sun et al. (2025) — LLM-based SATD repayment + BLEU-diff / LEMOD metrics
- [ ] ISACA (April 2025) — *IBM joins CMMI AI Working Group*

**Phase 3 — Process Frameworks + Metrics (Months 6–9)**
- [ ] Forsgren et al. (2021) — *SPACE framework* (ACM Queue)
- [ ] ISO/IEC 42001:2023 — *AI Management Systems*
- [ ] Santos et al. (2025) — *Agile Transformation CSFs* (JSERD)
- [ ] ICSSP 2024 — *Breaking Old Habits: SPI Success Factors*
- [ ] EuroSPI 2024 proceedings (Munich)
- [ ] PROFES 2024 proceedings (Tartu)

**Phase 4 — SLR & Paper Writing (Months 9–18)**
- [ ] Conduct own SLR on AI-Augmented SPI (target: 50–80 papers)
- [ ] Draft SLR paper → submit to IST or EMSE
- [ ] Begin framework / model design

---

#### 1.9 Key Literature Questions

- How is "process improvement" defined when AI participates as a code-producing agent?
- What are the boundaries between "AI tool use" and "AI process actor" in current SE literature?
- Has anyone proposed AI-authorship-aware quality metrics? If so, what are the gaps?
- How do SPI frameworks handle non-human process participants?
- What governance mechanisms exist for AI-automated software decisions?
- How do Thai/ASEAN organisations compare to Western benchmarks on AI tool adoption?

---

#### 1.10 Connections to Other Topics

- **→ Topic 2** (Technical Debt): cognitive/intent debt is a *product* of AI-augmented development that SPI must manage
- **→ Topic 3** (Agile CSF): Agile + AI adoption success factors share common organisational prerequisites
- **→ Topic 4** (LSS + AI): DMAIC is a natural backbone for the AI-augmented improvement loop
- **→ Topic 5** (GSD): distributed teams + AI tools amplify both benefits and risks of AI-augmented SPI
- **→ Topic 6** (Org Learning): AI must be embedded in a *learning culture*, not just a monitoring one

---

#### 1.11 Target Journals & Conferences

| Venue | Type | Impact | Notes |
|---|---|---|---|
| **EMSE** | Journal | High (Springer) | Best fit for empirical/case study work |
| **JSS** | Journal | High (Elsevier) | Good for framework + validation papers |
| **IST** | Journal | Mid-High (Elsevier) | Good for SLR papers |
| **PROFES 2026** | Conference | A-tier SPI | Dec 2026 · check CFP |
| **EuroSPI 2026** | Conference | B-tier SPI | Sep 2026 · Springer CCIS |
| **CIMPS 2026** | Conference | B-tier SPI | Oct 2026 · CMC journal special issue |
| **ICSSP 2026** | Conference | A-tier Processes | ACM DL proceedings |
| **ICSE-SEIP 2026** | Conference | A*-tier SE | Highly competitive; industry track |

---

## Topic 2 — Technical Debt in the Age of GenAI

> *AI reduces traditional TD through refactoring, but accelerates new forms — cognitive and intent debt.*

- **Cognitive debt**: team doesn't understand code they own
- **Intent debt**: team doesn't remember *why* code was built that way
- 8× increase in duplicated code blocks since AI coding adoption (GitClear 2025)
- Paradox: automation cleans debt faster than humans understand it

**Potential RQ:**
> *What novel technical debt taxonomies emerge from AI-assisted development, and how can SPI frameworks detect and manage them?*

**Papers to read:**
- [ ] arXiv:2603.22106 — *From Technical Debt to Cognitive and Intent Debt*
- [ ] arXiv:2306.10194 — *AI for Technical Debt Management* (15-paper SLR)

---

## Topic 3 — Agile Transformation: Critical Success Factors

> *What truly makes or breaks an Agile transformation, and how do organisational factors interact?*

- CSFs: leadership support, culture change, coaching, tooling
- Failure clusters: forced adoption, lack of psychological safety, no retrospective culture
- Underexplored: Agile transformation in Thai/Southeast Asian organisational contexts

**Potential RQ:**
> *What are the critical success and failure factors for Agile transformation in [specific domain/region], and how do they differ from Western-centric findings?*

**Papers to read:**
- [ ] Santos et al. (2025) — *What Leads to the Success of Agile Transformation Initiatives?* DOI: 10.5753/jserd.2025.4502
- [ ] ICSSP 2024 — *Breaking Old Habits: Success Factors in SPI*

---

## Topic 4 — Lean Six Sigma + AI Integration

> *LSS + IoT + AI is creating "intelligent improvement systems" — what does this mean for software engineering?*

- DMAIC pipeline augmented with ML bottleneck prediction
- Real-time IoT sensor data feeding Six Sigma dashboards
- Agile + LSS fusion gaining traction (2025 research confirms convergence)
- 42.9% turnaround improvement in a 2024 LSS case study

**Potential RQ:**
> *How can an AI-enhanced DMAIC model be applied to software development pipelines for continuous, autonomous process correction?*

**Papers to read:**
- [ ] ResearchGate (2025) — *Integration of Agile Methodologies with Lean Six Sigma in SE Projects*
- [ ] PEX Report 2025/26

---

## Topic 5 — SPI in Global/Distributed Software Development

> *Human factors, cultural distance, and coordination overhead remain persistent bottlenecks in GSD.*

- Communication, trust, and time-zone gaps are top cited barriers
- SPI initiatives in GSD often fail due to "process theater" — frameworks adopted without adapting them
- Underexplored: GSD + AI-mediated collaboration tools

**Potential RQ:**
> *How do human and cultural factors moderate the effectiveness of SPI initiatives in globally distributed software teams?*

**Papers to read:**
- [ ] SAC '17 — *Hypothetical Framework of Human-Related Success Factors for PI in GSD*
- [ ] EuroSPI 2024 proceedings (Munich) — GSD tracks

---

## Topic 6 — SPI as Organisational Learning

> *Repositioning SPI from a "planned activity" to an active, reflective learning process.*

- Draws on Argyris & Schön double-loop learning theory
- Retrospectives as knowledge management — not just ceremony
- Gap: most SPI research treats improvement as a project, not a culture

**Potential RQ:**
> *How can organisational learning theory reframe SPI practices to foster self-sustaining improvement cultures in software teams?*

**Papers to read:**
- [ ] Academia.edu (2025) — *SPI as Organizational Learning: An Active Learning Perspective*

---

# 🎯 Qualifying Exam (2110897)

Must pass within **4 semesters** of starting. Written + oral exam.

**5 exam subjects (must pass 3 of 5):**
- Discrete Mathematics / Structure & Computability
- Algorithm and Data Structure
- Computer Architecture & Organization
- Operating Systems & System Programming
- Software Engineering I & II

**SE overlap with research:**
- Software Engineering II → directly maps to SPI, process models, quality assurance
- Algorithm topics → relevant to AI-based code analysis methods

---

# 📚 Comprehensive Exam (2110896 — SE Track)

| Course Code | Subject | Open/Closed? |
|---|---|---|
| 2110623 | Software Requirements Engineering | Open book |
| 2110634 | Software Design & Development | Closed book |
| 2110724 | Software Testing & QA | Closed book |
| 2110722 | Software Project Management | Open book |
| 2110503 | Software Development Practice | Open book |
| 2110646 | UI/UX Design | Closed book |
| 2110727 | Software Evolution & Maintenance | Open book |

---

# 🔗 Key Conferences to Target

| Conference | Focus | Next Edition |
|---|---|---|
| PROFES | Product-focused SPI | Dec 2025 · Salerno, Italy |
| EuroSPI | Systems/Software/Services PI | Sep 2025 · Riga, Latvia |
| CIMPS | Software Process Improvement | Oct 2025 · Lima, Peru |
| ICSE-SEIP | SE in Practice (industrial) | 2026 TBC |
| ICSSP | Software & Systems Processes | 2025 |

---

# 🅿️ Parking Lot

*Half-formed ideas — revisit later*

- Could a "process health score" be derived from Git activity + CI pipeline telemetry alone?
- Is there a relationship between CMMI maturity level and AI adoption readiness?
- How does Thai software industry compare to global SPI adoption benchmarks?
- Sustainability angle: can SPI reduce energy usage in CI/CD pipelines?

---

# 📅 Log

| Date | Entry |
|---|---|
| 2026-05-29 | File created. Initial topic scan from knowledge explorer session. |
| 2026-05-29 | Deep dive added: Topic 1 — AI-Augmented SPI (11 sections: 3-lens framework, SPI stack mapping, measurement gap, 4 research directions, thesis framing, reading roadmap, literature questions, topic connections, target journals). |
| 2026-05-29 | Goodnotes export version created — clean formatting, tables replacing ASCII diagrams. |

---

*Chulalongkorn University · PhD Computer Engineering · 2569–2571*
