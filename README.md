<img src="assets/header.svg" width="100%" alt="Andrés Araque. I build polished products and the agent systems that ship them." />

I'm Andrés, a Mathematics student at **UCF** building ambitious products with AI agents.

My focus is **agentic engineering**: designing the context, tools, and verification loops that let agents deliver substantial software quickly. I care just as much about the result: a clear purpose, a restrained interface, and details that feel finished.

**[Résumé ↗](resume/Andres_Araque_Resume.pdf) · [Email](mailto:pipe.araque@gmail.com)**

### Selected work

<table>
  <tr>
    <td width="50%" valign="top"><a href="https://mlhacky.com"><img src="assets/hacky.png" alt="Hacky's live interface: a knit companion, a focused conversation, and teammate matches with relevant evidence." /></a></td>
    <td width="50%" valign="top"><a href="https://web-kohl-three-51.vercel.app/learn"><img src="assets/etude.png" alt="Étude's live learning graph and a personalized practice step for Twinkle, Twinkle, Little Star." /></a></td>
  </tr>
  <tr>
    <td><b>Hacky</b> · Focused context. Finished interactions.</td>
    <td><b>Étude</b> · Learner state. A useful next step.</td>
  </tr>
</table>

#### [Hacky](https://github.com/seeko-codes/Hacky) · ~32 hours · Knight Hacks IX

A conversation that finds the right teammate or mentor. Focused profile context and evidence-backed matches, expressed through a custom knit mascot, a native-feeling React interface, and carefully paced interactions.

I shaped the product and interface and used coding agents to build the prototype, React app, and conversational onboarding. A three-person team built the full experience. **[Try Hacky ↗](https://mlhacky.com)**

#### [Étude](https://github.com/Eric-Zhang-Developer/piano-arcade-gator-ai-days) · ~44 hours · Gator Hack V finalist

A piano tutor and rhythm game played on a real 88-key piano. **I owned the entire learning architecture:** a 207-skill graph, evidence-driven mastery model, diagnostic, and context that guides the next practice session.

The planner sees a relevant skill shortlist with learner evidence and goals. Code validates its choices and supplies a fallback. I directed the learning build through fresh worker sessions, focused briefs, separate PRs, browser checks, and CI. Built with Eric Zhang and Sharan Santharam. **[Explore Étude ↗](https://web-kohl-three-51.vercel.app/learn)**

#### [Donna](https://apps.apple.com/us/app/donna-social-intelligence/id6760481634) · On the App Store

Tell Donna what you want to do; she helps you meet the right people at UCF. I'm on the **founding development team**, building UI and backend logic and leading the current refactor toward an architecture agents can navigate and extend.

**[Website ↗](https://donnaai.co) · [App Store ↗](https://apps.apple.com/us/app/donna-social-intelligence/id6760481634)**

<sub>Build times are elapsed repository windows, rounded to the nearest hour. Hacky was a 36-hour hackathon; its later README edits are excluded. [Dates and method](BUILD_NOTES.md).</sub>

[Architecture and development notes →](PROJECTS.md)

### Currently building: Ultralearn

**Know where you stand. Know what to do next.**

An adaptive SAT math tutor that turns a learner's knowledge into one clear next step. It carries forward Étude's central idea: persistent learner state gives the agent the context to decide what to teach and when to review. Living ink becomes the graph, the questions, and the work itself.

**In development.** Follow the build and visual math explanations at **[@ultralearns](https://www.instagram.com/ultralearns/)**. The product's home will be **ultralearn.xyz**.

### The systems behind the products

- **[seeko-stack](https://github.com/seeko-codes/seeko-stack)** - my portable distribution of Firstmate, with outcome-focused workflows, bounded loops, and an agent-assisted setup. Built on Kun Chen's Firstmate ecosystem.
- **[Turn to Life](https://github.com/seeko-codes/turn-to-life)** - a reusable, purpose-first agent workflow: clarify the goal, build against it, verify the result, and preserve what the work taught.
- **[Skemify](https://github.com/seeko-codes/skemify-skill)** - turn documents and records into an evidence-backed knowledge tree that an agent can navigate.

**How I work:** Claude Code and Codex · focused parallel workers · durable specs and handoffs · context architecture · Git worktrees · reusable skills and hooks · browser-based verification · tests and CI. Findings feed back into the tools and instructions for the next run.

**Product stack:** TypeScript · React · Next.js · Vite · Electron · Python · PostgreSQL · Playwright · Vitest.

**Mathematical foundation:** AI & Machine Learning · Optimization Theory & Mathematical Modeling · Linear Algebra.
