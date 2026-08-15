# R&M Barrier Register v4

Reliability, maintainability, system health and human factors requirements obligated through the SMS pathway regardless of contract flow-down.

**Source standards.** GEIA-STD-0009A (SAE, 2008-08, revised 2020-05). SAE JA1011. SAE JA1010. MIL-STD-1530D w/Change 1 (13 Oct 2016). MIL-STD-882E w/Change 1 (27 Sep 2023). MIL-STD-1472H (15 Sep 2020). SM-0001 Issue C (2025).

Requirement text is paraphrased. The governing text is the standard.

**Severity convention.** 5 = Catastrophic, 4 = Severe, matching the CM deck. Note that MIL-STD-882E Table I runs the other way, 1 = Catastrophic, which matches the org register convention. Map carefully on transfer; the two scales are inverted relative to each other.

**Risk acceptance authority.** Unchanged from the CM case. Severity 4 to 5 acceptance sits with the Accountable Executive or delegate.

**Structural change from v3.** The register is now organised by function rather than by source standard, because six standards overlap and a barrier carrying three independent clause anchors across three standards is materially harder to argue away than the same content split into three single-anchored rows.

---

## 1. The argument is already written into MIL-STD-882E

Three clauses carry the case, and they should open the deck.

**4.1, 4.1.1, 4.1.2.** When the standard is invoked, Sections 3 and 4 apply. Tasks in Section 5 may be cited to *add* requirements. The definitions in 3.2 and all of Section 4 are the minimum mandatory requirements for an acceptable system safety effort for any DoD system. Tailoring under 882E can only add. It cannot subtract from the floor. That is the floor concept the CM case had to argue for, stated as a requirement in a DoD standard.

**4.2.2, 4.2.2.1, 4.2.2.2.** System safety personnel are not responsible for hazard management in other systems engineering functional disciplines. Each discipline is responsible for its own risk management and for obtaining its own risk acceptance from the appropriate risk acceptance authority. This answers the most common review deflection, which is that safety owns it. R&M owns its own hazard risk and must route its own acceptance.

**4.3.2.** Hazard identification shall consider the entire life cycle and shall use mishap data, user knowledge and skills, and lessons learned from legacy and similar systems. The barrier method used in this assessment is not an initiative. It is an obligation.

Two supporting clauses are worth their own slides. **4.3.4** sets a mitigation order of precedence running from hazard elimination down to signage, procedures, training and PPE, and states that the last tier should not be the only risk reduction for catastrophic or critical severity. **4.3.3.b** states that no amount of doctrine, training, warning, caution or PPE can move a mishap probability to eliminated.

## 2. Anchor verdict

| Document | Usable | Role |
|---|---|---|
| MIL-STD-882E w/Ch 1 | Yes | Governance, risk classification, acceptance routing, hazard analysis tasks |
| MIL-STD-1530D w/Ch 1 | Yes | Structural integrity, life management, inspection derivation, SHM credit |
| GEIA-STD-0009A | Yes | Reliability program across four life-cycle objectives |
| MIL-STD-1472H | Yes | Human engineering and design-for-maintainability criteria |
| JA1011 | Yes | Maintenance task and interval derivation |
| JA1010 | Marginal | Maintainability program framing only |
| ARP4761A | No | 2 obligations outside Appendix Q worked example, one boilerplate |
| ARP6883 | No | Landing gear case study requirement text |
| ARP6461A, ARP6407, JA6268, ARP5580, TA-HB-0009A | No | Guidance |

**What every usable standard says about its own tailoring.** 882E 4.1.1 permits tasks to be added only. 1530D 6.1 permits tailored contractual requirements, then 5.1.1 requires exceptions and their rationale including risk assessments to be documented in the ASIP Master Plan, which 4.1.b requires the PEO to approve before SRR. 0009A 1.3 permits tailoring and 4.5.1.1 requires all normative activities across all four objectives to be considered when preparing the Reliability Program Plan. JA1010 1.3 permits tailoring. None of the five permits silent omission. In every case tailoring is a documented, risk-assessed, approved act.

**Scope note.** 1530D binds through AFPD 63-1, AFI 63-101 and AFI 63-140 for USAF aircraft structure. 882E binds through the DoDI 5000 series. On products outside those pathways the physics is unchanged and the obligation disappears. That is the clearest single illustration of why the SMS pathway matters.

---

## 3. Barrier test

A requirement is a barrier when all three hold:

1. The hazard it addresses is one SM-0001 explicitly names in section 6.2.1, 6.2.3, 6.3 or 7.
2. Failure of the requirement directly enables that hazard without other healthy barriers in the path.
3. Documented historical events, or a documented industry pattern, demonstrate the consequence at Severity 4 or 5.

Candidates merge into one barrier where a program could not plausibly perform one while omitting the other, or where they cannot be independently audited apart. The count follows from applying that rule across six standards.

---

## 4. Cluster 1: Hazard and failure mode identification

| # | Barrier | Anchors | Event | Outcome | Sev |
|---|---|---|---|---|---|
| 01 | Characterise the user and environmental life-cycle loads the product will actually encounter, update, verify against measurement | 0009A 4.5.1.4, 5.5.1.4, 6.5.1.4, 7.5.1.4; 1530D 5.1.2, 5.2.3 | Air France 447 (2009) | 228 fatalities | 5 |
| 02 | Flow load estimates to component teams and to teams selecting COTS, NDI and CFI, reissue when updated | 0009A 4.5.1.5, 5.5.1.5, 6.5.1.5 | Boeing 787 battery (2013) | Fleet grounding | 5 |
| 03 | Identify failure modes and mechanisms from development start, confirmed by analysis or test, continuing after fielding | 0009A 5.5.1.6, 6.5.1.6, 7.5.1.6; 882E 4.3.2; JA1011 5.3.1, 5.3.4 | Lion Air 610 / Ethiopian 302 | 346 fatalities | 5 |
| 04 | Use mishap data and lessons learned from legacy and similar systems in hazard identification | 882E 4.3.2 | Cougar 91 precursor (2008); United 585 into USAir 427 | 17 and 157 fatalities | 5 |
| 05 | Analyse interfaces and faults of subsystems acting independently or in combination | 882E Task 205, Task 209 | United 232, Sioux City (1989) | 112 fatalities | 5 |
| 06 | Operating and support hazard analysis covering maintenance, servicing and support tasks | 882E Task 206 | Continental Express 2574 (1991); Eastern 855 (1983) | 14 fatalities; near loss | 5 |
| 07 | Treat human error as a failure mode for operators and maintainers, identified and mitigated rather than assumed away | 0009A 4.5.1.8, 7.5.1.10; 882E 4.3.2, 4.3.8, Task 206 | Air Midwest 5481 (2003); BA 5390 (1990) | 21 fatalities; near loss | 5 |
| 08 | Separate hidden from evident failure modes, assessing dormancy and multiple-failure exposure | JA1011 5.5.1.1, 5.5.1.2 | 737 rudder PCU, UA585 and US427 | 157 fatalities | 5 |

## 5. Cluster 2: Risk assessment and classification

| # | Barrier | Anchors | Event | Outcome | Sev |
|---|---|---|---|---|---|
| 09 | Assess severity and probability against the defined criteria, with tailored alternatives only where formally approved | 882E 4.3.3, Tables I to III | Lion Air 610 / Ethiopian 302 | 346 fatalities | 5 |
| 10 | Take no credit for doctrine, training, warning, caution or PPE in eliminating a hazard | 882E 4.3.3.b | Alaska 261 (2000) | 88 fatalities | 5 |
| 11 | Substantiate quantitative targets and document every numerical probability definition used | 882E 4.3.3.e; 1530D 5.1.3.1, 5.2.14, 5.5.6; 0009A 5.5.1.8 | Boeing 787 battery (2013) | Fleet grounding | 5 |
| 12 | Assess software contribution by control category and severity, assigning level-of-rigour tasks | 882E 4.4, Tables IV to VI | Software-caused mishap pattern | Pattern | 5 |
| 13 | Assess reliability feasibility in the user environment and communicate infeasibility to the customer | 0009A 4.5.1.6, 4.3 | KC-46 and F-35 sustainment | Program loss | 4 |

## 6. Cluster 3: Mitigation and design

