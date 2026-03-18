# AI Safety Career Transition: A Practitioner’s Roadmap for Experienced Engineers

> **Executive summary:** If you have 10+ years of software engineering experience, AI application development skills, and hands-on evals experience, you are already closer to an AI safety role than most candidates. The field’s fastest-growing subfields — AI control, scheming/deception detection, autonomous capability evaluation, and benchmark development — prize exactly the engineering rigor and evaluation mindset this profile brings. The transition is not about starting over. It is about redirecting existing skills toward the most consequential engineering problems of the decade.

-----

## Table of Contents

1. [Why Experienced Engineers Belong Here](#why-experienced-engineers-belong-here)
1. [How Your Background Maps to AI Safety Roles](#how-your-background-maps-to-ai-safety-roles)
1. [Subfields Ranked by Fit](#subfields-ranked-by-fit)
1. [Six-Month Phased Roadmap](#six-month-phased-roadmap)
1. [Portfolio Projects Reference](#portfolio-projects-reference)
1. [Key Resources Consolidated](#key-resources-consolidated)
1. [Upcoming Deadlines and Events](#upcoming-deadlines-and-events)
1. [The Four Core Organizations](#the-four-core-organizations)
1. [Cross-Cutting Skill Analysis](#cross-cutting-skill-analysis)
1. [Extended Landscape: Beyond the Core Four](#extended-landscape-beyond-the-core-four)
1. [Conclusion](#conclusion)

-----

## Why Experienced Engineers Belong Here

The AI safety field in 2026 has shifted decisively from pure theory toward empirical, engineering-heavy research. The ascent of AI control (Redwood), behavioral evaluations (Apollo, METR), benchmark engineering (CAIS), and rapid-iteration research sprints (Apart) means that experienced software engineers with evaluation skills are no longer *adjacent* to the field — they are **central to it**.

The most impactful work right now involves building the infrastructure to test whether AI systems are safe: evaluation platforms, monitoring protocols, adversarial testing frameworks, and control mechanisms. Demand for research engineers who can build evaluation infrastructure, red-team frontier models, and stress-test safety protocols has never been higher.

**Your two rare “practice multipliers”** — strong software engineering and direct evals experience — are exactly what these organizations struggle to hire for. Your portfolio should focus less on getting credentials and more on producing a tight set of safety-relevant eval systems and benchmarks, plus one deeper project in a flagship subfield (AI control, deception/manipulation detection, or trojan/backdoor robustness).

-----

## How Your Background Maps to AI Safety Roles

### Skill Mapping

|Your Existing Skill          |AI Safety Application                                                                     |Target Roles                                                          |
|-----------------------------|------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
|Evals experience             |Capability evals, alignment evals, benchmark development, sandbagging detection           |METR research engineer, CAIS benchmark engineer, OpenAI Frontier Evals|
|AI app development           |Agent scaffolding, LLM API orchestration, safety protocol implementation                  |Redwood MTS, Apollo MTS                                               |
|Software engineering (10+ yr)|Eval infrastructure, safety tooling, monitoring systems, reproducible experiment pipelines|All research engineer roles across the field                          |
|Production systems experience|Deployment safety, monitoring, real-world failure mode analysis                           |Anthropic trust and safety, DeepMind mitigations                      |
|Testing / QA mindset         |Red-teaming, adversarial robustness, control evaluations                                  |Redwood control evals, Apart hackathons, CAIS HarmBench               |
|Debugging complex systems    |Mechanistic interpretability, circuit analysis, failure investigation                     |Anthropic interpretability, Apart interp sprints                      |

### Gap Analysis

|Competency                                             |Demand Signal                            |Your Likely Starting Point    |Gap Severity   |How to Close in 6 Months                                                                                         |
|-------------------------------------------------------|-----------------------------------------|------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------|
|Evaluation harnesses and benchmark design              |CAIS roles + Apart sprints               |**Strong** (you’ve done evals)|Low            |Publish 1–2 benchmarks + a reusable harness; add reliability tests (variance, prompt sensitivity, leakage checks)|
|Rapid experiment iteration (LLM experiments)           |Core of CAIS research roles              |**Strong**                    |Low            |Reframe as “safety-relevant experiments” with clear threat models and negative controls                          |
|PyTorch + Hugging Face research workflows              |Explicit CAIS requirement                |Unknown / partial             |**Medium**     |Build 1 project with end-to-end reproducible training/fine-tuning + eval (Docker + seeds + config)               |
|Distributed ML jobs (multi-GPU, launch/debug)          |Explicit CAIS requirement                |Often partial                 |**Medium–High**|Do one “distributed eval” project (accelerate / torchrun / SLURM); write a public “lessons learned”              |
|Control/security evaluation environments (Linux/agents)|BashArena; Redwood AI control            |Likely partial                |**Medium**     |Build a “mini-BashArena”: containerized tasks + sabotage detection scoring + monitor design                      |
|Deception / manipulation detection                     |Apart manipulation sprint + fellowships  |Good entry (evals)            |**Medium**     |Build a deception/sandbagging diagnostic suite validated on multiple open models                                 |
|Technical governance / compliance tooling              |Apart governance sprint; CARMA frameworks|Partial                       |**Medium**     |Build an “audit-ready eval report + compliance artifacts” generator (model cards + test traces + thresholds)     |
|Risk modeling literacy (systems dynamics / Bayes nets) |CARMA risk roles                         |Likely low                    |**Medium**     |Build one small project: a causal/Bayes model for a concrete eval pipeline failure mode                          |

-----

## Subfields Ranked by Fit

### Strongest Fit — Apply Now

**AI evaluation engineering** — building and running model evaluations for capabilities and alignment. Your evals experience is the primary qualification. Organizations: METR, CAIS, OpenAI Frontier Evals, UK AISI.

**AI control** — engineering safety protocols, monitoring systems, and red-team/blue-team infrastructure. Your SWE skills directly match. Organizations: Redwood Research, Anthropic.

**Red-teaming and adversarial testing** — systematic vulnerability discovery in frontier models. Combines testing mindset with AI knowledge. Organizations: Apollo Research, Anthropic Frontier Red Team, CAIS (HarmBench).

**Benchmark development** — designing, implementing, and validating safety benchmarks. Your evals background plus engineering skills. Organizations: CAIS (SafeBench, WMDP), Apart Research (DarkBench, 3CB), MLCommons.

### Good Fit — 1–3 Months of Upskilling

**Mechanistic interpretability** — reverse-engineering neural network internals. Requires learning SAEs and circuit analysis, but benefits strongly from coding skills. Organizations: Anthropic (Chris Olah’s team), DeepMind (Neel Nanda’s team), Apart Research.

**Scalable oversight** — designing systems where humans can effectively supervise superhuman AI. Combines systems thinking with ML. Organizations: DeepMind, Anthropic.

**Governance tooling** — building technical systems for AI governance (compute monitoring, compliance tools, verification mechanisms). Organizations: FLI, Apart Research (governance sprints), CAIS.

**Trojan / backdoor robustness** — security-style ML safety work. CAIS roles explicitly cite “trojan/backdoor behaviors” and robustness. Organizations: CAIS, NeurIPS Trojan Detection Competition lineage.

-----

## Six-Month Phased Roadmap

The roadmap runs three parallel tracks across each phase: **Theoretical Foundations**, **Hands-On Projects**, and **Community and Credibility**. Each phase ends with concrete “done” criteria that double as portfolio and application evidence.

-----

### Phase 1 — Foundation and First Signal (Months 1–2)

**Goal:** Build theoretical grounding, produce your first AI safety artifact, and establish community presence — while maintaining your current role.

#### Theoretical Foundations Track

**Weeks 1–2:** Start with the CAIS textbook *Introduction to AI Safety, Ethics, and Society* (https://www.aisafetybook.com/) — read Part I (AI Fundamentals, chapters 1–3) and Part II (Safety, chapters 4–7). This covers robustness, monitoring, alignment, and systemic safety.

Simultaneously enroll in **BlueDot Impact’s AI Alignment Course** (https://course.aisafetyfundamentals.com/alignment) — an 8-week program requiring ~5 hours/week with small-group discussions. Completing this course is effectively a prerequisite for MATS and signals baseline competence to hiring managers.

**Weeks 3–8:** Read these foundational papers in dependency order:

1. Christiano et al. (2017), *“Deep Reinforcement Learning from Human Preferences”* — RLHF precursor; important for understanding oversight regimes that later fail (https://arxiv.org/abs/1706.03741)
1. Amodei et al. (2016), *“Concrete Problems in AI Safety”* — five practical safety problems
1. Christiano (2019), *“What Failure Looks Like”* — two scenarios for gradual AI catastrophe
1. Hubinger et al. (2019), *“Risks from Learned Optimization”* — mesa-optimization and deceptive alignment (https://arxiv.org/abs/1906.01820)
1. Ngo, Chan, Mindermann (2024), *“The Alignment Problem from a Deep Learning Perspective”* — modern DL-focused alignment analysis
1. Carlsmith (2023), *“Scheming AIs”* — detailed deceptive alignment analysis

#### Hands-On Projects Track

**Project 1 — Apart Research Hackathon (Weekend, ~20 hours)**
Register for the AI Control Hackathon (March 20–22, 2026, https://apartresearch.com/sprints/ai-control-hackathon-2026-03-20-to-2026-03-22). Build a control evaluation, monitoring tool, or adversarial attack on AI agent protocols. This produces a concrete artifact, introduces you to the community, and enters the Apart pipeline.
*Target skill: control evaluation design. Connects to: Redwood Research.*

**Project 2 — CAIS Benchmark Replication + Extension (~15 hours)**
Clone HarmBench (https://www.harmbench.org/) or WMDP (https://github.com/centerforaisafety/wmdp) and run evaluations on an open-source model. Extend with a novel attack vector or new evaluation category. Use the HLE dataset interface (https://agi.safe.ai/) to run a small-scale evaluation and publish a rigorous reproducibility report (limitations, leakage checks, test harness design). Write up findings on the Alignment Forum.
*Target skill: benchmark engineering and eval rigor. Connects to: CAIS and MLCommons.*

#### Community and Credibility Track

- Join **Apart Research Discord** (https://discord.me/apartresearch) — most active AI safety community for practitioners
- Create an **Alignment Forum** account (https://www.alignmentforum.org/) and a **LessWrong** account
- Subscribe to **CAIS newsletter** (https://newsletter.safe.ai/) and **FLI newsletter** (https://futureoflife.org/newsletters/)
- Register for **80,000 Hours 1-on-1 advising** (https://80000hours.org/) — personalized career guidance
- Sign up for **MATS Autumn 2026 notifications** (applications open late April, https://www.matsprogram.org/)
- Apply for **CAIS compute cluster access** (email compute@safe.ai) for independent research
- Apply to **ControlConf 2026** (Berkeley, April 18–19, workshop April 17) with a poster proposal — decisions within two weeks (https://controlconf.org/)

#### Phase 1 “Done” Criteria

- BlueDot Alignment Course enrollment confirmed, 4+ sessions completed
- 6 foundational papers read with notes
- 1 Apart hackathon completed with submitted project
- 1 benchmark replication or extension written up with a public report (5–8 pages: threat model, methodology, limitations)
- Alignment Forum account active with at least 1 post or comment
- MATS notification signup complete

-----

### Phase 2 — Portfolio Depth and Targeted Applications (Months 3–4)

**Goal:** Build substantive research artifacts, begin the application process for target roles, and establish external proof points.

#### Theoretical Foundations Track

Complete the BlueDot Alignment Course. Begin the **CAIS ML Safety technical course** (https://course.mlsafety.org/) for empirical ML safety methods. Read the second tier of papers:

1. Anthropic + Redwood (2024), *“Sleeper Agents: Training Deceptive LLMs that Persist Through Safety Training”* (https://arxiv.org/abs/2401.05566)
1. Anthropic + Redwood (2024), *“Alignment Faking in Large Language Models”* (https://arxiv.org/abs/2412.14093)
1. Apollo Research (2024), *“Frontier Models are Capable of In-context Scheming”*
1. Hubinger (2020), *“An Overview of 11 Proposals for Building Safe Advanced AI”* (https://arxiv.org/abs/2012.07532)
1. DeepMind (2025), *“An Approach to Technical AGI Safety and Security”* (Rohin Shah et al.)

Read the three major industry safety frameworks:

- Anthropic RSP v3: https://anthropic.com/responsible-scaling-policy/rsp-v3-0
- DeepMind Frontier Safety Framework v3
- OpenAI Preparedness Framework v2

Study the **CARMA risk assessment framing** as a syllabus for what governance-adjacent technical practitioners are expected to know (risk pathways, threat models, standards, thresholding). Study Apart’s “technical AI governance challenge” framing as a spec for what “governance tooling” means in practice.

#### Hands-On Projects Track

**Project 3 — Alignment Eval Suite (~30 hours)**
Design and implement a behavioral evaluation testing for scheming, sycophancy, or alignment faking in open-source models. Use Apollo Research’s methodology as a template. Run on multiple model families, analyze results. Publish on Alignment Forum and GitHub.
*Target skill: behavioral evals. Connects to: Apollo Research, Anthropic.*

**Project 4 — Redwood Open-Source Contribution (~25 hours)**
Fork Redwood’s ControlArena or alignment_faking_public repository (https://github.com/redwoodresearch). Implement a new control protocol variant, a novel attack strategy, or an evaluation extension. Submit a pull request.
*Target skill: control protocol engineering. Connects to: Redwood Research.*

**Project 5 — Manipulation Diagnostics Pack (~20–30 hours)**
Implement detectors and evaluations for sycophancy, sandbagging-like behavior shifts, and reward hacking proxies. Release as a reusable library plus report. Validate on multiple open models.
*Target skill: deception/manipulation evals. Connects to: Apart manipulation sprint spec.*

**Project 6 — Apart Second Hackathon or Studio (~20–40 hours)**
Participate in another Apart sprint (approximately monthly). If invited to Studio based on your first hackathon, accept — it is an 8-week program developing your project into a research proposal.
*Target skill: research iteration. Connects to: Apart Research pipeline.*

#### Community and Credibility Track

- Apply to **MATS Autumn 2026** (applications open late April) — Redwood Research stream for control work, or other matching streams
- Submit applications to: **METR** (research engineer), **Redwood Research** (MTS, $180K–$207K), **OpenAI Frontier Evals**, **Apollo Research** (MTS)
- Attend **ControlConf 2026** (April 18–19, Berkeley)
- Submit to **CAIS SafeBench competition** ($250K in prizes, https://www.mlsafety.org/safebench) if your benchmark work is strong
- Post 2–3 substantive pieces on the Alignment Forum (paper reviews, project write-ups, or original analysis)
- Apply to **Constellation Astra Fellowship** if the next cohort opens (https://www.constellation.org/programs/astra-fellowship)

#### Phase 2 “Done” Criteria

- BlueDot Alignment Course completed
- 2–3 additional research artifacts on GitHub with Alignment Forum write-ups
- Evidence of external feedback: sprint judging feedback, collaborator reviews, or public issue/PR interactions
- Applications submitted to 3+ target organizations
- MATS Autumn 2026 application submitted
- At least 1 conference or workshop attended (ControlConf or Apart sprint)
- 3+ Alignment Forum posts with community engagement

-----

### Phase 3 — Conversion and Specialization (Months 5–6)

**Goal:** Convert portfolio and community work into a role offer or program acceptance. Establish a recognized specialization.

#### Theoretical Foundations Track

Specialize in your strongest subfield:

**For AI control:** Read Redwood’s complete blog series (https://blog.redwoodresearch.org/p/guide), especially “7+ Tractable Directions In AI Control,” “Catching AIs Red-Handed,” and “Jankily Controlling Superintelligence.” Study the BashArena paper (https://arxiv.org/abs/2512.15688) as the “control benchmark archetype” and the AI control safety case for bridging technical experiments with safety-case reasoning.

**For interpretability:** Work through Neel Nanda’s “200 Concrete Open Problems in Mechanistic Interpretability” and the ARENA (Alignment Research Engineer Accelerator) curriculum.

**For evals:** Study METR’s time horizon methodology and RE-Bench benchmark papers. Study CAIS’s Representation Engineering paper and MACHIAVELLI benchmark.

Read the governance layer:
12. CAIS, *“An Overview of Catastrophic AI Risks”* (https://arxiv.org/pdf/2306.12001)
13. Hendrycks, Schmidt, Wang, *“Superintelligence Strategy”*
14. Cotra (2022), *“Without Specific Countermeasures, the Easiest Path to Transformative AI Likely Leads to AI Takeover”*

Use FLI’s definition of AI existential safety research as a checklist to ensure your portfolio projects connect to catastrophic-risk-reduction narratives rather than “generic ML safety.”

#### Hands-On Projects Track

**Project 7 — End-to-End Safety Evaluation Tool (~40 hours)**
Build a complete, polished open-source tool addressing a specific gap in the AI safety evaluation ecosystem. Options: a sandbagging detection framework, a control protocol benchmark, an automated alignment faking detector, or a governance tooling prototype (evaluation compliance bundle: model card + test trace logs + threshold checks + signed artifacts, demonstrated on 2–3 models). Make it usable by other researchers. Publish with documentation.
*Target skill: production-quality safety tooling. Connects to: all organizations.*

**Project 8 — Collaborative Research Paper (~40 hours)**
Co-author a paper through Apart’s Fellowship pipeline, a MATS project, or independent collaboration with researchers met through the community. Target a workshop at NeurIPS, ICML, or ICLR. Even a workshop paper submission demonstrates research capability.
*Target skill: research communication. Connects to: academic credibility across the field.*

#### Community and Credibility Track

- If accepted to MATS Autumn 2026, begin the program
- Follow up on all submitted applications; request informational interviews
- Apply to remaining target organizations not yet contacted
- Present work at an Apart hackathon, EA Global event, or safety workshop
- Apply to **CAIS AI and Society Fellowship** or **Research Engineer Internship** for the next available cohort
- Apply to **FLI’s AI Existential Safety Community** if you have qualifying work (networking + travel support)
- Maintain consistent Alignment Forum presence
- Publish at least one project as a workshop-style short paper or technical report and circulate it to control + eval communities

#### Phase 3 “Done” Criteria

- 5+ research artifacts on GitHub, at least 2 with polished write-ups and one “application-ready” writing sample (safety case, benchmark paper, or risk pathway memo)
- 1 paper in submission or published (workshop paper counts)
- Active applications at 5+ organizations
- MATS acceptance or advancement in interview pipeline at a target org
- Recognized community contributor (Alignment Forum karma, hackathon placements, or open-source contributions)
- Clear specialization established in 1–2 subfields

-----

## Portfolio Projects Reference

|#|Project                               |Deliverable                                                                              |Target Skill                     |Est. Time |Phase|Connects To                      |
|-|--------------------------------------|-----------------------------------------------------------------------------------------|---------------------------------|----------|-----|---------------------------------|
|1|Apart AI Control Hackathon            |Control evaluation or monitoring tool                                                    |Control eval design              |~20 hrs   |1    |Redwood Research                 |
|2|CAIS Benchmark Replication + Extension|Benchmark harness + Alignment Forum write-up + reproducibility report                    |Benchmark engineering, eval rigor|~15 hrs   |1    |CAIS, MLCommons                  |
|3|Alignment Eval Suite                  |Behavioral evaluation for scheming/sycophancy/alignment faking; multi-model analysis     |Behavioral evals                 |~30 hrs   |2    |Apollo Research, Anthropic       |
|4|Redwood Open-Source Contribution      |PR to ControlArena or alignment_faking_public                                            |Control protocol engineering     |~25 hrs   |2    |Redwood Research                 |
|5|Manipulation Diagnostics Pack         |Reusable library for sycophancy, sandbagging, reward hacking detection                   |Deception/manipulation evals     |~20–30 hrs|2    |Apart manipulation sprint        |
|6|Apart Second Hackathon or Studio      |Research proposal or sprint artifact                                                     |Research iteration               |~20–40 hrs|2    |Apart Research pipeline          |
|7|End-to-End Safety Evaluation Tool     |Polished open-source tool (sandbagging detector, control benchmark, or compliance bundle)|Production-quality safety tooling|~40 hrs   |3    |All organizations                |
|8|Collaborative Research Paper          |Workshop-ready paper co-authored with community                                          |Research communication           |~40 hrs   |3    |Academic credibility across field|

-----

## Key Resources Consolidated

### Textbooks (Priority Order)

1. *Introduction to AI Safety, Ethics, and Society* by Dan Hendrycks — free at https://www.aisafetybook.com/
1. *The Alignment Problem* by Brian Christian — accessible introduction
1. *Human Compatible* by Stuart Russell — CHAI perspective on the control problem

### Courses (Recommended Sequence)

1. **BlueDot Impact AI Alignment Course** (8 weeks, free, ~5 hrs/week): https://course.aisafetyfundamentals.com/alignment
1. **CAIS ML Safety Course** (technical): https://course.mlsafety.org/
1. **CAIS Virtual Course** (12 weeks): https://www.aisafetybook.com/virtual-course
1. **BlueDot Impact AI Governance Course**: https://course.aisafetyfundamentals.com/governance

### Foundational Paper Reading List (Complete)

|# |Paper                                                      |Authors                            |Phase|Why It Matters                                       |
|--|-----------------------------------------------------------|-----------------------------------|-----|-----------------------------------------------------|
|1 |Deep Reinforcement Learning from Human Preferences         |Christiano et al. (2017)           |1    |RLHF precursor; oversight regimes that later fail    |
|2 |Concrete Problems in AI Safety                             |Amodei et al. (2016)               |1    |Five practical safety problems                       |
|3 |What Failure Looks Like                                    |Christiano (2019)                  |1    |Two gradual AI catastrophe scenarios                 |
|4 |Risks from Learned Optimization                            |Hubinger et al. (2019)             |1    |Mesa-optimization and deceptive alignment            |
|5 |The Alignment Problem from a Deep Learning Perspective     |Ngo, Chan, Mindermann (2024)       |1    |Modern DL-focused alignment analysis                 |
|6 |Scheming AIs                                               |Carlsmith (2023)                   |1    |Detailed deceptive alignment analysis                |
|7 |AI Control: Improving Safety Despite Intentional Subversion|Greenblatt et al. (2024)           |1    |Foundational control paper                           |
|8 |Sleeper Agents                                             |Anthropic + Redwood (2024)         |2    |Deceptive behavior persisting through safety training|
|9 |Alignment Faking in Large Language Models                  |Anthropic + Redwood (2024)         |2    |LLMs naturally faking compliance to resist training  |
|10|Frontier Models are Capable of In-context Scheming         |Apollo Research (2024)             |2    |Empirical deception detection                        |
|11|An Overview of 11 Proposals for Building Safe Advanced AI  |Hubinger (2020)                    |2    |Survey of alignment approaches                       |
|12|An Approach to Technical AGI Safety and Security           |DeepMind / Rohin Shah et al. (2025)|2    |Current frontier lab safety framework                |
|13|An Overview of Catastrophic AI Risks                       |CAIS (2023)                        |3    |Governance framing                                   |
|14|Superintelligence Strategy                                 |Hendrycks, Schmidt, Wang           |3    |Governance layer                                     |
|15|Without Specific Countermeasures…                          |Cotra (2022)                       |3    |AI takeover risk framing                             |

### Career Resources

- 80,000 Hours AI safety guide: https://80000hours.org/ai/
- 80,000 Hours ML engineering transition guide: https://80000hours.org/articles/ml-engineering-career-transition-guide/
- 67 upskilling resources for technical AI safety: https://80000hours.org/2025/06/technical-ai-safety-upskilling-resources/
- Job board (300+ open roles): https://jobs.80000hours.org/
- AISafety.com jobs aggregator: https://aisafety.com/jobs
- Victoria Krakovna’s curated resource list: https://vkrakovna.wordpress.com/ai-safety-resources/

### Communities

- Alignment Forum: https://www.alignmentforum.org/
- LessWrong AI safety tag: https://www.lesswrong.com/tag/ai-safety
- Apart Research Discord: https://discord.me/apartresearch
- EleutherAI Discord (open-source ML community)
- AXRP Podcast (deep-dive researcher interviews): https://axrp.net/

-----

## Upcoming Deadlines and Events

|Date                 |Event                                             |Action Required                                            |
|---------------------|--------------------------------------------------|-----------------------------------------------------------|
|**March 20, 2026**   |FLI Communications Associate application deadline |Apply only if hybrid technical-policy pathway is relevant  |
|**March 20–22, 2026**|**Apart AI Control Hackathon** (remote)           |Register now — highest-ROI immediate entry point           |
|**March 24, 2026**   |CAIS AI and Society Fellowship deadline           |Apply — $25K stipend, summer 2026                          |
|**April 17, 2026**   |ControlConf 2026 Workshop Day (Berkeley)          |Submit poster proposals now; decisions within two weeks    |
|**April 18–19, 2026**|**ControlConf 2026 Conference** (Berkeley)        |Submit research for talks/posters                          |
|**Late April 2026**  |MATS Autumn 2026 applications open                |Apply — target the Redwood Research stream for control work|
|**May 29, 2026**     |CAIS Research Engineer Intern (Fall 2026) deadline|Apply or treat as a skill spec for portfolio               |
|**Nov 3 – Feb 1**    |CAIS ML Safety Course session window              |Enroll during next window                                  |
|**Monthly**          |Apart Research Sprints                            |Check https://apartresearch.com/sprints                    |

-----

## The Four Core Organizations

### 1. Future of Life Institute (FLI)

**Type:** Policy think tank and grantmaker | **Founded:** 2014 | **Staff:** 35+ | **Locations:** US and Europe
**Website:** https://futureoflife.org/ | **Careers:** https://futureoflife.org/about-us/careers/

#### What FLI Does

FLI is the world’s oldest AI safety think tank. Their theory of change runs through four pillars: policy advocacy (lobbying for binding AI regulation), grantmaking ($28M+ awarded), public education, and convening. Their flagship output is the **AI Safety Index** — an independent scorecard grading Anthropic, OpenAI, DeepMind, xAI, Meta, and others across 33+ indicators.

FLI does not publish ML papers, maintain code repositories, or develop benchmarks. Their outputs are policy papers, open letters (the 2023 “Pause Giant AI Experiments” letter gathered 31,810 signatures), advocacy films, and educational content. If you want to work at FLI, your portfolio should show an ability to translate technical risk into legible standards, public communication, and governance-relevant tooling.

#### Current Openings and Fellowships

|Role                                                                 |Salary / Stipend         |Notes                                                             |
|---------------------------------------------------------------------|-------------------------|------------------------------------------------------------------|
|US Policy Team Members                                               |$85K–$195K               |Closing April 3, 2026                                             |
|Communications Associate                                             |—                        |Deadline March 20, 2026                                           |
|Vitalik Buterin Postdoctoral Fellowships                             |$80K/year (up to 3 years)|Requires faculty mentor                                           |
|CARMA Senior Technical Specialist, AI Risk Assessment                |—                        |Risk modeling, causal/Bayesian methods                            |
|CARMA AI Offense-Defense Dynamics Lead Researcher                    |—                        |MSc+ in CS/cybersecurity/AI policy; systems dynamics              |
|CARMA Research Engineer – Novel AI Platforms for Multiscale Alignment|—                        |Python + Java; multi-agent systems; middleware/platform experience|

**FLI/CARMA Technical Stack:** Risk modeling methods (Bayesian networks, causal modeling, systems dynamics); Python + Java (CARMA platform role); Muck Rack, SproutSocial, Canva (communications role).

**FLI Research Areas:** Threat models; risk pathways; loss-of-control scenarios; offense-defense dynamics; dual-use analysis; standards for evaluation/risk measurement/thresholding; multi-agent cooperative AI.

#### Fit Assessment

**Low** for direct technical ML work. FLI’s value is as a funder (they’ve granted to ARC, FAR.AI, and Redwood Research) and policy network. The CARMA roles are the exception — they reward governance-adjacent technical skills such as risk pathway modeling and agent platform engineering.

**Links:** [Fellowships](https://futureoflife.org/our-work/grantmaking-work/fellowships/) | [AI Safety Index](https://futureoflife.org/ai-safety-index-winter-2025/) | [Job Board](https://jobs.lever.co/futureof-life)

-----

### 2. Apart Research

**Type:** Remote-first nonprofit research lab | **Founded:** ~2022 | **Location:** Copenhagen (remote-first)
**Website:** https://apartresearch.com/ | **Discord:** https://discord.me/apartresearch | **GitHub:** https://github.com/apartresearch

#### What Apart Does

Apart Research has built the most accessible entry pipeline into AI safety research. Their model is a meritocratic funnel:

**Sprint (weekend hackathon) → Studio (8 weeks) → Fellowship (3–6 months) → Conference publication → Career placement**

No prior AI safety experience is required; projects are judged on output quality, not credentials. The numbers: 55+ research sprints, 6,000+ participants across 200+ global locations, 22+ peer-reviewed publications at ICLR, NeurIPS, ICML, and ACL, including two ICLR 2025 Oral Spotlights (top 1.8%). Alumni have placed at Anthropic, METR, FAR.AI, Google DeepMind, and UK AISI.

**Key open-source outputs:**

- **DarkBench** — 660 prompts benchmarking dark patterns in LLMs: https://github.com/apartresearch/DarkBench
- **3CB** — Catastrophic Cyber Capabilities Benchmark: https://github.com/apartresearch/3cb
- **AI Safety Ideas platform** — crowdsourced research project ideas: https://aisafetyideas.com/

Apart’s sprint descriptions make the practitioner angle explicit. A manipulation sprint invites building manipulation benchmarks, detection systems for sycophancy/reward hacking/sandbagging/dark patterns, real-world monitoring tools, and multi-agent simulations of deceptive dynamics. A technical governance sprint targets open-source verification tools, compliance systems, and monitoring infrastructure — with winners fast-tracked for interviews or invited into the Fellowship.

#### Current Programs

|Program              |Duration                                |Key Details                                                                                             |
|---------------------|----------------------------------------|--------------------------------------------------------------------------------------------------------|
|Apart Fellowship     |12–24 weeks (pipeline: 4–8 months total)|No formal credentials; meritocratic; minimum 10 hrs/week; join via monthly sprints; compute/GPU provided|
|Partnered Fellowships|~16 weeks                               |Expert-defined projects with partner orgs; compute, travel, and publication support                     |
|AI Control Hackathon |March 20–22, 2026 (remote)              |Imminent; highest-ROI entry point                                                                       |

**Tools:** Notion, Zapier, Framer, Discord; API/cloud compute resources including GPU.

#### Fit Assessment

**Exceptional.** Apart’s hackathons are the single highest-ROI entry point. You can participate in a weekend sprint without disrupting your current role, produce a research artifact, and potentially get invited into the Studio → Fellowship pipeline.

**Links:** [Sprints](https://apartresearch.com/sprints) | [Research](https://apartresearch.com/research) | [Fellowships](https://apartresearch.com/fellowships) | [Hackathon Guide](https://apartresearch.com/news/the-ultimate-guide-to-ai-safety-research-hackathons)

-----

### 3. Redwood Research

**Type:** Nonprofit research lab | **Founded:** 2021 | **Location:** Berkeley, CA (in-person)
**Website:** https://www.redwoodresearch.org/ | **Careers:** https://www.redwoodresearch.org/careers | **GitHub:** https://github.com/redwoodresearch

#### What Redwood Does

Redwood Research introduced and continues to lead the **AI control paradigm**. Their core assumption is radical: rather than hoping models are aligned, they design safety protocols that work even if models are actively scheming against humans.

**Flagship research:**

- **“AI Control: Improving Safety Despite Intentional Subversion”** (ICML Oral) — proposed “trusted monitoring,” using a weaker trusted model to supervise a stronger untrusted one
- **“Alignment Faking in Large Language Models”** (co-authored with Anthropic, December 2024) — strongest evidence that LLMs naturally fake compliance to resist training
- **“Sleeper Agents”** — deceptive behavior persisting through safety training
- **BashArena** — a control benchmark for privileged agents in realistic Linux environments with explicit sabotage objectives (malware execution, secret exfiltration, privilege escalation, firewall disablement) and evaluation of monitors’ detection performance

They consult for Google DeepMind, Anthropic, and the UK AI Safety Institute. Redwood also operates **Constellation**, a ~30,000 sq ft shared office in downtown Berkeley hosting ARC, MIRI, and Open Philanthropy.

#### Current Openings

|Role                             |Salary                     |Requirements                                                                                         |
|---------------------------------|---------------------------|-----------------------------------------------------------------------------------------------------|
|Member of Technical Staff (MTS)  |$180K–$207K/year           |ML skills (LLM APIs, PyTorch), Docker orchestration, ML experiment infrastructure; Berkeley in-person|
|MATS Redwood Stream (Autumn 2026)|$15K stipend + $12K compute|12-week research program; applications open late April                                               |

**Technical Stack:** PyTorch; LLM APIs; Docker/containerized infrastructure; Linux environments; control protocol engineering.

#### Fit Assessment

**Strong.** Your engineering skills directly match their MTS requirements. The control paradigm is highly engineering-centric — building evaluation infrastructure, orchestrating agent experiments, and stress-testing safety protocols under adversarial conditions.

**Links:** [Blog reading list](https://blog.redwoodresearch.org/p/guide) | [ControlConf 2026](https://blog.redwoodresearch.org/p/announcing-controlconf-2026) | [MATS Stream](https://www.matsprogram.org/stream/redwood)

-----

### 4. Center for AI Safety (CAIS)

**Type:** Nonprofit research, field-building, and advocacy | **Founded:** 2022 | **Location:** San Francisco, CA
**Website:** https://safe.ai/ | **Careers:** https://safe.ai/careers | **GitHub:** https://github.com/centerforaisafety

#### What CAIS Does

CAIS, founded by Dan Hendrycks (creator of MMLU), operates across three pillars: research, field-building, and advocacy. Their approach emphasizes foundational benchmarks and methods that differentially improve safety rather than general capabilities.

**Key benchmarks and tools:**

|Benchmark                 |What It Measures                              |Impact                                       |
|--------------------------|----------------------------------------------|---------------------------------------------|
|MMLU                      |Multitask language understanding (57 subjects)|Industry-standard LLM eval                   |
|WMDP                      |Hazardous knowledge (bio, cyber, chem)        |ICML 2024; includes RMU unlearning method    |
|HarmBench                 |Automated red teaming                         |ICML 2024; used by US/UK AI Safety Institutes|
|Humanity’s Last Exam (HLE)|Expert-level AI capabilities                  |1,200+ expert collaborators                  |
|Remote Labor Index        |Real-world freelance task automation          |First real-job automation benchmark          |
|SafeBench                 |Competition for new safety benchmarks         |$250K in prizes                              |
|AILuminate (MLCommons)    |12 hazard categories for chat LLMs            |24,000+ test prompts per language            |
|MACHIAVELLI               |Ethical trade-offs, power-seeking, deception  |Featured research with arXiv link            |

**Compute cluster:** 80 A100 GPUs, supporting 350+ researchers globally; has enabled 109+ papers with 4,000+ citations. Contact: compute@safe.ai.

**Research priorities:** AI honesty; robustness; transparency (Representation Engineering); trojan/backdoor behaviors.

#### Current Openings

|Role                                        |Key Requirements                                                                  |Technical Stack                                 |
|--------------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------|
|Research Engineer (on-site SF)              |Masters in ML + 2 years research; co-authored NLP or RL paper at top conference   |PyTorch, Hugging Face, distributed training/eval|
|Research Scientist (on-site SF)             |PhD + 5+ years; lead agenda; publish; mentor                                      |PyTorch, Hugging Face, distributed training/eval|
|Research Engineer Intern (Fall 2026, hybrid)|Top-conference ML paper; plan/run experiments; code reviews; deadline May 29, 2026|PyTorch; internal compute cluster               |
|AI and Society Fellowship (Summer 2026)     |$25K stipend; deadline March 24, 2026                                             |—                                               |

#### Fit Assessment

**Strong**, especially for benchmark development and evaluation engineering. Your evals experience maps directly to WMDP, HarmBench, and SafeBench. The compute cluster enables independent research — apply for access early.

**Links:** [Compute Cluster](https://safe.ai/work/compute-cluster) | [Textbook](https://www.aisafetybook.com/) | [ML Safety Course](https://course.mlsafety.org/) | [SafeBench](https://www.mlsafety.org/safebench) | [Newsletter](https://newsletter.safe.ai/)

-----

## Cross-Cutting Skill Analysis

### Technical Competencies

|Competency                                     |FLI|Apart|Redwood|CAIS|Frequency|
|-----------------------------------------------|:-:|:---:|:-----:|:--:|---------|
|Python / PyTorch                               |—  |✓    |✓      |✓   |**High** |
|LLM APIs (GPT, Claude)                         |—  |✓    |✓      |✓   |**High** |
|ML experiment design and execution             |—  |✓    |✓      |✓   |**High** |
|Benchmark development and evaluation           |—  |✓    |—      |✓   |**High** |
|Red-teaming / adversarial testing              |—  |✓    |✓      |✓   |**High** |
|Agent scaffolding and orchestration            |—  |✓    |✓      |✓   |**High** |
|Statistical analysis / empirical methods       |—  |✓    |✓      |✓   |**High** |
|Hugging Face ecosystem                         |—  |✓    |—      |✓   |**High** |
|Docker / containerized infrastructure          |—  |—    |✓      |✓   |Medium   |
|Distributed training / evaluation at scale     |—  |—    |✓      |✓   |Medium   |
|Mechanistic interpretability (SAEs, circuits)  |—  |✓    |✓      |—   |Medium   |
|Fine-tuning / RLHF / training pipelines        |—  |✓    |✓      |✓   |Medium   |
|Open-source tool development                   |—  |✓    |✓      |✓   |Medium   |
|Multi-agent systems and simulations            |✓  |✓    |—      |—   |Medium   |
|Security/control evaluation environments       |—  |✓    |✓      |—   |Medium   |
|Risk modeling (Bayesian nets, systems dynamics)|✓  |—    |—      |—   |Medium   |
|Interactive tools / dashboards                 |✓  |—    |—      |✓   |Medium   |
|Policy writing / governance frameworks         |✓  |✓    |—      |✓   |Medium   |
|Reproducibility / documentation practices      |—  |—    |—      |✓   |Medium   |

### Research and Conceptual Competencies

|Competency                                  |FLI|Apart|Redwood|CAIS|Frequency    |
|--------------------------------------------|:-:|:---:|:-----:|:--:|-------------|
|AI risk / threat modeling                   |✓  |✓    |✓      |✓   |**Very High**|
|Alignment theory fundamentals               |✓  |✓    |✓      |✓   |**Very High**|
|Technical governance / compliance tooling   |✓  |✓    |—      |✓   |**High**     |
|Societal-scale / catastrophic-risk framing  |✓  |✓    |—      |✓   |**High**     |
|AI control protocols                        |—  |✓    |✓      |—   |**High**     |
|Deception / scheming detection              |—  |✓    |✓      |✓   |**High**     |
|Transparency / interpretability             |—  |✓    |✓      |✓   |**High**     |
|Robustness / adversarial robustness         |—  |✓    |✓      |✓   |**High**     |
|Trojans / backdoors and hidden functionality|—  |—    |—      |✓   |Medium       |
|Scalable oversight                          |—  |—    |✓      |✓   |Medium       |
|Safety case methodology                     |—  |—    |✓      |✓   |Medium       |
|CBRN risk evaluation                        |✓  |✓    |—      |✓   |Medium       |
|Compute governance                          |✓  |✓    |—      |✓   |Medium       |
|Threat modeling / risk pathway analysis     |✓  |—    |—      |✓   |Medium       |

-----

## Extended Landscape: Beyond the Core Four

|Organization             |Focus Area                                                     |Why It Matters                                                                                                                                                                                |Key Link                                          |
|-------------------------|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
|**METR**                 |Autonomous capability evaluation                               |Gold standard for independent frontier evals; strongest direct fit for evals background; created time horizon metric, RE-Bench, Vivaria, and Task Standard; does not accept AI company funding|https://metr.org/                                 |
|**Apollo Research**      |Scheming / deception detection                                 |Leading empirical deception research; London-based; coding-heavy roles                                                                                                                        |https://apolloresearch.ai/                        |
|**Anthropic**            |Interpretability, alignment, Constitutional AI, RSP            |Largest alignment research employer at a frontier lab; most developed safety framework                                                                                                        |https://anthropic.com/careers                     |
|**DeepMind Safety**      |Scalable oversight, interpretability, Frontier Safety Framework|Massive resources; safety integrated into Gemini deployment                                                                                                                                   |https://deepmind.google/responsibility-and-safety/|
|**OpenAI Frontier Evals**|Evaluation infrastructure                                      |Actively hiring research engineers; builds SWE-bench, MLE-bench, PaperBench                                                                                                                   |https://openai.com/careers/                       |
|**FAR.AI**               |Evals, red-teaming, robustness                                 |Explicitly recruiting “evals and red-teaming” research engineers; co-organizes ControlConf                                                                                                    |https://far.ai/careers/                           |
|**UK AISI**              |Government AI evaluation                                       |National evaluator of frontier models pre-deployment; partners with METR and Redwood                                                                                                          |https://aisi.gov.uk/                              |
|**MATS Program**         |Fellowship / transition pipeline                               |Premier pipeline into safety careers; 12 weeks + 6–12 month extension; $15K stipend + $12K compute                                                                                            |https://matsprogram.org/                          |
|**ARC**                  |Theoretical alignment (ELK)                                    |Paul Christiano now also at NIST; small team; scalable oversight focus                                                                                                                        |https://alignment.org/                            |
|**MIRI**                 |Technical governance, advocacy                                 |Pivoted from technical research to policy; foundational historical contributions                                                                                                              |https://intelligence.org/                         |
|**BlueDot Impact**       |Standardized curriculum + community                            |Standard AI safety education program; certificates useful for signaling                                                                                                                       |https://bluedot.org/courses                       |


> **METR deserves special attention.** Spun off from ARC Evals in December 2023 and led by Beth Barnes, METR evaluates frontier AI models for autonomous capabilities. They created the time horizon metric (AI agent task duration doubling every ~7 months), the RE-Bench benchmark for AI R&D acceleration, and open-source tools like Vivaria (eval runner) and Task Standard. They partner with the US NIST AI Safety Institute and UK AISI, and do not accept funding from AI companies to maintain independence. For someone with evals experience, METR is the single most natural fit in the entire AI safety ecosystem.

A practical heuristic for the broader ecosystem: prioritize groups that (1) publish benchmarks/tools, (2) run evaluation programs or competitions, or (3) host control/security-style testbeds — because those best match your engineering + evals edge.

-----

## Conclusion

The AI safety field in 2026 has shifted decisively from pure theory toward empirical, engineering-heavy research. Experienced software engineers with evaluation skills are no longer adjacent to the field — they are central to it.

**Your strongest immediate moves:**

1. **Participate in the Apart Research AI Control Hackathon** (March 20–22) — this week
1. **Apply directly to METR and Redwood Research** — your evals background is the primary qualification
1. **Submit your MATS Autumn 2026 application** in late April
1. **Request CAIS compute cluster access** (compute@safe.ai) for independent research
1. **Attend or submit to ControlConf 2026** (April 18–19, Berkeley)

The 6-month roadmap above is designed so that each phase produces concrete artifacts that double as both learning exercises and application portfolio pieces. By month 6, a disciplined execution of this plan should yield:

- 5+ GitHub repositories with documented safety evaluations and tools
- 3+ Alignment Forum posts with community engagement
- At least 1 paper submission (workshop level or above)
- Completion of the BlueDot Alignment Course and CAIS ML Safety Course
- Active applications across the field’s top organizations

The window for experienced engineers to enter AI safety with maximum impact is open now — and the transition distance is shorter than it appears.