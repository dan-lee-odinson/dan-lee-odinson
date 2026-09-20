<p align="center">
  <img
    width="100%"
    src="https://capsule-render.vercel.app/api?type=soft&height=200&color=gradient&text=Dan%20Lee-Odinson&reversal=true&fontSize=60&desc=Technical%20Program%20Management%20and%20Systems%20%7C%20Building%20Towards%20Space%20Systems%2C%20Mission%20Ops%2C%20and%20AI%20Systems%20Integration&descSize=15&descAlign=50&descAlignY=70"
    alt="Dan Lee-Odinson — Technical Program Management and Systems"
  />
</p>

<p align="center">
  <a href="https://orcid.org/0009-0009-9504-0796"><img src="https://img.shields.io/badge/ORCID-0009--0009--9504--0796-A6CE39?style=for-the-badge&logo=orcid&logoColor=white" alt="ORCID"></a>
  <a href="https://www.linkedin.com/in/dan-lee-odinson/"><img src="https://img.shields.io/badge/LinkedIn-dan--lee--odinson-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:dan.lee.odinson@gmail.com"><img src="https://img.shields.io/badge/Email-dan.lee.odinson@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

**Eleven years delivering enterprise software** — requirements, implementation, escalation triage, and unblocking the people who run live systems — now aimed at **mission operations, ground segment, and technical program management** in the space sector.

I direct multi-model AI workflows to do rigorous technical work, then publish it *with its limits intact*: twelve DOI-archived Zenodo deposits across four research programs, all ORCID-linked, all reproducible. Self-published, reproducible technical work with explicit scope limits; qualified external engineering review is the next validation step.

I scope rigorous technical work, verify it, ship it, and stand behind it. **Every claim below is checkable.**

---

## Operational track record

**Eleven years in enterprise HCM implementation** — software delivery, project leadership, requirements analysis, escalation handling, technical support. The number that matters is the **tempo**, not the total:

| | |
|---|---|
| **Throughput** | **20–35 concurrent client implementations maintained as a continuous rolling caseload**, sustained for three years at VensureHR |
| **Concurrency** | **60-client ongoing active caseload**, held continuously for seven years at HUB International |
| **Volume** | **~150 implementations at HUB International**, as sole technology specialist for the Northwest region / **~400 implementations at VensureHR**, as implementation consultant for ASO and PEO US client implementations |

A continuous, high-tempo delivery load — not a sequence of one-off projects. The queue stays full and I don't fall over. I've since moved onto an internal **SME support team**: triaging incoming issues, unblocking consultants running live implementations, owning the support queue.

What transfers is the tempo: triage under time pressure, escalation paths, unblocking operators mid-procedure, sustained load without a break in it. The domain is what the rest of this page is for.

`anomaly triage` · `escalation management` · `requirements analysis` · `technical program management`

---