| # | Barrier | Anchors | Event | Outcome | Sev |
|---|---|---|---|---|---|
| 14 | Select mitigation by the design order of precedence, with procedures, training and PPE never the sole mitigation for catastrophic or critical severity | 882E 4.3.4; 0009A 5.5.1.7, 7.5.1.7 | Alaska 261 (2000) | 88 fatalities | 5 |
| 15 | Assign slow damage growth to single-load-path and non-fail-safe designs; safe-life only by approval with damage tolerance evaluation | 1530D 5.1.3.5.1, 5.1.3.5.2 | Alaska 261 (2000) | 88 fatalities | 5 |
| 16 | Classify critical parts and processes, serialise and trace fracture-critical-traceable items, update the list as the design matures | 1530D 5.1.4.2 | F-15C breakup (2007); United 232 (1989) | Fleet grounded; 112 fatalities | 5 |
| 17 | Design connectors and fasteners to preclude mismating: keying, distinguishable location, no identical fasteners where wrong removal causes damage | 1472H 5.9.14.1, 5.9.14.3, 5.9.14.5, 5.9.11.1.1, 5.9.11.1.2 | BA 5390 (1990) | Near loss | 5 |
| 18 | Design in fault detection and isolation, with automatic detection where possible and identifiable status evidence at LRU level | 1472H 5.9.15.3, 5.9.15.4, 5.9.15.5 | Latent-failure pattern | Pattern | 5 |
| 19 | Provide indication when an item is out of tolerance or has failed, with visual and auditory alarm for malfunctions that could cause injury or damage | 1472H 5.9.16.1.2, 5.9.16.1.3, 5.9.16.1.5 | Alaska 261 (2000) | 88 fatalities | 5 |
| 20 | Design warning, alerting and audio signals to support the operator response the safety assessment assumes | 1472H 5.3.3, 5.7.2, 5.7.3 | British Midland 92, Kegworth (1989) | 47 fatalities | 5 |
| 21 | Size and locate access, covers and openings for the required maintenance task; use standard parts and modular replacement | 1472H 5.9.6, 5.9.7, 5.9.1.4, 5.9.1.5; JA1010 4.2 | Alaska 261 (2000) | 88 fatalities | 5 |
| 22 | Make labelling and marking legible, correctly located, unambiguous and visible during maintenance | 1472H 5.4, 5.9.14.4 | SM-0001 6.2.1 ambiguous data | Pattern | 5 |
| 23 | Establish corrosion prevention and control, with susceptibility evaluation and periodic reassessment | 1530D 5.1.5, 5.1.5.2, 5.2.7, 5.5.7; 1472H 5.9.1.3 | KC-130T Yuma (2017) | 16 fatalities | 5 |

## 7. Cluster 4: Verification and test

| # | Barrier | Anchors | Event | Outcome | Sev |
|---|---|---|---|---|---|
| 24 | Conduct reliability verification that is operationally realistic and based on the life-cycle loads | 0009A 4.5.1.7, 5.5.1.9, 6.5.1.9 | Kegworth (1989); Cougar 91 (2009) | 47 and 17 fatalities | 5 |
| 25 | Verify implementation and validate effectiveness of every selected mitigation | 882E 4.3.6 | Boeing 787 battery (2013) | Fleet grounding | 5 |
| 26 | Validate analysis methods, models and procedures, and verify software implementation, before reliance | 1530D 5.2 | Pattern | Pattern | 5 |
| 27 | Test durability to two lifetimes with production gates, on an article representative of operational configuration and manufacturing processes | 1530D 5.3.4, 5.3.4.1, 5.3.4.2 | Pattern | Pattern | 5 |
| 28 | Conduct teardown with fractographic examination, deriving the initial-quality distribution from discovered damage | 1530D 5.3.4.5 | Pattern | Pattern | 4 |
| 29 | Analyse every test finding to root cause, revise analyses until correlation is achieved, set operational limits before corrective action | 1530D 5.3.7, 5.3.8; 0009A 5.5.1.2 | Pattern | Pattern | 5 |
| 30 | Identify manufacturing variation and workmanship failure modes; analyse production test and screening failures to root cause | 0009A 6.5.1.6, 6.5.1.7 | Qantas 32 (2010); F-15C (2007) | Hull threatened; fleet grounded | 5 |
| 31 | Establish and demonstrate NDI capability, with special emphasis on fracture critical parts | 1530D 5.1.6, 5.5.5 | United 232, missed indication at overhaul | 112 fatalities | 5 |

## 8. Cluster 5: Maintenance program derivation

