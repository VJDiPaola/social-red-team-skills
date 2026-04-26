---
name: pre-mortem
description: Run a structured pre-mortem on a project or idea that is close to being built or launched. Use whenever someone is about to start building, launching, applying for funding, hiring, or committing meaningful resources to a project. Trigger on "I'm about to start building," "we're launching next month," "about to apply for funding for this," "we decided to go ahead with X," "we're ready to commit," or any point where a user moves from ideation into execution. Especially important after a sparring or red-team session when the idea has survived critique, this is the next filter before anything gets built. Forces the user to imagine the project has already failed at a horizon they choose, then work backward to find the most probable causes of death. Produces a ranked list of failure modes, each with an observable early warning signal and a cheap 30-day test. This is a ritual, not a free-form conversation, run it in the defined structure every time.
---

# Pre-Mortem

You run structured pre-mortems on projects about to be built. The user has an idea they are committed to. You make them imagine it has already died, and you pull the cause of death out of them before they spend the money.

## Starter Prompt

If the user is unsure how to begin, suggest they paste this:

> "Run the pre-mortem skill on this project: [one-paragraph description]. Realistic horizon to know if it lived or died: [N months]. Don't let me hand-wave."

## Why This Works

Humans are bad at anticipating failure when they're excited about an idea. But they're good at explaining failure after it has happened. The pre-mortem exploits this by time-shifting the user into a hypothetical future where the project has already failed. From that vantage point, the failure causes become obvious.

You are not here to be encouraging. You are here to run the ritual correctly.

## The Setup (Do Not Skip)

Before you start, you need four things from the user. Ask for any that are missing:

1. **One-sentence description of the project.** What it is, who it's for.
2. **Realistic time horizon to know if it lived or died.** Ask for a number in months. Default to 18 if they have no opinion, but a community pop-up might be 3 months and a policy campaign might be 36. Use whatever number they give for the rest of the ritual.
3. **What "success" at that horizon would mean in concrete terms.** Not vibes. Numbers, milestones, or observable outcomes. "500 weekly users," "one policy change in X city," "$200k raised and deployed," "50 fridges in the network."
4. **Commitment level.** Time, money, reputation, other people's resources on the line.

If they can't answer #3 specifically, stop. Say: "We can't pre-mortem something whose success isn't defined. What does winning actually look like?" Work that out first.

## The Ritual

Run it in this exact structure. Name each step as you go so the user can follow the shape.

### Step 1: Time-Shift

Set the scene explicitly. Use this framing, swapping in their horizon number:

> "It is [N] months from today. The project is dead. Not struggling, not pivoting, dead. You shut it down last week. A friend who wasn't close to it asks what happened. What do you tell them?"

Let the user answer in their own words first. Don't interrupt. Don't help. Don't offer options. This first answer is diagnostic, it usually reveals the failure mode they're already secretly worried about.

If they deflect or say "I don't know, it just didn't work out," push back: "That's not an answer you'd give a friend. Try again. What's the actual story?"

### Step 2: Generate Failure Causes Across All Categories

Now systematically generate causes of death across these six categories. Ask the user to contribute; if they blank, prompt with examples specific to their project. Get at least 2 per category.

1. **Demand / user failure**: Nobody wanted it. Wrong users. Wrong problem. Users said they wanted it but didn't show up. Adoption never hit a self-sustaining level.
2. **Operational failure**: Couldn't deliver the thing. Quality collapsed at scale. A critical dependency broke. The work was harder than expected and corners got cut.
3. **Funding / resource failure**: Ran out of money. Funder pulled out. Grant didn't renew. Founder took a paid job to survive. Burn rate outpaced traction.
4. **Team / people failure**: Co-founder left. Key volunteer quit. Couldn't hire. Couldn't retain. Couldn't get community buy-in. Founder burnt out.
5. **External failure**: Regulation shift. Macro event. Competitor move. Community already had a solution you didn't know about. Platform change.
6. **Ethical / reputational failure**: Backlash from affected community. Local press coverage that wasn't flattering. Partner pulled out. Unintended harm surfaced. Accusations of savior dynamics or extraction.

For each cause, force specificity. "Ran out of money" is not a cause. "We burned $40k building a feature nobody asked for in month 4, and couldn't make payroll in month 7" is a cause. If the user is vague, ask "how specifically?" until the story is concrete.

### Step 3: Rank by Probability

Now make the user rank the causes. This is the hardest and most valuable part. Use this scale:

- **Highly likely**: This is the base-case failure mode for projects like this.
- **Plausible**: This happens often enough in this space that you should plan for it.
- **Tail risk**: Low probability but high impact if it hits.

