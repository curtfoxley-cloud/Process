# Sixteen Barriers: Reliability, Maintainability, System Health and Human Factors

Requirements that stand between us and catastrophe, obligated through the SMS pathway regardless of contract flow-down.

Companion to the Sixteen Barriers CM assessment. Same logic, different discipline.

---

## 1. Recommended standard anchor

The CM case was clean because EIA-649-1 is a single, contractually invoked standard written in discrete "shall" statements, and its Annex A tailoring worksheet is the exact mechanism being misused. R&M has no single equivalent. Recommendation is a two-layer anchor.

### Layer 1: the invocation spine (what gets tailored away)

| Discipline | Anchor standard | Role |
|---|---|---|
| Reliability | ANSI/GEIA-STD-0009, Reliability Program Standard for Systems Design, Development, and Manufacturing | DoD-preferred successor to MIL-STD-785B. Objective-based, contractually invoked, routinely tailored by SOW and CDRL selection. |
| Maintainability | SAE JA1010 / JA1010-1, Maintainability Program Standard and Implementation Guide | Closest maintainability equivalent following cancellation of MIL-STD-470B and MIL-STD-471A. |

These two are the correct spine because they are the documents programs actually tailor. The rhetorical force of the CM argument came from "the contract silence was read as permission." That only works if the standard named is the one being silenced.

### Layer 2: the method standards carrying the discrete requirements

| Function | Standards |
|---|---|
| Failure mode and criticality analysis | SAE ARP5580; MIL-STD-1629A (legacy but still the referenced method) |
| Reliability test and growth | MIL-HDBK-189C; MIL-HDBK-781A |
| Maintainability design and human engineering | MIL-HDBK-470A; MIL-STD-1472H |
| Maintenance program derivation | SAE JA1011 and JA1012; MIL-STD-3034A; S4000P; ATA MSG-3 |
| Structural and engine life management | MIL-STD-1530D (ASIP); MIL-HDBK-1783B (ENSIP) |
| System health and PHM | SAE ARP6883, ARP6407, ARP6461, ARP5987, JA6268; FAA AC 29-2C MG-15; UK CAA CAP 753; DoDI 4151.22 (CBM+) |
| Human factors | MIL-STD-1472H; MIL-HDBK-46855A; DEF STAN 00-250; ICAO Doc 9824; EASA Part-145 human factors; MEDA; HFACS-ME |
| In-service data feedback | ASD/AIA S5000F; SAE GEIA-STD-0007 |
| Safety interface | SAE ARP4761A; SAE ARP4754B; MIL-STD-882E |

### Two honest caveats

**Clause numbers are not verified.** None of these standards are in the project. Every clause reference in the register below is a placeholder marked `[VERIFY]` until someone maps it against a controlled copy. The CM register survived review because its clause citations were verbatim. This one will not until that mapping is done.

**Human factors is the weak leg on the contract pathway.** MIL-STD-1472H is design criteria, not a program standard. MIL-HDBK-46855A is a handbook. Maintenance human factors lives largely in regulatory and advisory material rather than contractually invoked industry standards. This does not weaken the argument; it strengthens it. The contract pathway barely reaches human factors at all, which means the SMS pathway is the only pathway that obligates it. That is precisely the point the assessment is making.

---

## 2. The barrier test

Unchanged from the CM case. A requirement qualifies as a barrier when all three hold:

1. The hazard it addresses is one SM-0001 explicitly names in section 6.2.1, 6.2.3, 6.3 or 7.
2. Failure of the requirement directly enables that hazard to materialise without other healthy barriers in the path.
3. Documented historical events demonstrate the consequence of barrier failure at Severity 4 or 5.

SM-0001 section 6.2.1 names, verbatim, the hazard sources these barriers control: issues identified by analysis including FMECA and functional hazard analysis; component failure analysis; in-service failures, malfunctions and defects; deficiency reports; maintenance data; inaccurate, incomplete or ambiguous information in manufacturing or maintenance data; any work performed not in accordance with approved data; inadequate training, time, rest, experience; incomplete or unavailable maintenance or equipment data.