| # | Barrier | Anchors | Event | Outcome | Sev |
|---|---|---|---|---|---|
| 32 | Define and record operational context and performance standards for the derivation | JA1011 5.1.1, 5.1.4 | Pattern | Pattern | 4 |
| 33 | Carry out consequence assessment and policy selection as if no task is currently being done | JA1011 5.5.2, 5.6.4 | Alaska 261 (2000) | 88 fatalities | 5 |
| 34 | Ensure safety-consequence tasks reduce probability to an acceptable level | JA1011 5.7.1.1, 5.7.1.2 | Pattern | Pattern | 5 |
| 35 | Require on-condition tasks to have a defined potential failure condition, identifiable P-F interval, task interval shorter than the shortest likely P-F interval, physical feasibility and adequate warning time | JA1011 5.7.2.1 to 5.7.2.5 | Southwest 1380 (2018); G-REDL (2009) | 1 and 16 fatalities | 5 |
| 36 | Require discard and restoration tasks to have a demonstrable age of increasing conditional probability, with restoration returning resistance to an acceptable level | JA1011 5.7.3.1, 5.7.4.1 to 5.7.4.3 | Chalk's Ocean Airways 101 (2005) | 20 fatalities | 5 |
| 37 | Set failure-finding intervals against multiple-failure probability, confirming all covered components are functional | JA1011 5.7.5.1, 5.7.5.2, 5.7.5.4 | LN-OJF, Turøy (2016) | 13 fatalities | 5 |
| 38 | Permit run-to-failure only where there is no safety or environmental consequence, or the probability is acceptable without a task | JA1011 5.8.2.1, 5.8.2.2 | Pattern | Pattern | 5 |
| 39 | Derive structural inspection intervals from probability of detection and test data, against the defined fractional-life thresholds | 1530D 5.2.6, 5.4.3.1.1 | Southwest 1380 (2018) | 1 fatality | 5 |
| 40 | Maintain a force structural maintenance plan defining when, where and how, covering damage tolerance, durability and corrosion critical locations | 1530D 5.4.3, 5.5.9 | Chalk's Ocean Airways 101 (2005) | 20 fatalities | 5 |
| 41 | Select inspection methods accounting for accessibility and human factors alongside detection capability | 1530D 5.4.3.1.2; 1472H 5.9.6 | Continental Express 2574 (1991) | 14 fatalities | 5 |
| 42 | Review both the supporting information and the decisions periodically, with interval formulae logically supportable | JA1011 5.10.2, 5.11.1 | Alaska 261 interval escalation | 88 fatalities | 5 |

## 9. Cluster 6: In-service monitoring and closed-loop action

| # | Barrier | Anchors | Event | Outcome | Sev |
|---|---|---|---|---|---|
| 43 | Determine health-monitoring detection capability and intervals from sensor and system-level POD, with the POD methods approved before installation | 1530D 5.4.3.2 | LN-OJF, Turøy (2016) | 13 fatalities | 5 |
| 44 | Track individual item usage to defined data capture rates, adjusting intervals by actual measured usage, with impending-failure warning for rotorcraft dynamic components | 1530D 5.4.5, 5.5.2, 5.5.4 | CV-22 Yakushima (2023); G-REDL (2009) | 8 and 16 fatalities | 5 |
| 45 | Execute a usage spectra survey to confirm or update the design spectrum, evaluating usage severity annually | 1530D 5.4.4, 5.5.1 | Pattern | Pattern | 5 |
| 46 | Analyse field failures to root cause, mode and mechanism; compare predicted against actual and update the analyses | 0009A 7.5.1.6; 1530D 5.5.3 | Cougar 91, S-92 (2009) | 17 fatalities | 5 |
| 47 | Resolve field failure modes in a timely manner through an integrated team, with methods accessible to the customer | 0009A 7.5.1.7 | United 585 into USAir 427; CV-22 (2023) | 157 and 8 fatalities | 5 |
| 48 | Update reliability assessments from field experience, track corrective action effectiveness, apply growth methodology to new field failure modes | 0009A 7.5.1.8, 5.5.1.8 | Air France 447 pitot events preceding the accident | 228 fatalities | 5 |
| 49 | Maintain a closed-loop hazard tracking system with the defined minimum data elements, accessible to both parties | 882E 4.3.1.d, Task 106 | Nimrod XV230 (2006) | 14 fatalities | 5 |
| 50 | Apply field outputs so the inherent reliability of the fielded design is not degraded by maintenance action or process | 0009A 7.4.2 | Alaska 261 (2000); American 191 (1979) | 88 and 273 fatalities | 5 |
| 51 | Record damage and maintenance findings in a force management database and use them to test the accuracy of the predictions | 1530D 5.4.6, 5.5.12 | KC-130T Yuma (2017) | 16 fatalities | 5 |
| 52 | Substantiate repairs, reworks and modifications by revised analysis, with static ultimate load test where load paths are altered | 1530D 5.2.4, 5.3.1, 5.5.11 | Japan Airlines 123 (1985) | 520 fatalities | 5 |
| 53 | Wire life-cycle risk management into the configuration control process, and support mishap investigation with recommendations that minimise human error | 882E 4.3.8, Task 304 | Pattern | Pattern | 5 |

## 10. Cluster 7: Governance, tailoring and risk acceptance

