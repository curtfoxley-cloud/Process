# Physical Configuration Audit — core check set

The core checks the Physical Configuration Audit (PCA) team must perform for every Configuration Item (CI) designated for the PCA.

---

**1. Physical Item to Product Definition Data Inspection**

- **Check:** Physical Item and Product Definition Data Revision Alignment
- **Explanation:** Verify that the CI matches the exact revision level (not just the base part number) of its Product Definition Data (PDD).

**2. Serialization & Traceability Verification**

- **Check:** Part Traceability Numbers on the Physical Item against Part Traceability Requirements and the Trace Numbers on the As-Built records
- **Explanation:** Compare the actual physical serial numbers, batch/lot numbers, and heat numbers on the Physical Item against the part traceability requirements and the numbers listed on the As-Built records.
- **Identifier integrity:** Trace numbers are never re-used and never revised. A serial, lot or batch identifier that has been re-issued against a second article destroys the traceability of both, and no downstream record can distinguish them afterwards.
- **Life limits:** For every life-limited item installed in the CI, verify the life-limited designation, the assigned life limit, and the **life consumed at delivery**. For shelf-life materials — adhesives, sealants, potting compounds — verify cure or expiry evidence in the build records. A life-limited part delivered with no consumed-life record cannot be scheduled for removal at any point in its service life, and the omission is unrecoverable after delivery.

**3. As-Designed Child Items vs. As-Built Child Items BOM Reconciliation Verification**

- **Check:** Verify that all the CI's child items listed on the As-Designed dataset are listed in the applicable completed/closed As-Built records (including work orders and non-conformance records)
- **Explanation:** Verify that all physically "invisible" or minor child hardware of the CI, such as shims, washers, O-rings, potting compounds, adhesives, and thread-locker, listed on the Engineering Bill of Materials (EBOM) are accounted for in the physical build records.

**4. Open Engineering Change Commitments Check**

- **Check:** Engineering Change Commitments Incorporation for the CI
- **Explanation:** Physically verify that all approved Change Commitments applicable to the CI for the applicable milestone and effectivity, and temporary redlines or Flight Changes, have been correctly incorporated into the physical unit.

**5. Non-Conformance Records and Variance Verification**

- **Check:** Non-Conformance Records (NCRs) and Variances
- **Explanation:** Confirm that any physical non-conformance on the unit has been adjudicated by the appropriate authority based on its classification, that non-conformances that trip Variance gates have been adjudicated by the appropriate Variance authority based on its classification, and that no unresolved NCRs remain open against the CI.

**6. Interface & Workmanship Physical Inspection**

- **Check:** Form, Fit, Interface, and Assembly Quality of the CI
- **Explanation:** Inspect physical dimensions, critical interfaces, connector pinouts, wire harness routing, ground strap bonding, surface finishes, thermal coatings, and torque stripe applications against engineering specs.

**7. Nameplate & Marking Audit**

- **Check:** Nameplate, Marking, and Tagging Integrity
- **Explanation:** Verify that part markings, serial number plates, danger/warning labels, and UID barcodes are accurate, legible, permanently affixed, and correctly located according to PDD instructions.

**8. Embedded Software & Firmware Checksum Audit**

- **Check:** Software/Firmware Load & Version Verification
- **Explanation:** For CIs containing programmable logic (FPGAs, EEPROMs, microcontrollers), verify that the installed software build version, part number, and cryptographic checksum match the software drawing baseline.

**9. Manufacturing Documentation & Quality Buy-Off Audit**

- **Check:** Build Traveler and Quality Stamp Audit
- **Explanation:** Audit the shop traveler, inspection logs, and test records to ensure every required operation, torque measurement, and mandatory quality inspection point has a valid quality stamp or sign-off.

**10. FCA Unit to PCA Unit Difference Verification**

- **Check:** Differences between the CI being audited and the unit(s) used for the Functional Configuration Audit
- **Explanation:** Identify every difference between the PCA unit and the unit or units used for functional verification, and confirm the certification that those differences do not degrade functional characteristics. Identification alone is not sufficient — the certification is the deliverable. "Both were built to the same PDD" is not an answer: tooling, process, source and workmanship differ between preproduction and production builds even where the design data does not.

**11. Manufacturing Instruction to Product Definition Data Verification**

