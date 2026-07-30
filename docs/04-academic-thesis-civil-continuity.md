# Document IV

# Independent Failure Domains and Civil Continuity Infrastructure

### A Theoretical and Policy Framework for Decentralized Continuity of Civilization

**Working research monograph in the Decentralized Sovereignty canon**  
**Document IV · Living academic text · Version 0.1.0 (2026-07-30)**

| Field | Value |
| --- | --- |
| **Author** | Raphael Cardona (publishing as AlexBTC420) |
| **Companion doctrine** | Documents I–III ([Decentralized Sovereignty](01-decentralized-sovereignty.md), [Order Hail Mary](02-order-hail-mary.md), [U.S. Federal Legislative Strategy](03-us-federal-legislative-strategy.md)) |
| **Genre** | Interdisciplinary working paper (systems engineering · risk analysis · distributed systems · public policy) |
| **Status** | Published (living) — open to peer critique via [CONTRIBUTING.md](../CONTRIBUTING.md) |
| **License** | Source-available dual license — free to read/cite academically (Section A); commercial & government operational use requires Section B ([LICENSE](../LICENSE)) |
| **Disclaimer** | Not legal, financial, medical, or investment advice. Not a token offering. Claims labeled as empirical require citations; untested design theses are labeled as such. |

---

## Abstract

Modern societies concentrate critical functions—electric power, electronic payments, mobile communications, identity registries, knowledge access, and increasingly machine-assisted judgment—into a small number of tightly coupled socio-technical systems. Reliability engineering has long held that **redundancy without independence is not redundancy**: a backup that fails for the same reason as the primary is kindling, not resilience (cf. fault-tolerant system design; Perrow, 1984/1999; aviation and nuclear independence requirements). This monograph formalizes that principle at *civil* scale under the construct **Civil Continuity Infrastructure (CCI)** and the operational doctrine **Order Hail Mary**.

We argue that Continuity of Government (COG) and Continuity of Operations (COOP)—mature U.S. policy architectures oriented toward National Essential Functions (FEMA, n.d.; National Continuity Policy lineage)—are necessary but incomplete. They protect the state’s capacity to decide. They do not, by design, guarantee that ordinary communities can communicate, settle value, attest identity, access essential knowledge, apply local intelligence, or cooperate under temporary legitimacy rules when centralized digital services fail.

Synthesizing literatures on (i) complex socio-technical accidents and cascade risk, (ii) space-weather and high-impact low-frequency (HILF) hazards, (iii) critical infrastructure security and resilience policy, (iv) Byzantine fault-tolerant distributed agreement, (v) cryptographic self-custody and ledger systems, and (vi) privacy-preserving credentials, we propose six capability protocols—**SIGNAL, LEDGER, NAME, LIBRARY, MIND, COUNCIL**—each with a peacetime standing order and an independent-failure-domain evaluation criterion. We distinguish **decentralized infrastructure** (systems whose critical properties survive owner disappearance) from **speculative extraction markets** (systems whose incentives reward exit over utility)—a distinction essential for scholarly and legislative clarity.

**Primary thesis.** *The architectural properties that make certain decentralized systems difficult to centrally control are, under specified threat models, the same properties that make civil essential functions difficult to extinguish.* This claim is a design thesis, not a guarantee of catastrophe or of product performance. It is offered for falsification through tabletop exercises, field pilots, and independent review.

**Keywords:** civil continuity infrastructure; independent failure domains; continuity of government; critical infrastructure resilience; space weather; Byzantine fault tolerance; self-custody; mesh networking; knowledge continuity; local AI; disaster legitimacy; systems of systems risk

---

## 1. Introduction

### 1.1 Motivation

Industrial and post-industrial societies have achieved extraordinary efficiency by concentrating infrastructure: fewer clearinghouses, fewer hyperscale cloud regions, fewer mobile core operators, fewer identity providers, fewer model-hosting campuses. Concentration is not, *prima facie*, irrational—economies of scale, standardization, and capital intensity often improve mean performance. The problem for continuity science is the **joint distribution of failure**: when correlated shocks (geomagnetic disturbance, coordinated cyber operations, pandemic workforce collapse, financial-market freezes, kinetic attack on infrastructure) hit tightly coupled systems, efficiency becomes fragility (Perrow, 1984/1999; Rinaldi, Peerenboom, & Kelly, 2001).

Empirical precursors are not speculative:

- The **1859 Carrington Event** demonstrated that solar-driven geomagnetic disturbance can disable long-line electrical systems (then telegraphy) at continental scale (Cliver & Dietrich, 2013; historical synthesis in NOAA NESDIS, 2015). Modern risk models treat Carrington-class storms as high-impact, low-frequency events with multi-billion economic loss potential under incomplete mitigation (Oughton et al., 2019).
- The **1989 Hydro-Québec geomagnetic disturbance** produced a multi-hour blackout affecting millions, illustrating that even moderate space-weather events can couple into modern grids (Barnes & Van Dyke, 1990, as cited in space-weather impact literature; Oughton et al., 2019).
- Interdependency research shows that infrastructure failures propagate across sectors—power, communications, finance, water, transport—through both physical and logical couplings (Rinaldi et al., 2001; Haimes, 2009).

Parallel digital dependencies deepen the problem. Authentication, payment authorization, content distribution, and increasingly decision support depend on continuous reachability of remote services. When the “authentication server” fails, capability does not degrade gracefully to a simpler local mode; it often collapses entirely. The popular aphorism that civilization is “nine meals from anarchy” (variously attributed in preparedness folklore) is not a scientific law—but as a *mnemonic for thin buffers*, it aligns with resilience research emphasizing short logistical and institutional half-lives under disruption (see generally DHS/CISA critical infrastructure frameworks; FEMA continuity doctrine).

### 1.2 Research questions

**RQ1.** What formal criterion distinguishes a *civil failsafe* from a *correlated backup* that shares fate with the primary system?

**RQ2.** How should Continuity of Government / Continuity of Operations be complemented by a civil layer that preserves essential *societal* functions when official continuity facilities succeed but commercial digital fabric fails—or when both are stressed simultaneously?

**RQ3.** Can a small set of capability protocols, each grounded in existing technical and institutional literatures, be specified with standing orders that are evaluable in peacetime?

**RQ4.** How can policy distinguish *decentralized infrastructure research* from *speculative token markets* without collapsing both into a single political slogan?

### 1.3 Contributions

1. **Definitional:** Formalize **independent failure domains** as a civil-continuity evaluation criterion (Section 3).  
2. **Architectural:** Specify **Civil Continuity Infrastructure (CCI)** as complementary to COG/COOP (Section 4).  
3. **Operational:** Map six protocols with threat-linked standing orders and literature anchors (Section 5).  
4. **Analytic:** Separate casino dynamics from infrastructure properties with testable discriminants (Section 6).  
5. **Methodological:** Propose evaluation designs (tabletops, metrics, negative results) suitable for peer critique (Section 7).  
6. **Epistemic:** Label design theses versus measured claims; invite falsification (Sections 8–9).

### 1.4 Position in the canon

| Document | Role relative to this monograph |
| --- | --- |
| **I** | Normative manifesto and incentive diagnosis (public ethics of builders) |
| **II** | Operational failsafe doctrine (standing orders) |
| **III** | U.S. legislative pathway (policy design) |
| **IV (this text)** | Academic grounding, literature synthesis, formal criteria |

---

## 2. Literature Review and Disciplinary Positioning

### 2.1 Complex systems, normal accidents, and cascade risk

Perrow’s *Normal Accidents* (1984/1999) argues that systems combining **interactive complexity** and **tight coupling** produce accidents that are “normal” in the sense of being inevitable features of system structure, not mere operator error. Critical infrastructure scholarship extends this to multi-sector cascades: failure in one infrastructure can induce failure in others through physical, cyber, geographic, and logical interdependencies (Rinaldi et al., 2001). Haimes and colleagues develop hierarchical holographic modeling and risk filtration methods for systems-of-systems (Haimes, 2009).

**Implication for CCI.** Civil failsafes must be assessed not only for component reliability but for **correlation structure** with the primary infrastructure they purport to back up.

### 2.2 Reliability engineering and independence

In aviation, nuclear, and safety-critical computing, independence of redundant channels is a design requirement: common-mode failures (shared power, shared software, shared administrative authority) defeat redundancy. Distributed systems theory sharpens the adversarial case: Lamport, Shostak, and Pease (1982) formalize agreement under Byzantine faults—components that may fail arbitrarily or maliciously. Practical Byzantine Fault Tolerance (Castro & Liskov, 1999) and subsequent permissioned/permissionless consensus research operationalize agreement under partial synchrony and adversarial minorities (see surveys of BFT systems).

**Implication for CCI.** A civil ledger or identity system that depends on a single cloud region, single client implementation, or single administrative key is not “decentralized” in the fault-tolerance sense, regardless of marketing vocabulary (cf. critiques of decentralization theater in blockchain systems; Narayanan et al., 2016).

### 2.3 Space weather as a paradigmatic HILF hazard

The Carrington Event (September 1859) remains the canonical extreme geomagnetic storm in the observational record (Cliver & Dietrich, 2013; Love, 2024, on intensity estimation uncertainty). Contemporary socioeconomic frameworks estimate large GDP losses for Carrington-class scenarios when forecasting and mitigation are weak; improved forecasting substantially reduces expected loss (Oughton et al., 2019). The 2012 near-miss CME (Baker et al., 2013, as cited in space-weather literature) underscores that extreme events remain plausible on human timescales.

