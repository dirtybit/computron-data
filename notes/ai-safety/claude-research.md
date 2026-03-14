# AI safety career transition: a practitioner’s roadmap for experienced engineers

**An experienced software engineer with 10+ years, AI app development chops, and evals experience is already closer to an AI safety role than most candidates.** The field’s fastest-growing subfields — AI control, scheming detection, autonomous capability evaluation, and benchmark development — prize exactly the engineering rigor and evaluation mindset this profile brings. Across the four core organizations researched (FLI, Apart Research, Redwood Research, and CAIS) plus the broader landscape, demand for research engineers who can build evaluation infrastructure, red-team frontier models, and stress-test safety protocols has never been higher. METR, Redwood Research, Apollo Research, and OpenAI’s Frontier Evals team are actively hiring for roles where evals experience is the primary qualification. The transition is not about starting over — it’s about redirecting existing skills toward the most consequential engineering problems of the decade.

-----

## The four organizations: what each does and where you fit

### Future of Life Institute — policy powerhouse, not a technical lab

FLI is the world’s oldest AI safety think tank,   founded in 2014  with **35+ full-time staff** operating across the US and Europe.  Their theory of change runs through four pillars: policy advocacy (lobbying for binding AI regulation), grantmaking  (**$28M+ awarded**), public education, and convening. Their flagship output is the **AI Safety Index** — an independent scorecard grading Anthropic, OpenAI, DeepMind, xAI, Meta, and others across 33+ indicators,  reviewed by experts including Yoshua Bengio and Stuart Russell.

FLI does not publish ML papers, maintain code repositories, or develop benchmarks. Their outputs are policy papers, open letters (the 2023 “Pause Giant AI Experiments” letter gathered **31,810 signatures**),  advocacy films, and educational content. Current open roles are US Policy Team Members ($85K–$195K, closing April 3, 2026) and a Communications Associate.  Their **Vitalik Buterin Postdoctoral Fellowships** ($80K/year for up to 3 years) fund academic AI safety research but require a faculty mentor. 

**Fit for your profile:** Low for direct technical work. FLI’s value is as a **funder** (they’ve granted to ARC, FAR AI, and Redwood Research) and **policy network**. Monitor their grants program and newsletter for ecosystem intelligence, but don’t target them for an engineering role.

- Website: https://futureoflife.org/
- Careers: https://futureoflife.org/about-us/careers/
- Fellowships: https://futureoflife.org/our-work/grantmaking-work/fellowships/
- AI Safety Index: https://futureoflife.org/ai-safety-index-winter-2025/

### Apart Research — the fastest on-ramp for working engineers

Apart Research is a remote-first nonprofit founded ~2022 in Copenhagen that has built the most accessible entry pipeline into AI safety research. Their core insight: experienced technical professionals worldwide represent an untapped talent pool.  Their model is a **meritocratic funnel** — Sprint (weekend hackathon) → Studio (8 weeks) → Fellowship (3–6 months) → Conference publication → Career placement.  No prior AI safety experience required; projects are judged on output quality, not credentials. 

The numbers are remarkable: **55+ research sprints**, **6,000+ participants** across 200+ global locations,  **22+ peer-reviewed publications** at ICLR, NeurIPS, ICML, and ACL, including **two ICLR 2025 Oral Spotlights** (top 1.8%).  Their research spans AI security, model evaluation  (DarkBench benchmark), mechanistic interpretability, multi-agent systems, AI governance, and CBRN risk evaluation.