| # | Barrier | Anchors | Event | Outcome | Sev |
|---|---|---|---|---|---|
| 54 | Apply the minimum mandatory system safety requirements whenever the standard is invoked; tasks may be cited only to add | 882E 4.1, 4.1.1, 4.1.2 | Framing | Framing | 5 |
| 55 | Hold each engineering functional discipline responsible for its own hazard risk management and for obtaining its own risk acceptance from the appropriate authority | 882E 4.2.2, 4.2.2.1, 4.2.2.2 | Framing | Framing | 5 |
| 56 | Coordinate across disciplines because a mitigation optimised for one may create hazards in another | 882E 4.2.3 | Pattern | Pattern | 4 |
| 57 | Accept risk at the appropriate authority before exposure, with user representative concurrence for the higher levels, and re-accept when field data raises the assessed risk | 882E 4.3.7, 4.3.1.c; 1530D 5.5.6 | Air France 447 (2009); CV-22 (2023) | 228 and 8 fatalities | 5 |
| 58 | Document exceptions to the standard with rationale and risk assessment in the program plan, approved at the defined authority before the design review gate | 1530D 5.1.1, 4.1.a, 4.1.b, 4.1.e, 4.2; 0009A 4.5.1.1; JA1010 1.3 | Aloha 243 (1988); Nimrod XV230 (2006) | 1 and 14 fatalities | 5 |
| 59 | Escalate unresolved discipline issues to the named technical authority rather than absorbing them at team level | 1530D 5.1.4, 5.1.5, 5.1.6, 5.1.7; 0009A 5.5.1.7 | Nimrod XV230 (2006); Columbia (2003) | 14 and 7 fatalities | 5 |
| 60 | Maintain continuity of resources, skills, documented roles and accountability across life-cycle phases | 0009A 4.3, 5.3, 6.3, 7.3; JA1010 4.1, 4.3 | Nimrod XV230 (2006) | 14 fatalities | 4 |

---

## 11. Count and weight

| Figure | Meaning |
|---|---|
| 60 | clause-anchored barriers |
| 36 | with a specific documented event anchor rather than a pattern or framing |
| 54 | rated Severity 5 |
| 23 | anchored in two or more independent standards |
| 1,900+ | documented fatalities across the cited events |
| 6 | of fourteen supplied standards capable of anchoring any of it |

The multi-anchor figure matters more than the total. A barrier obligated independently by the system safety standard, the reliability standard and the structural integrity standard cannot be dismissed as one discipline's preference.

---

## 12. Failure mode patterns

**A. Optimistic classification.** A severity, probability, load estimate, design concept or detection coverage is assigned more favourably than the evidence supports and nothing downstream re-tests it. Barriers 01, 03, 08, 09, 11, 15, 43.

**B. Evidence-free interval.** A task, inspection interval or life limit is set or changed without the substantiation the clause requires. Barriers 33, 35, 36, 39, 42, 44, 45.

**C. Slow loop.** The fleet produces the signal and the organisation does not convert it into action before the second event. Barriers 04, 46, 47, 48, 49, 51.

**D. Bottom-tier mitigation.** A catastrophic or critical hazard is controlled solely by a procedure, a task, training or a warning, when the order of precedence requires elimination or design change to be attempted first. Barriers 10, 14, 15, 19.

**E. Undocumented exception.** A required activity is omitted without the rationale, risk assessment and approval the standard itself demands, and the acceptance never reaches the authority that owns that severity. Barriers 54, 55, 57, 58, 59.

Patterns D and E are the two that map most directly onto the organisational dispute rather than onto engineering error, and both are now anchored in explicit clause text rather than argued by analogy. Pattern E is the CM argument. Pattern D is new and is arguably the more powerful of the two, because 882E 4.3.4 states in its own words that a maintenance procedure is the weakest available control and should not stand alone against a catastrophic hazard.

---

## 13. Remaining gaps

Nothing in the current set obligates:

1. **Zonal and particular risk analysis as discrete named activities.** 882E Task 205 covers interfaces and combination faults, which carries the substance, but the zonal and particular-risk framing familiar from civil practice has no home. ARP4761A cannot supply it.
2. **Quantitative testability coverage metrics.** 1472H 5.9.15 obligates fault detection and isolation as a design property but sets no coverage, ambiguity-group or false-alarm-rate requirement. MIL-STD-2165 was the historical source and is cancelled.
3. **Maintainer fatigue and duty limitation.** No supplied standard addresses it. This sits in regulatory rather than industry-standard space.

These are stated rather than papered over. The register stands without them.