**Implication for CCI.** Threat models need not assume science fiction; they can use **documented HILF classes** already in national risk registers and academic risk analysis.

### 2.4 Critical infrastructure policy (U.S.)

U.S. policy designates critical infrastructure sectors and assigns coordination roles (Patriot Act lineage; PPD-21 historical frame; National Security Memorandum on Critical Infrastructure Security and Resilience, 2024, designating CISA as National Coordinator). Continuity doctrine centers **National Essential Functions** and agency COOP under presidential continuity policy and FEMA Federal Continuity Directives (FEMA continuity resource suite; NSPD-51/HSPD-20 lineage and successors).

**Gap.** These instruments optimize *governmental* essential functions and owner-operator resilience. They do not systematically fund or standardize **household- and community-scale digital continuity** (offline knowledge density, non-cellular messaging, self-custodied value continuity, local inference) as a national capability analogous to civil defense.

### 2.5 Cryptography, self-custody, and ledgers

Public-key cryptography enables possession of signing capability without continuous online authority (Diffie & Hellman, 1976; modern textbook treatment in Katz & Lindell). Bitcoin and related systems demonstrate globally replicated ledgers under adversarial conditions, with well-studied security, privacy, and incentive properties (Nakamoto, 2008; Narayanan et al., 2016). Academic and regulatory literatures also document substantial fraud, market-structure failures, and consumer harm in speculative cryptoasset markets—facts this canon treats as **incentive-design failures**, not as refutations of cryptographic settlement technology *per se*.

**Implication for CCI.** Self-custody and replicated ledgers are candidate tools for **value continuity under clearinghouse failure**, contingent on usability, legal clarity, and anti-fraud architecture—not as investment products.

### 2.6 Identity, selective disclosure, and trust webs

Classical public-key infrastructures centralize trust in certificate authorities—themselves SPOFs and compromise targets. Alternative models include web-of-trust designs, decentralized identifiers, and zero-knowledge credential systems that enable **selective disclosure** (prove a predicate without revealing underlying attributes). NIST digital identity guidelines (SP 800-63 series) and emerging verifiable-credential standards provide institutional hooks for offline-capable attestation research.

### 2.7 Knowledge continuity and cultural memory

Seed banks (e.g., Svalbard Global Seed Vault as institutional metaphor), offline digital libraries, and disaster-medicine field manuals represent **knowledge as infrastructure**. When knowledge is gated behind continuous cloud authentication, catastrophe removes not only comfort but know-how. This monograph treats offline essential archives as continuity assets analogous to physical stockpiles.

### 2.8 Local computation and AI concentration

Foundation-model serving is concentrating in a small number of providers and campuses. For continuity, the relevant property is not “AGI timelines” but **whether triage, logistics, and repair guidance remain available when wide-area networks fail**. Open weights and commodity local inference are research subjects for offline decision support—with known limits on reliability, hallucination, and safety that must be calibrated *before* reliance (standard ML risk literature; NIST AI RMF as institutional frame).

### 2.9 Post-disaster legitimacy

Disaster sociology and conflict studies observe that the most dangerous vacuum after systemic shock is often **legitimacy**: who decides allocation, dispute resolution, and federation with neighbors when normal institutions are slow or absent (classic themes in disaster research). Temporary, consent-based, sunset-bound protocols for local cooperation are therefore continuity infrastructure—not parallel sovereignty cosplay.

---

## 3. Theoretical Framework

### 3.1 Definitions

**Definition 1 (Essential civil function).**  
A capability whose sustained absence over days-to-weeks predictably produces severe harm to life, health, lawful commerce, or social coordination at community scale (communications; value settlement; identity attestation; essential knowledge access; decision support under uncertainty; cooperative allocation under stress).

**Definition 2 (Primary system).**  
The default socio-technical arrangement delivering an essential civil function under normal conditions (e.g., cellular + internet messaging; bank/card clearing; government ID databases; cloud SaaS knowledge; remote AI APIs; ordinary municipal administration).

**Definition 3 (Failsafe / backup domain).**  
An alternate arrangement intended to preserve a minimum viable level of the same function when the primary is degraded or unavailable.

**Definition 4 (Independent failure domain — civil).**  
A backup domain \(B\) for primary \(P\) exhibits independence to the extent that \(B\) does **not** share, to a material degree, the following with \(P\):

