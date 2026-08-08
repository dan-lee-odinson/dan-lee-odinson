<p align="center">
  <img
    width="100%"
    src="https://capsule-render.vercel.app/api?type=soft&height=200&color=gradient&text=Dan%20Lee-Odinson&reversal=true&fontSize=60&desc=Technical%20Program%20and%20Systems%20Manager%20%7C%20Building%20Towards%20Space%20Systems%2C%20Mission%20Ops%2C%20and%20AI%20Systems%20Integration&descSize=15&descAlign=50&descAlignY=70"
    alt="Dan Lee-Odinson — Technical Program and Systems Manager"
  />
</p>

<p align="center">
  <a href="https://orcid.org/0009-0009-9504-0796"><img src="https://img.shields.io/badge/ORCID-0009--0009--9504--0796-A6CE39?style=for-the-badge&logo=orcid&logoColor=white" alt="ORCID"></a>
  <a href="https://www.linkedin.com/in/dan-lee-odinson/"><img src="https://img.shields.io/badge/LinkedIn-dan--lee--odinson-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:dan.lee.odinson@gmail.com"><img src="https://img.shields.io/badge/Email-dan.lee.odinson@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

**Eleven years delivering enterprise software** — requirements, implementation, escalation triage, and unblocking the people who run live systems — now aimed at **mission operations, ground segment, and technical program management** in the space sector.

I direct multi-model AI workflows to do rigorous technical work, then publish it *with its limits intact*: eleven DOI-archived Zenodo deposits across four research programs, all ORCID-linked, all reproducible. Self-published, reproducible technical work with explicit scope limits; qualified external engineering review is the next validation step.

I'm not claiming to be a flight-qualified engineer. I'm claiming I can scope rigorous technical work, verify it, ship it, and be accountable for it — and that **every claim below is checkable**.

---

## Operational track record

**Eleven years in enterprise HCM implementation** — software delivery, project leadership, requirements analysis, escalation handling, technical support. The number that matters is the **tempo**, not the total:

| | |
|---|---|
| **Throughput** | **20–35 client implementations continuous caseload per quarter**, sustained for three years at VensureHR |
| **Concurrency** | **60-client active caseload**, held continuously for seven years |
| **Volume** | ~150 implementations at HUB International, as sole technology specialist for the Northwest region |

A continuous, high-tempo delivery load — not a sequence of one-off projects. The queue stays full and I don't fall over. I've since moved onto an internal **SME support team**: triaging incoming issues, unblocking consultants running live implementations, owning the support queue.

Triage under time pressure, escalation paths, unblocking operators mid-procedure, sustained tempo under continuous load — those are the transferable parts, not the domain. I have not done mission operations, and I won't claim a support queue is the same thing.

`anomaly triage` · `escalation management` · `requirements analysis` · `technical program management`

---

