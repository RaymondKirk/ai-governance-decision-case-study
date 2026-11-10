# AI governance decision: internal knowledge assistant

**Portfolio case study | Fictional organization and sample data | November 2026**

This is a worked example of how I would make a product decision under AI risk. It is not a client engagement, deployed system, completed audit, or NIST certification.

## The decision

Northstar Advisory (fictional), a 60-person professional services firm, wants an internal assistant to answer employee questions using approved policy documents. **Recommendation:** prepare a 20-user pilot, but do not launch until the gates below pass and an executive sponsor signs the decision. Keep client files, HR records, autonomous actions, and unrestricted search out of scope. Humans remain accountable for decisions made using the output.

| Product question | Pilot answer |
| --- | --- |
| Users | Trained operations and IT employees |
| Job to be done | Find the current approved policy and the passage supporting an answer |
| Data | Versioned, approved policy set only |
| Product owner | Operations lead |
| Risk decision owner | Executive sponsor, advised by security and privacy |
| Review point | End of pilot or any material change to model, data, permissions, or use |

**Proposed thresholds, not observed results:** at least 90% of sampled answers link to the correct current source; every pilot user has an escalation path; no confirmed unauthorized document disclosure. A citation alone does not prove an answer is correct, so reviewers must check both passage and answer.

## Risk and control choices

The [risk register](risk-register.csv) records failure modes, owners, controls, and evidence needed. The [sample decision record](decision-record.md) shows how a conditional decision stays pending until evidence exists. Three decisions remain separate: whether the use case is appropriate, whether the pilot may launch, and whether it may expand.

## Launch gates

- [ ] Inventory each source document, owner, version, classification, and retention period.
- [ ] Test source permissions, including denied access to restricted documents.
- [ ] Review vendor terms, data flows, retention, training use, subprocessors, and incident handling.
- [ ] Evaluate current, superseded, ambiguous, and unanswerable questions; save expected behavior and actual results.
- [ ] Require approved citations, an insufficient-evidence response, and human escalation.
- [ ] Set feedback, incident, rollback, and review owners.
- [ ] Record executive sign-off using actual test and review evidence.

## NIST AI RMF alignment

This example is structured around the [NIST AI Risk Management Framework Core](https://airc.nist.gov/airmf-resources/airmf/5-sec-core/):

| Function | Example artifact or decision |
| --- | --- |
| Govern | Named decision owner, risk tolerance, pilot gates, review cadence |
| Map | Intended use, users, data boundaries, foreseeable harms |
| Measure | Answer review, access tests, incident tracking |
| Manage | Pilot limits, escalation, rollback, expansion decision |

This mapping is illustrative; it does not claim full framework coverage. In a real engagement I would run the tests, review results with accountable owners, and record the actual decision.