| Independence axis | Shared-fate example (failure) | More independent example |
| --- | --- | --- |
| **Power** | Backup servers on same grid feeder | Local generation / hand-powered / long-life battery + low power radios |
| **Physical facility** | DR site in same metro cloud campus | Geographically and organizationally distinct nodes |
| **Administrative authority** | Same cloud IAM / same corporate control plane | No single admin key; multi-party or user-held keys |
| **Network dependency** | Requires same backbone/IX/ISP path | Mesh, amateur radio, sneakernet, delay-tolerant networking |
| **Permission dependency** | Requires continuous authorization from same IdP | Pre-distributed credentials / offline-verifiable attestations |
| **Vendor implementation** | Single binary / single client monoculture | Heterogeneous implementations of open specs |

**Definition 5 (Civil Continuity Infrastructure, CCI).**  
The portfolio of systems, practices, standards, and institutional arrangements that preserve essential civil functions under disruption by maximizing independent failure domains relative to primary commercial and governmental digital services—**without** replacing constitutional Continuity of Government.

**Definition 6 (Decentralized infrastructure vs. speculative extraction).**  

| Discriminant | Decentralized infrastructure | Speculative extraction market |
| --- | --- | --- |
| Success metric | Continuity, correctness, forkability under stress | Price appreciation, attention, exit liquidity |
| Failure mode | Documented, testable, improvable | Rug, freeze, abandonware, narrative collapse |
| Owner-disappearance test | System continues | System dies or becomes worthless |
| Disclosure | Open specs / measurable properties | Asymmetric information as feature |
| Relation to users | Participants / operators | Exit liquidity |

### 3.2 Core propositions

**Proposition 1 (Shared-fate nullity).**  
If a putative failsafe \(B\) fails under the same shock class that disables \(P\) because of shared axes in Definition 4, then \(B\) does not increase continuity for that shock class; it may increase *perceived* safety while increasing cascade risk (false redundancy).

**Proposition 2 (COG complementarity).**  
Let \(G\) be governmental essential functions under COG/COOP and \(C\) be essential civil functions under CCI. Maximizing \(G\) alone does not maximize social welfare under shocks that leave \(G\) intact but destroy commercial digital fabric serving \(C\), nor under shocks that stress both. CCI is a complement, not a substitute, for COG.

**Proposition 3 (Peacetime utility as drill).**  
A failsafe that is not exercised under normal conditions will not be reliably available under stress (training and exercise principles in emergency management; analogous to aviation currency requirements). Therefore CCI capabilities should provide **peacetime utility** whose daily use constitutes continuous validation.

**Proposition 4 (Incentive isomorphism).**  
Systems whose dominant rewards accrue to extraction rather than useful work will, under rational response, produce extraction—including in markets branded as “decentralized” (mechanism-design intuition; empirical crypto market microstructure literature as context). Continuity infrastructure must therefore be evaluated by **incentive alignment**, not slogans.

### 3.3 Scope conditions and non-claims

This framework **does not claim**:

1. That catastrophic collapse is imminent or certain.  
2. That any particular cryptocurrency, product, or company instantiates CCI.  
3. That decentralization is always preferable to centralization under normal efficiency metrics.  
4. That CCI replaces law enforcement, constitutional succession, or public health authority.  
5. That open-source or cryptographic tools are automatically secure or usable.

---

## 4. Continuity Architectures: COG, COOP, and CCI

### 4.1 What official continuity already solves

U.S. continuity policy aims to preserve **National Essential Functions**—the overarching responsibilities of the federal government to lead and sustain the nation under emergency conditions—and subordinate mission-essential functions within agencies (FEMA continuity guidance; presidential continuity directives lineage). Typical elements include orders of succession, delegations of authority, alternate facilities, continuity communications, vital records, human capital, training/exercises, devolution, and reconstitution.

These are serious, institutionalized practices. This monograph does not mock them.

### 4.2 The structural gap

Official continuity is optimized for **institutional survival and decision rights**. CCI is optimized for **population endurance and local coordination capacity**. Table 1 contrasts them.

**Table 1.** Continuity of Government vs. Civil Continuity Infrastructure

| Dimension | COG / COOP | CCI (this work) |
| --- | --- | --- |
| Primary beneficiary | Constitutional government & agencies | Households, communities, civil society |
| Success criterion | NEFs / MEFs continue | Essential civil functions continue at minimum viable level |
| Typical assets | Alternate sites, secure comms, succession | Mesh/radio, self-custody, offline archives, local models, local protocols |
| Activation | Plans, directives, exercises | Peacetime posture; “no switch” ideal |
| Failure if only this exists | Public digital life can still collapse | State decision capacity may still need COG |
| Relation | — | Complementary layer |

### 4.3 Design rule

> **Design Rule R1.** Fund and evaluate civil continuity by independent-failure-domain analysis (Definition 4), not by marketing claims of “decentralization.”