- **Check:** Sampled PDD against the manufacturing and work instructions actually used to build the CI
- **Explanation:** Compare the sampled PDD against the manufacturing instructions, work instructions and installation procedures used to build the CI, confirming that the instructions reflect the design detail at the governing revision and incorporate the authorised changes. Check 9 confirms the traveler was followed. This check confirms the traveler was right — a fully stamped traveler built to a superseded revision passes check 9 and fails the audit.

**12. Zone Foreign Object Debris Check (conditional)**

- **Check:** Foreign Object Debris in the zone or area in which the CI is embodied
- **Explanation:** Applicable only where the CI is embodied at the time of the PCA. Inspect the zone or area in which the CI is installed for foreign object debris — tools, loose hardware, swarf, consumables, rags, packaging — and confirm that the closeout inspection records for that zone are complete. Where the CI is not embodied at the time of the audit, the check is recorded as not applicable rather than omitted.

**13. Part Approval, Clearance, and Qualification Records Verification**

- **Check:** Approval, clearance and qualification status of the part types installed in the CI
- **Explanation:** Verify that every part type installed in the CI is approved and cleared for use, and that its qualification records support that use. This is distinct from check 1: check 1 asks whether the installed part is the part the PDD calls out, while this check asks whether that part type is permitted at all. Two paths defeat check 1 and are caught only here — a bench substitution of a functionally similar part under shortage pressure, which survives check 1 outright where the PDD carries an "or equivalent" note; and a part de-listed after the PDD was released, through obsolescence, source disqualification or counterfeit alert, where a correct PDD calls out a part that is no longer approved today. Release control is a point-in-time control and both failures occur after it.

**14. Part Certification Status and Plan Status Verification**

- **Check:** Certification status of the CI and its parts, and the status of the applicable certification plan items
- **Explanation:** Verify the certification and qualification status of the CI and its constituent parts, and the status of the certification plan items applicable to the CI at this milestone: which are complete and closed, which remain open, and whether any certification credit depends on a configuration other than the one being audited. An open certification plan item is not necessarily a finding at this milestone; an open item that nobody can identify, or a certification credit resting on a superseded configuration, is.

**15. Material and Process Conformance Verification**

- **Check:** Material specifications and special process requirements in the PDD against the material notes and process records on the As-Built records
- **Explanation:** Verify the material chain in three links, not two: the material specification called out in the PDD, against the material note recorded on the As-Built records, against the **material certification for the heat or lot number** identified in check 2. The two-link version catches a build record that disagrees with the design; only the third link catches a build record that faithfully records what was ordered when what was delivered differed. Apply the same chain to special processes — heat treat, plating, coating, non-destructive inspection — where the process certification stands in place of the material certificate. Where the PDD permits a substitute or equivalent material, verify that the substitution was approved rather than selected at the bench.
- **Limit of the check:** a PCA cannot verify material by inspection. It verifies the evidence chain, and its findings are breaks in that chain, not conclusions about the material itself.
- **Anchor:** Air France 4590. A replacement thrust-reverser wear strip was made of titanium alloy rather than the specified stainless steel. The as-installed configuration no longer matched approved design, and no downstream party could detect a discrepancy from the records. 113 fatalities.

**16. Next Higher Assembly Traceability Verification**

- **Check:** Traceability of the CI upward to its next higher assembly
- **Explanation:** Verify that the CI's traceability records resolve upward to the next higher assembly, so that the fleet-wide question — where else did articles from this lot or heat go — is answerable after an escape. Check 2 traces inward to the article; this traces outward from it.
- **Conceptual collectors:** where the next higher item in the PDD is a conceptual collector with no physical next higher assembly, the check records that fact and its rationale, and traces instead to the highest physical assembly or installation the CI resolves into. Recorded as such rather than omitted — an absent link and a link that does not exist are different statements, and only one of them is a finding.

**17. Sub-Supplier End Item Inspection and Test Confirmation**

- **Check:** Completion of inspection and test of sub-supplier equipment end items at point of manufacture
- **Explanation:** For every sub-supplier end item installed in the CI, confirm that the required inspection and test was completed **at point of manufacture**, and that the records supporting it are traceable to the articles actually installed in this unit. Where first article inspection was required for a newly sourced item, confirm the results are complete rather than merely present.
- **Note:** EIA-649-1A requires this confirmation to appear within the PCA minutes. It is written here as a check rather than a filing instruction because a confirmation nobody performs still files.

**18. Pre-Audit Spares and Repair Parts Configuration Verification**