Key open-source outputs include **DarkBench** (660 prompts benchmarking dark patterns in LLMs,  https://github.com/apartresearch/DarkBench), **3CB** (Catastrophic Cyber Capabilities Benchmark,  https://github.com/apartresearch/3cb), and interpretability starter templates. Their **AI Safety Ideas** platform (https://aisafetyideas.com/) crowdsources research project ideas.

**Fit for your profile:** Exceptional. Apart’s hackathons are the single highest-ROI entry point. You can participate in a weekend sprint without disrupting your current role, produce a research artifact, and potentially get invited into the Studio → Fellowship pipeline.  Alumni have placed at  Anthropic, METR, FAR.AI,   Google DeepMind, and UK AISI. The **AI Control Hackathon** (March 20–22, 2026) is imminent.

- Sprints: https://apartresearch.com/sprints
- Research: https://apartresearch.com/research
- Discord: https://discord.me/apartresearch
- GitHub: https://github.com/apartresearch
- Hackathon guide: https://apartresearch.com/news/the-ultimate-guide-to-ai-safety-research-hackathons

### Redwood Research — the AI control pioneers

Redwood Research is a Berkeley-based nonprofit (founded 2021) that introduced and continues to lead the **AI control** paradigm. Their core assumption is radical: rather than hoping models are aligned, they design safety protocols that work **even if models are actively scheming against humans**.  This conservative worst-case approach has become central to frontier AI safety. 

Their flagship paper, “AI Control: Improving Safety Despite Intentional Subversion” (ICML Oral), proposed “trusted monitoring” — using a weaker trusted model to supervise a stronger untrusted one.  With Anthropic, they co-authored the landmark **“Alignment Faking in Large Language Models”** paper (December 2024), providing the strongest evidence that LLMs naturally fake compliance to resist training.   They also contributed to the **“Sleeper Agents”** paper showing deceptive behavior persists through safety training.  

They consult for Google DeepMind, Anthropic, and the UK AI Safety Institute.  Redwood also operates **Constellation**, a ~30,000 sq ft shared office in downtown Berkeley hosting ARC, MIRI, and Open Philanthropy.

**Current hiring:** Member of Technical Staff at **$180K–$207K/year**,  requiring ML skills (LLM APIs, PyTorch), software engineering (Docker orchestration, ML experiment infrastructure), and deep interest in AI safety. Berkeley, in-person. The **MATS Redwood stream** (Autumn 2026 applications open late April) offers a 12-week research program  with $15K stipend + $12K compute. 

**Fit for your profile:** Strong. Your engineering skills directly match their MTS requirements. The control paradigm is highly engineering-centric — building evaluation infrastructure, orchestrating agent experiments, and stress-testing safety protocols.

- Website: https://www.redwoodresearch.org/
- Careers: https://www.redwoodresearch.org/careers
- Blog reading list: https://blog.redwoodresearch.org/p/guide
- ControlConf 2026 (April 18–19, Berkeley): https://blog.redwoodresearch.org/p/announcing-controlconf-2026
- GitHub: https://github.com/redwoodresearch
- MATS stream: https://www.matsprogram.org/stream/redwood

### Center for AI Safety — benchmarks, compute, and field-building

CAIS, founded in 2022 by **Dan Hendrycks** (creator of MMLU, the most widely used LLM benchmark)  and based in San Francisco, operates across three pillars: research, field-building, and advocacy.  Their technical contributions are extraordinary — they’ve produced multiple benchmarks that have become industry standards.

Key benchmarks and tools:

|Benchmark                 |What it measures                              |Impact                                       |
|--------------------------|----------------------------------------------|---------------------------------------------|
|**MMLU**                  |Multitask language understanding (57 subjects)|Industry-standard LLM eval                   |
|**WMDP**                  |Hazardous knowledge (bio, cyber, chem)        |ICML 2024; includes RMU unlearning method    |
|**HarmBench**             |Automated red teaming                         |ICML 2024; used by US/UK AI Safety Institutes|
|**Humanity’s Last Exam**  |Expert-level AI capabilities                  |1,200+ expert collaborators                  |
|**Remote Labor Index**    |Real-world freelance task automation          |First real-job automation benchmark          |
|**SafeBench**             |Competition for new safety benchmarks         |$250K in prizes                              |
|**AILuminate** (MLCommons)|12 hazard categories for chat LLMs            |24,000+ test prompts per language            |

CAIS lists **17 open roles** on 80,000 Hours,  including the **AI and Society Fellowship** (summer 2026, $25K stipend, deadline March 24, 2026)  and **Research Engineer Intern** positions.  Their free **compute cluster** supports  **350+ researchers** globally and has enabled **109+ papers with 4,000+ citations**.  Their textbook, *Introduction to AI Safety, Ethics, and Society* (https://www.aisafetybook.com/), is the most comprehensive single resource for the field.

**Fit for your profile:** Strong, especially for benchmark development and evaluation engineering. Your evals experience maps directly to WMDP, HarmBench, and SafeBench. The compute cluster (free access — email compute@safe.ai) enables independent research. 

- Website: https://safe.ai/
- Careers: https://safe.ai/careers
- Compute cluster: https://safe.ai/work/compute-cluster
- Textbook: https://www.aisafetybook.com/
- ML Safety course: https://course.mlsafety.org/
- GitHub: https://github.com/centerforaisafety
- SafeBench: https://www.mlsafety.org/safebench
- Newsletter: https://newsletter.safe.ai/

-----

## Cross-cutting skill analysis: what the field demands

Aggregating across all four organizations’ job postings, fellowship descriptions, hackathon requirements, and research outputs reveals a clear competency map. The table below separates technical from conceptual competencies, ranked by frequency of mention.

### Technical competencies across organizations

|Competency                                   |FLI|Apart|Redwood|CAIS|Frequency|
|---------------------------------------------|---|-----|-------|----|---------|
|Python / PyTorch                             |—  |✓    |✓      |✓   |High     |
|LLM APIs (GPT, Claude)                       |—  |✓    |✓      |✓   |High     |
|ML experiment design & execution             |—  |✓    |✓      |✓   |High     |
|Benchmark development & evaluation           |—  |✓    |—      |✓   |High     |
|Docker / containerized infrastructure        |—  |—    |✓      |✓   |Medium   |
|Red-teaming / adversarial testing            |—  |✓    |✓      |✓   |High     |
|Agent scaffolding & orchestration            |—  |✓    |✓      |✓   |High     |
|Mechanistic interpretability (SAEs, circuits)|—  |✓    |✓      |—   |Medium   |
|Statistical analysis / empirical methods     |—  |✓    |✓      |✓   |High     |
|Fine-tuning / RLHF / training pipelines      |—  |✓    |✓      |✓   |Medium   |
|Open-source tool development                 |—  |✓    |✓      |✓   |Medium   |
|Policy writing / governance frameworks       |✓  |✓    |—      |✓   |Medium   |

### Research/conceptual competencies across organizations

|Competency                    |FLI|Apart|Redwood|CAIS|Frequency|
|------------------------------|---|-----|-------|----|---------|
|AI risk / threat modeling     |✓  |✓    |✓      |✓   |Very High|
|Alignment theory fundamentals |✓  |✓    |✓      |✓   |Very High|
|AI control protocols          |—  |✓    |✓      |—   |High     |
|Deception / scheming detection|—  |✓    |✓      |✓   |High     |
|Scalable oversight            |—  |—    |✓      |✓   |Medium   |
|Safety case methodology       |—  |—    |✓      |✓   |Medium   |
|CBRN risk evaluation          |✓  |✓    |—      |✓   |Medium   |
|Compute governance            |✓  |✓    |—      |✓   |Medium   |
|Catastrophic risk frameworks  |✓  |—    |—      |✓   |Medium   |

-----

## How your background maps to AI safety roles

Your profile — **10+ years software engineering, AI application development, evals experience** — maps to AI safety competencies more directly than most candidates realize. Here is the specific mapping:

|Your existing skill              |AI safety application                                                                     |Target roles                                                          |
|---------------------------------|------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
|**Evals experience**             |Capability evals, alignment evals, benchmark development, sandbagging detection           |METR research engineer, CAIS benchmark engineer, OpenAI Frontier Evals|
|**AI app development**           |Agent scaffolding, LLM API orchestration, safety protocol implementation                  |Redwood MTS (Docker + agent orchestration), Apollo MTS                |
|**Software engineering (10+ yr)**|Eval infrastructure, safety tooling, monitoring systems, reproducible experiment pipelines|All research engineer roles across the field                          |
|**Production systems experience**|Deployment safety, monitoring, real-world failure mode analysis                           |Anthropic trust & safety, DeepMind mitigations                        |
|**Testing/QA mindset**           |Red-teaming, adversarial robustness, control evaluations                                  |Redwood control evals, Apart hackathons, CAIS HarmBench               |
|**Debugging complex systems**    |Mechanistic interpretability, circuit analysis, failure investigation                     |Anthropic interpretability, Apart interp sprints                      |

### Subfields ranked by fit for your profile

**Strongest fit (apply now):**

- **AI evaluation engineering** — building and running model evaluations for capabilities and alignment. Your evals experience is the primary qualification. Organizations: METR, CAIS, OpenAI Frontier Evals, UK AISI.
- **AI control** — engineering safety protocols, monitoring systems, and red-team/blue-team infrastructure. Your SWE skills directly match. Organizations: Redwood Research, Anthropic.
- **Red-teaming and adversarial testing** — systematic vulnerability discovery in frontier models. Combines testing mindset with AI knowledge. Organizations: Apollo Research, Anthropic Frontier Red Team, CAIS (HarmBench).
- **Benchmark development** — designing, implementing, and validating safety benchmarks. Your evals background plus engineering skills. Organizations: CAIS (SafeBench, WMDP), Apart Research (DarkBench, 3CB), MLCommons.

**Good fit (1–3 months upskilling):**

- **Mechanistic interpretability** — reverse-engineering neural network internals. Requires learning SAEs, circuit analysis, but benefits from strong coding skills. Organizations: Anthropic (Chris Olah’s team), DeepMind (Neel Nanda’s team), Apart Research.
- **Scalable oversight** — designing systems where humans can effectively supervise superhuman AI. Combines systems thinking with ML. Organizations: DeepMind, Anthropic.
- **Governance tooling** — building technical systems for AI governance (compute monitoring, compliance tools, verification mechanisms). Organizations: FLI, Apart Research (governance sprints), CAIS.

-----

## Six-month phased transition roadmap

### Phase 1: Foundation and first signal (Months 1–2)

The goal of this phase is to build theoretical grounding, produce your first AI safety artifact, and establish community presence. You should be able to complete this while maintaining your current role.

**Theoretical foundations track:**

Start with the CAIS textbook *Introduction to AI Safety, Ethics, and Society* (https://www.aisafetybook.com/) — read Part I (AI Fundamentals, chapters 1–3) and Part II (Safety, chapters 4–7) in the first two weeks. This covers robustness, monitoring, alignment, and systemic safety.   Simultaneously enroll in **BlueDot Impact’s AI Alignment Course** (https://course.aisafetyfundamentals.com/alignment), an 8-week program requiring ~5 hours/week with small-group discussions.  Completing this course is effectively a prerequisite for MATS  and signals baseline competence to hiring managers.

Read these foundational papers in dependency order during weeks 3–8:

1. Amodei et al. (2016), “Concrete Problems in AI Safety” — five practical safety problems
1. Christiano (2019), “What Failure Looks Like” — two scenarios for gradual AI catastrophe
1. Hubinger et al. (2019), “Risks from Learned Optimization” — mesa-optimization, deceptive alignment (https://arxiv.org/abs/1906.01820)
1. Ngo, Chan, Mindermann (2024), “The Alignment Problem from a Deep Learning Perspective” — modern DL-focused alignment analysis
1. Carlsmith (2023), “Scheming AIs” — detailed deceptive alignment analysis 
1. Greenblatt et al. (2024), “AI Control: Improving Safety Despite Intentional Subversion” (https://arxiv.org/abs/2312.06942) — foundational control paper

**Hands-on projects track:**

**Project 1: Apart Research Hackathon Participation (Weekend, ~20 hours)**
Register for the **AI Control Hackathon** (March 20–22, 2026, https://apartresearch.com/sprints/ai-control-hackathon-2026-03-20-to-2026-03-22). Build a control evaluation, monitoring tool, or adversarial attack on AI agent protocols.  This produces a concrete artifact, introduces you to the community, and enters the Apart pipeline. Target skill: control evaluation design. Connects to: Redwood Research’s work.

**Project 2: Replicate a CAIS benchmark locally (~15 hours)**
Clone HarmBench (https://www.harmbench.org/) or WMDP (https://github.com/centerforaisafety/wmdp)  and run evaluations on an open-source model. Extend with a novel attack vector or new evaluation category. Write up findings on the Alignment Forum. Target skill: benchmark engineering. Connects to: CAIS and MLCommons work.

**Community and credibility track:**

- Join Apart Research Discord (https://discord.me/apartresearch) — most active AI safety community for practitioners
- Create an Alignment Forum account (https://www.alignmentforum.org/) and LessWrong account
- Subscribe to CAIS newsletter (https://newsletter.safe.ai/) and FLI newsletter (https://futureoflife.org/newsletters/)
- Register for 80,000 Hours 1-on-1 advising (https://80000hours.org/) — personalized career guidance 
- Sign up for MATS Autumn 2026 notifications (applications open late April, https://www.matsprogram.org/) 
- Apply for CAIS compute cluster access (email compute@safe.ai) for independent research

**Phase 1 “done” criteria:**

- BlueDot Alignment Course enrollment confirmed, 4+ sessions completed
- 6 foundational papers read with notes
- 1 Apart hackathon completed with submitted project
- 1 benchmark replication or extension written up
- Alignment Forum account active with at least 1 post or comment
- MATS notification signup complete

### Phase 2: Portfolio depth and targeted applications (Months 3–4)

This phase builds substantive research artifacts and begins the application process for target roles.

**Theoretical foundations track:**

Complete the BlueDot Alignment Course. Begin the **CAIS ML Safety technical course** (https://course.mlsafety.org/) for empirical ML safety methods. Read the second tier of papers:

1. Anthropic + Redwood (2024), “Sleeper Agents: Training Deceptive LLMs that Persist Through Safety Training” (https://arxiv.org/abs/2401.05566)
1. Anthropic + Redwood (2024), “Alignment Faking in Large Language Models” (https://arxiv.org/abs/2412.14093)
1. Apollo Research (2024), “Frontier Models are Capable of In-context Scheming”
1. Hubinger (2020), “An Overview of 11 Proposals for Building Safe Advanced AI”  (https://arxiv.org/abs/2012.07532)
1. DeepMind (2025), “An Approach to Technical AGI Safety and Security” (Rohin Shah et al.)

Read the three major industry safety frameworks:

- Anthropic RSP v3: https://anthropic.com/responsible-scaling-policy/rsp-v3-0
- DeepMind Frontier Safety Framework v3
- OpenAI Preparedness Framework v2

**Hands-on projects track:**

**Project 3: Build an alignment eval suite (~30 hours)**
Design and implement a behavioral evaluation testing for scheming, sycophancy, or alignment faking in open-source models. Use Apollo Research’s methodology as a template. Run on multiple model families, analyze results. Publish on Alignment Forum and GitHub. Target skill: behavioral evals. Connects to: Apollo Research, Anthropic.

**Project 4: Contribute to Redwood’s open-source control infrastructure (~25 hours)**
Fork Redwood’s ControlArena (https://github.com/redwoodresearch) or alignment_faking_public repository. Implement a new control protocol variant, a novel attack strategy, or an evaluation extension. Submit a pull request. Target skill: control protocol engineering. Connects to: Redwood Research.

**Project 5: Apart Research second hackathon or Studio (~20–40 hours)**
Participate in another Apart sprint (they run approximately monthly). If invited to Studio based on your first hackathon performance, accept — it’s an 8-week program developing your hackathon project into a research proposal.   Target skill: research iteration. Connects to: Apart Research pipeline.

**Community and credibility track:**

- Apply to **MATS Autumn 2026** (applications open late April) — Redwood Research stream for control work,  or other streams matching your interests
- Submit applications to: **METR** (research engineer), **Redwood Research** (MTS, $180K–$207K), **OpenAI Frontier Evals**, **Apollo Research** (MTS)
- Attend **ControlConf 2026** (April 18–19, Berkeley, https://blog.redwoodresearch.org/p/announcing-controlconf-2026) — Redwood’s AI control conference
- Submit to CAIS **SafeBench** competition ($250K in prizes, https://www.mlsafety.org/safebench)  if your benchmark work is strong
- Post 2–3 substantive pieces on the Alignment Forum (paper reviews, project write-ups, or original analysis)
- Apply for **Constellation Astra Fellowship** if the next cohort opens (https://www.constellation.org/programs/astra-fellowship)

**Phase 2 “done” criteria:**

- BlueDot Alignment Course completed
- 2–3 additional research artifacts on GitHub with Alignment Forum write-ups
- Applications submitted to 3+ target organizations
- MATS Autumn 2026 application submitted
- At least 1 conference or workshop attended (ControlConf or Apart sprint)
- 3+ Alignment Forum posts with community engagement

### Phase 3: Conversion and specialization (Months 5–6)

This phase focuses on converting portfolio and community work into a role offer or program acceptance.

**Theoretical foundations track:**

Specialize in your strongest subfield. For AI control, read Redwood’s complete blog series (https://blog.redwoodresearch.org/p/guide), especially “7+ Tractable Directions In AI Control,” “Catching AIs Red-Handed,” and “Jankily Controlling Superintelligence.”  For interpretability, work through Neel Nanda’s “200 Concrete Open Problems in Mechanistic Interpretability” and the ARENA (Alignment Research Engineer Accelerator) curriculum. For evals, study METR’s time horizon methodology and RE-Bench benchmark papers.

Read the governance layer:
12. CAIS, “An Overview of Catastrophic AI Risks” (https://arxiv.org/pdf/2306.12001)
13. Hendrycks + Schmidt + Wang, “Superintelligence Strategy”
14. Cotra (2022), “Without Specific Countermeasures, the Easiest Path to Transformative AI Likely Leads to AI Takeover”

**Hands-on projects track:**

**Project 6: End-to-end safety evaluation tool (~40 hours)**
Build a complete, polished open-source tool that addresses a specific gap in the AI safety evaluation ecosystem. Options: a sandbagging detection framework (building on Apart’s research), a control protocol benchmark, or an automated alignment faking detector. Make it usable by other researchers. Publish with documentation. Target skill: production-quality safety tooling. Connects to: all organizations.

**Project 7: Collaborative research paper (~40 hours)**
Co-author a paper through Apart’s Fellowship pipeline, a MATS project, or independent collaboration with researchers met through the community. Target a workshop at NeurIPS, ICML, or ICLR. Even a workshop paper submission demonstrates research capability.  Target skill: research communication. Connects to: academic credibility across the field.

**Community and credibility track:**

- If accepted to MATS Autumn 2026, begin the program
- Follow up on all submitted applications; request informational interviews
- Apply to remaining target organizations not yet contacted
- Present work at an Apart hackathon, EA Global event, or safety workshop
- Apply to **CAIS AI and Society Fellowship** or **Research Engineer Internship** for the next available cohort
- Maintain consistent Alignment Forum presence

**Phase 3 “done” criteria:**

- 5+ research artifacts on GitHub, at least 2 with polished write-ups
- 1 paper in submission or published (workshop paper counts)
- Active applications at 5+ organizations
- MATS acceptance or advancement in interview pipeline at a target org
- Recognized community contributor (Alignment Forum karma, hackathon placements, or open-source contributions)
- Clear specialization established in 1–2 subfields

-----

## Extended landscape: organizations and programs beyond the core four

|Organization                |Focus area                               |What it adds                                                                                       |Key link                                          |
|----------------------------|-----------------------------------------|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
|**METR**                    |Autonomous capability evaluation         |Gold standard for independent frontier evals; strongest direct fit for evals background            |https://metr.org/                                 |
|**Apollo Research**         |Scheming/deception detection             |Leading empirical deception research; London-based; coding-heavy roles                             |https://www.apolloresearch.ai/                    |
|**Anthropic alignment team**|Interpretability, Constitutional AI, RSP |Largest alignment research employer at a frontier lab; RSP is most developed safety framework      |https://www.anthropic.com/careers                 |
|**DeepMind safety team**    |Scalable oversight, interpretability, FSF|Massive resources; safety integrated into Gemini deployment                                        |https://deepmind.google/responsibility-and-safety/|
|**OpenAI Frontier Evals**   |Evaluation infrastructure                |Actively hiring research engineers; builds SWE-bench, MLE-bench, PaperBench                        |https://openai.com/careers/                       |
|**MIRI**                    |Technical governance, advocacy           |The OG safety org; pivoted from technical research to policy; foundational historical contributions|https://intelligence.org/                         |
|**ARC**                     |Theoretical alignment (ELK)              |Pure theory approach; Paul Christiano now also at NIST; small team                                 |https://www.alignment.org/                        |
|**MATS**                    |Fellowship/transition program            |Premier pipeline into safety careers; 12 weeks + 6–12 month extension; $15K stipend + $12K compute |https://www.matsprogram.org/                      |
|**FAR.AI**                  |Evals, red-teaming, robustness           |Explicitly recruiting “evals and red-teaming” research engineers                                   |https://www.far.ai/careers/                       |
|**UK AISI**                 |Government AI evaluation                 |National evaluator of frontier models pre-deployment; partners with METR and Redwood               |https://www.aisi.gov.uk/                          |

**METR deserves special attention.** Spun off from ARC Evals in December 2023 and led by Beth Barnes,  METR evaluates frontier AI models for autonomous capabilities.  They created the **time horizon metric** (showing AI agent task duration doubling every ~7 months),  the **RE-Bench** benchmark for AI R&D acceleration, and open-source tools like **Vivaria** (eval runner) and **Task Standard**. They’ve pre-deployment tested GPT-4,  GPT-4.5, GPT-5, GPT-5.1, Claude 3.5 Sonnet, Claude 3.7, and Claude Opus 4.6.  They partner with the US NIST AI Safety Institute and UK AISI.  METR does not accept funding from AI companies to maintain independence.  For someone with evals experience, **METR is the single most natural fit in the entire AI safety ecosystem.**

-----

## Key resources and learning materials consolidated

**Textbooks (in priority order):**

1. *Introduction to AI Safety, Ethics, and Society* by Dan Hendrycks — free at https://www.aisafetybook.com/
1. *The Alignment Problem* by Brian Christian — accessible introduction
1. *Human Compatible* by Stuart Russell — CHAI perspective on the control problem

**Courses (in recommended sequence):**

1. BlueDot Impact AI Alignment Course (8 weeks, free):  https://course.aisafetyfundamentals.com/alignment
1. CAIS ML Safety Course (technical): https://course.mlsafety.org/
1. BlueDot Impact AI Governance Course:  https://course.aisafetyfundamentals.com/governance
1. CAIS Virtual Course (12 weeks): https://www.aisafetybook.com/virtual-course

**Career resources:**

- 80,000 Hours AI safety guide: https://80000hours.org/ai/
- 80,000 Hours ML engineering transition guide: https://80000hours.org/articles/ml-engineering-career-transition-guide/
- 67 upskilling resources for technical AI safety: https://80000hours.org/2025/06/technical-ai-safety-upskilling-resources/
- Job board (300+ open roles): https://jobs.80000hours.org/
- AISafety.com jobs aggregator:  https://www.aisafety.com/jobs
- Victoria Krakovna’s curated resource list: https://vkrakovna.wordpress.com/ai-safety-resources/

**Communities:**

- Alignment Forum: https://www.alignmentforum.org/
- LessWrong AI safety tag: https://www.lesswrong.com/tag/ai-safety
- Apart Research Discord: https://discord.me/apartresearch
- EleutherAI Discord (open-source ML community)
- AXRP Podcast (deep-dive researcher interviews): https://axrp.net/

**Key upcoming deadlines and events:**

- Apart AI Control Hackathon: March 20–22, 2026
- CAIS AI and Society Fellowship application deadline: March 24, 2026
- ControlConf 2026 (Berkeley): April 18–19, 2026
- MATS Autumn 2026 applications: Open late April 2026
- Apart Research sprints: Approximately monthly (check https://apartresearch.com/sprints)

-----

## Conclusion: the field needs builders, not just theorists

The AI safety field in 2026 has shifted decisively from pure theory toward empirical, engineering-heavy research.  The ascent of AI control (Redwood), behavioral evaluations (Apollo, METR), benchmark engineering (CAIS), and rapid-iteration research sprints (Apart) means that **experienced software engineers with evaluation skills are no longer adjacent to the field — they are central to it**. The most impactful work right now involves building the infrastructure to test whether AI systems are safe: evaluation platforms, monitoring protocols, adversarial testing frameworks, and control mechanisms.

Your strongest immediate moves are to participate in an Apart Research hackathon this month, apply directly to METR and Redwood Research, submit your MATS Autumn 2026 application in late April, and request CAIS compute cluster access for independent research. The 6-month roadmap above is designed so that each phase produces concrete artifacts that double as both learning exercises and application portfolio pieces. By month 6, a disciplined execution of this plan should produce 5+ GitHub repositories, 3+ Alignment Forum posts, at least 1 paper submission, completion of the BlueDot Alignment Course, and active applications across the field’s top organizations.

The window for experienced engineers to enter AI safety with maximum impact is open now, and the transition distance is shorter than it appears.