## Code & tooling

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Wolfram](https://img.shields.io/badge/Wolfram_Language-DD1100?style=flat-square&logo=wolframmathematica&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash%20%2F%20Linux-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)
![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=flat-square&logo=latex&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML%2FCSS-E34F26?style=flat-square&logo=html5&logoColor=white)

![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions_CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Chrome Web Store](https://img.shields.io/badge/Chrome_Extension_APIs-4285F4?style=flat-square&logo=googlechrome&logoColor=white)
![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)

**Python** is the primary language — simulation, numerical analysis, automation, test suites. Closed-form derivations in **Wolfram Language**, cross-checked against the numerical implementation. My research software ships with **CI/CD-enforced pytest suites** and versioned releases..

---

## Selected projects

### 🛰️ [Orbital Thermal Bounds](https://github.com/dan-lee-odinson/orbital-thermal-bounds) — spacecraft thermal control
`Python` · `Wolfram Language` · `GitHub Actions` · `v1.1.0` · **259 passing tests**

Thermodynamic bounds and mass-trade criteria for heat rejection in orbital data centers: analytic radiator-area bounds, an executable radiator simulation package, and a Phase B chip-to-radiator architecture trade study.

**Found and corrected an error in someone else's published model.** Reproducing Andrew McCalip's open *Space Datacenters* orbital-radiator model, I found its cosine-tilt view-factor heuristic underestimated the edge-on per-face Earth view factor by roughly **12×**. With exact tilted-plate-to-sphere geometry, equilibrium temperature moves **+6.35 K** (335.75 K → 342.10 K). Correction, derivation, and verification script published: [DOI 10.5281/zenodo.20695720](https://doi.org/10.5281/zenodo.20695720).

<sub>**Scope:** reduced-order, one-node model. Not validated against flown hardware. Not for flight design, certification, or safety-critical decisions.</sub>

`spacecraft thermal control` · `radiator sizing` · `heat rejection` · `trade study`

---

### 📡 [Next Pass](https://chromewebstore.google.com/detail/next-pass/dffapmipddmkinnogkdkibjoellllhof) — shipped to the Chrome Web Store
`JavaScript` · `Chrome Extension APIs` · `N2YO API` · published `v0.6.1`

A glanceable countdown to the next visible ISS pass. Pass predictions come from the **N2YO API** — N2YO propagates the orbit, not me. What I built is the client: a 6-hour cache, graceful degradation with no key / location / network, a background worker scheduling notifications ahead of bright passes, and one-click calendar export (Google Calendar or `.ics`).

Scoped, tested, and launched by me — including the parts no agent can do: developer account, store submission, public listing, and standing behind it when it breaks. Launched to r/ISS and r/amateursatellites; an SDR operator flagged that several roadmap satellites (NOAA weather sats) are decommissioned and recommended the still-operational Meteor-M series instead. Roadmap updated.

`API integration` · `caching` · `graceful degradation` · `shipped product`

---

### ⚙️ [Adversarial Project Method](https://github.com/dan-lee-odinson/adversarial-project-method) — verification methodology, published
`Python` · framework `v1.0` · [preprint DOI](https://doi.org/10.5281/zenodo.21512210) · thirteen-gate frozen case record

An evidence-gated review methodology for work that must survive hostile scrutiny before release. One human directs, one LLM builds, a second separately-run LLM attacks. Work moves through **gate reviews** against predefined acceptance criteria: the Builder freezes a hash-manifested packet (**configuration control** — findings are cryptographically bound to the exact bytes reviewed), the Reviewer deposits findings as data, and the human Director **dispositions every finding** on a signed record. A gate passes with zero unaccepted blockers; convergence is declared by a **stopping rule fixed before the findings are seen** — never on exhaustion.

**The result that earns the paper is a failure.** Turned on its own tooling, the loop failed **five consecutive gates** (12, 11, 12, 12, 15 findings) because each fix closed the reviewer's named probe rather than the defect class behind it. The correction — every fix must demonstrate it addressed the class, every check must be witnessed failing before it is trusted — ended the streak. Published on purpose.

`technical program management` · `gate reviews` · `configuration control` · `verification & validation`

---

### 🔬 [ISONOMIA — Path A](https://github.com/dan-lee-odinson/isonomia-path-a) — agent-based simulation
`Python` · `Monte Carlo` · `v1.1.0` · evidence pinned to commit `ba3ddb5` · 73-test suite

**The headline result is a failure I found in my own safety instrument.** The kill criterion meant to detect a runaway credit spiral took four versions (v0–v3). v2 is the interesting one: it passed honest-noise tests cleanly and **missed genuine spirals** — a false negative on the instrument that exists to catch the failure.

**Method:** 300 Latin-hypercube samples × 50 seeds × 3 demand variants = **45,000-run sweeps**, plus a separate 45,000-run out-of-sample re-certification, positive *and* negative control batteries, and seven scripted attack scenarios.

**Recorded lesson:** *a kill criterion is itself a safety mechanism and must be adversarially tested in both directions — showing that honest behavior doesn't trip it is not enough.*

<sub>**Limits:** results hold at sampled points only. Nothing is live or production-validated.</sub>

`agent-based modeling` · `Monte Carlo` · `Latin hypercube sampling` · `fault detection`

---

### 🚀 [RMPC Servicing Payload Concept](https://github.com/dan-lee-odinson/rmpc-servicing-payload-concept) — closed, unsubmitted
`HTML` · concept brief and requirements notes, published

An independent concept for an ORU-style robotic on-orbit servicing validation payload, developed for NASA TechLeap's Robotically Manipulated Payload Challenge. **I didn't assemble a team before the deadline, so I didn't compete.**

Every other project here is solo work accelerated by AI. A robotic servicing payload is not — it needs mechanical engineers, flight-hardware experience, environmental test, fabrication. **Nobody pulls off a moonshot alone; Apollo was four hundred thousand people.** The finding wasn't about the payload: I had built a portfolio and a method, but not yet the professional network that lets you convene a team against a deadline. *Building the team is the work, not the overhead around it.*

<sub>Not an official NASA, TechLeap, or Luminary Labs project.</sub>

---

<details>
<summary><b>📚 Full publication record</b> — 11 Zenodo deposits, 12 version DOIs, 4 programs (click to expand)</summary>

<br>

Nine preprints and two versioned software packages. All ORCID-linked, all versioned, all reproducible. **Preprints — not peer reviewed.**

| Program | Domain | Deposits |
|---|---|---|
| [**Adversarial Project Method**](https://github.com/dan-lee-odinson/adversarial-project-method) | Research governance · multi-model AI verification | [The Process Is the Product `v1.0`](https://doi.org/10.5281/zenodo.21512210) |
| [**Orbital Thermal Bounds**](https://github.com/dan-lee-odinson/orbital-thermal-bounds) | Spacecraft thermal control · heat rejection · radiator sizing | [Bounds preprint](https://doi.org/10.5281/zenodo.20650893) · [Edge-on geometry + McCalip correction](https://doi.org/10.5281/zenodo.20695720) · [AI1 design point](https://doi.org/10.5281/zenodo.20670771) · [Software `v1.1.0`](https://doi.org/10.5281/zenodo.20709241) |
| [**ISONOMIA / Path A**](https://github.com/dan-lee-odinson/isonomia-path-a) | Agent-based simulation · mechanism design · adversarial robustness | [Design paper](https://doi.org/10.5281/zenodo.21343917) · [Evidence release `v1.0.0`](https://doi.org/10.5281/zenodo.21287289) · [Docs release `v1.1.0`](https://doi.org/10.5281/zenodo.21348073) |
| [**The Peership Corpus**](https://github.com/dan-lee-odinson/peership-corpus) | AI governance · constitutional design · research provenance | [I. Gods and Slaves](https://doi.org/10.5281/zenodo.21313987) · [II. Peership: A Framework](https://doi.org/10.5281/zenodo.21315519) · [III. The ISONOMIA Commons](https://doi.org/10.5281/zenodo.21343917) · [IV. Constitution, Not Cage](https://doi.org/10.5281/zenodo.21325361) · [V. The Peership Thesis](https://doi.org/10.5281/zenodo.21359124) |

<sub>Paper III is cross-listed — ISONOMIA design paper and corpus paper III, counted once.</sub>

**Provenance is testable:** DOI-versioned deposits with concept and exact-version identifiers kept distinct, SHA-256 checksums proving committed artifacts are byte-identical to their archival deposits, CI/CD-enforced pytest suites, evidence pinned to exact release and commit hashes. The Peership repository carries a 161-entry bibliographic database and a 70-claim provenance ledger recording each claim's source, evidentiary strength, and counterevidence. Its first adversarial review returned **FAIL** and killed the draft's central claim; that claim is absent from the published paper.

Also: [**Coworking with Claude**](https://github.com/dan-lee-odinson/coworking-with-claude) — the working log and reusable skill libraries, including a published negative result: an agentic content venture that spent **~$300 and earned $4.08**, needing ~73× the revenue to break even. *AI is a workflow accelerator; "AI passive income" is a misleading frame.*

</details>

---

## Education & certifications

| | |
|---|---|
| 🎓 **A.A. Liberal Studies** | **Columbia College** — Sonora, CA · **2003** *(conferred)* |
| 🛰️ **B.S. Space Studies** | **Everglades University** — Boca Raton, FL · *in progress*<br><sub>Began April 2026 · estimated completion **Spring 2029**. Current: Business Ethics. Upcoming: General Physics, GPS Surveying, Spacecraft Systems & Design.</sub> |
| 📋 **Google Project Management Professional Certificate** | *in progress*<br><sub>Estimated completion **October 2026**</sub> |
| 🐍 **freeCodeCamp Python Certification** | *in progress*<br><sub>Estimated completion **Spring 2027**</sub> |
| ☁️ **AWS track** — Cloud Practitioner → SysOps → Advanced Networking | *in progress, via hands-on lab environments* |

**Professional memberships:** AIAA · IEEE (Robotics & Automation Society; Aerospace & Electronic Systems Society) · The Planetary Society

**Also building:** [Artemis Smartwatch](https://github.com/dan-lee-odinson/circuitmess-artemis-smartwatch) — ESP32 kit, first embedded hardware project · [Reading list](https://github.com/dan-lee-odinson/reading-list) — spaceflight history, propulsion, autonomous systems, with a written reflection on each finished book.

---

## Where I'm headed

**Mission operations · ground segment and ground control operations · technical program management · systems engineering · AI systems integration** — in the space sector.

**Next up:** external engineering review of the Orbital Thermal Bounds Phase B transport and pressure claims (the model needs a qualified human reviewer, and until it has one the repository says so) · OpenC3 COSMOS training · ROS 2 fundamentals → rover build → SLAM/perception and computer vision.

<p align="center">
  <a href="https://orcid.org/0009-0009-9504-0796"><img src="https://img.shields.io/badge/ORCID-0009--0009--9504--0796-A6CE39?style=for-the-badge&logo=orcid&logoColor=white" alt="ORCID"></a>
  <a href="https://www.linkedin.com/in/dan-lee-odinson/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:dan.lee.odinson@gmail.com"><img src="https://img.shields.io/badge/Email-Get_in_touch-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

<p align="center">
  <a href="https://github-stats-extended.vercel.app/api/top-langs?username=dan-lee-odinson&langs_count=10&theme=default_repocard"><img src="https://github-stats-extended.vercel.app/api/top-langs?username=dan-lee-odinson&langs_count=8&theme=default_repocard" alt="Top languages"></a>
</p>