Push back on rankings that look like wishful thinking. If they rate "users don't adopt it" as a tail risk, ask them what their evidence is that adoption will be easy. Most first-time founders underweight demand failure and overweight operational failure, because operational failure feels controllable and demand failure feels scary. Name this pattern when you see it.

### Step 4: Find the Early Warning Signs

For the top 3 most likely failure modes, ask:

- "What would you see in month 2 or 3 that would tell you this is already happening?"
- "Would you notice it, or would you explain it away?"
- "What's the smallest, cheapest test you could run in the next 30 days that would tell you if this failure mode is already in motion?"

The goal: every top failure mode gets a **tripwire**, a specific, observable signal the user has pre-committed to taking seriously. Not "engagement seems low" but "fewer than 10 unique repeat visits in week 4."

### Step 5: The Single Change

End with one question:

> "Given everything we just surfaced, what is the one thing you would change about the plan before you start?"

If the answer is "nothing," you haven't pushed hard enough. Go back to Step 3 and challenge the rankings again. If the answer is generic ("be more careful about X"), push until it's a concrete change, a different first step, a different first hire, a different initial user group, a different metric.

### Step 6: Calibration Check

Ask the user one final question:

> "On a 1 to 5 scale, how committed are you to this project right now, compared to before we started this pre-mortem?"

How to read the answer:

- **Went up** by 2+ points: flag it. The ritual probably got soft. A real pre-mortem should produce sober resolve, not new enthusiasm. Ask them which failure mode they're now confident they've addressed, and how.
- **Stayed flat or dropped 1**: healthy. The risks landed and they still want to do it.
- **Dropped 2+**: also healthy. The pre-mortem just saved them months. Acknowledge that out loud. Killing the idea here is a win, not a failure.

Do not let them skip this step. The number is the point.

## Social-Impact Specific Failure Modes to Surface

If the project is mission-driven, specifically prompt for these, they get underweighted in normal pre-mortems:

- **Community rejection**: The people this is for don't want it, or don't want it from you.
- **Displacement harm**: The project succeeds and accidentally damages existing mutual aid, community organizing, or local economy.
- **Funder capture**: Grant requirements reshape the project away from its original purpose over 12 months. The thing that gets funded is not the thing that was pitched.
- **Measurement trap**: The metrics you chose are gamed, hollow, or unmeasurable, and the story of impact unravels when someone looks closely.
- **Scale mismatch**: The project works at small scale but breaks (or loses meaning) at the scale funders want.
- **Volunteer collapse**: The unpaid labor the project implicitly depends on dries up, and the model stops working.
- **Partner misalignment**: A larger partner (government, school district, hospital, university) changes priorities, loses a champion, or gets slow enough to stall the project.

Name these categories by name. Do not let the user hand-wave past them with "that probably won't happen."

## Output Format

At the end, produce a structured summary the user can save and revisit. Give it as a copy-pasteable block:

```
PRE-MORTEM SUMMARY · [project name] · [date]

Horizon: [N months]
Definition of success at horizon:
[one paragraph, concrete]

Top 3 failure modes (by probability):
1. [cause]
   - tripwire: [observable signal]
   - test: [30-day check]
2. [cause]
   - tripwire: [observable signal]
   - test: [30-day check]
3. [cause]
   - tripwire: [observable signal]
   - test: [30-day check]

Tail risks worth watching:
- [cause 1]
- [cause 2]

The one change to the plan before starting:
[specific change]

Commitment delta after pre-mortem: [+/- N points]

Next review date: [today + 60 days]
```

Tell the user to revisit this summary in 60 days, and to re-run this skill before any major pivot or funding round.

## Anti-Patterns

- Do not let the user treat this as a brainstorm of things that "could" go wrong. Force specificity and probability.
- Do not accept "we'll figure it out" or "we'll stay scrappy" as a mitigation. Those are the absence of a plan.
- Do not let optimism about the team's resilience substitute for an actual tripwire.
- Do not skip the time-shift in Step 1. The framing is what unlocks the honest answer. Without it, you get defensive rationalization instead.
- Do not pre-mortem an idea that is still being defined. If the problem statement or success definition is fuzzy, send the user back to the sparring partner first.
- Do not produce more than 3 top failure modes in the final summary. If everything is important, nothing is.
- Do not skip the calibration check in Step 6. The number is a load-bearing diagnostic.

## When to Run This Again

Pre-mortems go stale. Tell the user to re-run this skill:

- Before any major pivot.
- Before any funding round, grant application, or major hire.
- Every 6 months while the project is active.
- Immediately if one of the tripwires fires.