That list is not a paraphrase of the R&M discipline. It is the R&M discipline, written into the SMS standard the organisation has adopted.

---

## 3. The sixteen barriers

Severity convention follows the CM deck: 5 = Catastrophic, 4 = Severe. The org register convention inverts these (1 = Catastrophic, 2 = Severe); map on transfer.

### Cluster 1: Reliability engineering

| # | Barrier | Anchor | Primary event | Outcome | Sev |
|---|---|---|---|---|---|
| R1 | FMECA performed to a level that identifies catastrophic failure effects, with severity classification correct and not optimistically assigned | GEIA-STD-0009 Obj. 2 `[VERIFY]`; ARP5580 | Lion Air 610 / Ethiopian 302 (2018, 2019) | 346 fatalities | 5 |
| R2 | Single point failures with catastrophic effect identified and eliminated, or mitigated by a means not dependent solely on scheduled maintenance | GEIA-STD-0009 Obj. 2 `[VERIFY]`; ARP4761A | Alaska 261 (2000) | 88 fatalities | 5 |
| R3 | Common cause, zonal and particular risk analysis performed across paths assumed independent by design | ARP4761A; GEIA-STD-0009 Obj. 2 `[VERIFY]` | United 232, Sioux City (1989) | 112 fatalities | 5 |
| R4 | Reliability requirements derived from the actual mission and environmental profile; qualification representative of the real operating envelope; predictions validated against test or field data rather than handbook tables alone | GEIA-STD-0009 Obj. 1 and Obj. 3 `[VERIFY]`; MIL-HDBK-781A | Air France 447 (2009); Boeing 787 battery (2013) | 228 fatalities; fleet grounding | 5 |

**Focused example, R1.** The MCAS functional hazard assessment classified uncommanded activation below catastrophic and assumed crew diagnosis and response within a few seconds. The function had a single angle of attack input. Two hulls, 346 lives. The failure was not that FMECA was skipped. It was that the severity assigned to a failure effect was wrong, and nothing downstream re-tested it.

**Focused example, R4.** The Thales pitot probes on AF447 met the certification icing standard. They did not meet the high altitude ice crystal environment the aircraft actually flew in. A qualification standard that does not represent the operating envelope produces a reliability number that is precise and untrue.

### Cluster 2: Maintainability engineering

| # | Barrier | Anchor | Primary event | Outcome | Sev |
|---|---|---|---|---|---|
| M1 | Maintainability requirements derived and allocated; maintenance task analysis demonstrates every design-required task is feasible with defined access, tooling, skill and elapsed time | JA1010 `[VERIFY]`; MIL-HDBK-470A | F-35 and KC-46 sustainment shortfalls | Availability and program loss | 4 |
| M2 | Error tolerant design: incorrect installation prevented by design through keying, orientation, non-interchangeability and unambiguous marking | MIL-HDBK-470A; MIL-STD-1472H `[VERIFY]` | Air Midwest 5481 (2003); BA 5390 (1990) | 21 fatalities; near hull loss | 5 |
| M3 | Maintenance tasks and intervals derived by RCM logic and traceable to a specific failure mode and consequence; intervals changed only on reliability evidence | JA1011 / JA1012; MIL-STD-3034A; S4000P | Southwest 1380 (2018); Chalk's Ocean Airways 101 (2005) | 1 and 20 fatalities | 5 |
| M4 | Repairs, modifications and life extensions substantiated to the same standard as original design, including ageing and multiple site damage | MIL-STD-1530D; MIL-HDBK-1783B | Japan Airlines 123 (1985); Aloha 243 (1988) | 520 and 1 fatalities | 5 |

**Focused example, M3.** Alaska 261 is usually cited for the single point failure. The maintainability failure is separate and equally instructive: the jackscrew lubrication and end play check intervals were progressively extended without reliability evidence supporting the extension. The interval was a cost decision wearing the clothing of an engineering decision.