> **Design Rule R2.** Prefer open specifications and heterogeneous implementations to reduce monoculture risk (common-mode software failure).

> **Design Rule R3.** Prefer peacetime-useful systems over pure “break glass” stockpiles that are never drilled.

---

## 5. The Six Protocols: Capability Layer of Order Hail Mary

Each protocol states: function, threat link, technical/institutional antecedents, standing order, and independence checklist. Standing orders are **behavioral hypotheses** for field testing, not proven universal prescriptions.

### 5.1 SIGNAL — Communications continuity

**Function.** Exchange messages without a single commercial tower, ISP, or cloud relay as SPOF.  
**Threat link.** Cellular/backhaul loss; IX failure; targeted tower destruction; long-duration power loss to radiosites.  
**Antecedents.** Amateur radio emergency service (historical disaster performance); mobile ad hoc networks; delay-tolerant networking (Fall, 2003); mesh networking research; FirstNet/public-safety LTE as *complementary* official layer (not a substitute for citizen offline paths).  
**Standing order.** Own and practice one communications path requiring no company subscription and no single tower—before you need it.  
**Independence checklist.** Path survives loss of commercial mobile core; power budget realistic offline; operators trained.

### 5.2 LEDGER — Value continuity

**Function.** Enable lawful exchange of value when banking hours, card networks, or RTGS-like clearing are unavailable.  
**Threat link.** Clearing freezes; bank IT failure; cyber attack on payment processors; loss of connectivity to authorization hosts.  
**Antecedents.** Bearer instruments historically; public-key authorization; replicated ledgers (Nakamoto, 2008; Narayanan et al., 2016); offline signing with later settlement patterns in payments research.  
**Standing order.** Hold *some* value under keys you control; understand possession versus permissioned balances.  
**Independence checklist.** Settlement path not solely dependent on a single custodian’s database; fraud/theft risks explicitly mitigated; **not** marketed as investment return.  
**Caveat.** Legal and consumer-protection constraints are first-class; CCI does not license crime or promise yield (Document I covenant).

### 5.3 NAME — Identity continuity

**Function.** Attest relevant identity attributes when central registries are unavailable or untrusted for a session.  
**Threat link.** IdP outage; civil registry destruction; mass surveillance pressure forcing over-collection.  
**Antecedents.** PKI; web of trust; NIST SP 800-63; verifiable credentials; zero-knowledge proof systems for selective disclosure.  
**Standing order.** Establish keys and community attestations *before* failure; prefer prove-minimum, reveal-nothing-else.  
**Independence checklist.** Verification possible offline or on degraded nets; no single registrar required for last-resort recognition within a community of practice.

### 5.4 LIBRARY — Knowledge continuity

**Function.** Preserve essential know-how (water, sanitation, first aid, power, agriculture, basic engineering, law summaries) offline.  
**Threat link.** Cloud lockout; CDN failure; institutional website disappearance; loss of expert reachability.  
**Antecedents.** Seed vaults as metaphor for redundancy of critical genetic material; WHO/ICRC field manuals; offline digital libraries; LOCKSS-style multi-copy preservation.  
**Standing order.** Maintain one offline essential archive and one teachable skill.  
**Independence checklist.** Usable without login; integrity-checkable (hashes); multi-copy geographic diversity.

### 5.5 MIND — Compute continuity

**Function.** Provide local decision support when remote AI/datacenter services are unreachable.  
**Threat link.** Cloud inference outage; backbone loss; provider policy denial; correlated GPU-campus failure.  
**Antecedents.** Edge computing; open-weight models; NIST AI Risk Management Framework (risk framing); human factors on automation bias.  
**Standing order.** If hardware permits, run a local model and **calibrate** failure modes before reliance.  
**Independence checklist.** Runs offline; known error profile; human remains responsible for high-stakes acts.  
**Design thesis (labeled).** Local open models are a *partial* hedge for judgment continuity—not a replacement for experts or democratic authority.

### 5.6 COUNCIL — Governance continuity

**Function.** Pre-commit transparent, consent-based, sunset-bound rules for local cooperation under stress.  
**Threat link.** Legitimacy vacuum; rumor; coercive entrepreneurs; inability to federate aid.  
**Antecedents.** Disaster sociology; polycentric governance (Ostrom, 1990); emergency management incident command as *official* complement; temporary special districts and mutual aid agreements.  
**Standing order.** Know your people; practice small-scale cooperative decisions with written rules and audit trails.  
**Independence checklist.** Rules exist before crisis; sunsets and appeal paths defined; explicitly non-sovereign / non-insurgent framing (Document II: complementary to lawful government).

### 5.7 Protocol interdependency (systems-of-systems)