- **Check:** Configuration of spares and repair parts released before the PCA
- **Explanation:** Where spares or repair parts for the CI were provisioned and released **prior to** the audit, confirm from the baseline and release records that what was delivered is currently configured — that is, that it matches the configuration this audit is establishing, or that the difference is identified and dispositioned.
- **Why it matters:** an interim release made before the audit can be built to a configuration the audit is about to supersede, and those articles are already in the field or in a store. The audit unit passing every other check does not tell you anything about them.

---

## Notes on the additions beyond the original nine

**Check 10** is a configuration management floor requirement, not a discretionary check. It is anchored in the repeated escapes between development, early production and full-rate production articles on the KC-46 programme.

**Check 11** covers a failure the existing checks are structurally blind to. Checks 1 and 9 both pass on a unit built correctly, and correctly stamped, to instructions that reflect a superseded revision of the PDD.

**Check 12** is scoped to the zone rather than the CI, because the debris risk created by embodying a CI is a zone risk. Its anchor is tools, rags and debris repeatedly found in delivered KC-46 aircraft.

## Corrections applied

- **Part numbers do not carry revision levels.** The PDD defining the part does. A change requiring a different part produces a new part number. Check 1 therefore reads as written — the CI is verified against the correct revision of its PDD — and the insufficiency in current practice is that matching part numbers establishes identity only, not conformity to the governing revision.
- **A PCA may take place after the CI has been embodied in the aircraft**, provided the CI is acceptable. Embodiment is not a barrier to the audit, and audit access requirements extend to the installed CI and its zone.
- **A PCA may occur prior to flight test**, so Flight Changes may be imposed against the CI or its interfaces at the time of the audit. Check 4 verifies correct incorporation for the applicable milestone and effectivity; it does not require that no Flight Change remain open.


---

## Output of the audit

The checks are not the deliverable. EIA-649-1A mandates the following, and the first four are what most teams already recognise as "the output."

**1. PCA findings.** Every non-compliance identified by any of the eighteen checks is documented by configuration management and provided to the Acquirer for appropriate action, and evaluated by the project lead for the action it requires. Documenting each non-compliance and providing it is a configuration management floor requirement in its own right, in the same cluster as the obligation to conduct the audit at all.

**2. Action items.** Each with its issue, agreed closure plan, responsible individual and agreed suspense date.

**3. Minutes — as an evidence package, not a narrative.** Alongside the proceedings, attendees, decisions and the identification of everything examined with the revision level each document carried on the day, the standard requires the following to be provided **within the minutes**:

- The complete product drawings and associated lists package — model data, cut-away drawings or model-based definitions — with the associated manufacturing instruction sheets or equivalent manufacturing data, for each item of hardware or software identified.
- Completed inspection reports for the selected drawings **and** their associated manufacturing instructions.
- Records of the configuration baselines, for comparison against the engineering change control procedures and the release system — including interim releases of spares and repair parts provisioned before the audit (check 18).
- Confirmation that inspection and test of sub-supplier equipment end items was completed at point of manufacture (check 17).
- The parts selection list supporting the examination that the proper parts are installed (checks 1 and 13).

**4. Records that findings and action items have been rectified.** Post-audit actions completed as assigned or directed.

**5. A configuration audit summary report.** Covering the applicable audit action items and the discrepancy information derived from the audit checklist package.

**6. A detailed configuration audit summary report — prepared only after successful verification that the completed action items are complete, and then provided.** The two reports are deliberately sequenced: the first states what was found, the second states what was verifiably closed. A single report issued on the strength of claimed closure collapses the two and loses the distinction that matters.

**7. An invitation to the Acquirer** — or the Acquirer's designated representative — to witness any inspection, test or audit that has to be re-accomplished.

**8. Where the PCA is conducted in increments, a final system-level PCA** confirming that the system product baseline is correct.

**9. The final product baseline itself.** Establishing it is the purpose of the audit, not a consequence of it.

A check performed and not recorded has not been performed, so far as anyone outside the room can later establish.

### A note on the checklist package

The summary report requirement describes the discrepancy information as deriving from the **audit checklist package**. The standard therefore presumes such a package exists. The eighteen checks in this document are that package — which is a firmer basis for formalising them than the observation that prompted the work.

---

## Appendix — Candidate raised, not adopted

**Retrofit incorporation records** where the CI is embodied and carries retrofit effectivity — probably a sentence inside check 4 rather than a new check. Anchored to Alaska 261, where the as-maintained configuration of the failed jackscrew could not be reliably reconstructed across its service life.
