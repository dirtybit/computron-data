# AI Safety Practitioner’s Roadmap

You already possess the two rarest “practice multipliers” that AI safety organizations struggle to hire for: strong software engineering and direct evaluations experience. The field’s fastest-growing subfields — AI control, scheming detection, autonomous capability evaluation, and benchmark development — prize exactly the engineering rigor and evaluation mindset your profile brings.

Across the four core organizations researched (FLI, Apart Research, Redwood Research, and CAIS) plus the broader landscape, demand for research engineers who can build evaluation infrastructure, red-team frontier models, and stress-test safety protocols has never been higher. METR, Redwood Research, Apollo Research, and OpenAI’s Frontier Evals team are actively hiring for roles where evals experience is the primary qualification.

The transition is not about starting over — it’s about redirecting existing skills toward the most consequential engineering problems of the decade. A six-month plan that makes you a credible technical candidate is less about “getting a credential” and more about producing a tight portfolio of safety-relevant eval systems and benchmarks, plus one deeper project in a flagship subfield (AI control, deception/manipulation detection, or trojan/backdoor robustness).

-----

## Organization Deep Dives

### 1. Future of Life Institute (FLI) — Policy Powerhouse, Not a Technical Lab

**Overview:** FLI is the world’s oldest AI safety think tank, founded in 2014, with 35+ full-time staff across the US and Europe. Their theory of change runs through four pillars: policy advocacy (lobbying for binding AI regulation), grantmaking ($28M+ awarded), public education, and convening. Their flagship output is the AI Safety Index — an independent scorecard grading Anthropic, OpenAI, DeepMind, xAI, Meta, and others across 33+ indicators, reviewed by experts including Yoshua Bengio and Stuart Russell.

**Research Agenda:** FLI’s “grantmaking/fellowship” materials define “AI existential safety research” in terms of analyzing pathways to existential catastrophe and developing technical approaches to reduce that risk — including interpretability/verification, ensuring objectives do not incentivize deception/resource-seeking, formalisms for analyzing advanced systems, and cybersecurity threats to system integrity. They also run an “AI Existential Safety Community,” a network of faculty and researchers with membership tied to fellowship/community applications.

**Key Outputs:** FLI does not publish ML papers, maintain code repositories, or develop benchmarks. Their outputs are policy papers, open letters (the 2023 “Pause Giant AI Experiments” letter gathered 31,810 signatures), advocacy films, and educational content.

**Current Openings:**

|Role                                                                   |Details                                                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
|US Policy Team Members                                                 |$85K–$195K, closing April 3, 2026                                                               |
|Communications Associate                                               |Deadline March 20, 2026                                                                         |
|Vitalik Buterin Postdoctoral Fellowships                               |$80K/year for up to 3 years (requires faculty mentor)                                           |
|Senior Technical Specialist, AI Risk Assessment (CARMA)                |Risk pathway analyses + technical governance frameworks; 5+ years AI safety/alignment/governance|
|AI Offense-Defense Dynamics Lead Researcher (CARMA)                    |Model how AI capabilities shift offense vs. defense; MSc+ required                              |
|Research Engineer – Novel AI Platforms for Multiscale Alignment (CARMA)|Agent execution environments & multi-agent platforms; MS/PhD or equivalent; Python + Java       |

**Fit for Your Profile:** Low for direct technical work at FLI itself. However, CARMA-affiliated roles (risk assessment, offense-defense dynamics, multi-agent platform engineering) are more technically relevant. FLI’s primary value to you is as a funder (they’ve granted to ARC, FAR AI, and Redwood Research) and policy network. Monitor their grants program and newsletter for ecosystem intelligence.

**Key Links:**

- Website: https://futureoflife.org/
- Careers: https://futureoflife.org/about-us/careers/ and https://jobs.lever.co/futureof-life
- Fellowships: https://futureoflife.org/our-work/grantmaking-work/fellowships/
- AI Safety Index: https://futureoflife.org/ai-safety-index-winter-2025/
- AI Existential Safety Community: https://futureoflife.org/about-us/our-people/ai-existential-safety-community/

-----

### 2. Apart Research — The Fastest On-Ramp for Working Engineers

**Overview:** Apart Research is a remote-first nonprofit founded ~2022 in Copenhagen that has built the most accessible entry pipeline into AI safety research. Their core insight: experienced technical professionals worldwide represent an untapped talent pool. Their model is a meritocratic funnel — Sprint (weekend hackathon) → Studio (8 weeks) → Fellowship (3–6 months) → Conference publication → Career placement. No prior AI safety experience required; projects are judged on output quality, not credentials.

**Research Agenda:** Apart’s agenda spans AI security & safety, evaluation & testing, mechanistic interpretability, multi-agent systems, AI governance, and CBRN risk evaluation. Sprint themes explicitly target open-source benchmarks, monitoring/detection tools, manipulation benchmarks, detection systems for sycophancy/reward hacking/sandbagging/dark patterns, and governance-focused empirical research.

**Impact Numbers:** 55+ research sprints, 6,000+ participants across 200+ global locations, 22+ peer-reviewed publications at ICLR, NeurIPS, ICML, and ACL, including two ICLR 2025 Oral Spotlights (top 1.8%).

**Key Open-Source Outputs:**