Protocols are not fully orthogonal: SIGNAL enables COUNCIL coordination; LIBRARY feeds MIND; NAME binds LEDGER counterparties. Evaluation must include **joint drills**, not only unit tests—consistent with interdependency analysis (Rinaldi et al., 2001).

---

## 6. Analytic Separation: Infrastructure vs. Casino Dynamics

A recurring scholarly and policy error is synecdoche: treating all cryptographic ledger activity as identical to speculative mania. This monograph insists on discriminants (Definition 6).

**Empirical motivation for separation.** Academic and regulatory records document substantial fraud, wash trading concerns, pump-and-dump patterns, and consumer losses in cryptoasset markets. Simultaneously, the same cryptographic primitives underpin authentic security engineering (secure messaging, code signing, authenticated software updates). Conflating these collapses policy into either naive boosterism or indiscriminate prohibition.

**Test T1 (Owner disappearance).** If the founding company vanishes, do user-critical properties continue?  
**Test T2 (Admin key).** Can a small set of operators unilaterally freeze, seize, or rewrite user state without transparent due process encoded and auditable?  
**Test T3 (Incentive).** Do rewards accrue primarily to useful work and security, or to attention and exit?  
**Test T4 (Disclosure).** Are critical mechanisms open to independent reimplementation?

Systems failing T1–T4 may still be profitable financial objects; they are poor CCI candidates.

---

## 7. Methods for Evaluation and Falsification

### 7.1 Tabletop and functional exercises

Adapt FEMA exercise methodology to civil scenarios, e.g.:

- **Scenario S1:** 14-day multi-county electric outage + degraded cellular.  
- **Scenario S2:** Payments authorization outage with intact power.  
- **Scenario S3:** Identity-provider outage during evacuation.  
- **Scenario S4:** Carrington-class GMD with transformer stress and GNSS degradation (parameters from space-weather literature; uncertainty acknowledged per Love, 2024).

**Scoring.** Binary and graded items on Definition 4 axes; time-to-first-message; percent of households with offline LIBRARY pack; error rates of MIND assistance; presence of COUNCIL minutes with sunsets.

### 7.2 Proposed metrics (indicative)

| Metric | Protocol | Falsification interest |
| --- | --- | --- |
| \(M_1\): Fraction of drill messages delivered without commercial cellular | SIGNAL | If near zero after training investment, standing order fails practicality |
| \(M_2\): Median time to offline-verifiable payment intent | LEDGER | If unusable by non-experts, not civil-grade |
| \(M_3\): Offline verification success rate for pre-issued credentials | NAME | If requires cloud always, independence fails |
| \(M_4\): Household density of integrity-checked essential archives | LIBRARY | If density ~0, knowledge continuity is rhetorical |
| \(M_5\): Task success of local model vs. baseline under offline constraint | MIND | If harm > help after calibration, restrict claims |
| \(M_6\): Existence of practiced, sunset-bound local rules | COUNCIL | If only paper plans, Proposition 3 fails |

### 7.3 Negative results policy

In the spirit of scientific integrity (and Document I’s “label bets as bets”), failed drills and negative benchmarks must be publishable. A continuity doctrine that cannot admit failure is marketing.

### 7.4 Ethical constraints on research

No live testing that endangers persons or critical systems; no unauthorized access; respect human-subjects norms where surveys or behavioral studies are run; dual-use awareness for communications and financial tools.

---

## 8. Limitations

1. **Working paper status.** This is not a completed dissertation with original large-N empirical results; it is a structured research monograph synthesizing prior art into a civil-continuity framework.  
2. **Citation completeness.** Living document: bibliography will expand under peer critique (open issues invited for missing canonical sources).  
3. **Jurisdiction.** Policy discussion is U.S.-centric in institutional detail; technical propositions aim at broader applicability.  
4. **Uncertainty in HILF magnitudes.** Carrington-class intensity and return periods remain scientifically uncertain (Love, 2024); economic loss figures are model-dependent (Oughton et al., 2019).  
5. **Usability gap.** Cryptographic self-custody and mesh networking have historically poor consumer UX; CCI success is constrained by human factors as much as theory.  
6. **Adversarial governments.** In highly repressive contexts, some CCI tools face legal and safety tradeoffs beyond this paper’s scope.  
7. **Not a product evaluation.** No claim that WokeSocial, WokeNet, or any named implementation currently meets CCI criteria.

---

## 9. Discussion

### 9.1 Toward a research program

A doctoral-scale program following from this monograph would include: (a) formalization of independence scores; (b) comparative case studies of disasters where commercial digital fabric failed; (c) controlled field experiments on SIGNAL/LIBRARY density; (d) legal analysis of self-custody and amateur communications in continuity contexts; (e) HCI studies on non-expert operation of offline credentials and local models; (f) public-economics models of CCI as a public good with free-rider problems.