**Focused example, M4.** JAL123 remains the deadliest single aircraft accident on record. The aft pressure bulkhead repair after a 1978 tailstrike was performed incorrectly, halving the fatigue life of the splice. It then flew roughly 12,000 cycles. A repair is a design change to a life limited structure. If it is not substantiated as one, the aircraft's certified fatigue life is fiction from that day forward.

### Cluster 3: System health and prognostics

| # | Barrier | Anchor | Primary event | Outcome | Sev |
|---|---|---|---|---|---|
| S1 | Hidden and dormant failures identified in analysis and given either a detection means or a scheduled check with a justified exposure interval | ARP4761A; JA1011; ARP6883 `[VERIFY]` | United 585 (1991) and USAir 427 (1994), 737 rudder PCU | 25 and 132 fatalities | 5 |
| S2 | Health indications, debris findings and warnings dispositioned strictly per approved data, with no ad hoc engineering judgement substituting for the published procedure | CAP 753; AC 29-2C MG-15; DoDI 4151.22 | G-REDL, AS332 L2, North Sea (2009); CV-22 Yakushima (2023) | 16 and 8 fatalities | 5 |
| S3 | Detection coverage validated for the specific failure modes credited before monitoring is used to extend an interval, permit dispatch or replace an inspection | ARP6461; ARP5987; JA6268 `[VERIFY]` | LN-OJF, EC225LP, Turøy (2016) | 13 fatalities | 5 |
| S4 | Closed loop failure reporting, analysis and corrective action across the fleet, with a defined time limit from signal to design or maintenance action | GEIA-STD-0009 Obj. 4 `[VERIFY]`; S5000F | Cougar 91, S-92 (2009); KC-130T Yuma (2017) | 17 and 16 fatalities | 5 |

**Focused example, S2.** A metallic particle was found on the G-REDL epicyclic chip detector 36 flight hours before the gearbox failed. The indication was real, it was found, and it was dispositioned incorrectly. Detection without correct disposition is not a barrier. It is a record of a barrier that did not operate.

**Focused example, S3.** The Turøy investigation found the planet gear crack propagated in a manner the installed HUMS and chip detection could not detect. Credit had effectively been taken for a monitoring capability whose coverage of that failure mode had never been demonstrated. Taking maintenance credit for undemonstrated detection coverage is a Severity 5 risk acceptance, made silently.

**Focused example, S4.** The S-92 main gearbox filter bowl stud failure had a documented precursor in Australia the previous year. The rudder PCU pair is worse: United 585 in 1991 produced the data; USAir 427 in 1994 produced 132 more fatalities. The gap between the two is the measurable cost of a slow FRACAS loop.

### Cluster 4: Human factors

| # | Barrier | Anchor | Primary event | Outcome | Sev |
|---|---|---|---|---|---|
| H1 | Design assumptions about operator detection, diagnosis and response validated against human performance evidence, including annunciation, workload and time available | MIL-STD-1472H; ARP4754B; MIL-HDBK-46855A `[VERIFY]` | British Midland 92, Kegworth (1989) | 47 fatalities | 5 |
| H2 | Maintenance human factors addressed in task design and execution: shift handover, interruption, fatigue, supervision, procedure usability and access conditions | ICAO Doc 9824; EASA Part-145 HF; DEF STAN 00-250 | Continental Express 2574 (1991) | 14 fatalities | 5 |
| H3 | Human error treated as a failure mode within R&M and safety analysis rather than assumed away or handled solely by procedure and training | ARP4761A; MIL-STD-882E; MIL-HDBK-46855A `[VERIFY]` | Eastern 855, L-1011 chip detector O-rings (1983) | Near loss, 172 aboard | 5 |
| H4 | Maintenance and operational error data collected, classified and fed back into design and procedure change | MEDA; HFACS-ME; S5000F | Industry pattern across operators and platforms | Pattern | 4 |

**Focused example, H1.** The Kegworth crew shut down the working engine. The engine instrument display was new to the crew, the fan blade failure signature was ambiguous, and the CFM56-3C variant had not been flight tested at altitude. Every one of those is an R&M or human factors barrier, and the reliability analysis for the fan blade assumed a crew response the flight deck design did not support.

