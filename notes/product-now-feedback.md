
### Website & Product Concept
> The AI operating system for Product and Engineering
>
> One intelligent system that connects every workflow, aligns every team and accelerates product velocity.

It’s a little too broad, could be supported with some concrete material like examples, capabilities, visuals, demo video etc (gif screenshot). what the day-to-day experience is like feels missing

what does productnow do to help teams accomplish this? 
features section can clarify this.
The feature cards are too abstract, feels a little buzzwordy. 

What does "Connects every tool, epic and workflow into a shared intelligence layer" actually mean in practice? 
Use cases / workflows missing.
Which tools? 
What does the connection look like? A visitor can't tell if this is a Jira plugin, a Notion replacement, or a Slack bot.


**Overall concept**
What’s not clear to me during my experience:
 - Is this a document hub for docs like PRDs, or it’s another layer where I am supposed to connect all the tools (notion, slack, linear) i used in my prod dev and this should be a centralized intelligence layer on top of all.
 - If I am writing specs/docs in ProductNow using/referring some other resources (notion pages, etc) how am i supposed to make sure that one of them is the source of truth. ppl can make edits to docs so out of sync can happen easily.
 - 



### Experience

Idea: Alternative take on the product workflow. Doc is not the process, but the deliverable. Reaching to PRD, specs, strategy docs is a process where various phases of research can be done, ideas/notes are collected over time, brainstorming or discussion kind of 

Idea: It would be interesting to make productnow docs accessible to claude code so it can refer to the PRD while planning etc.

Inference latency can be very high sometimes even for minor generations like to-the-point edits, asking questions. 

Bug?: Guided tour started again when I logged in even if i finished it the first time.


Bug? Clicking logo expand left panel (drawer), but it covers the main page content 
![[2026-03-25_13-54-36.png]]
Bug? Connected it to my personal Slack but it still says no slack config yet
  Would be good to have some inline links in the connectors page next to each connector type for documentation/help page. no help content on connectors in help center.


Initial doc editing page:
 - Am I supposed to write a doc here or what I am writing is more like a prompt?
 - It could be more like agent/chat interface (similar to the left panel)


Trials:
 - Brief prompt on a project idea, limited details high level scope and resource info
Generated a very long bloated document with lots of details (hence decisions). I’d still be in charge of authroing this isntead of giving up total control to generate a 3-5 page long doc that I need to review.

Flow could be start from a high level outline with the given details, call out missing details and areas needs to be elaborated, for each take my input, ask questions and create the doc together. the agent should do the most of the work but I am still in charge and can follow how we got to the first draft revision from the very first prompt i shared. instead of having to review a huge text dump. 

intelligence would be more useful for things like tighenening the scope, making decisions on how to phase the product, charting potential critical cases, edge cases, calling out things to be considerd and help me make those decisions bringing in external resources like web search etc.


i tried a sharing some notes on a project, with more details like features, expected behavior, tech decisions, rough timeline, risks i am worried about etc 

the goal is to see how it can process the scattered notes with details and decisions and generate a doc based on that. does it respect my existing notes, overrides or omits things? how does it extend?

brief mode
it preserved my notes generally that was good. but it came with stuff which is hard to justify (no source/citation)
 - Research demonstrates that teams lose 20.5% of productive time to tool switching
 - Market validation shows annotation-focused tools like Markup.io and Frame.io outperform full whiteboard platforms
 - rollout plan was supposed to be 8 week but expanded to 16 week with no reasoning or headsup.
 - expanded the scope by adding new features or extending existing ones without asking me
 - invented metrics/target without flagging


Post-generation Editing

Inaccurate estimations:
****Why descope:**** Export is a convenience feature, not core to the handoff workflow. Users can screenshot the canvas if needed.

****Impact:**** Saves 1-2 weeks in Sprint 5-6. Export requires canvas-to-image rendering library integration and testing across formats.

****Workaround:**** Users can take screenshots or share the live canvas link instead.

---

Reviewing edits in the agent/chat panel is difficult. It shows a big block of text even if there’s a minor change within that few paragraph long text (e.g. replace 16-week to 8-week), it would be good to review these changes on the actual document. 
![[2026-03-26_11-27-41.png]]
Also, while reviewing the proposed changes, I’d love to leave some comments and feedback and so we can take another pass to refine those. 

Diff view can be messy some times hard to read. it might be good check how google docs, notion etc shows changes across revisions. something similar to that can be useful here
![[2026-03-26_11-28-51.png]]