- **DarkBench** — 660 prompts benchmarking dark patterns in LLMs (https://github.com/apartresearch/DarkBench)
- **3CB** — Catastrophic Cyber Capabilities Benchmark (https://github.com/apartresearch/3cb)
- Interpretability starter templates
- AI Safety Ideas platform: https://aisafetyideas.com/

**Current Openings/Programs:**

|Program                         |Details                                                                                                                                     |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
|Apart Fellowship                |12–24 weeks; meritocratic (output-based selection via sprints); 10+ hrs/week minimum; provides API/GPU compute, research engineering support|
|Partnered Fellowships           |~16 weeks with partner orgs; expert mentorship; compute/travel/publication support                                                          |
|Hackathons Program Manager      |Large-scale program/event management; Notion, Zapier, Framer, Discord stack                                                                 |
|“Exceptional Talent” application|General application route                                                                                                                   |

**Fit for Your Profile:** Exceptional. Apart’s hackathons are the single highest-ROI entry point. You can participate in a weekend sprint without disrupting your current role, produce a research artifact, and potentially get invited into the Studio → Fellowship pipeline. Alumni have placed at Anthropic, METR, FAR.AI, Google DeepMind, and UK AISI.

**Key Links:**

- Sprints: https://apartresearch.com/sprints
- AI Control Hackathon (Mar 20–22, 2026): https://apartresearch.com/sprints/ai-control-hackathon-2026-03-20-to-2026-03-22
- Research: https://apartresearch.com/research
- Fellowships: https://apartresearch.com/fellowships
- Discord: https://discord.me/apartresearch
- GitHub: https://github.com/apartresearch
- Hackathon guide: https://apartresearch.com/news/the-ultimate-guide-to-ai-safety-research-hackathons

-----

### 3. Redwood Research — The AI Control Pioneers

**Overview:** Redwood Research is a Berkeley-based nonprofit (founded 2021) that introduced and continues to lead the AI control paradigm. Their core assumption: rather than hoping models are aligned, design safety protocols that work even if models are actively scheming against humans. This conservative worst-case approach has become central to frontier AI safety.

**Research Agenda & Key Papers:**

- **“AI Control: Improving Safety Despite Intentional Subversion”** (ICML Oral) — proposed “trusted monitoring” using a weaker trusted model to supervise a stronger untrusted one
- **“Alignment Faking in Large Language Models”** (with Anthropic, December 2024) — strongest evidence that LLMs naturally fake compliance to resist training
- **“Sleeper Agents”** — showing deceptive behavior persists through safety training
- **BashArena** — control setting for privileged agents in realistic Linux environments, with sabotage objectives (malware execution, secret exfiltration, privilege escalation, firewall disablement) and evaluation of detection performance

**Consulting & Operations:** They consult for Google DeepMind, Anthropic, and the UK AI Safety Institute. Redwood also operates Constellation, a ~30,000 sq ft shared office in Berkeley hosting ARC, MIRI, and Open Philanthropy.

**Current Openings:**

|Role                             |Details                                                                                                                          |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
|Member of Technical Staff        |$180K–$207K/year; ML skills (LLM APIs, PyTorch), software engineering (Docker, ML experiment infrastructure); Berkeley, in-person|
|MATS Redwood Stream (Autumn 2026)|Applications open late April; 12-week research program; $15K stipend + $12K compute                                              |

**Fit for Your Profile:** Strong. Your engineering skills directly match MTS requirements. The control paradigm is highly engineering-centric — building evaluation infrastructure, orchestrating agent experiments, and stress-testing safety protocols. Redwood roles strongly reward engineers who can build realistic testbeds and evaluate offense/defense protocols under adversarial pressure.

**Key Links:**

- Website: https://www.redwoodresearch.org/
- Careers: https://www.redwoodresearch.org/careers
- Blog reading list: https://blog.redwoodresearch.org/p/guide
- ControlConf 2026 (April 18–19, Berkeley): https://controlconf.org/
- BashArena: https://www.bash-arena.com/
- GitHub: https://github.com/redwoodresearch
- MATS stream: https://www.matsprogram.org/stream/redwood

-----

### 4. Center for AI Safety (CAIS) — Benchmarks, Compute, and Field-Building

**Overview:** CAIS, founded in 2022 by Dan Hendrycks (creator of MMLU) and based in San Francisco, operates across three pillars: research, field-building, and advocacy. Their approach emphasizes a pipeline of prioritization → piloting → evaluation vs. projections → scaling/pivoting. They explicitly prioritize “foundational benchmarks and methods” that differentially improve safety rather than improving general capabilities.

**Key Benchmarks and Tools:**

|Benchmark                 |What It Measures                              |Impact                                       |
|--------------------------|----------------------------------------------|---------------------------------------------|
|MMLU                      |Multitask language understanding (57 subjects)|Industry-standard LLM eval                   |
|WMDP                      |Hazardous knowledge (bio, cyber, chem)        |ICML 2024; includes RMU unlearning method    |
|HarmBench                 |Automated red teaming                         |ICML 2024; used by US/UK AI Safety Institutes|
|Humanity’s Last Exam      |Expert-level AI capabilities                  |1,200+ expert collaborators                  |
|Remote Labor Index        |Real-world freelance task automation          |First real-job automation benchmark          |
|SafeBench                 |Competition for new safety benchmarks         |$250K in prizes                              |
|AILuminate (MLCommons)    |12 hazard categories for chat LLMs            |24,000+ test prompts per language            |
|MACHIAVELLI               |Ethical trade-offs / power-seeking / deception|Behavioral measurement in game environments  |
|Representation Engineering|Transparency / interpretability / steering    |Featured research with arXiv publication     |
|AI Dashboard              |Capability + risk indices for frontier models |Evaluation dashboard at dashboard.safe.ai    |

**Research Areas:** Honesty, robustness, transparency, and trojan/backdoor behaviors. Their compute cluster (80 A100 GPUs) supports 350+ researchers globally with 109+ papers and 4,000+ citations.

**Current Openings:**

|Role                                |Details                                                                                             |
|------------------------------------|----------------------------------------------------------------------------------------------------|
|Research Engineer (on-site SF)      |Masters + 2 years research; PyTorch + Hugging Face; distributed ML; co-authored top-conference paper|
|Research Scientist (on-site SF)     |PhD + 5 years; lead agenda; end-to-end experiments; publish and mentor                              |
|Research Engineer Intern (Fall 2026)|Deadline May 29, 2026; PyTorch; publication goal                                                    |
|AI and Society Fellowship           |Summer 2026; $25K stipend; deadline March 24, 2026                                                  |
|Communications Lead (Research)      |Translate technical research into public explainers                                                 |
|Director of Development             |5+ years nonprofit fundraising                                                                      |
|Head of Public Engagement/Comms     |10+ years senior comms                                                                              |
|Head of Social                      |5–8 years running social platforms                                                                  |

**Fit for Your Profile:** Strong, especially for benchmark development and evaluation engineering. Your evals experience maps directly to WMDP, HarmBench, and SafeBench. Note: The compute cluster may have eligibility limitations (new external applications potentially limited to Schmidt Sciences AI safety grant recipients) — verify current access policy before relying on it.

**Key Links:**

- Website: https://safe.ai/
- Careers: https://safe.ai/careers and https://jobs.lever.co/aisafety
- Compute cluster: https://safe.ai/work/compute-cluster (email compute@safe.ai)
- Textbook: https://www.aisafetybook.com/
- ML Safety course: https://course.mlsafety.org/
- GitHub: https://github.com/centerforaisafety
- SafeBench: https://www.mlsafety.org/safebench
- AI Dashboard: https://dashboard.safe.ai/
- Humanity’s Last Exam: https://agi.safe.ai/
- Newsletter: https://newsletter.safe.ai/

-----

## Cross-Cutting Skill Demand Analysis

### Most In-Demand Technical Competencies

|Competency                                      |FLI      |Apart|Redwood|CAIS|Frequency|
|------------------------------------------------|---------|-----|-------|----|---------|
|Python / PyTorch                                |—        |✓    |✓      |✓   |High     |
|LLM APIs (GPT, Claude)                          |—        |✓    |✓      |✓   |High     |
|ML experiment design & execution                |—        |✓    |✓      |✓   |High     |
|Benchmark development & evaluation              |—        |✓    |—      |✓   |High     |
|Running LLM experiments end-to-end              |—        |✓    |✓      |✓   |High     |
|Red-teaming / adversarial testing               |—        |✓    |✓      |✓   |High     |
|Agent scaffolding & orchestration               |—        |✓    |✓      |✓   |High     |
|Writing/publishing research artifacts           |—        |✓    |✓      |✓   |High     |
|Multi-agent systems & simulations               |✓ (CARMA)|✓    |—      |—   |High     |
|Hugging Face ecosystem                          |—        |—    |—      |✓   |Medium   |
|Docker / containerized infrastructure           |—        |—    |✓      |✓   |Medium   |
|Distributed training/evaluation at scale        |—        |—    |—      |✓   |Medium   |
|Security/control-style eval environments        |—        |—    |✓      |—   |Medium   |
|Mechanistic interpretability (SAEs, circuits)   |—        |✓    |✓      |—   |Medium   |
|Statistical analysis / empirical methods        |—        |✓    |✓      |✓   |High     |
|Fine-tuning / RLHF / training pipelines         |—        |✓    |✓      |✓   |Medium   |
|Open-source tool development                    |—        |✓    |✓      |✓   |Medium   |
|Platform/tooling engineering for safety research|✓ (CARMA)|—    |—      |✓   |Medium   |
|Risk modeling (Bayesian nets, systems dynamics) |✓ (CARMA)|—    |—      |—   |Low      |
|Policy writing / governance frameworks          |✓        |✓    |—      |✓   |Medium   |

### Most In-Demand Research/Conceptual Competencies

|Competency                                      |FLI      |Apart|Redwood|CAIS|Frequency|
|------------------------------------------------|---------|-----|-------|----|---------|
|AI risk / threat modeling                       |✓        |✓    |✓      |✓   |Very High|
|Alignment theory fundamentals                   |✓        |✓    |✓      |✓   |Very High|
|Societal-scale / catastrophic-risk framing      |✓        |—    |—      |✓   |High     |
|Technical governance / compliance / verification|✓ (CARMA)|✓    |—      |—   |High     |
|AI control protocols                            |—        |✓    |✓      |—   |High     |
|Deception / scheming / manipulation detection   |—        |✓    |✓      |✓   |High     |
|Transparency / interpretability as safety lever |—        |✓    |—      |✓   |High     |
|Robustness / adversarial robustness             |—        |—    |—      |✓   |Medium   |
|Trojans/backdoors and hidden functionality      |—        |—    |—      |✓   |Medium   |
|Honesty / truthfulness failures                 |—        |—    |—      |✓   |Medium   |
|Scalable oversight                              |—        |—    |✓      |✓   |Medium   |
|Safety case methodology                         |—        |—    |✓      |✓   |Medium   |
|CBRN risk evaluation                            |✓        |✓    |—      |✓   |Medium   |
|Compute governance                              |✓        |✓    |—      |✓   |Medium   |
|Catastrophic risk frameworks                    |✓        |—    |—      |✓   |Medium   |

-----

## How Your Background Maps to AI Safety

### Direct Skill-to-Role Mapping

|Your Existing Skill          |AI Safety Application                                                                     |Target Roles                                                          |
|-----------------------------|------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
|Evals experience             |Capability evals, alignment evals, benchmark development, sandbagging detection           |METR research engineer, CAIS benchmark engineer, OpenAI Frontier Evals|
|AI app development           |Agent scaffolding, LLM API orchestration, safety protocol implementation                  |Redwood MTS (Docker + agent orchestration), Apollo MTS                |
|Software engineering (10+ yr)|Eval infrastructure, safety tooling, monitoring systems, reproducible experiment pipelines|All research engineer roles across the field                          |
|Production systems experience|Deployment safety, monitoring, real-world failure mode analysis                           |Anthropic trust & safety, DeepMind mitigations                        |
|Testing/QA mindset           |Red-teaming, adversarial robustness, control evaluations                                  |Redwood control evals, Apart hackathons, CAIS HarmBench               |
|Debugging complex systems    |Mechanistic interpretability, circuit analysis, failure investigation                     |Anthropic interpretability, Apart interp sprints                      |

### Skill Gap Assessment

|Competency                               |Demand Signal                            |Your Likely Starting Point|Gap Severity|How to Close in 6 Months                                                                       |
|-----------------------------------------|-----------------------------------------|--------------------------|------------|-----------------------------------------------------------------------------------------------|
|Evaluation harnesses & benchmark design  |CAIS roles + Apart sprints               |Strong (you’ve done evals)|Low         |Publish 1–2 benchmarks + reusable harness with reliability tests                               |
|Rapid experiment iteration               |Core of CAIS research roles              |Strong                    |Low         |Reframe as “safety-relevant experiments” with threat models and negative controls              |
|PyTorch + Hugging Face research workflows|Explicit CAIS requirement                |Unknown / partial         |Medium      |Build 1 end-to-end training/fine-tuning + eval project (Docker + seeds + config)               |
|Distributed ML jobs (multi-GPU)          |Explicit CAIS requirement                |Often partial             |Medium–High |Do one “distributed eval” project (accelerate / torchrun / slurm); write public lessons learned|
|Control/security eval environments       |BashArena focus; AI control positioning  |Likely partial            |Medium      |Build a “mini-BashArena”: containerized tasks + sabotage detection + monitor design            |
|Deception/manipulation detection         |Apart manipulation sprint + fellowships  |Good entry (evals)        |Medium      |Build a deception/sandbagging diagnostic suite; validate on multiple open models               |
|Technical governance / compliance tooling|Apart governance sprint; CARMA frameworks|Partial                   |Medium      |Build an “audit-ready eval report” generator (model cards + test traces + thresholds)          |
|Risk modeling literacy                   |CARMA risk roles                         |Likely low                |Medium      |Build one causal/Bayes model for a concrete eval pipeline failure mode                         |

### Subfields Ranked by Profile Fit

**Strongest fit (apply now):**

1. **AI evaluation engineering** — building and running model evaluations for capabilities and alignment. Your evals experience is the primary qualification. *Organizations: METR, CAIS, OpenAI Frontier Evals, UK AISI.*
1. **AI control** — engineering safety protocols, monitoring systems, and red-team/blue-team infrastructure. Your SWE skills directly match. *Organizations: Redwood Research, Anthropic.*
1. **Red-teaming and adversarial testing** — systematic vulnerability discovery in frontier models. Combines testing mindset with AI knowledge. *Organizations: Apollo Research, Anthropic Frontier Red Team, CAIS (HarmBench).*
1. **Benchmark development** — designing, implementing, and validating safety benchmarks. Your evals background plus engineering skills. *Organizations: CAIS (SafeBench, WMDP), Apart Research (DarkBench, 3CB), MLCommons.*

**Good fit (1–3 months upskilling):**

1. **Mechanistic interpretability** — reverse-engineering neural network internals. Requires learning SAEs, circuit analysis, but benefits from strong coding skills. *Organizations: Anthropic (Chris Olah’s team), DeepMind (Neel Nanda’s team), Apart Research.*
1. **Scalable oversight** — designing systems where humans can effectively supervise superhuman AI. Combines systems thinking with ML. *Organizations: DeepMind, Anthropic.*
1. **Governance tooling** — building technical systems for AI governance (compute monitoring, compliance tools, verification mechanisms). *Organizations: FLI, Apart Research (governance sprints), CAIS.*

-----

## Unified Six-Month Transition Roadmap

This plan is organized into three parallel tracks (Theory, Hands-On Projects, Community & Credibility). Each phase produces concrete artifacts that double as both learning exercises and application portfolio pieces.

-----

### Phase 1: Foundations + First Signal (Months 1–2)

**Goal:** Build theoretical grounding, produce your first AI safety artifact, and establish community presence — all while maintaining your current role.

#### Theory Track

**Primary Resources (Weeks 1–2):**

- Start with the CAIS textbook *Introduction to AI Safety, Ethics, and Society* (https://www.aisafetybook.com/) — read Part I (AI Fundamentals, chapters 1–3) and Part II (Safety, chapters 4–7). Covers robustness, monitoring, alignment, and systemic safety.
- Enroll in BlueDot Impact’s AI Alignment Course (https://course.aisafetyfundamentals.com/alignment) — 8-week program, ~5 hours/week with small-group discussions. Effectively a prerequisite for MATS and signals baseline competence to hiring managers.

**Foundational Papers (Weeks 3–8), read in dependency order:**

|#|Paper                                                                                                                     |Key Concept                                                                |
|-|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
|1|Amodei et al. (2016), “Concrete Problems in AI Safety”                                                                    |Five practical safety problems                                             |
|2|Christiano (2019), “What Failure Looks Like”                                                                              |Two scenarios for gradual AI catastrophe                                   |
|3|Christiano et al., “Deep RL from Human Preferences”                                                                       |RLHF precursor; oversight regimes that later fail                          |
|4|Hubinger et al. (2019), “Risks from Learned Optimization” (https://arxiv.org/abs/1906.01820)                              |Mesa-optimization, deceptive alignment, why behavioral evals can be brittle|
|5|Ngo, Chan, Mindermann (2024), “The Alignment Problem from a DL Perspective”                                               |Modern deep learning-focused alignment analysis                            |
|6|Carlsmith (2023), “Scheming AIs”                                                                                          |Detailed deceptive alignment analysis                                      |
|7|Greenblatt et al. (2024), “AI Control: Improving Safety Despite Intentional Subversion” (https://arxiv.org/abs/2312.06942)|Foundational control paper                                                 |

#### Hands-On Projects Track

**Project 1: Apart Research Hackathon (Weekend, ~20 hours)**
Register for the AI Control Hackathon (March 20–22, 2026). Build a control evaluation, monitoring tool, or adversarial attack on AI agent protocols. This produces a concrete artifact, introduces you to the community, and enters the Apart pipeline.

- *Target skill:* Control evaluation design
- *Connects to:* Redwood Research’s work

**Project 2: Replicate a CAIS Benchmark (~15 hours)**
Clone HarmBench (https://www.harmbench.org/) or WMDP (https://github.com/centerforaisafety/wmdp) and run evaluations on an open-source model. Extend with a novel attack vector or new evaluation category. Write up findings on the Alignment Forum.

- *Target skill:* Benchmark engineering
- *Connects to:* CAIS and MLCommons work

**Alternative/Additional: Reproduce + extend a CAIS-style eval dashboard (2–3 weeks)**
Build a lightweight dashboard mirroring the “capability + risk index” idea, running on a reproducible harness. Include calibration/overconfidence metrics.

- *Target skill:* Benchmarking + dashboards + eval reliability
- *Connects to:* CAIS AI Dashboard approach

#### Community & Credibility Track

- Join Apart Research Discord (https://discord.me/apartresearch)
- Create Alignment Forum (https://www.alignmentforum.org/) and LessWrong accounts
- Subscribe to CAIS newsletter (https://newsletter.safe.ai/) and FLI newsletter (https://futureoflife.org/newsletters/)
- Register for 80,000 Hours 1-on-1 advising (https://80000hours.org/)
- Sign up for MATS Autumn 2026 notifications (https://www.matsprogram.org/)
- Apply for CAIS compute cluster access (email compute@safe.ai)

#### Phase 1 “Done” Criteria

- [ ] BlueDot Alignment Course enrollment confirmed, 4+ sessions completed
- [ ] 7 foundational papers read with written notes/summaries
- [ ] 1 Apart hackathon completed with submitted project
- [ ] 1 benchmark replication or extension written up
- [ ] 1 public repo with a clean eval harness + short report (5–8 pages) explaining threat model, methodology, and limitations
- [ ] Alignment Forum account active with at least 1 post or comment
- [ ] MATS notification signup complete

-----

### Phase 2: Portfolio Depth + Targeted Applications (Months 3–4)

**Goal:** Build substantive research artifacts and begin the application process for target roles.

#### Theory Track

**Complete and continue:**

- Complete the BlueDot Alignment Course
- Begin the CAIS ML Safety technical course (https://course.mlsafety.org/) for empirical ML safety methods

**Second-tier papers:**

|# |Paper                                                                                                       |Key Concept                                   |
|--|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
|8 |Anthropic + Redwood (2024), “Sleeper Agents” (https://arxiv.org/abs/2401.05566)                             |Deceptive LLMs persist through safety training|
|9 |Anthropic + Redwood (2024), “Alignment Faking in LLMs” (https://arxiv.org/abs/2412.14093)                   |LLMs faking compliance to resist training     |
|10|Apollo Research (2024), “Frontier Models are Capable of In-context Scheming”                                |Empirical deception research                  |
|11|Hubinger (2020), “Overview of 11 Proposals for Building Safe Advanced AI” (https://arxiv.org/abs/2012.07532)|Landscape of safety proposals                 |
|12|DeepMind (2025), “An Approach to Technical AGI Safety and Security” (Rohin Shah et al.)                     |Industry safety framework                     |

**Technical safety pillars (matched to org agendas):**

- *Transparency/interpretability:* CAIS’s “Representation Engineering” paper (https://arxiv.org/abs/2310.01405)
- *Agentic risk & ethical behavior:* CAIS’s MACHIAVELLI benchmark paper (https://arxiv.org/abs/2304.03279)
- *Control framing:* ControlConf framing + BashArena paper (https://arxiv.org/abs/2512.15688)

**Industry safety frameworks (read all three):**

- Anthropic RSP v3: https://anthropic.com/responsible-scaling-policy/rsp-v3-0
- DeepMind Frontier Safety Framework v3
- OpenAI Preparedness Framework v2

#### Hands-On Projects Track

**Project 3: Build an Alignment Eval Suite (~30 hours)**
Design and implement behavioral evaluations testing for scheming, sycophancy, or alignment faking in open-source models. Use Apollo Research’s methodology as a template. Run on multiple model families, analyze results. Publish on Alignment Forum and GitHub.

- *Target skill:* Behavioral evals
- *Connects to:* Apollo Research, Anthropic

**Project 4: Contribute to Redwood’s Open-Source Control Infrastructure (~25 hours)**
Fork Redwood’s ControlArena or alignment_faking_public repository. Implement a new control protocol variant, novel attack strategy, or evaluation extension. Submit a pull request.

- *Alternative:* Build a “mini-BashArena” — containerized Linux admin tasks + sabotage objectives + scoring + monitor baseline with FPR/TPR measurement (4–6 weeks)
- *Target skill:* Control protocol engineering
- *Connects to:* Redwood Research

**Project 5: Apart Research Second Hackathon or Studio (~20–40 hours)**
Participate in another Apart sprint. If invited to Studio based on first hackathon performance, accept — it’s an 8-week program developing your project into a research proposal.

- *Target skill:* Research iteration
- *Connects to:* Apart Research pipeline

**Project 6 (Optional): Trojan/Backdoor Detection Baseline Suite (3–5 weeks)**
Pipeline that plants triggers in small open models (or uses existing backdoored checkpoints) and tests detection methods. Publish eval harness + results.

- *Target skill:* Robustness, backdoor detection, dataset discipline
- *Connects to:* CAIS trojan/backdoor emphasis and trojan competition lineage

#### Community & Credibility Track

- Apply to MATS Autumn 2026 (applications open late April) — Redwood Research stream for control work
- Submit applications to: METR (research engineer), Redwood Research (MTS, $180K–$207K), OpenAI Frontier Evals, Apollo Research (MTS)
- Attend ControlConf 2026 (April 18–19, Berkeley) — submit poster proposal even if preliminary
- Submit to CAIS SafeBench competition ($250K in prizes) if benchmark work is strong
- Post 2–3 substantive pieces on the Alignment Forum
- Apply for Constellation Astra Fellowship if next cohort opens (https://www.constellation.org/programs/astra-fellowship)

#### Phase 2 “Done” Criteria

- [ ] BlueDot Alignment Course completed
- [ ] 2–3 additional research artifacts on GitHub with Alignment Forum write-ups
- [ ] 1 “deep project” repo (mini-BashArena or trojan suite or governance prototype) with reproducible runs and clear eval protocol
- [ ] Applications submitted to 3+ target organizations
- [ ] MATS Autumn 2026 application submitted
- [ ] At least 1 conference or workshop attended (ControlConf or Apart sprint)
- [ ] 3+ Alignment Forum posts with community engagement
- [ ] Evidence of external feedback: sprint judging, collaborator reviews, or public issue/PR interactions

-----

### Phase 3: Conversion + Specialization (Months 5–6)

**Goal:** Convert portfolio and community work into a role offer or program acceptance.

#### Theory Track

**Specialize in your strongest subfield:**

- *For AI control:* Read Redwood’s complete blog series (https://blog.redwoodresearch.org/p/guide), especially “7+ Tractable Directions In AI Control,” “Catching AIs Red-Handed,” and “Jankily Controlling Superintelligence”
- *For interpretability:* Work through Neel Nanda’s “200 Concrete Open Problems in Mechanistic Interpretability” and the ARENA curriculum
- *For evals:* Study METR’s time horizon methodology and RE-Bench benchmark papers

**Governance literacy for practitioners:**

- CAIS, “An Overview of Catastrophic AI Risks” (https://arxiv.org/pdf/2306.12001)
- Hendrycks + Schmidt + Wang, “Superintelligence Strategy”
- Cotra (2022), “Without Specific Countermeasures, the Easiest Path to Transformative AI Likely Leads to AI Takeover”
- CARMA’s risk assessment framing (study role requirements as a “syllabus”)
- Apart’s “technical AI governance challenge” framing (verification tools, compliance systems, monitoring infrastructure)
- FLI’s definition of AI existential safety research (connect portfolio to catastrophic-risk-reduction narratives)

#### Hands-On Projects Track

**Project 7: End-to-End Safety Evaluation Tool (~40 hours)**
Build a complete, polished open-source tool addressing a specific gap in the AI safety evaluation ecosystem. Options: sandbagging detection framework, control protocol benchmark, automated alignment faking detector, or a “manipulation diagnostics pack” (sycophancy, sandbagging-like behavior shifts, reward hacking proxies as a reusable library). Make it usable by other researchers. Publish with documentation.

- *Target skill:* Production-quality safety tooling
- *Connects to:* All organizations

**Project 8 (Optional): Governance Tooling Prototype (3–5 weeks)**
Build an “evaluation compliance bundle” generator: model card + test trace logs + threshold checks + signed artifacts. Demonstrate on 2–3 models.

- *Target skill:* Technical governance / auditability
- *Connects to:* Apart technical governance sprint; CARMA standards/thresholding

**Project 9: Collaborative Research Paper (~40 hours)**
Co-author a paper through Apart’s Fellowship pipeline, a MATS project, or independent collaboration. Target a workshop at NeurIPS, ICML, or ICLR. Even a workshop paper submission demonstrates research capability.

- *Target skill:* Research communication
- *Connects to:* Academic credibility across the field

#### Community & Credibility Track

- If accepted to MATS Autumn 2026, begin the program
- Follow up on all submitted applications; request informational interviews
- Apply to remaining target organizations not yet contacted
- Present work at an Apart hackathon, EA Global event, or safety workshop
- Apply to CAIS AI and Society Fellowship or Research Engineer Internship for next cohort
- Apply to FLI’s AI Existential Safety Community for faculty/researcher networking + travel support
- Maintain consistent Alignment Forum presence
- Publish at least one project as a workshop-style short paper or technical report; circulate to relevant communities

#### Phase 3 “Done” Criteria

- [ ] 5+ research artifacts on GitHub, at least 2 with polished write-ups
- [ ] 2–3 polished portfolio artifacts, each mapped to a target org’s agenda
- [ ] 1 paper in submission or published (workshop paper counts)
- [ ] 1 “application-ready” writing sample (safety case / benchmark paper / risk pathway memo)
- [ ] Active applications at 5+ organizations
- [ ] MATS acceptance or advancement in interview pipeline at a target org
- [ ] Recognized community contributor (AF karma, hackathon placements, or open-source contributions)
- [ ] Clear specialization established in 1–2 subfields

-----

## Extended Landscape: Organizations Beyond the Core Four

|Organization             |Focus Area                               |What It Adds                                                                                                                                                                                                                                                                                   |Key Link                                          |
|-------------------------|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
|**METR**                 |Autonomous capability evaluation         |Gold standard for independent frontier evals; strongest direct fit for evals background. Created time horizon metric, RE-Bench, Vivaria, Task Standard. Pre-deployment tested GPT-4, GPT-4.5, GPT-5, Claude 3.5 Sonnet, Claude 3.7, Claude Opus 4.6. Does not accept funding from AI companies.|https://metr.org/                                 |
|**Apollo Research**      |Scheming/deception detection             |Leading empirical deception research; London-based; coding-heavy roles                                                                                                                                                                                                                         |https://www.apolloresearch.ai/                    |
|**Anthropic**            |Interpretability, Constitutional AI, RSP |Largest alignment research employer at a frontier lab; RSP is most developed safety framework                                                                                                                                                                                                  |https://www.anthropic.com/careers                 |
|**DeepMind Safety**      |Scalable oversight, interpretability, FSF|Massive resources; safety integrated into Gemini deployment                                                                                                                                                                                                                                    |https://deepmind.google/responsibility-and-safety/|
|**OpenAI Frontier Evals**|Evaluation infrastructure                |Actively hiring research engineers; builds SWE-bench, MLE-bench, PaperBench                                                                                                                                                                                                                    |https://openai.com/careers/                       |
|**FAR.AI**               |Evals, red-teaming, robustness           |Co-organizes ControlConf with Redwood; explicitly recruiting evals and red-teaming research engineers                                                                                                                                                                                          |https://www.far.ai/careers/                       |
|**UK AISI**              |Government AI evaluation                 |National evaluator of frontier models pre-deployment; partners with METR and Redwood                                                                                                                                                                                                           |https://www.aisi.gov.uk/                          |
|**MATS**                 |Fellowship/transition program            |Premier pipeline into safety careers; 12 weeks + 6–12 month extension; $15K stipend + $12K compute                                                                                                                                                                                             |https://www.matsprogram.org/                      |
|**MIRI**                 |Technical governance, advocacy           |The OG safety org; pivoted from technical research to policy; foundational historical contributions                                                                                                                                                                                            |https://intelligence.org/                         |
|**ARC**                  |Theoretical alignment (ELK)              |Pure theory approach; Paul Christiano now also at NIST; small team                                                                                                                                                                                                                             |https://www.alignment.org/                        |

**METR deserves special attention.** For someone with evals experience, METR is the single most natural fit in the entire AI safety ecosystem. Spun off from ARC Evals in December 2023 and led by Beth Barnes, METR evaluates frontier AI models for autonomous capabilities. They partner with the US NIST AI Safety Institute and UK AISI and maintain independence by not accepting funding from AI companies.

-----

## Consolidated Resources

### Textbooks (Priority Order)

1. *Introduction to AI Safety, Ethics, and Society* by Dan Hendrycks — free at https://www.aisafetybook.com/
1. *The Alignment Problem* by Brian Christian — accessible introduction
1. *Human Compatible* by Stuart Russell — CHAI perspective on the control problem

### Courses (Recommended Sequence)

1. BlueDot Impact AI Alignment Course (8 weeks, free): https://course.aisafetyfundamentals.com/alignment
1. CAIS ML Safety Course (technical): https://course.mlsafety.org/ — session window Nov 3 to Feb 1
1. BlueDot Impact AI Governance Course: https://course.aisafetyfundamentals.com/governance
1. CAIS Virtual Course (12 weeks): https://www.aisafetybook.com/virtual-course
1. ARENA (Alignment Research Engineer Accelerator) curriculum — for mechanistic interpretability

### Career Resources

- 80,000 Hours AI safety guide: https://80000hours.org/ai/
- ML engineering transition guide: https://80000hours.org/articles/ml-engineering-career-transition-guide/
- 67 upskilling resources for technical AI safety: https://80000hours.org/2025/06/technical-ai-safety-upskilling-resources/
- Job board (300+ open roles): https://jobs.80000hours.org/
- AISafety.com jobs aggregator: https://www.aisafety.com/jobs
- Victoria Krakovna’s curated resource list: https://vkrakovna.wordpress.com/ai-safety-resources/

### Communities

- Alignment Forum: https://www.alignmentforum.org/
- LessWrong AI safety tag: https://www.lesswrong.com/tag/ai-safety
- Apart Research Discord: https://discord.me/apartresearch
- EleutherAI Discord (open-source ML community)
- AXRP Podcast (deep-dive researcher interviews): https://axrp.net/

### Complete Reading List (All 14 Papers)

|# |Paper                                                                                  |Phase|
|--|---------------------------------------------------------------------------------------|-----|
|1 |Amodei et al. (2016), “Concrete Problems in AI Safety”                                 |1    |
|2 |Christiano (2019), “What Failure Looks Like”                                           |1    |
|3 |Christiano et al., “Deep RL from Human Preferences”                                    |1    |
|4 |Hubinger et al. (2019), “Risks from Learned Optimization”                              |1    |
|5 |Ngo, Chan, Mindermann (2024), “The Alignment Problem from a DL Perspective”            |1    |
|6 |Carlsmith (2023), “Scheming AIs”                                                       |1    |
|7 |Greenblatt et al. (2024), “AI Control: Improving Safety Despite Intentional Subversion”|1    |
|8 |Anthropic + Redwood (2024), “Sleeper Agents”                                           |2    |
|9 |Anthropic + Redwood (2024), “Alignment Faking in LLMs”                                 |2    |
|10|Apollo Research (2024), “Frontier Models are Capable of In-context Scheming”           |2    |
|11|Hubinger (2020), “Overview of 11 Proposals for Building Safe Advanced AI”              |2    |
|12|DeepMind (2025), “An Approach to Technical AGI Safety and Security”                    |2    |
|13|CAIS, “An Overview of Catastrophic AI Risks”                                           |3    |
|14|Hendrycks + Schmidt + Wang, “Superintelligence Strategy”                               |3    |

-----

## Key Upcoming Deadlines and Events

|Event / Deadline                       |Date             |Action                                 |
|---------------------------------------|-----------------|---------------------------------------|
|Apart AI Control Hackathon             |March 20–22, 2026|Register and participate               |
|FLI Communications Associate deadline  |March 20, 2026   |Apply if relevant                      |
|CAIS AI and Society Fellowship deadline|March 24, 2026   |Apply ($25K stipend)                   |
|ControlConf 2026 workshop (Berkeley)   |April 17, 2026   |Attend; submit poster proposal         |
|ControlConf 2026 conference (Berkeley) |April 18–19, 2026|Attend; network with Redwood/FAR.AI    |
|MATS Autumn 2026 applications open     |Late April 2026  |Apply immediately (Redwood stream)     |
|CAIS Research Engineer Intern deadline |May 29, 2026     |Apply (Fall 2026 cohort)               |
|Apart Research sprints                 |~Monthly         |Check https://apartresearch.com/sprints|
|CAIS ML Safety course window           |Nov 3 – Feb 1    |Enroll when open                       |

-----

## Conclusion

The AI safety field in 2026 has shifted decisively from pure theory toward empirical, engineering-heavy research. The ascent of AI control (Redwood), behavioral evaluations (Apollo, METR), benchmark engineering (CAIS), and rapid-iteration research sprints (Apart) means that experienced software engineers with evaluation skills are no longer adjacent to the field — they are central to it.

Your strongest immediate moves:

1. **This week:** Register for the Apart AI Control Hackathon (March 20–22)
1. **This month:** Apply to CAIS AI and Society Fellowship (deadline March 24); submit ControlConf poster proposal
1. **Next month:** Attend ControlConf 2026; apply to METR and Redwood Research directly
1. **Late April:** Submit MATS Autumn 2026 application
1. **Ongoing:** Request CAIS compute cluster access; build portfolio artifacts; maintain Alignment Forum presence

By month 6, disciplined execution of this plan should produce: 5+ GitHub repositories, 3+ Alignment Forum posts, at least 1 paper submission, completion of the BlueDot Alignment Course, and active applications across the field’s top organizations. The window for experienced engineers to enter AI safety with maximum impact is open now, and the transition distance is shorter than it appears.