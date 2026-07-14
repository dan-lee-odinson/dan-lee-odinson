# Dan Lee-Odinson

**Enterprise implementation and technical operations professional moving into space systems.** Eleven years delivering enterprise software, triaging escalations, and unblocking the people who run the systems.

Three things I have actually done:

- **Shipped a product.** [Next Pass](https://chromewebstore.google.com/detail/next-pass/dffapmipddmkinnogkdkibjoellllhof), a satellite-pass tracking extension, is live on the Chrome Web Store at `v0.6.1` — developer account, store review, public listing, real users, and my name on it when it breaks.
- **Found and corrected an error in someone else's published model.** Reproducing Andrew McCalip's open *Space Datacenters* orbital-radiator model, I found that its cosine-tilt view-factor heuristic underestimated the edge-on per-face Earth view factor by roughly **12×**. With exact tilted-plate-to-sphere geometry, the equilibrium temperature moves **+6.35 K** (335.75 K → 342.10 K). The correction, the derivation, and the verification script are published: [DOI 10.5281/zenodo.20695720](https://doi.org/10.5281/zenodo.20695720).
- **Found a false negative in my own safety instrument.** In an agent-economy simulation, the kill criterion that was supposed to detect runaway credit spirals passed every honest-behavior test and **missed genuine spirals**. It took four versions (v0–v3) before it held. I published that as the headline result.

*Method, in one line:* I direct multi-model workflows — Claude drafts and builds, a second vendor's model is prompted to attack the output, and the workflow is human-in-the-loop by design. I diagnosed the false negative, I found the view-factor error, and I am accountable for every disposition.

**ORCID:** [0009-0009-9504-0796](https://orcid.org/0009-0009-9504-0796) · **LinkedIn:** [dan-lee-odinson](https://www.linkedin.com/in/dan-lee-odinson/) · **Email:** dan.lee.odinson [at] gmail dot com

---

## Self-published technical record — preprints, not peer reviewed

Ten DOI-archived Zenodo works — **eight preprints and two versioned software packages**, across eleven version DOIs — in three research programs. All ORCID-linked, all versioned, all reproducible. **No qualified human engineer has externally reviewed any of it.** That is the next thing I need, and I say so in the repositories themselves.

| Program | Domain | Deposits |
|---|---|---|
| [**Orbital Thermal Bounds**](https://github.com/dan-lee-odinson/orbital-thermal-bounds) | Spacecraft thermal control · heat rejection · radiator sizing | [Bounds preprint](https://doi.org/10.5281/zenodo.20650893) · [Edge-on geometry + McCalip correction](https://doi.org/10.5281/zenodo.20695720) · [AI1 design point (SpaceX)](https://doi.org/10.5281/zenodo.20670771) · [Software `v1.1.0`](https://doi.org/10.5281/zenodo.20709241) |
| [**ISONOMIA / Path A**](https://github.com/dan-lee-odinson/isonomia-path-a) | Agent-based simulation · mechanism design · adversarial robustness | [Design paper](https://doi.org/10.5281/zenodo.21343917) · [Evidence release `v1.0.0`](https://doi.org/10.5281/zenodo.21287289) · [Docs release `v1.1.0`](https://doi.org/10.5281/zenodo.21348073) |
| [**The Peership Corpus**](https://github.com/dan-lee-odinson/peership-corpus) | AI governance · constitutional design · research provenance | [I. Gods and Slaves](https://doi.org/10.5281/zenodo.21313987) · [II. Peership: A Framework](https://doi.org/10.5281/zenodo.21315519) · [III. The ISONOMIA Commons](https://doi.org/10.5281/zenodo.21343917) · [IV. Constitution, Not Cage](https://doi.org/10.5281/zenodo.21325361) · [V. The Peership Thesis](https://doi.org/10.5281/zenodo.21359124) |

Paper III is cross-listed: it is the ISONOMIA design paper and corpus paper III, counted once.

---

## Selected work

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

## The method

Claude drafts and builds; a second vendor's model is prompted to attack the result, and the attack prompts are published so a reader can verify the reviewer was told to attack rather than to bless. Nothing is accepted or rejected by a model — the workflow is **human-in-the-loop** by design and a human is accountable for every call.

Provenance is testable: DOI-versioned deposits with concept and exact-version identifiers kept distinct, SHA-256 checksums proving committed artifacts are byte-identical to their archival deposits, CI/CD-enforced pytest suites, evidence pinned to an exact release and commit hash. The Peership repository carries the fullest form of that apparatus — a 161-entry bibliographic database, a 70-claim provenance ledger recording each claim's source, evidentiary strength, and counterevidence, and per-paper adversarial reviews with their prompts published. Its first adversarial review returned **FAIL** and killed the draft's central claim; that claim is absent from the published paper.

Every artifact I publish names, in its own text, the claims it does not establish. That is not verification and validation. It is the precondition for it.

---

## Operational track record

**Eleven years in enterprise HCM implementation** — software delivery, project leadership, client enablement, requirements gathering, escalation handling, and technical support.

I've since moved into an internal **SME support team**: triaging incoming issues, unblocking the consultants running live implementations, and owning the support queue.

Triage under time pressure, escalation paths, unblocking operators mid-procedure — those are the transferable parts, not the domain. I have not done mission operations, and I am not going to claim that a support queue is the same thing as one.

`anomaly triage` · `escalation management` · `requirements analysis` · `technical program management`

---

## Continuing education

**B.S. Space Studies — Everglades University** (began April 2026; in progress). Currently in *Aviation Law & Regulations*; upcoming: General Physics, GPS Surveying, Spacecraft Systems & Design.

**Certifications.** Google Project Management Professional Certificate — in progress. AWS track (Cloud Practitioner → SysOps → Advanced Networking) via hands-on lab environments.

**Programming and systems.** Python is the primary language — automation, simulation, data analysis. Supporting work in SQL, Bash/Linux, and cloud operations.

**[Reading list](https://github.com/dan-lee-odinson/reading-list)** — spaceflight history, propulsion, autonomous systems, systems thinking, with a written reflection on each finished book.

**[Artemis Smartwatch](https://github.com/dan-lee-odinson/circuitmess-artemis-smartwatch)** — ESP32 kit assembly underway; first embedded hardware project. Build log in progress; no code published yet.

Member: AIAA · IEEE (Robotics & Automation Society; Aerospace & Electronic Systems Society) · The Planetary Society.

---

## What's next

Planned work, not accomplishments:

- **External engineering review** of the Orbital Thermal Bounds Phase B transport and pressure claims. The model needs a qualified human reviewer, and until it has one, the repository says so.
- **ROS 2 fundamentals**, then a rover build, then SLAM/perception and computer vision.
- **[RMPC servicing payload concept](https://github.com/dan-lee-odinson/rmpc-servicing-payload-concept)** — an independent concept study for an ORU-style robotic on-orbit servicing validation payload (grapple/release, relocation, alignment verification, inspection support), written up as a [concept page](https://dan-lee-odinson.github.io/rmpc-servicing-payload-concept/). Team-forming toward a prospective NASA TechLeap application: no team recruited, no application submitted. Not an official NASA, TechLeap, or Luminary Labs project.

---

## Where I'm headed

Mission operations, systems engineering, technical program management, and solutions engineering in the space sector.

I am not claiming to be an astrophysicist or a flight-qualified engineer. I am claiming that I can direct rigorous technical work, verify it, publish it with its limits intact, and be accountable for it — and that the record above is checkable.

**[LinkedIn](https://www.linkedin.com/in/dan-lee-odinson/)** · **[ORCID 0009-0009-9504-0796](https://orcid.org/0009-0009-9504-0796)** · dan.lee.odinson [at] gmail dot com
