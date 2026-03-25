

I love this concept — let me first do thorough research on Alexa's current device ecosystem, settings, and support documentation to ground everything properly.Now I have a solid research foundation. Let me build a comprehensive exploration of this concept, grounded in real Alexa settings and pain points.Here's an interactive exploration of your concept, grounded entirely in real Alexa settings and documented user pain points. I built 5 detailed use cases you can click through, each with four tabs:

**The 5 scenarios** — chosen for maximum complexity and real-world frustration:

1.  **Child-Proofing a Shared Echo** — 7 separate settings paths across Amazon Kids, voice purchasing, content filters, Do Not Disturb, and communication controls, collapsed into one panel. Catches the Voice Deactivation gotcha that lets kids undo your filters by voice.
    
2.  **Multi-Room Audio Across Mixed Devices** — tackles the infamous "network error" that gives zero diagnostic info. The AI detects Wi-Fi band mismatches (2.4 vs 5GHz), Bluetooth speaker conflicts, and model-mismatch stereo pairing impossibilities upfront.
    
3.  **Complex Morning Routine for a Two-Schedule Household** — the thermostat conflict (Partner A leaving shouldn't trigger eco-mode while Partner B is still home) is invisible in the flat action-list UI. A visual timeline makes it obvious.
    
4.  **Privacy Lockdown for an Airbnb Guest Device** — 15+ scattered settings including the ones hosts almost always miss: calendar events and Amazon Photos leaking on the Echo Show ambient display.
    
5.  **Nighttime Security Orchestration** — 4 coordinated routines across Ring, smart locks, motion sensors, and Alexa Guard presented as one cohesive security layer instead of separate, disconnected configurations.
    

The "Generated UI Preview" tab on each case shows what the AI would actually produce — interactive toggles, warnings for hidden gotchas, and pre-set recommended values. This is the core of your concept: turning "read this 2,000 word guide" into "here are the 9 controls that matter for your specific situation."

Let me research more complex Alexa configuration pain points that fit this pattern perfectly.Now I have comprehensive research on several more pain-point scenarios. Let me expand the artifact with new use cases that all follow the pattern: manual solution exists, but it's cumbersome and non-trivial.Now I'll insert the 5 new expanded use cases into the existing artifact:Now let me update the design principles to reflect the expanded scope:Now update the use cases section description to reflect the expanded count:The artifact now has **10 comprehensive use cases** — all following your criterion of "manual solution exists but it's cumbersome and non-trivial." Here's what I added:

**5 new scenarios:**

**✈️ Two-Week Vacation Home Simulation** — The nastiest one. Alexa's vacation prep spans 4 disconnected feature domains (Guard, Away Lighting, Modes, Routines) across 3 separate apps (Alexa, Ring, thermostat). The real killer is the pet sitter exception: they need daily entry access without triggering the security system. Currently requires you to set up Home/Away Modes *first* (a hidden prerequisite) before Vacation Mode even appears as an option. The AI treats the pet sitter as a first-class "trusted visitor window" concept with suppressed alerts during their time slot.

**👨‍👩‍👧‍👦 4-Person Household Personalization** — Alexa has *five* different identity systems (Voice ID, Visual ID, Alexa Profiles, Household Profiles, Amazon Kids) with confusing overlap and different setup paths. The 14-year-old needs an Alexa Profile (not Amazon Kids — too restrictive at that age), but Amazon Kids can only be toggled per-device, so enabling it on the shared kitchen Echo locks *everyone* into child mode. The AI generates a household matrix showing who gets what, with a dependency-ordered setup sequence.

**🔕 Taming Notification Overload** — 8+ separate notification sources, each configured in a different app section. The crucial insight most users miss: Brief Mode makes Alexa's *responses* shorter but doesn't reduce the *number* of notifications. The AI categorizes everything into priority tiers (security → personal → suppress) with bulk mute actions, and applies Do Not Disturb across all 6 devices at once instead of individually.

**🎵 Whole-Home Audio Optimization** — EQ must be set per-device (no batch control), but each Echo model has different speaker capabilities. Boosting bass on an Echo Pop literally produces rattling, not depth. Room acoustics matter (bathroom tile amplifies treble, kitchen noise needs Adaptive Listening). The AI generates purpose-driven profiles: music room, podcast kitchen, audiobook bedroom, focus office.

**👵 Setting Up Echo for an Elderly Parent** — No "senior mode" exists. Requires 16+ settings across accessibility, safety, communication, and simplification — with a hidden $20/month subscription (Alexa Together) for fall detection. The AI prioritizes Safety first, catches the medication reminder persistence gap (standard reminders stop after one dismissal), and recommends wake word changes if "Alexa" is hard to remember.

**⚡ Whole-Home Energy Optimization** — Alexa has no concept of electricity rate schedules. Users must manually create 10+ time-based routines for peak avoidance, pre-cooling strategy, EV charge shifting, and weekday/weekend variants — each built action-by-action. The AI designs it as one unified energy strategy with the pre-cooling concept (run HVAC on cheap power *before* peak, then coast) automated.

I also expanded the **Design Principles** section with two new principles: *Dependency-Aware Sequencing* (hidden prerequisites like "modes must exist before vacation mode") and *Persona-Driven Defaults* (age-appropriate settings, accessibility presets).






```js
import { useState } from "react";

const useCases = [
  {
    id: "childproof",
    title: "Child-Proofing a Shared Echo",
    emoji: "🛡️",
    persona: "Parent with a 6-year-old and a shared Echo Show 8 in the kitchen",
    problem:
      "Setting up parental controls on Alexa requires navigating 5+ different settings screens across Amazon Kids, voice purchasing, Do Not Disturb scheduling, Drop-In restrictions, explicit content filters, and communication controls. Each must be configured per-device. Parents often miss critical settings like voice deactivation toggles that let kids undo filters.",
    currentJourney: [
      "Search 'Alexa parental controls' → land on a 2,000-word guide",
      "Open Alexa app → Devices → select Echo Show → scroll to Amazon Kids → toggle on → Setup Amazon FreeTime",
      "Fill in child profile (name, age, gender) → consent flow → 2FA verification",
      "Separately: Settings → Account Settings → Voice Purchasing → toggle off or set PIN",
      "Separately: Settings → Music & Podcasts → toggle Explicit Filter on",
      "Separately: Settings → Device Settings → select device → Do Not Disturb → toggle Scheduled → set times",
      "Separately: Settings → Communication → Drop-In → set to 'My Household' or 'Off'",
      "Forget to disable Voice Deactivation → child says 'Alexa, turn off explicit filter' → back to square one",
    ],
    aiApproach: {
      userSays:
        "My 6-year-old uses our kitchen Echo Show. I want to make it safe for her but still usable for me and my partner.",
      systemResponse: [
        "Interprets intent: child safety + shared adult use → identifies 7 relevant settings across 4 app sections",
        "Generates a single unified control panel with all child-safety toggles pre-recommended",
        "Highlights the commonly missed 'Voice Deactivation' toggle with a warning callout",
        "Shows a time-schedule builder for Do Not Disturb (bedtime blocking)",
        "Pre-fills age-appropriate defaults based on child's age (6 → stricter filters)",
      ],
      generatedUI: {
        type: "Child Safety Control Panel",
        sections: [
          {
            name: "Content Filters",
            controls: [
              { label: "Explicit Music Filter", type: "toggle", recommended: true, value: true },
              { label: "Voice Deactivation of Filters", type: "toggle", recommended: false, value: false, warning: "If ON, anyone can say 'Alexa, turn off explicit filter'" },
              { label: "Kid Skills Only Mode", type: "toggle", recommended: true, value: true },
            ],
          },
          {
            name: "Purchasing & Ordering",
            controls: [
              { label: "Voice Purchasing", type: "toggle", recommended: false, value: false },
              { label: "Purchase Confirmation PIN", type: "pin", recommended: true, value: "••••" },
            ],
          },
          {
            name: "Communication Boundaries",
            controls: [
              { label: "Drop-In Access", type: "select", options: ["Anyone", "My Household Only", "Off"], recommended: "My Household Only", value: "My Household Only" },
              { label: "Calling & Messaging", type: "toggle", recommended: false, value: false },
            ],
          },
          {
            name: "Schedule Controls",
            controls: [
              { label: "Do Not Disturb (Bedtime)", type: "timerange", recommended: true, value: "8:30 PM – 7:00 AM" },
              { label: "Daily Time Limit", type: "duration", recommended: true, value: "2 hours" },
            ],
          },
        ],
      },
    },
    impact:
      "7 separate navigation paths collapsed into 1 unified panel. Zero chance of missing the Voice Deactivation gotcha. Time: ~2 minutes vs ~25 minutes.",
  },
  {
    id: "multiroom",
    title: "Multi-Room Audio Across Mixed Devices",
    emoji: "🔊",
    persona: "User with 5 Echo devices (2× Echo Dot 3rd Gen, 1× Echo Studio, 1× Echo Show 8, 1× Echo Pop) across different rooms",
    problem:
      "Setting up multi-room music groups requires all devices on the same Wi-Fi network and Amazon account. Users with mesh networks or dual-band routers frequently hit 'network error' when trying to group devices — one device on 2.4GHz and another on 5GHz causes silent failures. Stereo pairing only works with identical models. Bluetooth-connected external speakers break multi-room sync entirely. The Alexa app gives a generic 'network error' with no diagnostic info.",
    currentJourney: [
      "Alexa app → Devices → '+' → Combine Speakers → Multi-Room Music",
      "Select first device → second device greys out with 'Network Error'",
      "Search forums → discover dual-band Wi-Fi issue → no way to check band in Alexa app",
      "Log into router admin panel → find device → check frequency band → manually reassign",
      "Return to Alexa app → retry → still fails → factory reset device → re-setup from scratch",
      "Try to add Echo Studio to stereo pair with Echo Dot → discover model mismatch restriction",
      "Finally get group working → try Bluetooth speaker → audio drops from group entirely",
    ],
    aiApproach: {
      userSays:
        "I want music playing in every room of my house at the same time. I have Echo devices in the living room, kitchen, bedroom, office, and bathroom.",
      systemResponse: [
        "Queries all registered devices → shows a visual map of devices with their network status",
        "Detects that Echo Dot (Office) is on 5GHz while others are on 2.4GHz → flags the mismatch",
        "Identifies that the Echo Studio can't stereo-pair with Dot but CAN join a multi-room group",
        "Warns that the bathroom Echo Pop connected via Bluetooth speaker will break sync",
        "Generates a drag-and-drop group builder with real-time compatibility validation",
      ],
      generatedUI: {
        type: "Multi-Room Audio Builder",
        sections: [
          {
            name: "Your Devices",
            controls: [
              { label: "Echo Dot — Living Room", type: "device", status: "ready", network: "2.4GHz", value: true },
              { label: "Echo Studio — Living Room", type: "device", status: "ready", network: "2.4GHz", value: true },
              { label: "Echo Show 8 — Kitchen", type: "device", status: "ready", network: "2.4GHz", value: true },
              { label: "Echo Dot — Office", type: "device", status: "warning", network: "5GHz", value: false, warning: "Different Wi-Fi band. Move to 2.4GHz to join group." },
              { label: "Echo Pop — Bathroom", type: "device", status: "warning", network: "2.4GHz (BT speaker attached)", value: false, warning: "Bluetooth speakers break multi-room sync. Disconnect to join." },
            ],
          },
          {
            name: "Group Configuration",
            controls: [
              { label: "Group Name", type: "text", value: "Everywhere", recommended: true },
              { label: "Preferred Music Service", type: "select", options: ["Amazon Music", "Spotify", "Apple Music"], value: "Spotify" },
              { label: "Stereo Pair (Living Room)", type: "toggle", recommended: false, value: false, warning: "Echo Studio + Echo Dot can't stereo pair (different models). Both can play in group independently." },
            ],
          },
        ],
      },
    },
    impact:
      "Diagnoses the actual root cause (Wi-Fi band mismatch, Bluetooth conflict) instead of showing a generic 'network error'. Prevents impossible stereo-pair attempts. Visual device map eliminates guesswork.",
  },
  {
    id: "routine",
    title: "Building a Complex Morning Routine",
    emoji: "🌅",
    persona: "Couple where one partner leaves at 6:30 AM and the other at 8:30 AM, with smart lights, thermostat, and coffee maker",
    problem:
      "Alexa Routines support sequential actions with wait delays, but building a multi-phase morning routine for a household with different schedules requires creating multiple separate routines, understanding trigger types (time, voice, alarm dismiss), and correctly ordering actions with wait delays. There's no visual timeline — just a flat list of actions. Users can't easily see timing conflicts or test the routine without actually running it.",
    currentJourney: [
      "Alexa app → More → Routines → '+' → name routine 'Good Morning'",
      "Add trigger: Schedule → 6:15 AM → Weekdays only",
      "Add action: Smart Home → Lights → Bedroom → 30% warm white",
      "Add action: Wait → 5 minutes",
      "Add action: Smart Home → Lights → Bedroom → 70%",
      "Add action: Smart Home → Coffee Maker (smart plug) → On",
      "Add action: Alexa Says → Weather forecast",
      "Realize this only works for Partner A → need a SECOND routine for Partner B at 8:15 AM",
      "Create second routine → accidentally overlap thermostat settings → house goes cold at 7 AM when Partner B is still home",
      "No way to visualize both routines on a timeline → trial and error over multiple mornings",
    ],
    aiApproach: {
      userSays:
        "My partner leaves for work at 6:30 and I leave at 8:30. We want a morning routine that gradually wakes us up, makes coffee, reads the news, and adjusts the thermostat — but it shouldn't turn things off when my partner leaves because I'm still home.",
      systemResponse: [
        "Understands the dual-schedule household constraint — this is the key insight traditional guides miss",
        "Generates a visual timeline showing both schedules side-by-side",
        "Identifies the thermostat conflict: 'leaving mode' at 6:30 would affect Partner B",
        "Suggests splitting into 3 routines: Shared Wake-Up, Partner A Departure, Partner B Departure",
        "Builds conditional logic: thermostat only goes to eco-mode after BOTH have left",
      ],
      generatedUI: {
        type: "Morning Routine Timeline Builder",
        sections: [
          {
            name: "6:15 AM — Shared Wake-Up",
            controls: [
              { label: "Bedroom Lights", type: "ramp", value: "30% → 70% → 100% over 15 min" },
              { label: "Coffee Maker (Smart Plug)", type: "toggle", value: true, recommended: true },
              { label: "Thermostat", type: "temp", value: "68°F (from 64°F night mode)" },
              { label: "News Briefing", type: "toggle", value: true },
            ],
          },
          {
            name: "6:30 AM — Partner A Leaves",
            controls: [
              { label: "Announcement", type: "text", value: "'Have a great day!' on kitchen Echo" },
              { label: "Bedroom Lights", type: "info", value: "Keep ON (Partner B still home)", warning: "Would normally turn off in a 'leaving' routine" },
              { label: "Thermostat", type: "info", value: "Keep at 68°F (Partner B still home)" },
            ],
          },
          {
            name: "8:30 AM — Partner B Leaves",
            controls: [
              { label: "All Lights", type: "toggle", value: false },
              { label: "Thermostat", type: "temp", value: "62°F (eco mode)" },
              { label: "Robot Vacuum", type: "toggle", value: true },
              { label: "Security Cameras", type: "toggle", value: true },
            ],
          },
        ],
      },
    },
    impact:
      "Visual timeline prevents the thermostat conflict. Dual-schedule awareness is built in. 3 coordinated routines generated from a single natural-language description instead of manual trial-and-error.",
  },
  {
    id: "privacy",
    title: "Privacy Lockdown for a Guest-Accessible Device",
    emoji: "🔒",
    persona: "Airbnb host with an Echo Show 15 in the rental unit",
    problem:
      "Hosts need to provide guests with smart home control (lights, thermostat, info) while preventing access to the host's Amazon account, purchase history, personal calendar, drop-in to other household devices, and voice recordings. There's no 'guest mode' — hosts must manually disable 15+ individual settings, and Alexa's privacy hub buries critical controls across multiple screens. Voice recordings are saved by default, creating potential liability.",
    currentJourney: [
      "Settings → Alexa Privacy → Manage Your Alexa Data → toggle 'Don't save voice recordings'",
      "Settings → Alexa Privacy → Manage how your data improves Alexa → opt out of all",
      "Settings → Account Settings → Voice Purchasing → Off",
      "Settings → Communication → Drop-In → Off for this device",
      "Settings → Communication → Calling & Messaging → Off",
      "Settings → Device Settings → [device] → Do Not Disturb → schedule around check-in/out",
      "Settings → Notifications → disable all personal notifications",
      "Realize calendar events still show on Echo Show ambient display → disable separately",
      "Realize photos from Amazon Photos rotate on screen → disable or set to a specific album",
      "Realize guests can still access browsing history via Echo Show → clear and restrict",
      "Every single setting resets if device is factory reset between guests",
    ],
    aiApproach: {
      userSays:
        "I'm an Airbnb host. I want my guests to control lights, thermostat, and ask Alexa basic questions — but nothing personal should be accessible. No purchases, no access to my other devices, no saved recordings.",
      systemResponse: [
        "Recognizes 'guest/rental mode' intent → maps to 15+ privacy-relevant settings",
        "Categorizes into: Data Privacy, Account Protection, Communication Lockdown, Display Privacy, Smart Home Access",
        "Generates a single 'Guest Mode' configurator with all settings pre-set to maximum privacy",
        "Flags the commonly forgotten items: calendar display, photo rotation, notification leakage",
        "Offers a 'reset checklist' for between-guest turnovers",
      ],
      generatedUI: {
        type: "Guest Mode Configurator",
        sections: [
          {
            name: "Data & Recordings",
            controls: [
              { label: "Save Voice Recordings", type: "toggle", recommended: false, value: false },
              { label: "Use Recordings to Improve Alexa", type: "toggle", recommended: false, value: false },
              { label: "Auto-Delete Recordings", type: "select", options: ["Don't save", "3 months", "18 months"], recommended: "Don't save", value: "Don't save" },
            ],
          },
          {
            name: "Account Protection",
            controls: [
              { label: "Voice Purchasing", type: "toggle", recommended: false, value: false },
              { label: "Personal Calendar Display", type: "toggle", recommended: false, value: false, warning: "Your calendar events show on the Echo Show ambient screen by default" },
              { label: "Amazon Photos Rotation", type: "select", options: ["Off", "Specific Album Only", "All Photos"], recommended: "Off", value: "Off", warning: "Personal photos display by default" },
              { label: "Personal Notifications", type: "toggle", recommended: false, value: false },
            ],
          },
          {
            name: "Communication Lockdown",
            controls: [
              { label: "Drop-In", type: "toggle", recommended: false, value: false },
              { label: "Calling & Messaging", type: "toggle", recommended: false, value: false },
              { label: "Announcements from Other Devices", type: "toggle", recommended: false, value: false },
            ],
          },
          {
            name: "Guest Capabilities (Keep ON)",
            controls: [
              { label: "Smart Lights Control", type: "toggle", value: true, recommended: true },
              { label: "Thermostat Control", type: "toggle", value: true, recommended: true },
              { label: "Weather & General Questions", type: "toggle", value: true, recommended: true },
              { label: "Music (Amazon Music Free Tier)", type: "toggle", value: true, recommended: true },
              { label: "Timers & Alarms", type: "toggle", value: true, recommended: true },
            ],
          },
        ],
      },
    },
    impact:
      "15+ scattered settings unified into one 'Guest Mode' panel. Catches the calendar/photo leakage that 90% of hosts miss. Generates a turnover checklist. Could be saved as a profile and re-applied between guests.",
  },
  {
    id: "nightsecurity",
    title: "Nighttime Security Automation",
    emoji: "🌙",
    persona: "Homeowner with Ring cameras, smart locks, motion sensors, Echo devices in 4 rooms, and smart lights",
    problem:
      "Creating a comprehensive 'Night Mode' requires coordinating devices across multiple ecosystems (Ring, smart locks, Alexa routines, light groups). Users need to: create a routine that locks doors, arms cameras, sets motion-triggered lighting, enables Alexa Guard mode, and configures announcements — while handling exceptions like the bathroom night light and ensuring the midnight-snack path stays motion-lit. The Alexa app treats each of these as separate configuration domains.",
    currentJourney: [
      "Create routine 'Good Night' → add actions one by one from a flat list",
      "Smart Home → All Lights → Off... but wait, need bathroom night light at 5%",
      "Have to turn off lights by GROUP, then separately set bathroom light → correct ordering matters",
      "Add smart lock action → requires separate Ring/lock app skill to be linked",
      "Add Guard mode → hidden in Settings → Guard → toggle, not available as routine action on all devices",
      "Want motion-triggered hallway light after 11 PM → requires a SEPARATE routine with motion sensor trigger + time condition",
      "Want Ring cameras to announce on Echo when motion detected → yet another separate routine",
      "No way to see all of these as one cohesive 'night security system'",
    ],
    aiApproach: {
      userSays:
        "When I say goodnight, I want everything locked down and secure. All lights off except a dim bathroom night light. If someone walks to the kitchen at night, the hallway should light up briefly. Ring cameras should alert me to any outdoor motion. And everything should unlock at 6 AM.",
      systemResponse: [
        "Decomposes into 4 coordinated routines: Goodnight trigger, Motion response, Camera alerts, Morning unlock",
        "Identifies device dependencies: Ring skill must be linked, smart lock must be discovered, Guard mode availability",
        "Generates a visual 'security layer' diagram showing what happens at each stage",
        "Handles the exception cases: bathroom night light stays on, hallway responds to motion, kitchen path is lit",
        "Creates the morning 'undo' routine automatically",
      ],
      generatedUI: {
        type: "Night Security Orchestrator",
        sections: [
          {
            name: "Trigger: 'Alexa, Goodnight'",
            controls: [
              { label: "All Lights Off (except exceptions)", type: "toggle", value: true, recommended: true },
              { label: "Bathroom Night Light", type: "brightness", value: "5% warm white" },
              { label: "Front Door Smart Lock", type: "toggle", value: true, recommended: true },
              { label: "Back Door Smart Lock", type: "toggle", value: true, recommended: true },
              { label: "Alexa Guard Mode", type: "toggle", value: true, recommended: true },
              { label: "Do Not Disturb (all Echos)", type: "toggle", value: true },
              { label: "Thermostat → Night Mode", type: "temp", value: "65°F" },
            ],
          },
          {
            name: "After 11 PM: Motion Responses",
            controls: [
              { label: "Hallway Motion → Hallway Light", type: "conditional", value: "20% for 3 minutes" },
              { label: "Kitchen Motion → Under-Cabinet Lights", type: "conditional", value: "15% for 5 minutes" },
              { label: "Outdoor Motion → Ring Alert to Bedroom Echo", type: "conditional", value: "Chime + camera feed on Echo Show", warning: "Override Do Not Disturb for security alerts" },
            ],
          },
          {
            name: "6:00 AM — Morning Unlock",
            controls: [
              { label: "Disable Guard Mode", type: "toggle", value: true },
              { label: "Unlock Doors", type: "toggle", value: false, warning: "Recommended: keep locked, unlock manually or via morning routine" },
              { label: "Resume Normal Lighting", type: "toggle", value: true },
              { label: "Disable Do Not Disturb", type: "toggle", value: true },
            ],
          },
        ],
      },
    },
    impact:
      "4 separate routines + 3 settings changes designed as one cohesive system. Exception handling (bathroom light, motion paths) built in. Morning 'undo' auto-generated. Cross-ecosystem coordination (Ring + Alexa + smart locks) presented as a unified security layer.",
  },
  {
    id: "vacation",
    title: "Two-Week Vacation Home Simulation",
    emoji: "✈️",
    persona: "Family leaving for 14-day trip with Ring cameras, smart lights in 6 rooms, smart thermostat, Echo devices, smart locks, and a pet sitter visiting daily",
    problem:
      "Alexa's vacation preparation spans 4 separate feature domains that don't talk to each other: Guard mode (Settings → Guard), Away Lighting (Devices → any light → Settings → Away Lighting), Home/Away Modes (requires initial mode setup before vacation mode even appears), and Routines (for thermostat, lock scheduling). The pet sitter complicates everything — they need entry access at specific times without disabling security. Away Lighting uses ML-based patterns but you can't choose WHICH lights participate without going into each light individually. Guard's smart alerts will flood your phone if Ring cameras detect the pet sitter as motion events.",
    currentJourney: [
      "Settings → Guard → enable → select sounds (smoke, CO, glass break) → individually",
      "Devices → select EACH light individually → Settings → Away Lighting → toggle on (repeat 6 times)",
      "Realize you need Home/Away modes set up FIRST before Vacation Mode appears as an option",
      "Settings → Modes → Set Up Home Mode → configure → Set Up Away Mode → configure → THEN 'Add Vacation Mode' appears",
      "Create a routine for thermostat: eco mode 58°F while away, but 68°F during pet sitter window (noon–2pm daily)",
      "Create a routine for smart lock: auto-unlock at 11:55 AM for pet sitter, re-lock at 2:05 PM",
      "Ring app (separate!) → set motion zones to exclude pet sitter's usual path → but this disables that zone entirely",
      "Realize Ring camera alerts + Guard smart alerts will fire simultaneously → duplicate notifications",
      "Set up Do Not Disturb on all Echos → but then miss genuine security alerts",
      "No single view showing 'here's what happens during your vacation' across all these systems",
    ],
    aiApproach: {
      userSays:
        "We're going on vacation for 2 weeks starting Saturday. Our pet sitter Sarah comes daily around noon for 2 hours. I want the house to look occupied, stay secure, but not blast me with false alerts every time Sarah visits.",
      systemResponse: [
        "Detects multi-system coordination need: Guard + Away Lighting + Modes + Routines + Ring + Smart Locks",
        "Identifies the pet sitter exception as the core complexity — creates a 'trusted visitor window' concept",
        "Pre-checks that Home/Away modes are set up (prerequisite for Vacation Mode) and flags if missing",
        "Generates a vacation timeline showing what happens at each phase: departure, daily simulation, pet sitter window, night security, return",
        "Creates smart alert filtering: suppress Ring motion alerts during pet sitter window, escalate all others",
        "Selects which lights participate in Away Lighting based on room visibility from outside (front rooms yes, interior closets no)",
      ],
      generatedUI: {
        type: "Vacation Mode Planner",
        sections: [
          {
            name: "Trip Details",
            controls: [
              { label: "Departure", type: "datetime", value: "Saturday, Mar 28 — 8:00 AM" },
              { label: "Return", type: "datetime", value: "Saturday, Apr 11 — 6:00 PM" },
              { label: "Thermostat (Away)", type: "temp", value: "58°F (eco mode)", recommended: true },
              { label: "Thermostat (Pet Sitter Window)", type: "temp", value: "68°F (noon–2 PM daily)" },
            ],
          },
          {
            name: "Away Lighting — Room Selection",
            controls: [
              { label: "Living Room (street-facing)", type: "toggle", value: true, recommended: true },
              { label: "Kitchen (street-facing)", type: "toggle", value: true, recommended: true },
              { label: "Master Bedroom (upstairs, visible)", type: "toggle", value: true, recommended: true },
              { label: "Bathroom (interior)", type: "toggle", value: false, recommended: false },
              { label: "Closet/Hallway (interior)", type: "toggle", value: false, recommended: false },
              { label: "Porch Light", type: "toggle", value: true, recommended: true, warning: "Dusk-to-dawn schedule recommended instead of Away Lighting randomization" },
            ],
          },
          {
            name: "Pet Sitter Window (Daily: 11:55 AM – 2:05 PM)",
            controls: [
              { label: "Smart Lock → Auto-Unlock at 11:55 AM", type: "toggle", value: true, recommended: true },
              { label: "Smart Lock → Auto-Lock at 2:05 PM", type: "toggle", value: true, recommended: true },
              { label: "Suppress Ring Motion Alerts (indoor cams)", type: "toggle", value: true, recommended: true, warning: "Only suppresses indoor cameras during this window. Outdoor cameras stay active." },
              { label: "Guard Mode → Pause Smart Alerts (this window only)", type: "toggle", value: true, recommended: true },
              { label: "Thermostat → Warm to 68°F", type: "toggle", value: true },
            ],
          },
          {
            name: "Security & Alerts",
            controls: [
              { label: "Alexa Guard (smoke, CO, glass break)", type: "toggle", value: true, recommended: true },
              { label: "Away Lighting (ML-randomized)", type: "toggle", value: true, recommended: true },
              { label: "Ring Outdoor Cameras → Always Alert", type: "toggle", value: true, recommended: true },
              { label: "Ring Indoor Cameras → Alert (except pet sitter window)", type: "conditional", value: "Active outside 11:55 AM – 2:05 PM" },
              { label: "Duplicate Alert Suppression", type: "toggle", value: true, recommended: true, warning: "Prevents Ring + Guard from sending the same event twice" },
            ],
          },
        ],
      },
    },
    impact:
      "10+ separate configuration steps across 3 apps (Alexa, Ring, thermostat) unified into one vacation planner. Pet sitter exception handled as a first-class concept instead of an afterthought. Away Lighting room selection batched instead of per-light. Duplicate alert suppression prevents notification fatigue.",
  },
  {
    id: "household",
    title: "4-Person Household Personalization",
    emoji: "👨‍👩‍👧‍👦",
    persona: "Family of 4: two adults (different music/news preferences, separate Amazon accounts), a 14-year-old teen, and a 7-year-old child, sharing 4 Echo devices across the home",
    problem:
      "Alexa supports Voice ID, Visual ID, Alexa Profiles, Household Profiles, and Amazon Kids — but these are 5 different systems with different setup paths, different capabilities, and confusing overlap. Voice ID recognizes who's speaking to personalize music and calendars, but Household Profiles require linking Amazon accounts for shared Prime and purchases. Amazon Kids requires a separate child profile per device. The teen wants Spotify (linked to Parent A's profile), the 7-year-old needs Amazon Kids content, Parent B wants Apple Music. Each person's flash briefing, calendar, and shopping list should be separate. Setting this up correctly requires ~20 distinct configuration steps across multiple app sections, and one misstep (like the teen using Parent A's voice profile) causes the wrong shopping list and calendar to appear.",
    currentJourney: [
      "Parent A: More → Settings → Your Profile & Family → set up own Alexa Profile → Voice ID training (say phrases aloud)",
      "Parent B: Sign out of Alexa app → sign back in with same Amazon ID → select 'I'm someone else' → create profile → Voice ID training",
      "OR: Parent B has separate Amazon account → Settings → Household Profile → link accounts → share Prime benefits",
      "Wait ~20 minutes for Voice ID data to sync across all 4 Echo devices",
      "Teen: Create Alexa Profile (not Amazon Kids — they're 14) → Voice ID training → BUT can't link their own Spotify directly",
      "7-year-old: Settings → Amazon Kids → create child profile → enable per-device → consent flow → content filtering",
      "Realize Amazon Kids can only be toggled per-device, not per-person → shared kitchen Echo treats everyone as a child when Kids mode is on",
      "Parent A: Settings → Music & Podcasts → set default to Amazon Music → link Spotify for teen under their profile",
      "Parent B: Switch to their profile → Settings → Music & Podcasts → set default to Apple Music",
      "Each person: Settings → Flash Briefing → customize news sources (repeat 3× for adults + teen)",
      "Each person: Link personal calendar → Settings → Calendar → add account (repeat per person)",
      "Discover that Voice ID sometimes confuses Parent A and teen voices → wrong calendar/music plays",
      "No single dashboard showing 'who gets what' across the household",
    ],
    aiApproach: {
      userSays:
        "There are 4 of us — me, my wife, our 14-year-old, and our 7-year-old. We all use the Echos differently. I want Amazon Music, my wife wants Apple Music, our teen wants Spotify, and our youngest needs kid-safe content. Everyone should get their own news, calendar, and shopping list.",
      systemResponse: [
        "Maps the 4-person household to the correct mix of systems: Alexa Profiles (adults + teen) + Amazon Kids (7-year-old) + Household Profiles (if separate Amazon accounts)",
        "Identifies the critical distinction: teen gets an Alexa Profile (not Amazon Kids) — age-appropriate but not child-locked",
        "Detects the Amazon Kids per-device problem: recommends specific Echo devices for Kids mode vs shared family devices",
        "Generates a household matrix showing who gets what service, on which device, with which profile type",
        "Flags the voice confusion risk between Parent A and teen — suggests re-training Voice ID in different rooms",
        "Creates a step-by-step setup sequence optimized for dependencies (account linking → profiles → voice training → services)",
      ],
      generatedUI: {
        type: "Household Personalization Matrix",
        sections: [
          {
            name: "Parent A — Alex",
            controls: [
              { label: "Profile Type", type: "info", value: "Alexa Profile + Voice ID + Visual ID" },
              { label: "Default Music", type: "select", options: ["Amazon Music", "Spotify", "Apple Music"], value: "Amazon Music", recommended: "Amazon Music" },
              { label: "Flash Briefing", type: "info", value: "NPR, Reuters, Wall Street Journal" },
              { label: "Calendar", type: "info", value: "Google Calendar (work)" },
              { label: "Shopping List", type: "info", value: "Personal (linked to Amazon account)" },
              { label: "Voice ID Status", type: "device", value: true },
            ],
          },
          {
            name: "Parent B — Jamie",
            controls: [
              { label: "Profile Type", type: "select", options: ["Alexa Profile (same account)", "Household Profile (separate account)"], value: "Household Profile (separate account)", recommended: "Household Profile (separate account)" },
              { label: "Default Music", type: "select", options: ["Amazon Music", "Spotify", "Apple Music"], value: "Apple Music", recommended: "Apple Music" },
              { label: "Flash Briefing", type: "info", value: "BBC, The Economist" },
              { label: "Calendar", type: "info", value: "iCloud Calendar (personal)" },
              { label: "Voice ID Status", type: "device", value: true },
            ],
          },
          {
            name: "Teen (14) — Riley",
            controls: [
              { label: "Profile Type", type: "info", value: "Alexa Profile (NOT Amazon Kids)", warning: "At 14, Amazon Kids is too restrictive. Alexa Profile gives personalization without child-locking the device." },
              { label: "Default Music", type: "info", value: "Spotify (linked via Parent A's account)" },
              { label: "Explicit Music Filter", type: "toggle", value: true, recommended: true },
              { label: "Voice Purchasing", type: "toggle", value: false, recommended: false },
              { label: "Voice ID Status", type: "device", value: true, warning: "Re-train if frequently confused with Parent A. Train in different rooms." },
            ],
          },
          {
            name: "Child (7) — Casey",
            controls: [
              { label: "Profile Type", type: "info", value: "Amazon Kids (child profile)" },
              { label: "Kids-Enabled Devices", type: "info", value: "Bedroom Echo Dot (dedicated) + Kitchen Echo (shared, via Voice ID)", warning: "On shared devices, Amazon Kids activates when Casey's voice is recognized." },
              { label: "Content Age Filter", type: "select", options: ["Ages 3-5", "Ages 6-8", "Ages 9-12"], value: "Ages 6-8", recommended: "Ages 6-8" },
              { label: "Daily Time Limit", type: "duration", value: "1.5 hours" },
              { label: "Calling & Messaging", type: "toggle", value: false, recommended: false },
            ],
          },
          {
            name: "Setup Sequence (Dependency Order)",
            controls: [
              { label: "Step 1: Link Amazon Household (if separate accounts)", type: "info", value: "Required before Household Profiles work" },
              { label: "Step 2: Create all 4 Alexa Profiles", type: "info", value: "Adults + teen on same Alexa account" },
              { label: "Step 3: Train Voice ID (each person, separately)", type: "info", value: "~5 min each, allow 20 min sync" },
              { label: "Step 4: Link music services per profile", type: "info", value: "Must switch active profile before linking" },
              { label: "Step 5: Configure Amazon Kids for Casey", type: "info", value: "Per-device toggle + child profile + content filter" },
              { label: "Step 6: Set Flash Briefing per person", type: "info", value: "Switch profile → Settings → Flash Briefing (repeat)" },
            ],
          },
        ],
      },
    },
    impact:
      "20+ configuration steps organized into a dependency-aware sequence. Household matrix makes 'who gets what' visible at a glance. Catches the teen-vs-child profile distinction, the per-device Amazon Kids limitation, and the voice confusion risk. Estimated: 30 min guided vs 2+ hours trial and error.",
  },
  {
    id: "notifications",
    title: "Taming Notification Overload",
    emoji: "🔕",
    persona: "User with 6 Echo devices, Ring doorbell, 3 smart home skills, Amazon Prime shopping, and a connected thermostat — receiving 30+ daily notifications",
    problem:
      "Alexa notifications come from at least 8 separate sources: Amazon Shopping (orders, deliveries, deals), Hunches (smart home suggestions), Skills (each has its own toggle), Reminders, Communications (calls, messages, Drop-In), Smart Home alerts (motion, temperature, sensors), Flash Briefing auto-play, and 'By the way' post-response suggestions. Each is configured in a different app section. The yellow notification ring provides no indication of priority or source. There's no way to say 'only alert me about security, not packages' without toggling 15+ individual switches. Brief Mode reduces verbosity but NOT notification volume.",
    currentJourney: [
      "More → Settings → Notifications → Amazon Shopping → individually toggle: Out for Delivery, Delivered, Order Updates, Deals",
      "More → Settings → Notifications → Hunches → gear icon → toggle off suggestions (automatic actions are configured elsewhere)",
      "More → Settings → Notifications → Manage Skills → scroll through EVERY enabled skill → toggle notifications individually",
      "More → Settings → Notifications → Things to Try → toggle off ('By the way' suggestions)",
      "Devices → select each Echo → Device Settings → Do Not Disturb → schedule (repeat for all 6 devices individually)",
      "Ring app (separate) → Notification Settings → Motion Alerts → per-camera toggles",
      "Thermostat app (separate) → Notification Settings → adjust temperature thresholds",
      "More → Settings → Alexa Preferences → Brief Mode → toggle (reduces response length, NOT notifications)",
      "Still getting flooded → realize Announcements is a separate category → Settings → Notifications → Announcements → toggle",
      "No priority system — a smoke alarm alert looks identical (yellow ring) to a package delivery update",
    ],
    aiApproach: {
      userSays:
        "Alexa won't stop interrupting me. I'm getting package updates, 'by the way' suggestions, skill notifications, doorbell alerts, and hunch suggestions all day. I only care about security alerts and my personal reminders. Everything else should be silent.",
      systemResponse: [
        "Audits all active notification sources — surfaces the complete list of what's generating alerts",
        "Categorizes by type: Security/Safety (keep), Personal (keep), Convenience (suppress), Marketing/Suggestions (suppress)",
        "Identifies that Ring, thermostat, and skill notifications each require different app/settings paths",
        "Generates a priority-based control panel with bulk category actions: 'Mute all shopping', 'Mute all suggestions'",
        "Creates per-device Do Not Disturb schedules in batch instead of one-by-one",
        "Explains that Brief Mode ≠ fewer notifications (a crucial distinction users consistently misunderstand)",
      ],
      generatedUI: {
        type: "Notification Priority Manager",
        sections: [
          {
            name: "🔴 Security & Safety — Keep Active",
            controls: [
              { label: "Ring Doorbell Press Alerts", type: "toggle", value: true, recommended: true },
              { label: "Ring Camera Motion (outdoor, night)", type: "conditional", value: "10 PM – 6 AM only" },
              { label: "Alexa Guard (smoke, CO, glass break)", type: "toggle", value: true, recommended: true },
              { label: "Smart Lock Alerts (unexpected unlock)", type: "toggle", value: true, recommended: true },
            ],
          },
          {
            name: "🟡 Personal — Keep Active",
            controls: [
              { label: "Reminders & Timers", type: "toggle", value: true, recommended: true },
              { label: "Calendar Notifications", type: "toggle", value: true, recommended: true },
              { label: "Calls & Messages from Contacts", type: "toggle", value: true },
            ],
          },
          {
            name: "⚪ Shopping — Suppress",
            controls: [
              { label: "Out for Delivery", type: "toggle", value: false, recommended: false },
              { label: "Delivered", type: "toggle", value: false, recommended: false },
              { label: "Order Updates", type: "toggle", value: false, recommended: false },
              { label: "Deals & Recommendations", type: "toggle", value: false, recommended: false },
            ],
          },
          {
            name: "⚪ Suggestions & Proactive — Suppress",
            controls: [
              { label: "Hunches (smart home suggestions)", type: "toggle", value: false, recommended: false, warning: "Disables suggestions only. Hunches automatic actions controlled separately in Settings → Hunches → Automatic Actions." },
              { label: "'By the Way' Post-Response Tips", type: "toggle", value: false, recommended: false },
              { label: "'Things to Try' Suggestions", type: "toggle", value: false, recommended: false },
              { label: "Skill Notifications (bulk)", type: "toggle", value: false, recommended: false, warning: "Mutes all 3 skill notification sources at once." },
            ],
          },
          {
            name: "⚪ Device Behavior — Quiet Mode",
            controls: [
              { label: "Brief Mode (shorter responses)", type: "toggle", value: true, recommended: true, warning: "Brief Mode makes Alexa's RESPONSES shorter. It does NOT reduce the NUMBER of notifications." },
              { label: "Adaptive Listening", type: "toggle", value: true, recommended: true },
              { label: "Do Not Disturb (all 6 devices, batched)", type: "timerange", value: "10 PM – 7 AM", warning: "Applied to all Echo devices at once instead of configuring each individually" },
            ],
          },
        ],
      },
    },
    impact:
      "15+ individual toggles across 4 app sections + 2 external apps organized into a priority-based panel. Bulk actions for entire categories. Per-device DND done once instead of 6 times. Clarifies the Brief Mode vs notification volume confusion that trips up most users.",
  },
  {
    id: "audio",
    title: "Whole-Home Audio Optimization",
    emoji: "🎵",
    persona: "User with Echo Studio (living room), Echo Show 8 (kitchen), Echo Dot 5th Gen (bedroom), Echo Dot 3rd Gen (bathroom), Echo Pop (office) — each room has a different purpose",
    problem:
      "Alexa's equalizer (bass/midrange/treble, -6 to +6) must be configured per-device with no batch controls or presets. Each device has different speaker capabilities — boosting bass on an Echo Pop does nothing useful, while the Echo Studio handles dramatic EQ changes. There are no room-acoustic presets, no purpose-based profiles (music vs podcasts vs sleep), and no way to see all EQ settings side by side. Default music service, playback quality, and preferred speaker also must be set per device. Multi-room groups add complexity: mixing devices of different generations causes audio latency sync issues. Volume normalization across devices with vastly different power is entirely manual.",
    currentJourney: [
      "Devices → Echo & Alexa → select Echo Studio → gear icon → Audio Settings → Equalizer → adjust 3 sliders",
      "Repeat for Echo Show 8 → different optimal settings for smaller speakers",
      "Repeat for Echo Dot 5th Gen → different again, less bass capability",
      "Repeat for Echo Dot 3rd Gen → older generation, different audio profile entirely",
      "Repeat for Echo Pop → minimal speaker, EQ barely makes a difference",
      "Set default music service per device: Devices → each device → gear → Music & Podcasts → set preferred service (5 times)",
      "Set preferred speaker for each room group: Devices → room group → gear → Preferred Speaker → select",
      "Create multi-room group: Devices → '+' → Combine Speakers → Multi-Room Music → select devices → name group",
      "Play music → Echo Studio overpowers Echo Pop → manually adjust volume on each during playback",
      "Try stereo pairing Echo Studio + Echo Dot → not allowed (model mismatch)",
      "Switch to podcasts → EQ is wrong (too much bass for voice) → re-adjust each device manually again",
      "No way to switch between 'music EQ' and 'podcast EQ' profiles",
    ],
    aiApproach: {
      userSays:
        "I want great sound in every room. Living room is for music and movies, kitchen for podcasts while cooking, bedroom for audiobooks and sleep sounds, office for focus music, bathroom for shower playlists. Optimize each device for its purpose.",
      systemResponse: [
        "Inventories all 5 devices with their speaker capabilities and generation-specific limitations",
        "Maps each room to its purpose → derives optimal EQ profiles per device and room acoustics",
        "Identifies that Echo Pop and Echo Dot 3rd Gen have limited bass response — recommends midrange-focused tuning",
        "Generates per-room audio profiles with EQ, volume, and service recommendations",
        "Creates multi-room group with volume normalization suggestions to balance speaker power differences",
        "Flags that purpose-based EQ switching has no native profile feature — suggests voice command workarounds",
      ],
      generatedUI: {
        type: "Whole-Home Audio Optimizer",
        sections: [
          {
            name: "Living Room — Echo Studio (Music & Movies)",
            controls: [
              { label: "Bass", type: "info", value: "+4 (Studio handles deep bass well)" },
              { label: "Midrange", type: "info", value: "+1" },
              { label: "Treble", type: "info", value: "+2" },
              { label: "Default Service", type: "select", options: ["Amazon Music HD", "Spotify", "Apple Music"], value: "Amazon Music HD", recommended: "Amazon Music HD" },
              { label: "Multi-Room Relative Volume", type: "info", value: "Level 5/10 (powerful speaker, lower relative)" },
            ],
          },
          {
            name: "Kitchen — Echo Show 8 (Podcasts & Cooking)",
            controls: [
              { label: "Bass", type: "info", value: "-2 (reduce muddiness for voice clarity)" },
              { label: "Midrange", type: "info", value: "+4 (optimize for spoken word)" },
              { label: "Treble", type: "info", value: "+2 (crisp dialogue)" },
              { label: "Adaptive Listening", type: "toggle", value: true, recommended: true, warning: "Kitchen noise causes Alexa to cut you off early. This adds a longer listening pause." },
            ],
          },
          {
            name: "Bedroom — Echo Dot 5th Gen (Audiobooks & Sleep)",
            controls: [
              { label: "Bass", type: "info", value: "+1 (gentle warmth)" },
              { label: "Midrange", type: "info", value: "+3 (narrator voice clarity)" },
              { label: "Treble", type: "info", value: "0 (neutral, avoid harshness at night)" },
              { label: "Sleep Timer Default", type: "duration", value: "45 minutes" },
              { label: "Alarm Volume", type: "info", value: "Set separately from media", warning: "Alarm volume won't change when you lower media for sleep sounds" },
            ],
          },
          {
            name: "Office — Echo Pop (Focus Music)",
            controls: [
              { label: "Bass", type: "info", value: "0 (Pop distorts at high bass)", warning: "Echo Pop's small speaker produces rattling, not depth, when bass is boosted. Keep neutral." },
              { label: "Midrange", type: "info", value: "+2" },
              { label: "Treble", type: "info", value: "+1" },
              { label: "DND (work hours)", type: "timerange", value: "9 AM – 5 PM weekdays" },
            ],
          },
          {
            name: "Bathroom — Echo Dot 3rd Gen (Shower Playlists)",
            controls: [
              { label: "Bass", type: "info", value: "+2 (compensate for tile reflections)" },
              { label: "Midrange", type: "info", value: "0" },
              { label: "Treble", type: "info", value: "-1 (reduce sharpness from hard surfaces)", warning: "Tiled bathrooms amplify treble. Pull back to avoid harshness." },
              { label: "Default Volume", type: "info", value: "7/10 (compensate for shower noise)" },
              { label: "Brief Mode", type: "toggle", value: true, recommended: true, warning: "Shorter responses are easier to hear over running water" },
            ],
          },
        ],
      },
    },
    impact:
      "5 devices × 3+ settings each = 15+ individual adjustments presented as purpose-driven room profiles. Device capability awareness prevents useless EQ tweaks. Room acoustics considered (tile, open space, kitchen noise). Volume normalization for multi-room groups. Alarm vs media volume distinction surfaced.",
  },
  {
    id: "elderly",
    title: "Setting Up Echo for an Elderly Parent",
    emoji: "👵",
    persona: "Adult child configuring an Echo Show 8 and Echo Dot for their 78-year-old mother who lives alone, has mild hearing loss, limited tech literacy, and takes 3 daily medications",
    problem:
      "There is no 'senior mode' or accessibility profile in Alexa. Making an Echo accessible for an elderly user requires adjusting 12+ settings across accessibility, communication, routines, reminders, emergency contacts, display, and interaction behavior — all buried in different sections. Alexa's speaking rate, Adaptive Listening, larger text on Echo Show, Drop-In for family check-ins, fall detection (Alexa Together subscription), medication reminders, and emergency calling must each be found and configured separately. The adult child is likely setting this up remotely or during a brief visit, under time pressure.",
    currentJourney: [
      "Initial: register Echo to parent's Amazon account (or own account → Household Profile complications)",
      "Devices → Echo Show → gear → Accessibility → enable Show Captions for on-screen text",
      "Devices → Echo Show → gear → Display → increase text size → adjust brightness → set Night Mode schedule",
      "Voice command: 'Alexa, speak slower' OR Settings → Accessibility → Speaking Rate → adjust",
      "Settings → Accessibility → Adaptive Listening → enable (gives more time before timeout)",
      "Settings → Communication → Drop-In → enable for 'My Household' (family check-in)",
      "Settings → Communication → Alexa Emergency Assistant → emergency contacts → link Alexa Together ($20/mo, separate setup flow)",
      "Create medication reminders: 'Alexa, remind me to take blood pressure med every day at 9 AM' → repeat per medication",
      "Realize recurring reminders have no confirmation tracking → if parent says 'stop' it just stops, no record of whether med was taken",
      "Create routines: morning check-in (weather + reminders + photos), evening wind-down",
      "Settings → Notifications → reduce to only essential → disable all shopping, suggestions, skills",
      "Settings → Account Settings → Voice Purchasing → OFF (prevent accidental orders)",
      "Program emergency contacts → enable 'Call for Help' functionality",
      "Echo Dot in bedroom: separate device settings for sleep-friendly behavior",
      "Test everything → realize parent struggles to remember the wake word → consider changing to 'Echo' or 'Computer'",
    ],
    aiApproach: {
      userSays:
        "I'm setting up an Echo Show and Echo Dot for my 78-year-old mom who lives alone. She has mild hearing loss, takes 3 daily medications, and I want to be able to check in on her. Keep it as simple as possible for her.",
      systemResponse: [
        "Recognizes 'elderly parent living alone' pattern → activates accessibility, safety, and simplification priorities",
        "Maps hearing loss → speaking rate, volume, captions, Adaptive Listening adjustments",
        "Maps living alone → emergency contacts, Drop-In for family, Alexa Together fall detection",
        "Maps 3 medications → structured recurring reminders with names and times",
        "Maps low tech literacy → minimal notifications, intuitive wake word, simplified display",
        "Generates setup organized by priority: Safety → Communication → Accessibility → Daily Routines → Clutter Removal",
        "Flags the Alexa Together subscription requirement for fall detection",
      ],
      generatedUI: {
        type: "Senior Accessibility Configurator",
        sections: [
          {
            name: "🔴 Safety & Emergency",
            controls: [
              { label: "Emergency Contact #1", type: "text", value: "You (son/daughter) — mobile" },
              { label: "Emergency Contact #2", type: "text", value: "Neighbor — Janet — mobile" },
              { label: "Alexa Emergency Assistant", type: "toggle", value: true, recommended: true, warning: "Enables 'Alexa, call for help' to reach emergency contacts" },
              { label: "Alexa Together (fall detection)", type: "toggle", value: true, recommended: true, warning: "Requires $19.99/month subscription. Detects falls, sends alerts, provides 24/7 urgent response." },
              { label: "Drop-In (family check-in)", type: "select", options: ["Off", "My Household Only", "Approved Contacts"], value: "My Household Only", recommended: "My Household Only" },
              { label: "Voice Purchasing", type: "toggle", value: false, recommended: false },
            ],
          },
          {
            name: "🟡 Hearing & Interaction",
            controls: [
              { label: "Speaking Rate", type: "select", options: ["Slower", "Default", "Faster"], value: "Slower", recommended: "Slower" },
              { label: "Default Volume", type: "info", value: "7/10 (compensate for hearing loss)" },
              { label: "Show Captions", type: "toggle", value: true, recommended: true },
              { label: "Text Size (Echo Show)", type: "select", options: ["Small", "Medium", "Large", "Extra Large"], value: "Extra Large", recommended: "Extra Large" },
              { label: "Adaptive Listening", type: "toggle", value: true, recommended: true, warning: "Extra time to finish speaking before Alexa responds" },
              { label: "Wake Word", type: "select", options: ["Alexa", "Echo", "Computer", "Amazon"], value: "Alexa", warning: "If your mom struggles with 'Alexa', try 'Echo' or 'Computer' — some find these easier" },
            ],
          },
          {
            name: "💊 Medication Reminders",
            controls: [
              { label: "Blood Pressure Med", type: "info", value: "Daily at 8:00 AM" },
              { label: "Thyroid Med", type: "info", value: "Daily at 8:00 AM (with breakfast)" },
              { label: "Evening Med", type: "info", value: "Daily at 8:00 PM" },
              { label: "Reminder Persistence", type: "info", value: "Repeat every 15 min until acknowledged", warning: "Standard reminders stop after dismissal. Consider a routine with follow-up announcements." },
            ],
          },
          {
            name: "📞 Communication Setup",
            controls: [
              { label: "Approved Callers", type: "info", value: "Family only (you, sibling, neighbor Janet)" },
              { label: "Unknown Caller Blocking", type: "toggle", value: true, recommended: true },
              { label: "Family Announcements", type: "toggle", value: true, recommended: true, warning: "You can send voice messages: 'Alexa, announce on Mom's Echo: dinner at 6!'" },
            ],
          },
          {
            name: "🌙 Daily Routines",
            controls: [
              { label: "Morning (8 AM)", type: "info", value: "Greeting → Weather → Med Reminder → Family Photos" },
              { label: "Evening (8 PM)", type: "info", value: "Med Reminder → Tomorrow's Weather → Gentle Music → Night Mode" },
              { label: "Night Mode", type: "timerange", value: "9 PM – 7 AM (dim display, clock only)" },
              { label: "Bedroom Echo Dot Volume (night)", type: "info", value: "3/10" },
            ],
          },
          {
            name: "🔇 Remove Clutter",
            controls: [
              { label: "Shopping Notifications", type: "toggle", value: false, recommended: false },
              { label: "Hunches & Suggestions", type: "toggle", value: false, recommended: false },
              { label: "'By the Way' Tips", type: "toggle", value: false, recommended: false },
              { label: "Skill Notifications", type: "toggle", value: false, recommended: false },
              { label: "Brief Mode", type: "toggle", value: true, recommended: true },
              { label: "Echo Show Ambient Display", type: "select", options: ["Family Photos Only", "Clock Only", "Rotating Content"], value: "Family Photos Only", recommended: "Family Photos Only" },
            ],
          },
        ],
      },
    },
    impact:
      "16+ scattered settings organized into priority categories (Safety → Accessibility → Communication → Comfort). Catches the Alexa Together subscription for fall detection. Medication reminders with persistence. Wake word recommendation for memorability. All clutter stripped. Setup: ~20 min guided vs 1.5+ hours hunting through articles.",
  },
  {
    id: "energysave",
    title: "Whole-Home Energy Optimization",
    emoji: "⚡",
    persona: "Homeowner with smart thermostat (Ecobee), 14 smart bulbs, 6 smart plugs, an EV charger on a smart outlet, and peak-rate electricity billing (6–10 PM weekdays costs 3× more)",
    problem:
      "Alexa has no concept of electricity rate schedules or cost optimization. Users must manually create time-based routines for peak-hour reduction, but this requires: knowing device power draw (no energy monitoring in Alexa), creating separate routines for peak-start and peak-end, shifting EV charging to off-peak, configuring a pre-cooling strategy (cool the house BEFORE peak so HVAC coasts through), and handling weekday vs weekend differences. Alexa's Energy Dashboard shows basic usage but doesn't tie to cost or suggest optimizations. Each routine action must be added one device at a time, and weekday/weekend variants require duplicating everything.",
    currentJourney: [
      "Research: figure out utility's peak/off-peak schedule (not in Alexa, check utility website)",
      "More → Routines → '+' → 'Peak Start' → Schedule → 6 PM weekdays → add actions one by one for each device",
      "Realize there's no 'dim ALL lights to 50%' bulk action for light groups — must add each light separately",
      "Create 'Pre-Cool' routine → 4:30 PM → thermostat → lower to 72°F before peak rates hit",
      "Create 'Peak End' routine → 10 PM → restore all settings to normal",
      "Create 'EV Charge Start' → 10 PM → smart plug ON (cheap off-peak power)",
      "Create 'EV Charge Stop' → 6 AM → smart plug OFF",
      "Realize weekends have different rates → duplicate ALL routines with weekend-specific schedules",
      "Alexa Energy Dashboard shows device usage time but NOT estimated cost or wattage",
      "No single view showing the overall energy strategy across all separate routines",
    ],
    aiApproach: {
      userSays:
        "My electricity is 3× more expensive between 6 and 10 PM on weekdays. I want to minimize what we use during peak hours without sacrificing comfort. I have an EV that charges overnight. Help me set everything up to save money.",
      systemResponse: [
        "Understands time-of-use rate structure → maps peak (6–10 PM weekdays), off-peak, and weekend (flat)",
        "Identifies high-draw devices: EV charger (biggest), thermostat HVAC (second), smart plug appliances",
        "Generates a pre-cooling strategy: cool house 90 min before peak, coast through at higher setpoint",
        "Creates EV charging window: start at off-peak (10 PM), stop before morning",
        "Dims lights and reduces plug loads during peak automatically",
        "Handles weekday vs weekend differentiation in one unified view instead of duplicate routines",
      ],
      generatedUI: {
        type: "Energy Optimization Planner",
        sections: [
          {
            name: "Your Rate Schedule",
            controls: [
              { label: "Peak Hours", type: "info", value: "6 PM – 10 PM (Weekdays only)" },
              { label: "Peak Rate", type: "info", value: "~$0.36/kWh (3× off-peak)" },
              { label: "Off-Peak Rate", type: "info", value: "~$0.12/kWh" },
              { label: "Weekends", type: "info", value: "Flat rate ~$0.14/kWh — no restrictions" },
            ],
          },
          {
            name: "4:30 PM — Pre-Peak Preparation (Weekdays)",
            controls: [
              { label: "Thermostat → Pre-cool to 72°F", type: "toggle", value: true, recommended: true, warning: "Cools house before peak rates hit. HVAC runs on cheap electricity, then coasts." },
              { label: "EV Charger → Stop if still charging", type: "toggle", value: true, recommended: true },
              { label: "Appliance Reminder Announcement", type: "toggle", value: true, warning: "'Peak rates start in 90 min — run dishwasher/laundry now if needed'" },
            ],
          },
          {
            name: "6:00 PM — Peak Starts (Weekdays)",
            controls: [
              { label: "Thermostat → Raise to 76°F", type: "temp", value: "76°F (coast on pre-cooling)" },
              { label: "All Lights → Dim to 50%", type: "brightness", value: "50% all rooms" },
              { label: "Entertainment (TV, speakers)", type: "toggle", value: true, warning: "Quality of life priority — keep active" },
              { label: "Non-Essential Plugs (chargers, fans)", type: "toggle", value: false, recommended: false },
              { label: "EV Charger", type: "toggle", value: false, recommended: false, warning: "Charging during peak costs ~3× more" },
            ],
          },
          {
            name: "10:00 PM — Off-Peak / Restore",
            controls: [
              { label: "Thermostat → Return to 74°F", type: "temp", value: "74°F" },
              { label: "Lights → Restore to 100%", type: "brightness", value: "100% (or follow night routine)" },
              { label: "EV Charger → Start Charging", type: "toggle", value: true, recommended: true },
              { label: "Smart Plugs → Restore all", type: "toggle", value: true },
            ],
          },
          {
            name: "Weekend Override",
            controls: [
              { label: "Disable All Peak Restrictions", type: "toggle", value: true, recommended: true, warning: "Flat weekend rate — no need for peak-hour limits. EV can charge anytime." },
            ],
          },
        ],
      },
    },
    impact:
      "10+ time-based routines (peak start/end, pre-cool, EV start/stop × weekday/weekend) designed as one unified energy strategy. Pre-cooling concept automated. EV shifted to off-peak. Weekend handled without duplicating every routine. Cost context provided alongside each action.",
  },
];

const ToggleControl = ({ label, value, recommended, warning }) => {
  const [on, setOn] = useState(value);
  return (
    <div style={{ display: "flex", alignItems: "flex-start", justifyContent: "space-between", padding: "10px 0", borderBottom: "1px solid rgba(255,255,255,0.06)" }}>
      <div style={{ flex: 1, marginRight: 12 }}>
        <div style={{ display: "flex", alignItems: "center", gap: 8, flexWrap: "wrap" }}>
          <span style={{ fontSize: 13, color: "#e8e4e0", fontFamily: "'DM Sans', sans-serif" }}>{label}</span>
          {recommended !== undefined && (
            <span style={{
              fontSize: 9, padding: "2px 6px", borderRadius: 3, fontWeight: 600, letterSpacing: 0.5,
              background: recommended === on ? "rgba(74,222,128,0.15)" : "rgba(251,191,36,0.15)",
              color: recommended === on ? "#4ade80" : "#fbbf24",
              fontFamily: "'DM Mono', monospace",
              textTransform: "uppercase",
            }}>
              {recommended === on ? "✓ Recommended" : "⚠ Review"}
            </span>
          )}
        </div>
        {warning && (
          <div style={{ fontSize: 11, color: "#f59e0b", marginTop: 4, lineHeight: 1.4, fontStyle: "italic", fontFamily: "'DM Sans', sans-serif" }}>
            {warning}
          </div>
        )}
      </div>
      <button
        onClick={() => setOn(!on)}
        style={{
          width: 44, height: 24, borderRadius: 12, border: "none", cursor: "pointer", position: "relative",
          background: on ? "#4ade80" : "rgba(255,255,255,0.15)", transition: "all 0.2s ease", flexShrink: 0, marginTop: 2,
        }}
      >
        <div style={{
          width: 18, height: 18, borderRadius: 9, background: "#fff", position: "absolute", top: 3,
          left: on ? 23 : 3, transition: "left 0.2s ease", boxShadow: "0 1px 3px rgba(0,0,0,0.3)",
        }} />
      </button>
    </div>
  );
};

const OtherControl = ({ label, type, value, recommended, warning, options }) => {
  return (
    <div style={{ padding: "10px 0", borderBottom: "1px solid rgba(255,255,255,0.06)" }}>
      <div style={{ display: "flex", alignItems: "center", gap: 8, marginBottom: 6, flexWrap: "wrap" }}>
        <span style={{ fontSize: 13, color: "#e8e4e0", fontFamily: "'DM Sans', sans-serif" }}>{label}</span>
        {type === "device" && (
          <span style={{
            fontSize: 9, padding: "2px 6px", borderRadius: 3, fontWeight: 600,
            background: value === "warning" || warning ? "rgba(251,146,60,0.15)" : "rgba(74,222,128,0.15)",
            color: value === "warning" || warning ? "#fb923c" : "#4ade80",
            fontFamily: "'DM Mono', monospace",
          }}>
            {warning ? "⚠ Issue" : "✓ Ready"}
          </span>
        )}
      </div>
      {type === "select" && (
        <div style={{ display: "flex", gap: 6, flexWrap: "wrap" }}>
          {(options || []).map((opt) => (
            <span key={opt} style={{
              fontSize: 11, padding: "4px 10px", borderRadius: 4,
              background: opt === value ? "rgba(99,102,241,0.3)" : "rgba(255,255,255,0.06)",
              color: opt === value ? "#a5b4fc" : "#9ca3af",
              border: opt === recommended ? "1px solid rgba(74,222,128,0.3)" : "1px solid transparent",
              fontFamily: "'DM Sans', sans-serif", cursor: "pointer",
            }}>
              {opt}
            </span>
          ))}
        </div>
      )}
      {type !== "select" && type !== "toggle" && type !== "device" && (
        <div style={{
          fontSize: 12, color: "#a5b4fc", padding: "6px 10px", borderRadius: 4,
          background: "rgba(99,102,241,0.1)", fontFamily: "'DM Mono', monospace",
          border: "1px solid rgba(99,102,241,0.2)",
        }}>
          {String(value)}
        </div>
      )}
      {warning && (
        <div style={{ fontSize: 11, color: "#f59e0b", marginTop: 6, lineHeight: 1.4, fontStyle: "italic", fontFamily: "'DM Sans', sans-serif" }}>
          {warning}
        </div>
      )}
    </div>
  );
};

export default function AlexaAIGuide() {
  const [activeCase, setActiveCase] = useState(null);
  const [activeTab, setActiveTab] = useState("problem");

  const selected = useCases.find((c) => c.id === activeCase);

  return (
    <div style={{
      minHeight: "100vh", background: "#0c0b0f",
      fontFamily: "'DM Sans', sans-serif", color: "#e8e4e0",
    }}>
      <link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,wght@0,300;0,400;0,500;0,600;0,700;1,400&family=DM+Mono:wght@400;500&family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,600;0,9..144,700;1,9..144,400&display=swap" rel="stylesheet" />

      {/* Header */}
      <div style={{
        padding: "48px 32px 40px", maxWidth: 1100, margin: "0 auto",
        borderBottom: "1px solid rgba(255,255,255,0.06)",
      }}>
        <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 16 }}>
          <div style={{
            width: 36, height: 36, borderRadius: 8,
            background: "linear-gradient(135deg, #6366f1, #8b5cf6)", display: "flex",
            alignItems: "center", justifyContent: "center", fontSize: 18,
          }}>◈</div>
          <span style={{ fontSize: 11, fontFamily: "'DM Mono', monospace", color: "#6366f1", letterSpacing: 2, textTransform: "uppercase" }}>
            Concept Exploration
          </span>
        </div>
        <h1 style={{
          fontSize: "clamp(28px, 4vw, 44px)", fontWeight: 700, lineHeight: 1.15, margin: "0 0 16px",
          fontFamily: "'Fraunces', serif",
          background: "linear-gradient(135deg, #e8e4e0, #a5b4fc)", WebkitBackgroundClip: "text", WebkitTextFillColor: "transparent",
        }}>
          AI-Powered Interactive<br />Self-Service for Alexa
        </h1>
        <p style={{ fontSize: 16, color: "#9ca3af", maxWidth: 680, lineHeight: 1.65, margin: 0 }}>
          Replacing text-heavy user guides with an intelligent interaction layer that understands
          what you're trying to accomplish and generates purpose-built UI controls — grounded
          in real Alexa device settings and configuration paths.
        </p>
      </div>

      {/* Architecture overview */}
      <div style={{
        maxWidth: 1100, margin: "0 auto", padding: "40px 32px",
        borderBottom: "1px solid rgba(255,255,255,0.06)",
      }}>
        <h2 style={{ fontFamily: "'Fraunces', serif", fontSize: 22, fontWeight: 600, margin: "0 0 24px", color: "#a5b4fc" }}>
          How It Works
        </h2>
        <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(220px, 1fr))", gap: 16 }}>
          {[
            { step: "01", title: "Natural Language Intent", desc: "User describes what they want to accomplish in plain language, not which setting to change." },
            { step: "02", title: "Guide-Grounded Reasoning", desc: "AI maps the intent to real Alexa settings, referencing official device documentation and known app navigation paths." },
            { step: "03", title: "Cross-Setting Awareness", desc: "Identifies ALL related settings across different app sections — including commonly missed ones that cause failures." },
            { step: "04", title: "Generated Control UI", desc: "Produces a specialized, task-specific interface with toggles, selectors, time pickers, and warnings — not a wall of text." },
          ].map((s) => (
            <div key={s.step} style={{
              padding: 20, borderRadius: 10, border: "1px solid rgba(255,255,255,0.06)",
              background: "rgba(255,255,255,0.02)",
            }}>
              <div style={{ fontFamily: "'DM Mono', monospace", fontSize: 11, color: "#6366f1", marginBottom: 8, letterSpacing: 1 }}>{s.step}</div>
              <div style={{ fontSize: 15, fontWeight: 600, marginBottom: 8, color: "#e8e4e0" }}>{s.title}</div>
              <div style={{ fontSize: 13, color: "#9ca3af", lineHeight: 1.55 }}>{s.desc}</div>
            </div>
          ))}
        </div>
      </div>

      {/* Use Cases */}
      <div style={{ maxWidth: 1100, margin: "0 auto", padding: "40px 32px" }}>
        <h2 style={{ fontFamily: "'Fraunces', serif", fontSize: 22, fontWeight: 600, margin: "0 0 8px", color: "#a5b4fc" }}>
          Real-World Use Cases
        </h2>
        <p style={{ fontSize: 13, color: "#6b7280", marginBottom: 24 }}>
          Each grounded in actual Alexa app settings, navigation paths, and documented user frustrations. Every scenario has a manual solution — but it's cumbersome, error-prone, and scattered across multiple app sections.
        </p>

        {/* Case selector */}
        <div style={{ display: "flex", gap: 8, flexWrap: "wrap", marginBottom: 32 }}>
          {useCases.map((c) => (
            <button
              key={c.id}
              onClick={() => { setActiveCase(c.id); setActiveTab("problem"); }}
              style={{
                padding: "10px 16px", borderRadius: 8, border: "1px solid",
                borderColor: activeCase === c.id ? "#6366f1" : "rgba(255,255,255,0.08)",
                background: activeCase === c.id ? "rgba(99,102,241,0.12)" : "rgba(255,255,255,0.02)",
                color: activeCase === c.id ? "#a5b4fc" : "#9ca3af",
                cursor: "pointer", fontSize: 13, fontFamily: "'DM Sans', sans-serif",
                fontWeight: activeCase === c.id ? 600 : 400, transition: "all 0.2s ease",
              }}
            >
              <span style={{ marginRight: 6 }}>{c.emoji}</span> {c.title}
            </button>
          ))}
        </div>

        {/* Case detail */}
        {selected && (
          <div style={{
            borderRadius: 12, border: "1px solid rgba(99,102,241,0.15)",
            background: "rgba(99,102,241,0.03)", overflow: "hidden",
          }}>
            {/* Case header */}
            <div style={{ padding: "24px 28px", borderBottom: "1px solid rgba(255,255,255,0.06)" }}>
              <div style={{ fontSize: 11, fontFamily: "'DM Mono', monospace", color: "#6366f1", marginBottom: 8, letterSpacing: 1, textTransform: "uppercase" }}>
                Persona
              </div>
              <div style={{ fontSize: 14, color: "#d1d5db", lineHeight: 1.5 }}>
                {selected.persona}
              </div>
            </div>

            {/* Tab switcher */}
            <div style={{ display: "flex", borderBottom: "1px solid rgba(255,255,255,0.06)" }}>
              {[
                { key: "problem", label: "The Problem Today" },
                { key: "journey", label: "Current Journey (Manual)" },
                { key: "ai", label: "AI-Powered Approach" },
                { key: "ui", label: "Generated UI Preview" },
              ].map((tab) => (
                <button
                  key={tab.key}
                  onClick={() => setActiveTab(tab.key)}
                  style={{
                    padding: "12px 20px", border: "none", cursor: "pointer", fontSize: 12,
                    fontFamily: "'DM Sans', sans-serif", fontWeight: activeTab === tab.key ? 600 : 400,
                    background: activeTab === tab.key ? "rgba(99,102,241,0.1)" : "transparent",
                    color: activeTab === tab.key ? "#a5b4fc" : "#6b7280",
                    borderBottom: activeTab === tab.key ? "2px solid #6366f1" : "2px solid transparent",
                    transition: "all 0.15s ease",
                  }}
                >
                  {tab.label}
                </button>
              ))}
            </div>

            {/* Tab content */}
            <div style={{ padding: "24px 28px" }}>
              {activeTab === "problem" && (
                <div>
                  <p style={{ fontSize: 14, color: "#d1d5db", lineHeight: 1.7, margin: 0 }}>
                    {selected.problem}
                  </p>
                  <div style={{
                    marginTop: 20, padding: "14px 18px", borderRadius: 8,
                    background: "rgba(239,68,68,0.06)", border: "1px solid rgba(239,68,68,0.15)",
                  }}>
                    <div style={{ fontSize: 11, fontFamily: "'DM Mono', monospace", color: "#ef4444", marginBottom: 6, letterSpacing: 1 }}>
                      IMPACT
                    </div>
                    <div style={{ fontSize: 13, color: "#fca5a5", lineHeight: 1.5 }}>
                      {selected.impact}
                    </div>
                  </div>
                </div>
              )}

              {activeTab === "journey" && (
                <div>
                  <div style={{ fontSize: 11, fontFamily: "'DM Mono', monospace", color: "#f59e0b", marginBottom: 16, letterSpacing: 1 }}>
                    STEP-BY-STEP (ACTUAL ALEXA APP NAVIGATION)
                  </div>
                  {selected.currentJourney.map((step, i) => (
                    <div key={i} style={{
                      display: "flex", gap: 14, marginBottom: 12, alignItems: "flex-start",
                    }}>
                      <div style={{
                        width: 22, height: 22, borderRadius: 11, flexShrink: 0,
                        background: "rgba(251,191,36,0.1)", border: "1px solid rgba(251,191,36,0.2)",
                        display: "flex", alignItems: "center", justifyContent: "center",
                        fontSize: 10, color: "#fbbf24", fontFamily: "'DM Mono', monospace", fontWeight: 600,
                      }}>
                        {i + 1}
                      </div>
                      <div style={{ fontSize: 13, color: "#d1d5db", lineHeight: 1.55, fontFamily: "'DM Mono', monospace" }}>
                        {step}
                      </div>
                    </div>
                  ))}
                </div>
              )}

              {activeTab === "ai" && (
                <div>
                  <div style={{
                    padding: "16px 18px", borderRadius: 8, marginBottom: 20,
                    background: "rgba(99,102,241,0.08)", border: "1px solid rgba(99,102,241,0.2)",
                  }}>
                    <div style={{ fontSize: 11, fontFamily: "'DM Mono', monospace", color: "#818cf8", marginBottom: 8, letterSpacing: 1 }}>
                      USER SAYS
                    </div>
                    <div style={{ fontSize: 14, color: "#e8e4e0", lineHeight: 1.6, fontStyle: "italic" }}>
                      "{selected.aiApproach.userSays}"
                    </div>
                  </div>
                  <div style={{ fontSize: 11, fontFamily: "'DM Mono', monospace", color: "#4ade80", marginBottom: 14, letterSpacing: 1 }}>
                    SYSTEM REASONING
                  </div>
                  {selected.aiApproach.systemResponse.map((r, i) => (
                    <div key={i} style={{
                      display: "flex", gap: 12, marginBottom: 10, alignItems: "flex-start",
                    }}>
                      <div style={{ color: "#4ade80", fontSize: 14, flexShrink: 0, marginTop: 1 }}>→</div>
                      <div style={{ fontSize: 13, color: "#d1d5db", lineHeight: 1.55 }}>{r}</div>
                    </div>
                  ))}
                </div>
              )}

              {activeTab === "ui" && (
                <div>
                  <div style={{
                    display: "inline-block", fontSize: 10, fontFamily: "'DM Mono', monospace",
                    color: "#818cf8", marginBottom: 20, padding: "4px 10px", borderRadius: 4,
                    background: "rgba(99,102,241,0.1)", letterSpacing: 1,
                  }}>
                    GENERATED: {selected.aiApproach.generatedUI.type.toUpperCase()}
                  </div>
                  {selected.aiApproach.generatedUI.sections.map((section, i) => (
                    <div key={i} style={{
                      marginBottom: 20, borderRadius: 10, padding: "18px 20px",
                      background: "rgba(255,255,255,0.02)",
                      border: "1px solid rgba(255,255,255,0.06)",
                    }}>
                      <div style={{
                        fontSize: 12, fontWeight: 600, color: "#a5b4fc", marginBottom: 12,
                        fontFamily: "'DM Mono', monospace", letterSpacing: 0.5,
                      }}>
                        {section.name}
                      </div>
                      {section.controls.map((ctrl, j) => {
                        if (ctrl.type === "toggle") {
                          return <ToggleControl key={j} {...ctrl} />;
                        }
                        return <OtherControl key={j} {...ctrl} />;
                      })}
                    </div>
                  ))}
                  <div style={{
                    marginTop: 16, padding: "14px 18px", borderRadius: 8,
                    background: "rgba(74,222,128,0.06)", border: "1px solid rgba(74,222,128,0.15)",
                  }}>
                    <div style={{ fontSize: 11, fontFamily: "'DM Mono', monospace", color: "#4ade80", marginBottom: 6, letterSpacing: 1 }}>
                      RESULT
                    </div>
                    <div style={{ fontSize: 13, color: "#86efac", lineHeight: 1.5 }}>
                      {selected.impact}
                    </div>
                  </div>
                </div>
              )}
            </div>
          </div>
        )}

        {!selected && (
          <div style={{
            padding: "60px 32px", textAlign: "center", borderRadius: 12,
            border: "1px dashed rgba(255,255,255,0.08)", background: "rgba(255,255,255,0.01)",
          }}>
            <div style={{ fontSize: 32, marginBottom: 12 }}>☝️</div>
            <div style={{ fontSize: 15, color: "#6b7280" }}>Select a use case above to explore the full breakdown</div>
          </div>
        )}
      </div>

      {/* Key principles */}
      <div style={{
        maxWidth: 1100, margin: "0 auto", padding: "40px 32px 60px",
        borderTop: "1px solid rgba(255,255,255,0.06)",
      }}>
        <h2 style={{ fontFamily: "'Fraunces', serif", fontSize: 22, fontWeight: 600, margin: "0 0 24px", color: "#a5b4fc" }}>
          Design Principles
        </h2>
        <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(280px, 1fr))", gap: 16 }}>
          {[
            {
              title: "Augment, Don't Replace",
              desc: "This is an interaction layer on top of existing settings — not a replacement. Every generated UI element maps to real Alexa app settings paths. Advanced users can still navigate manually.",
            },
            {
              title: "Intent → Settings Graph",
              desc: "A single user intent like 'make this safe for my kid' maps to 7+ settings across 4+ app sections. The AI maintains a graph of setting dependencies, prerequisites (e.g., Home/Away modes required before Vacation Mode), and conflicts.",
            },
            {
              title: "Surface the Hidden Gotchas",
              desc: "Voice Deactivation letting kids undo filters. Calendar events leaking on Echo Show. Wi-Fi band mismatches causing silent failures. Brief Mode ≠ fewer notifications. The AI knows what users typically miss and surfaces it proactively.",
            },
            {
              title: "Task-Specific UI Generation",
              desc: "Not a generic settings page. Each interface is purpose-built: a timeline for routines, a device map for multi-room audio, a household matrix for profiles, an energy schedule for cost optimization.",
            },
            {
              title: "Cross-Ecosystem Coordination",
              desc: "Real setups span Ring, smart locks, Hue, thermostats, EV chargers, and more. The AI understands skill dependencies, protocol requirements (Zigbee, Matter, Wi-Fi), account linking, and subscription prerequisites like Alexa Together.",
            },
            {
              title: "Dependency-Aware Sequencing",
              desc: "Setup steps have hidden prerequisites: Household Profiles need linked accounts, Vacation Mode needs Home/Away Modes, Voice ID needs 20 min to sync. The AI orders steps correctly so nothing fails silently.",
            },
            {
              title: "Persona-Driven Defaults",
              desc: "A 6-year-old triggers stricter filters than a 14-year-old. An elderly parent gets larger text and slower speech. A vacation setup prioritizes security. The AI pre-fills intelligent defaults based on the described situation.",
            },
            {
              title: "Reversible & Saveable",
              desc: "Generated configurations can be saved as profiles ('Guest Mode', 'Night Security', 'Peak Hours', 'Senior Setup') and toggled. Changes are previewed before applying. Nothing is destructive.",
            },
          ].map((p, i) => (
            <div key={i} style={{
              padding: 20, borderRadius: 10, border: "1px solid rgba(255,255,255,0.06)",
              background: "rgba(255,255,255,0.02)",
            }}>
              <div style={{ fontSize: 15, fontWeight: 600, marginBottom: 8, color: "#e8e4e0" }}>{p.title}</div>
              <div style={{ fontSize: 13, color: "#9ca3af", lineHeight: 1.6 }}>{p.desc}</div>
            </div>
          ))}
        </div>
      </div>
    </div>
  );
}