## Code & tooling

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)
![Wolfram](https://img.shields.io/badge/Wolfram_Language-DD1100?style=flat-square&logo=wolframmathematica&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash%20%2F%20Linux-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)
![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=flat-square&logo=latex&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML%2FCSS-E34F26?style=flat-square&logo=html5&logoColor=white)

![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![JUnit](https://img.shields.io/badge/JUnit-25A162?style=flat-square&logo=junit5&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions_CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Gradle](https://img.shields.io/badge/Gradle-02303A?style=flat-square&logo=gradle&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=android&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white)
![Chrome Web Store](https://img.shields.io/badge/Chrome_Extension_APIs-4285F4?style=flat-square&logo=googlechrome&logoColor=white)
![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)

**Python** is the primary language — simulation, numerical analysis, automation, test suites. Closed-form derivations in **Wolfram Language**, cross-checked against the numerical implementation. **Kotlin** is the newest addition, picked up to build MUNINN on Android. My research software ships with **CI/CD-enforced pytest suites** and versioned releases.

---

## Selected projects

### 🛰️ [Orbital Thermal Bounds](https://github.com/dan-lee-odinson/orbital-thermal-bounds) — spacecraft thermal control
`Python` · `Wolfram Language` · `GitHub Actions` · `v1.1.0` · **259 passing tests**

Thermodynamic bounds and mass-trade criteria for heat rejection in orbital data centers: analytic radiator-area bounds, an executable radiator simulation package, and a Phase B chip-to-radiator architecture trade study.

**Found and corrected an error in someone else's published model.** Reproducing Andrew McCalip's open *Space Datacenters* orbital-radiator model, I found its cosine-tilt view-factor heuristic underestimated the edge-on per-face Earth view factor by roughly **12×**. With exact tilted-plate-to-sphere geometry, equilibrium temperature moves **+6.35 K** (335.75 K → 342.10 K). Correction, derivation, and verification script published: [DOI 10.5281/zenodo.20695719](https://doi.org/10.5281/zenodo.20695719).

<sub>**Scope:** reduced-order, one-node model. Not validated against flown hardware. Not for flight design, certification, or safety-critical decisions.</sub>

`spacecraft thermal control` · `radiator sizing` · `heat rejection` · `trade study`

---

### 📡 [Next Pass](https://chromewebstore.google.com/detail/next-pass/dffapmipddmkinnogkdkibjoellllhof) — shipped to the Chrome Web Store
`JavaScript` · `Chrome Extension APIs` · `N2YO API` · published `v0.6.1`

A glanceable countdown to the next visible ISS pass. Pass predictions come from the **N2YO API** — N2YO propagates the orbit, not me. What I built is the client: a 6-hour cache, graceful degradation with no key / location / network, a background worker scheduling notifications ahead of bright passes, and one-click calendar export (Google Calendar or `.ics`).

Scoped, tested, and launched by me — including the parts no agent can do: developer account, store submission, public listing, and standing behind it when it breaks. Launched to r/ISS and r/amateursatellites; an SDR operator flagged that several roadmap satellites (NOAA weather sats) are decommissioned and recommended the still-operational Meteor-M series instead. Roadmap updated.

`API integration` · `caching` · `graceful degradation` · `shipped product`

---

### 🎛️ [Failure is Not an Option](https://finaogame.com/) — playable flight director game
`TypeScript` · `HTML/CSS` · `Vite` · `GitHub Pages` · **Free browser demo**

A narrative game about the people, decisions, and responsibility of Mission Control. The first playable scenario is inspired by **Gemini VIII**: choose supplemental ground rehearsals, question your controllers, weigh incomplete reports, and make a return decision whose consequences carry into the debrief, relationships, and preparation for the next mission.

**My role spans the whole delivery:** concept, scope, historical research, narrative and art direction, multi-model AI coordination, playtesting, and release decisions. I direct the work across Claude and Codex, review the results, and own what ships. The game combines illustrated 2D scenes, Apollo-inspired controls, an original soundtrack, and a deterministic simulation with replay verification. Historical sources and fictional departures are documented rather than blended into an implied reconstruction.

One playtest exposed a design failure: the Procedures Binder revealed mission information before the player encountered it. The resulting rule now governs the Binder, Evidence, and History: **nothing appears before it is encountered in play, and every addition is visibly announced.** A small example of translating player feedback into a clear requirement and a verified change.

**Available now:** one Gemini VIII demo, ending with a Gemini IX-A preparation plan. **Long-term vision:** a campaign from Gemini toward Artemis, with decisions carrying across missions. The full campaign is in development; no release date is announced.

**[Play the demo](https://finaogame.com/demo/)** · [Source code](https://github.com/dan-lee-odinson/failure-is-not-an-option)

<sub>**Scope:** an independent, non-commercial game, not operational training or a flight-qualified simulator. Created using generative AI with human creative direction, review, and final decision-making. Not affiliated with, authorized, sponsored, or endorsed by NASA. Code: MIT; original content: CC BY 4.0, subject to the repository's licence terms and third-party exceptions.</sub>

`interactive systems` · `historical research` · `requirements & acceptance testing` · `AI-directed delivery` · `shipped product`

---

### 🚀 [Shuttle Explorer](https://shuttleexplorer.com/) — interactive Discovery STS-26
`JavaScript` · `three.js` · `WebGL` · `Blender` · `GitHub Pages` · **Live site**

STS-26 was the first launch I watched, at six years old. Discovery flying again on September 29, 1988, thirty-two months after Challenger. This is that vehicle and that mission in a browser: rotate and zoom the spacecraft, pull the assemblies apart and put them back, and switch between the launch stack, the orbiter alone, and Discovery riding NASA 905, the Boeing 747 Shuttle Carrier Aircraft.

Open the payload bay and deploy an illustrative Canadarm. Go inside a reconstructed crew cabin with the flight deck and middeck labeled. Take a main engine apart in assembled, cutaway, and separate-parts views. Four reading pages carry the mission history, the five veterans who flew it, why STS-26 stayed with me, and the source credits.

No build step, no backend, no account, no API key. Models, textures, and the Draco decoder all ship with the site. It's static files on GitHub Pages.

**Every asset's provenance is checkable.** Each one has a row in [`ASSET-LICENSE-MAP.csv`](https://github.com/dan-lee-odinson/shuttle-explorer/blob/main/ASSET-LICENSE-MAP.csv) naming its source and its rights boundary, and a `PACKAGE-MANIFEST.sha256` hashes all 98 files. The STS-26 patch is the one asset whose rights split two ways. It is public domain in the United States, having been created solely by NASA, and insignia use is restricted under 14 CFR 1221 independently of copyright, which the notices say. The asset map carries its Commons source, the hash of the full-resolution original, and the hash of the downscaled copy that ships here.

**[Explore it](https://shuttleexplorer.com/)** · [Source code](https://github.com/dan-lee-odinson/shuttle-explorer)

<sub>**Scope:** an educational visual reconstruction, not flight software, validated engineering CAD, a training system, or a physics simulation. Geometry, materials, markings, mechanisms, and separation paths are approximations, and some cabin and engine references depict later configurations. Built with AI assistance under my direction and review. Not affiliated with, authorized, sponsored, or endorsed by NASA. Code: MIT; original art and writing: CC BY 4.0, subject to the repository's licence terms and third-party exceptions.</sub>

`WebGL` · `3D reconstruction` · `historical research` · `asset provenance` · `shipped product`

---

### 📱 [MUNINN](https://github.com/dan-lee-odinson/muninn) — mission ops vocabulary trainer
`Kotlin` · `Jetpack Compose` · `Android 8.0+` · `v1.0.0` · 15 JUnit tests

An Android trainer for the working vocabulary of spacecraft operations: **154 terms** across mission operations, ground systems, spacecraft systems, and operations management, played as a six-phase campaign that follows a mission's real life from pre-launch reviews through disposal and passivation. Each phase certifies on a 12-question exam (10 correct to pass) and unlocks the next. XP climbs a rank ladder lifted straight from a control room: **Trainee → Console Operator → Flight Controller → Ops Lead → Flight Director.**

Wrong answers are drawn from the same domain as the right one, so the quiz drills the difference between neighboring concepts rather than the shape of the correct button. Game logic is plain Kotlin with no Android dependencies, covered by 15 JUnit tests. The content is one JSON file, so adding a term updates the quizzes and the phase counts at runtime. No permissions, no network, no accounts.

**My first Kotlin and first Android build**, written because I wanted it to exist. In Norse myth Odin flies two ravens; Muninn is the one that carries memory. Vocabulary is the part of mission ops you can't reason your way through — either you know what an ORR is when someone says it, or you're behind for the rest of the meeting.

**Knowing the words is not the job.** A console seat is earned in simulation runs and certification on live spacecraft, and this app provides neither. It teaches the floor.

<sub>**Scope:** definitions are original prose synthesized from the standard mission-ops literature — NASA SE Handbook, CCSDS, ECSS, and the ODMSP, all listed in the repo. A study aid, not a controlled glossary, and not affiliated with any operator or agency.</sub>

`mission operations` · `ground segment` · `Android development` · `self-directed study`

---

### ⚙️ [Adversarial Project Method](https://github.com/dan-lee-odinson/adversarial-project-method) — verification methodology, published
`Python` · framework `v1.0` · [preprint DOI](https://doi.org/10.5281/zenodo.21512209) · thirteen-gate frozen case record

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

<details>
<summary><b>📚 Full publication record</b> — 12 Zenodo deposits, 18 versions, 4 programs (click to expand)</summary>

<br>

Nine preprints and three versioned software packages. All ORCID-linked, all versioned, all reproducible.

| Program | Domain | Deposits |
|---|---|---|
| [**Adversarial Project Method**](https://github.com/dan-lee-odinson/adversarial-project-method) | Research governance · multi-model AI verification | [The Process Is the Product](https://doi.org/10.5281/zenodo.21512209) · [Software `v1.0.0`](https://doi.org/10.5281/zenodo.21536231) |
| [**Orbital Thermal Bounds**](https://github.com/dan-lee-odinson/orbital-thermal-bounds) | Spacecraft thermal control · heat rejection · radiator sizing | [Bounds preprint](https://doi.org/10.5281/zenodo.20650893) · [Edge-on geometry + McCalip correction](https://doi.org/10.5281/zenodo.20695719) · [AI1 design point](https://doi.org/10.5281/zenodo.20670771) · [Software `v1.1.0`](https://doi.org/10.5281/zenodo.20709241) |
| [**ISONOMIA / Path A**](https://github.com/dan-lee-odinson/isonomia-path-a) | Agent-based simulation · mechanism design · adversarial robustness | [Design paper](https://doi.org/10.5281/zenodo.21338479) · [Software `v1.1.0`](https://doi.org/10.5281/zenodo.21287288) |
| [**The Peership Corpus**](https://github.com/dan-lee-odinson/peership-corpus) | AI governance · constitutional design · research provenance | [I. Gods and Slaves](https://doi.org/10.5281/zenodo.21313986) · [II. Peership: A Framework](https://doi.org/10.5281/zenodo.21315518) · [III. The ISONOMIA Commons](https://doi.org/10.5281/zenodo.21338479) · [IV. Constitution, Not Cage](https://doi.org/10.5281/zenodo.21325360) · [V. The Peership Thesis](https://doi.org/10.5281/zenodo.21359123) |

<sub>Paper III is cross-listed — ISONOMIA design paper and corpus paper III, counted once.</sub>

**Provenance is testable:** DOI-versioned deposits with concept and exact-version identifiers kept distinct, SHA-256 checksums proving committed artifacts are byte-identical to their archival deposits, CI/CD-enforced pytest suites, evidence pinned to exact release and commit hashes. The Peership repository carries a 161-entry bibliographic database and a 70-claim provenance ledger recording each claim's source, evidentiary strength, and counterevidence. Its first adversarial review returned **FAIL** and killed the draft's central claim; that claim is absent from the published paper.

Also: [**The Cosmic Intelligence**](https://thecosmicintelligence.substack.com) — the Substack, where the arguments behind the deposits above get made in public: machine authority, the governance of autonomous systems, and the space industry's reasoning about both. New pieces post regularly.

Also: [**Coworking with Claude**](https://github.com/dan-lee-odinson/coworking-with-claude) — the working log and reusable skill libraries, including a published negative result: an agentic content venture that spent **~$300 and earned $4.08**, needing ~73× the revenue to break even. *AI is a workflow accelerator; "AI passive income" is a misleading frame.*

</details>

---

## Education & training

| | |
|---|---|
| 🎓 **A.A. Liberal Studies** | **Columbia College** — Sonora, CA · **2003** *(conferred)* |
| 🛰️ **B.S. Space Studies** | **Everglades University** — Boca Raton, FL · *in progress*<br><sub>Began April 2026 · **36 of 120 credits, 4.0 GPA, Dean's List** · estimated completion **Spring 2029**. Current: AVM 2120 Air Cargo. Upcoming: GPS Surveying, Spacecraft Systems & Design.</sub> |

**Completed training**

| | |
|---|---|
| 📋 **Google Project Management Professional Certificate** | Completed **31 August 2026** · seven courses, including Agile Project Management |
| 🐍 **freeCodeCamp Python Developer Certification** | Completed **29 August 2026** · roughly 300 hours across five projects that had to pass automated tests |
| 🛰️ **NASA ARSET — Fundamentals of Remote Sensing** | Certificate of completion, **6 September 2026** · NASA's certificate records participation in the training |
| ⚙️ **UNSW Sydney — Introduction to Systems Engineering** | Course certificate, **19 September 2026** · nine modules, Capability Systems Centre · [verify](https://coursera.org/verify/1E1AKF5U7UCB) |
| 🔬 **NASA Open Science Essentials** | Certificate of achievement, **19 September 2026** · NASA Science Mission Directorate |

**In progress:** NASA *Open Science 101* · Elements of AI, *Introduction to AI* · AWS *Cloud Practitioner Essentials*

**Professional memberships:** AIAA *(student)* · IEEE *(student; Robotics & Automation Society, Aerospace & Electronic Systems Society)* · INCOSE *(student)* · National Space Club Florida Committee *(student)* · The Planetary Society

**Also building:** [Artemis Smartwatch](https://github.com/dan-lee-odinson/circuitmess-artemis-smartwatch) — ESP32 kit, first embedded hardware project · [Reading list](https://github.com/dan-lee-odinson/reading-list) — spaceflight history, propulsion, autonomous systems, with a written reflection on each finished book.

---

## Where I'm headed

**Mission operations · ground segment and ground control operations · technical program management · systems engineering · AI systems integration** — in the space sector.

**Next up:** external engineering review of the Orbital Thermal Bounds Phase B transport and pressure claims (the model needs a qualified human reviewer, and until it has one the repository says so) · INCOSE ASEP · FCC Amateur Radio Technician · Amateur Space Program Design

<p align="center">
  <a href="https://orcid.org/0009-0009-9504-0796"><img src="https://img.shields.io/badge/ORCID-0009--0009--9504--0796-A6CE39?style=for-the-badge&logo=orcid&logoColor=white" alt="ORCID"></a>
  <a href="https://www.linkedin.com/in/dan-lee-odinson/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:dan.lee.odinson@gmail.com"><img src="https://img.shields.io/badge/Email-Get_in_touch-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

<p align="center">
  <a href="https://github-stats-extended.vercel.app/api/top-langs?username=dan-lee-odinson&langs_count=10&theme=default_repocard"><img src="https://github-stats-extended.vercel.app/api/top-langs?username=dan-lee-odinson&langs_count=10&theme=default_repocard" alt="Top languages"></a>
</p>