### 9.2 Policy translation

Document III translates this framework into phased U.S. legislative strategy (study/pilot → authorization → appropriations → rights clarity), deliberately avoiding token-bill optics. Academic reviewers should judge Document III as **policy design**, not as empirical proof.

### 9.3 Relationship to “decentralization” discourse

This work reclaims decentralization as **fault-isolation architecture** and **political condition of non-domination over essential rails**, not as a synonym for asset speculation. That reclamation is normative (Document I) and technical (this Document IV) simultaneously—an interdisciplinary necessity.

---

## 10. Conclusion

We have argued that civil societies over-index on centralized digital primaries and under-invest in independent civil failsafes. Continuity of Government remains necessary; it is not sufficient for continuity of civilization understood as ordinary people’s capacity to endure. By formalizing independent failure domains, defining Civil Continuity Infrastructure, and specifying six evaluable protocols with literature anchors, this monograph supplies a research-grade backbone for the Order Hail Mary doctrine.

The appropriate academic posture is neither millenarian panic nor complacent efficiency worship. It is the engineer’s question, asked of civilization’s backups:

> **If the owner, the grid, the tower, and the IdP disappeared tomorrow—what still works, and who practiced it?**

That question is falsifiable in the field. This text invites the experiment.

---

## Acknowledgments

This living monograph sits within the Decentralized Sovereignty canon and benefits from open critique. Readers are requested to file citation gaps, methodological objections, and field reports via the repository issue tracker.

---

## Glossary (selected)

| Term | Meaning in this text |
| --- | --- |
| CCI | Civil Continuity Infrastructure |
| COG | Continuity of Government |
| COOP | Continuity of Operations |
| HILF | High-impact, low-frequency (hazard class) |
| NEF | National Essential Function |
| SPOF | Single point of failure |
| BFT | Byzantine fault tolerance |
| GMD / GIC | Geomagnetic disturbance / geomagnetically induced current |

---

## References

*Note: This bibliography prioritizes peer-reviewed, governmental, and canonical technical sources. Incomplete entries will be expanded as the living document matures. Access dates omitted for classic works; URLs provided where they are the stable official source.*

### Systems risk, complexity, and infrastructure interdependency

Haimes, Y. Y. (2009). *Risk modeling, assessment, and management* (3rd ed.). Wiley.

Perrow, C. (1999). *Normal accidents: Living with high-risk technologies* (Rev. ed.). Princeton University Press. (Original work published 1984)

Rinaldi, S. M., Peerenboom, J. P., & Kelly, T. K. (2001). Identifying, understanding, and analyzing critical infrastructure interdependencies. *IEEE Control Systems Magazine, 21*(6), 11–25. https://doi.org/10.1109/37.969131

### Space weather and extreme geomagnetic storms

Cliver, E. W., & Dietrich, W. F. (2013). The 1859 space weather event revisited: Limits of extreme activity. *Journal of Space Weather and Space Climate, 3*, A31. https://doi.org/10.1051/swsc/2013053

Love, J. J. (2024). On the uncertain intensity estimate of the 1859 Carrington storm. *Journal of Space Weather and Space Climate*. https://doi.org/10.1051/swsc/2024015 (see journal record for final citation details)

National Oceanic and Atmospheric Administration, NESDIS. (2015, October 19). *When solar storms attack: Space weather and our infrastructure*. https://www.nesdis.noaa.gov/news/when-solar-storms-attack-space-weather-and-our-infrastructure

Oughton, E. J., Hapgood, M., Richardson, G. S., Beggan, C. D., Thomson, A. W. P., Gibbs, M., Burnett, C., Gaunt, C. T., Trichas, M., Dada, R., & Horne, R. B. (2019). A risk assessment framework for the socioeconomic impacts of electricity transmission infrastructure failure due to space weather: An application to the United Kingdom. *Risk Analysis, 39*(5), 1022–1043. https://doi.org/10.1111/risa.13229

### Distributed systems and fault tolerance

Castro, M., & Liskov, B. (1999). Practical Byzantine fault tolerance. In *Proceedings of the Third Symposium on Operating Systems Design and Implementation (OSDI)* (pp. 173–186). USENIX Association.

Fall, K. (2003). A delay-tolerant network architecture for challenged internets. In *Proceedings of SIGCOMM ’03* (pp. 27–34). ACM. https://doi.org/10.1145/863955.863960

Lamport, L., Shostak, R., & Pease, M. (1982). The Byzantine generals problem. *ACM Transactions on Programming Languages and Systems, 4*(3), 382–401. https://doi.org/10.1145/357172.357176

### Cryptography, ledgers, and digital currency technology