--------

I'd deeply appreciate your feedback on two key areas:

### Document Generation

How does the document generation experience feel overall?

*   Does web search integration work as expected? Are you satisfied with the quality of first-draft documents?
*   Do you find the templates useful? Are there any that stand out, or suggestions for additional templates we should add?

### AI-Assisted Drafting

When editing documents, can you effectively use the AI assistant to direct your edits?

*   Can you reference web content and request broader edits? Does the assistant behave as you'd expect?
*   How do the various visualizations feel? Do any stand out as particularly useful?
    *   If you click the "..." in the top bar, you'll see our full list, else you can type `/` to access the list inline
*   I've been experimenting with setting a section to "Audio" and having the agent summarize the document. Then playing it back at 2x speed — does this sound valuable to you?
    *   You can change the output type of a section using the "..." in the section title > Content type > Audio

We have an MCP server and numerous improvements to review next, but I'd love to hear first whether the drafting experience feels solid. Any and all feedback is greatly appreciated!



Prompt #1

 We're building a smart notification system for our B2B SaaS platform (project management tool, ~2000 DAU).
  Users are complaining about notification fatigue — they get 50-80 notifications/day and miss the important ones.

  We want to ship an AI-powered notification prioritization feature that:
  - Learns which notifications each user actually acts on
  - Batches low-priority notifications into a daily digest
  - Surfaces urgent items (blockers, direct mentions, deadline changes) immediately
  - Lets users give thumbs up/down feedback to tune the model

  Write a PRD for this. Engineering has 2 backend engineers and 1 ML engineer available.
  We want to ship an MVP in 6 weeks. We use PostgreSQL, Redis, and deploy on AWS.
  The PM stakeholder is concerned about users missing critical notifications during the learning period.


---

Prompt #2
```
Turn these project notes into a structured product requirements document:

  ---

  PROJECT: In-app collaborative whiteboard for our design handoff tool

  BACKGROUND NOTES (from kickoff + stakeholder sync):
  - Designers keep screenshotting Figma frames and pasting into Slack to discuss changes
  - Engineers say they lose context because discussions happen across 4 different tools
  - We tried embedding Miro but the iframe performance was terrible on lower-end machines
  - Decision: build our own lightweight canvas, NOT a full whiteboard — just enough for annotation and discussion
  - Sarah (design lead) wants infinite canvas. I think we should start with fixed-frame canvas tied to each design file. Easier to scope.
  - Jake from eng says we should use Canvas API not SVG for performance. He benchmarked it and SVG chokes at ~200 elements.

  CORE FEATURES (must-have for v1):
  - Draw arrows and rectangles on top of design screenshots
  - Sticky notes with text (max 280 chars, keep it short)
  - @mention teammates to pull them into a discussion
  - Real-time cursors so you can see who's looking at what
  - Comments anchored to specific regions of the canvas
  - Export canvas as PNG for stakeholder presentations

  THINGS WE EXPLICITLY WON'T DO IN V1:
  - No pen/freehand drawing (too complex, and we're not competing with Miro)
  - No video/audio — just async collaboration
  - No version history (we'll just let people create new canvases)
  - No mobile support. Desktop web only.

  TECH DECISIONS ALREADY MADE:
  - Canvas API (not SVG) per Jake's benchmarks
  - WebSocket for real-time sync, we already have the infra from our chat feature
  - Store canvas state as JSON blobs in Postgres JSONB column
  - Operational transforms for conflict resolution — Mike has experience with this from his last company
  - Auth: reuse existing session tokens, no new auth flow needed

  OPEN QUESTIONS:
  - How do we handle large design files? Some Figma exports are 15MB+ PNGs
  - Should canvas state sync be event-sourced or last-write-wins?
  - Do we need rate limiting on the WebSocket connections?
  - What happens to canvases when the linked design file is updated in Figma?

  TIMELINE:
  - We told leadership 8 weeks but honestly that's aggressive for 3 engineers
  - Sprint 1-2: canvas rendering + basic shapes
  - Sprint 3-4: real-time sync + mentions
  - Sprint 5-6: comments + export
  - Sprint 7-8: polish, bug fixes, internal dogfooding

  RISKS I'M WORRIED ABOUT:
  - Real-time sync is always harder than you think
  - Jake is the only one who knows Canvas API well — bus factor of 1
  - If we scope creep into freehand drawing we'll blow the timeline
  - Postgres JSONB might not scale if canvases get really complex — but probably fine for v1