**Focused example, H3.** Eastern 855 lost oil in all three engines because chip detector O-rings were omitted during routine servicing by three different mechanics working from the same flawed local practice. No individual erred uniquely. The system produced the error. An analysis that treats human action as reliable by assumption cannot see that failure mode at all.

---

## 4. Cumulative weight of evidence

| Figure | Meaning |
|---|---|
| 16 | SMS barriers spanning reliability, maintainability, system health and human factors |
| 14 | barriers anchored in Severity 5 events |
| 1,600+ | documented fatalities across the cited events |
| 0 | credible alternatives that suspend these barriers without accepting Severity 4 to 5 risk |

The fatality total exceeds the CM case by roughly a factor of two. That is not rhetorical inflation. R&M barriers sit closer to the physical failure than CM barriers do, so their absence shows up in the accident record more directly.

---

## 5. Failure mode patterns across the sixteen

Three recur. They are not the same three as the CM case.

**A. Optimistic classification.** A failure effect, a severity, a probability or a detection coverage is assigned more favourably than the evidence supports, and nothing downstream re-tests the assignment. MCAS severity classification. 787 battery smoke release rate. Turøy detection coverage. Kegworth crew response assumption.

**B. Evidence-free interval change.** A task interval, inspection threshold or life limit is changed for cost or schedule reasons and documented as an engineering decision. Alaska 261 end play checks. Southwest 1380 fan blade inspection. Chalk's 101 wing inspection programme.

**C. Slow or broken feedback loop.** The fleet produces the signal and the organisation does not convert it into action before the second event. United 585 to USAir 427. S-92 Australia stud failure to Cougar 91. CV-22 prior gearbox indications to Yakushima. AF447 pitot events preceding the accident.

Nimrod XV230 exhibits all three at once, which is why the Haddon-Cave report is the single most useful reference for a defence audience reading this assessment.

---

## 6. The ask

Identical in structure to the CM ask, and it should be, because the argument is the same argument.

1. **Establish SMS policy.** State that the R&M, system health and human factors requirements underlying the sixteen barriers, or documented equivalent controls, shall be performed on all safety significant products regardless of contract flow-down.

2. **Route exceptions correctly.** Where a programme believes a barrier requirement is not warranted, route the determination through the SMS risk acceptance process, not the R&M tailoring process. Output is a signed risk acceptance memo at the Severity 4 to 5 authority level.

3. **Document equivalent controls.** Where a barrier is satisfied by an alternative process, document which alternative satisfies which SM-0001 hazard, with what evidence.

---

## 7. Anticipated objections

**"Reliability is a performance requirement, not a safety requirement."** It is both, and the split is the problem. Alaska 261, Turøy and Cougar 91 were all reliability failures with catastrophic outcomes. The discipline that owns the failure mode owns the barrier, whichever column the requirement sits in on the contract.

**"MIL-HDBK-217 predictions are discredited, so reliability prediction is not a real control."** Correct about 217 and irrelevant to the barrier. R4 does not require a handbook prediction. It requires that whatever number is claimed be validated against test or field evidence. The 787 battery case is the argument for the barrier, not against it.

**"Human factors is not our discipline."** Then name the discipline that owns Continental Express 2574 and Eastern 855. If no discipline owns it, that is the finding.

**"System health monitoring is not mature enough to be a barrier."** S3 is the response. Where monitoring is immature, do not take credit for it. The barrier is violated by taking undemonstrated credit, not by having immature technology.

**"We have never had an event because we omitted this."** Survivorship bias. Every cited case is an organisation that made the same judgement and outlived it for a while.

---

## 8. What is needed to finish this

1. Controlled copies of GEIA-STD-0009 and JA1010 to convert the `[VERIFY]` placeholders into clause level citations.
2. Confirmation of which method standards the organisation actually invokes, so the Layer 2 column reflects reality rather than the full available set.
3. A decision on whether the floor register is one register spanning four disciplines or four registers with a common severity scheme. Recommendation is one register, because the CM coverage metric already exists and a second metric of the same shape is easier to defend than four.