Diffie, W., & Hellman, M. E. (1976). New directions in cryptography. *IEEE Transactions on Information Theory, 22*(6), 644–654. https://doi.org/10.1109/TIT.1976.1055638

Nakamoto, S. (2008). *Bitcoin: A peer-to-peer electronic cash system*. https://bitcoin.org/bitcoin.pdf

Narayanan, A., Bonneau, J., Felten, E., Miller, A., & Goldfeder, S. (2016). *Bitcoin and cryptocurrency technologies: A comprehensive introduction*. Princeton University Press.

### Identity, security engineering, and AI risk framing

National Institute of Standards and Technology. (n.d.). *Digital identity guidelines* (NIST SP 800-63 series). https://pages.nist.gov/800-63-3/

National Institute of Standards and Technology. (2023). *Artificial Intelligence Risk Management Framework (AI RMF 1.0)* (NIST AI 100-1). https://doi.org/10.6028/NIST.AI.100-1

National Institute of Standards and Technology. (2016/2018+). *Systems security engineering* (NIST SP 800-160 series). https://csrc.nist.gov/publications/sp800

### Continuity of government / operations and critical infrastructure policy

Cybersecurity and Infrastructure Security Agency. (2024). *National Security Memorandum on Critical Infrastructure Security and Resilience* (overview and implementation materials). https://www.cisa.gov/topics/critical-infrastructure-security-and-resilience/national-security-memorandum-critical-infrastructure-security-and-resilience

Federal Emergency Management Agency. (n.d.). *Continuity resource toolkit* and Federal Continuity Directives. https://www.fema.gov/emergency-managers/national-preparedness/continuity

U.S. Government. (2007). *National Security Presidential Directive 51 / Homeland Security Presidential Directive 20* (National Continuity Policy) and successor continuity instruments. (Consult current National Continuity Policy materials for operative text.)

### Governance and collective action

Ostrom, E. (1990). *Governing the commons: The evolution of institutions for collective action*. Cambridge University Press.

### Canon-internal references (non-peer-reviewed doctrine)

Cardona, R. (2026a). *Decentralized Sovereignty* (Document I). https://github.com/AlexBTC420/order-hail-mary

Cardona, R. (2026b). *Order Hail Mary: The Decentralized Sovereignty Failsafe Doctrine* (Document II). https://github.com/AlexBTC420/order-hail-mary

Cardona, R. (2026c). *U.S. Federal Legislative Strategy* (Document III). https://github.com/AlexBTC420/order-hail-mary

---

## Appendix A — Mapping Document II Standing Orders to Academic Constructs

| Standing order (Document II) | Academic construct (this paper) |
| --- | --- |
| Own a no-tower comms path | Independence on network & permission axes (Def. 4); DTN/mesh antecedents |
| Hold some value with own keys | Authorization without continuous intermediary; bearer-capability analogy |
| Establish keys + attestations early | Pre-positioned credentials; web-of-trust / VC models |
| Offline archive + teachable skill | Knowledge as stockpile; multi-copy preservation |
| Local model + calibration | Edge inference; automation bias control |
| Know your people; practice rules | Polycentric governance; legitimacy under stress |

---

## Appendix B — Suggested Peer-Review Checklist

Reviewers are invited to assess:

- [ ] Are Definitions 1–6 internally consistent?  
- [ ] Are Propositions 1–4 stated as falsifiable or clearly normative?  
- [ ] Are HILF citations appropriately uncertain (not alarmist)?  
- [ ] Is the COG complementarity claim fair to existing FEMA/CISA doctrine?  
- [ ] Are crypto infrastructure vs. casino discriminants operationalizable?  
- [ ] What mandatory citations are missing for a dissertation literature review in your field?  
- [ ] Which metrics \(M_1\)–\(M_6\) are poorly specified?

Open an issue: `Academic review: Document IV — <topic>`.

---

## Appendix C — Versioning and Living-Document Protocol

Material changes to claims, definitions, or bibliography must:

1. Update this file on `main`;  
2. Add a [CHANGELOG.md](../CHANGELOG.md) entry;  
3. Prefer pull requests that add citations over ones that only escalate rhetoric;  
4. Never silently weaken the infrastructure-vs-casino distinction or the “no profit promise” covenant of Document I.

---

## Document control

| Version | Date | Notes |
| --- | --- | --- |
| 0.1.0 | 2026-07-30 | Initial academic monograph: definitions, propositions, six-protocol literature anchors, evaluation design, core bibliography |

*Document IV of the Decentralized Sovereignty canon.*  
*Argue with it. Cite it. Improve the references. Falsify the standing orders in the field.*

**Corresponding repository:** https://github.com/AlexBTC420/order-hail-mary
