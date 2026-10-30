# Context, craft, and agentic delivery

I build the systems that help agents do useful work, and the interfaces that make that work worth using. These projects show both sides: agents inside the product and agents building the product.

## Hacky: Hackathons, built just for you

**Knight Hacks IX · three-person team · approximately 32-hour repository window**

Hacky personalizes the hackathon around your goals. The team gathered Knight Hacks' event information into navigable context for a Gemini agent: people, schedules, sponsors, rules, and deadlines. Through chat, it finds relevant teammates and mentors, recommends events and sponsor opportunities for your project, and helps you keep track of the weekend. Built-in messaging lets you talk with teammates and potential collaborators.

My work shaped the product direction, prototype, React interface, and conversational onboarding through agentic development. The experience is deliberately focused: a knit companion, answer chips, evidence-backed cards, and a human choosing when to send.

The team's implementation makes that restraint concrete:

- Stable instructions and an event guide precede changing profile context. The server supplies the signed-in person's profile and a bounded conversation history. [Context assembly](https://github.com/seeko-codes/Hacky/blob/main/server/agent/prompts.ts), [history](https://github.com/seeko-codes/Hacky/blob/main/server/agent/history.ts).
- Search produces rich cards for the interface and compact evidence for the model. Presentation data need not occupy the model's context. [Tool output projection](https://github.com/seeko-codes/Hacky/blob/main/server/agent/tools.ts).
- Tools use the current person's identity and event. The agent drafts introductions; the person sends them. [Tool contracts](https://github.com/seeko-codes/Hacky/blob/main/shared/contract.ts), [product rules](https://github.com/seeko-codes/Hacky/blob/main/AGENTS.md).

Ryan owned the backend and matching implementation. The complete application is a team result.

**[Live product](https://mlhacky.com) · [Source](https://github.com/seeko-codes/Hacky)**

## Étude: The piano tutor that knows you better than yourself

**Gator Hack V finalist · three-person team · approximately 44-hour repository window**

Étude carries the study-management burden so the learner can sit down and play. It makes two connected choices: learn new material or retrieve earlier learning; practice piano performance or work on music theory. The aim is to target useful gaps while keeping earlier learning available through spaced retrieval. Practice happens on a connected real 88-key piano.

I owned the entire learning architecture. A tutor needs to know what a learner knows; Étude makes that knowledge explicit and usable by an agent. Its [curriculum](https://github.com/Eric-Zhang-Developer/piano-arcade-gator-ai-days/tree/main/web/src/learn/frontend/mastery/curriculum) contains 207 skills and 481 links across pitch, rhythm, keys, chords, expression, and pieces.

- **Evidence updates state.** Recorded attempts update mastery beliefs over a connected curriculum. Assisted or revealed answers are treated differently from independent retrieval; mastery requires repeated evidence. [State replay](https://github.com/Eric-Zhang-Developer/piano-arcade-gator-ai-days/blob/main/web/src/learn/frontend/mastery/engine/replay.ts).
- **State selects context.** The planner receives at most 20 relevant candidates, including belief, evidence counts, mastered connections, due checks, and goal songs. It chooses a small practice session from that shortlist. [Candidates](https://github.com/Eric-Zhang-Developer/piano-arcade-gator-ai-days/blob/main/web/src/learn/frontend/mastery/decide/candidates.ts), [prompt](https://github.com/Eric-Zhang-Developer/piano-arcade-gator-ai-days/blob/main/web/src/learn/frontend/mastery/decide/prompt.ts).
- **Code checks the decision.** Runtime validation rejects invalid plans, limits new material, and keeps activity selection consistent with learner state. Missing credentials, model failures, and invalid replies have a deterministic fallback. [Validation](https://github.com/Eric-Zhang-Developer/piano-arcade-gator-ai-days/blob/main/web/src/learn/frontend/mastery/decide/validate.ts), [fallback](https://github.com/Eric-Zhang-Developer/piano-arcade-gator-ai-days/blob/main/web/src/learn/frontend/mastery/decide/index.ts).

Étude schedules cold checks at increasing intervals. Its shipped mastery engine does not continuously decay belief with time. Ultralearn carries this work forward toward a stateful tutor for any learning domain, starting with SAT math.

The development process used the same principle: keep state outside a single conversation, and give each agent the context its task needs. In my learning lane, a talking agent broke the work into focused briefs for fresh Claude Code worker sessions. Workers delivered separate PRs; specs, handoffs, browser checks, and CI supported integration. The repository documents this process and credits my tutor work. [Development workflow](https://github.com/Eric-Zhang-Developer/piano-arcade-gator-ai-days/blob/main/docs/devpost.md), [project story](https://github.com/Eric-Zhang-Developer/piano-arcade-gator-ai-days/blob/main/docs/story.md).

Eric Zhang led the piano game, and Sharan Santharam the backend. Their work makes the full tutor-and-game experience possible.

**[Learning experience](https://web-kohl-three-51.vercel.app/learn) · [Source](https://github.com/Eric-Zhang-Developer/piano-arcade-gator-ai-days)**

## Donna: building with a founding team

Donna helps UCF students turn an intention into an introduction: a study partner, a pickup game, or someone to get food with. It is publicly available on the App Store.

I'm part of the founding development team, working across UI and backend logic. I currently lead the refactor toward an architecture agents can understand and extend, with useful tools and relevant context.

**[Official website](https://donnaai.co) · [App Store](https://apps.apple.com/us/app/donna-social-intelligence/id6760481634)**

## Ultralearn: the continuing education thread

I'm building a stateful tutor for any learning domain, starting with SAT math. The aim is to generalize the learning architecture explored in Étude: represent a domain as a knowledge graph, update a learner's mastery from evidence, and use that persistent state to guide what comes next. The app is in development; support for other domains is the broader goal.

The companion **[content-factory](https://github.com/seeko-codes/content-factory)** is an agent-driven content pipeline that learns from its own performance. It connects production and export review with audience-performance analysis and human-approved improvements to future content. It supports the visual math explanations on **[@ultralearns](https://www.instagram.com/ultralearns/)**.

---

[Build timestamps and method](BUILD_NOTES.md) · [Back to profile](README.md)
