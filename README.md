[# Dan Lee-Odinson

**Technical Program & Systems Manager | Transitioning to Space Mission Operations, Ground Segment / Ground Control, and AI Systems Integration.** ](https://capsule-render.vercel.app/api?type=soft&height=200&color=gradient&text=Dan%20Lee-Odinson&reversal=true&fontSize=60&desc=Technical%20Program%20and%20Systems%20Manager%20|%20Building%20Towards%20Space%20Systems,%20Mission%20Ops,%20and%20AI%20Systems%20Integration&descSize=15&descAlign=50&descAlignY=70)

# Eleven years delivering enterprise software, triaging escalations, and unblocking the people who run the systems.

Four things I have actually done:

- **Shipped a product.** [Next Pass](https://chromewebstore.google.com/detail/next-pass/dffapmipddmkinnogkdkibjoellllhof), a satellite-pass tracking extension, is live on the Chrome Web Store at `v0.6.1` — developer account, store review, public listing, real users, and my name on it when it breaks.
- **Found and corrected an error in someone else's published model.** Reproducing Andrew McCalip's open *Space Datacenters* orbital-radiator model, I found that its cosine-tilt view-factor heuristic underestimated the edge-on per-face Earth view factor by roughly **12×**. With exact tilted-plate-to-sphere geometry, the equilibrium temperature moves **+6.35 K** (335.75 K → 342.10 K). The correction, the derivation, and the verification script are published: [DOI 10.5281/zenodo.20695720](https://doi.org/10.5281/zenodo.20695720).
- **Found a false negative in my own safety instrument.** In an agent-economy simulation, the kill criterion that was supposed to detect runaway credit spirals passed every honest-behavior test and **missed genuine spirals**. It took four versions (v0–v3) before it held. I published that as the headline result.
- **Published the process itself — and made it survive its own review.** [*The Process Is the Product*](https://doi.org/10.5281/zenodo.21512210) documents the human-directed, multi-model adversarial workflow behind everything on this page, and [adversarial-project-method](https://github.com/dan-lee-odinson/adversarial-project-method) ships it as a reusable framework with the complete thirteen-gate case record — **including the five consecutive failed gate reviews** that forced a standard of proof and a stopping rule. The failures are published on purpose.

*Method, in one line:* I direct multi-model workflows — Claude drafts and builds, a second vendor's model is prompted to attack the output, and the workflow is human-in-the-loop by design. I diagnosed the false negative, I found the view-factor error, and I am accountable for every disposition. The method is now published and reusable: [preprint](https://doi.org/10.5281/zenodo.21512210) · [framework](https://github.com/dan-lee-odinson/adversarial-project-method).

**ORCID:** [0009-0009-9504-0796](https://orcid.org/0009-0009-9504-0796) · **LinkedIn:** [dan-lee-odinson](https://www.linkedin.com/in/dan-lee-odinson/) · **Email:** dan.lee.odinson [at] gmail dot com

---

## Self-published technical record — preprints, not peer reviewed

Eleven DOI-archived Zenodo works — **nine preprints and two versioned software packages**, across twelve version DOIs — in four research programs. All ORCID-linked, all versioned, all reproducible. **No qualified human engineer has externally reviewed any of it.** That is the next thing I need, and I say so in the repositories themselves.

| Program | Domain | Deposits |
|---|---|---|
| [**Adversarial Project Method**](https://github.com/dan-lee-odinson/adversarial-project-method) | Research governance · multi-model AI verification · configuration-controlled review | [The Process Is the Product `v1.0`](https://doi.org/10.5281/zenodo.21512210) |
| [**Orbital Thermal Bounds**](https://github.com/dan-lee-odinson/orbital-thermal-bounds) | Spacecraft thermal control · heat rejection · radiator sizing | [Bounds preprint](https://doi.org/10.5281/zenodo.20650893) · [Edge-on geometry + McCalip correction](https://doi.org/10.5281/zenodo.20695720) · [AI1 design point (SpaceX)](https://doi.org/10.5281/zenodo.20670771) · [Software `v1.1.0`](https://doi.org/10.5281/zenodo.20709241) |
| [**ISONOMIA / Path A**](https://github.com/dan-lee-odinson/isonomia-path-a) | Agent-based simulation · mechanism design · adversarial robustness | [Design paper](https://doi.org/10.5281/zenodo.21343917) · [Evidence release `v1.0.0`](https://doi.org/10.5281/zenodo.21287289) · [Docs release `v1.1.0`](https://doi.org/10.5281/zenodo.21348073) |
| [**The Peership Corpus**](https://github.com/dan-lee-odinson/peership-corpus) | AI governance · constitutional design · research provenance | [I. Gods and Slaves](https://doi.org/10.5281/zenodo.21313987) · [II. Peership: A Framework](https://doi.org/10.5281/zenodo.21315519) · [III. The ISONOMIA Commons](https://doi.org/10.5281/zenodo.21343917) · [IV. Constitution, Not Cage](https://doi.org/10.5281/zenodo.21325361) · [V. The Peership Thesis](https://doi.org/10.5281/zenodo.21359124) |

Paper III is cross-listed: it is the ISONOMIA design paper and corpus paper III, counted once.

---

## Selected work

### [Adversarial Project Method](https://github.com/dan-lee-odinson/adversarial-project-method) — the workflow, formalized and published

*Framework `v1.0` · [preprint DOI](https://doi.org/10.5281/zenodo.21512210) · thirteen-gate frozen case record · CC BY 4.0 / Apache-2.0*

An evidence-gated review methodology for work that must survive hostile scrutiny before release. One human directs. One LLM builds. A second, separately run LLM attacks. Work moves through **gate reviews** against predefined acceptance criteria: the Builder freezes a hash-manifested packet (**configuration control** — the reviewer's findings are cryptographically bound to the exact bytes reviewed, so "which version did the reviewer inspect?" becomes unaskable), the Reviewer deposits findings as data rather than instructions, and the human Director **dispositions every finding** on a verbatim, signed record. A gate passes with zero unaccepted product blockers; convergence is declared by a **stopping rule** fixed before the findings are seen — never on exhaustion.

The result that earns the paper is a failure mode with a name. Turned on its own tooling, the loop failed **five consecutive gates** (12, 11, 12, 12, 15 findings) because each fix closed the reviewer's named probe rather than the defect class behind it. The correction — every fix must demonstrate it addressed the class, every check must be witnessed failing before it is trusted — ended the streak, and it is the paper's most transferable result. The mechanisms are deliberate borrowings, named in the text: Stage-Gate reviews, Agile definition-of-done, test-driven development's red-before-green, maker-checker segregation of duties, and Lean stop-the-line — recomposed for one accountable human directing several AI systems.

`technical program management` · `gate reviews` · `configuration control` · `verification & validation` · `human-in-the-loop AI`

### [Next Pass](https://chromewebstore.google.com/detail/next-pass/dffapmipddmkinnogkdkibjoellllhof) — shipped to the Chrome Web Store

*Published `v0.6.1` · built in short daily sprints · [build log](https://github.com/dan-lee-odinson/coworking-with-claude#project-3--next-pass-my-first-app)*

A glanceable countdown to the next visible ISS pass. Pass predictions come from the **N2YO API** — N2YO propagates the orbit, not me. What I built is the client: a 6-hour cache, graceful degradation when there is no key, location, or network, a background worker scheduling desktop notifications ahead of bright passes, and one-click calendar export (Google Calendar or `.ics`).

Scoped, tested, and launched by me — including the parts no agent can do: the developer account, the store submission, the listing, and standing behind it in public. The bugs that mattered were found by *using* the extension, never by reading the code.

Launched to r/ISS and r/amateursatellites. An SDR operator pointed out that several satellites on the roadmap (NOAA weather sats) are decommissioned, and recommended the still-operational Meteor-M series instead. I updated the roadmap.

`API integration` · `caching` · `graceful degradation` · `shipped product`

### [Orbital Thermal Bounds](https://github.com/dan-lee-odinson/orbital-thermal-bounds) — spacecraft thermal control

*Python · Wolfram Language · GitHub Actions · `v1.1.0`*

Thermodynamic bounds and mass-trade criteria for heat rejection in orbital data centers: analytic radiator-area bounds, an executable radiator simulation package, the **McCalip model reproduction and +6.35 K correction** described above, and a Phase B chip-to-radiator architecture trade-study framework. Closed-form bounds are derived symbolically in Wolfram Language and cross-checked against the numerical implementation; **CI/CD-enforced pytest suite, 259 passing tests**.

**Scope:** a reduced-order, **one-node** model. **Not validated against flown hardware.** **Not** intended for flight design, certification, or safety-critical decisions. Phase B's central transport and pressure claims have **not** been validated by a qualified external engineering reviewer.

`spacecraft thermal control` · `radiator sizing` · `heat rejection` · `trade study`

### [ISONOMIA — Path A](https://github.com/dan-lee-odinson/isonomia-path-a) — agent-based simulation

*Python · `v1.1.0` · evidence pinned to `v1.0.0` / commit `ba3ddb5`*

**The headline result is a failure.** I built a kill criterion — the safety instrument meant to detect a runaway credit spiral — inside an agent-economy simulation. It went through four versions (v0–v3) because it kept failing, and the interesting failure was v2: it passed honest noise cleanly and **missed genuine spirals**. A false negative on the instrument that exists to catch the failure. v0 halted every honest launch; v1 false-positived on honest shock transients (2,299 trips in 45,000 runs); v2's magnitude floor let real spirals through; v3 required active-agent normalization. The recorded lesson: *a kill criterion is itself a safety mechanism and must be adversarially tested in both directions — showing that honest behavior doesn't trip it is not enough.*

**Method:** 300 Latin-hypercube parameter samples × 50 seeds × 3 demand variants = **45,000-run sweeps**, plus a separate 45,000-run out-of-sample re-certification. Positive *and* negative control batteries. Seven scripted attack scenarios. CI calibration-lock, 73-test suite.

**Limits:** results hold at **sampled points only**; no claim is made about unsampled points in the continuous parameter space. Nothing is live or production-validated.

`agent-based modeling` · `Monte Carlo` · `Latin hypercube sampling` · `fault detection`

### [Coworking with Claude](https://github.com/dan-lee-odinson/coworking-with-claude) — the working log, including what failed

*Multi-model workflow practice · reusable skill libraries*

How to direct agentic workflows, give them durable context, and stay accountable for the output. It carries the reusable skills behind the projects above.

It also carries a **published negative result**. An agentic content-generation venture, run as a business experiment: **~$300 spent, $4.08 earned** — a 1.36% recovery, needing roughly **73× the revenue** just to break even. The pipeline worked; the business thesis did not. Conclusion, published rather than buried: *AI is a workflow accelerator, but "AI passive income" is a misleading frame — AI can build the machine, it does not create demand.*

---

## The method — published as [adversarial-project-method](https://github.com/dan-lee-odinson/adversarial-project-method)

The workflow that produced everything above is now itself a published, reusable artifact: [*The Process Is the Product: A Human-Directed, Multi-Model Adversarial Workflow for Trustworthy AI-Assisted Research*](https://doi.org/10.5281/zenodo.21512210) (preprint, `v1.0`), plus the framework repository — the `METHOD.md` spec, packaging rules, templates, verification tools, deployment docs, and the frozen thirteen-gate case record of the method reviewing its own tooling.

Claude drafts and builds; a second vendor's model is prompted to attack the result, and the attack prompts are published so a reader can verify the reviewer was told to attack rather than to bless. Nothing is accepted or rejected by a model — the workflow is **human-in-the-loop** by design and a human is accountable for every call.

Provenance is testable: DOI-versioned deposits with concept and exact-version identifiers kept distinct, SHA-256 checksums proving committed artifacts are byte-identical to their archival deposits, CI/CD-enforced pytest suites, evidence pinned to an exact release and commit hash. The Peership repository carries the fullest form of that apparatus — a 161-entry bibliographic database, a 70-claim provenance ledger recording each claim's source, evidentiary strength, and counterevidence, and per-paper adversarial reviews with their prompts published. Its first adversarial review returned **FAIL** and killed the draft's central claim; that claim is absent from the published paper.

Every artifact I publish names, in its own text, the claims it does not establish. That is not verification and validation. It is the precondition for it.

---

## Operational track record

**Eleven years in enterprise HCM implementation** — software delivery, project leadership, requirements analysis, escalation handling, and technical support. The number that matters is the **tempo**, not the total:

| | |
|---|---|
| **Throughput** | **20–35 client implementations per quarter**, sustained for three years |
| **Concurrency** | **60-client active caseload**, held continuously for seven years |
| **Volume** | ~150 implementations at HUB International, as sole technology specialist for the Northwest region |

That is a continuous, high-tempo delivery load — not a sequence of one-off projects. It means the queue stays full and I don't fall over.

I've since moved onto an internal **SME support team**: triaging incoming issues, unblocking the consultants running live implementations, and owning the support queue.

Triage under time pressure, escalation paths, unblocking operators mid-procedure, sustained tempo under continuous load — those are the transferable parts, not the domain. I have not done mission operations, and I am not going to claim that a support queue is the same thing as one.

`anomaly triage` · `escalation management` · `requirements analysis` · `technical program management`

---

## Continuing education

**B.S. Space Studies — Everglades University** (began April 2026; in progress). Currently in *Business Ethics*; upcoming: General Physics, GPS Surveying, Spacecraft Systems & Design.

**Certifications.** Google Project Management Professional Certificate — in progress. AWS track (Cloud Practitioner → SysOps → Advanced Networking) via hands-on lab environments.

**Programming and systems.** Python is the primary language — automation, simulation, data analysis. Supporting work in SQL, Bash/Linux, and cloud operations.

**[Reading list](https://github.com/dan-lee-odinson/reading-list)** — spaceflight history, propulsion, autonomous systems, systems thinking, with a written reflection on each finished book.

**[Artemis Smartwatch](https://github.com/dan-lee-odinson/circuitmess-artemis-smartwatch)** — ESP32 kit assembly underway; first embedded hardware project. Build log in progress; no code published yet.

Member: AIAA · IEEE (Robotics & Automation Society; Aerospace & Electronic Systems Society) · The Planetary Society.

---

## The first thing I couldn't do alone

**[RMPC Servicing Payload Concept](https://github.com/dan-lee-odinson/rmpc-servicing-payload-concept) — closed. No team assembled in time; no application submitted.**

I developed an independent concept for an ORU-style robotic on-orbit servicing validation payload (grapple/release, relocation, alignment verification, inspection support), published a [concept page](https://dan-lee-odinson.github.io/rmpc-servicing-payload-concept/), and set out to recruit a team for NASA TechLeap's Robotically Manipulated Payload Challenge. I didn't get the team together before the deadline, so I didn't compete.

It was a deliberate reach, and it found the ceiling of everything else on this page. **Every other project here is solo work accelerated by AI** — the extension, the thermal model, the simulations. A robotic servicing payload is not: it needs mechanical engineers, flight-hardware experience, environmental-test experience, fabrication. No amount of individual effort or AI leverage substitutes for people who have actually built and qualified hardware.

So the finding wasn't about the payload. **I had built a portfolio and a method, but not yet the professional network that lets you convene a team against a deadline.** Team formation is its own discipline, and it runs on relationships you build *before* you need them.

**Nobody pulls off a moonshot alone.** Apollo was four hundred thousand people. The whole reason I want this industry is to be part of *the teams* that support these missions — and this is the project that taught me that building the team is the work, not the overhead around it. What changes: build the network before the next deadline (AIAA, IEEE, university labs, makerspaces), start from an existing group rather than strangers, secure one credible hardware lead before announcing, and back-plan from team formation rather than the technical concept.

The concept brief and requirements notes stay published. *Not an official NASA, TechLeap, or Luminary Labs project.*

---

## What's next

Planned work, not accomplishments:

- **Testing whether the method survives a team.** The paper names the experiments a single-operator case study cannot run: whether the Director / Builder / Reviewer role separation holds across multiple people, and whether the overhead is justified by measured error reduction against a lighter baseline. The framework is public so those experiments can be run against it — by me or by anyone.
- **External engineering review** of the Orbital Thermal Bounds Phase B transport and pressure claims. The model needs a qualified human reviewer, and until it has one, the repository says so.
- **ROS 2 fundamentals**, then a rover build, then SLAM/perception and computer vision.

---

## Where I'm headed

Mission operations, ground segment and ground control operations, technical program management, systems engineering, and AI systems integration in the space sector.

I am not claiming to be an astrophysicist or a flight-qualified engineer. I am claiming that I can direct rigorous technical work, verify it, publish it with its limits intact, and be accountable for it — and that the record above is checkable.

**[LinkedIn](https://www.linkedin.com/in/dan-lee-odinson/)** · **[ORCID 0009-0009-9504-0796](https://orcid.org/0009-0009-9504-0796)** · dan.lee.odinson [at] gmail dot com


[![GitHub Stats](https://github-stats-extended.vercel.app/api/top-langs?username=dan-lee-odinson&langs_count=10&theme=default_repocard)](https://github-stats-extended.vercel.app/api/top-langs?username=dan-lee-odinson&langs_count=10&theme=default_repocard)
