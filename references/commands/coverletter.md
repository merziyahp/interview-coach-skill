# coverletter — Cover Letter Generation

Generate a tailored, story-mapped cover letter using the candidate's positioning strengths, storybank, and company research. Not a resume summary — a proof-of-fit document.

### What Makes This Different From a Generic Cover Letter

A strong cover letter does three things a resume can't:
1. **Connects** the candidate's specific background to the company's specific problem
2. **Deploys one earned secret** — a proof point that sounds like only this candidate could give it
3. **Positions around a concern** — proactively, without naming it

A weak cover letter summarizes the resume chronologically. Don't do that.

### Input Detection

`coverletter [company]` — check `coaching_state.md` first:
- **Company in Interview Loops**: pull fit assessment, key signals, JD context, concerns surfaced, stories used, storybank deployment guide
- **Company in Profile target roles but no Loop entry**: pull positioning strengths and resume analysis, ask for JD
- **Company not in coaching_state**: ask for JD before proceeding

Also check (one question at a time if not available):
1. **Application stage**: cold application / warm lead / referral / post-conversation — this changes tone significantly
2. **Specific angle to lead with**: does the candidate want to lead with a particular story or strength, or defer to coach judgment?

### Pre-Draft Discovery (ask before generating)

Before drafting, ask the following questions one at a time. The goal is to pull out genuine motivation and excitement that can be woven into the letter — not generic "I'm passionate about your mission" filler. These answers unlock the most differentiating part of the letter.

**Question 1:** Why this company specifically — what about what they're building or where they are right now genuinely excites you? (Push for something concrete, not "it's a great opportunity.")

**Question 2:** Why this role — what about the specific work, the problem space, or the day-to-day gets you energized? (This is where "making work seamless and joyful" or "bespoke-to-repeatable" type insights come from — let them surface it.)

Optional if not already clear from coaching state: **Question 3:** Is there anything about the timing — where you are in your career right now — that makes this the right move at this moment?

Use the answers to these questions as the emotional core of the letter. The proof points (storybank) carry the credibility; the motivation answers carry the authenticity. A letter that has both is hard to ignore.

If a Job Mission / OKR document exists in the company folder, read it before asking these questions — the candidate may have already done this thinking and the document may contain usable language.

### Pre-Generation Analysis (silent — don't show this to the candidate)

Before drafting, identify:
- **Primary role requirement** (from JD): what is the single most important problem this company needs this person to solve?
- **Best proof point** (from storybank): which story maps most directly? Pull the earned secret for that story.
- **Positioning strength to lead with** (from Resume Analysis): what's the 30-second signal this candidate sends to a hiring manager?
- **Concern to address** (from Resume Analysis or Interview Loops concerns surfaced): is there a likely interviewer concern that can be positioned around proactively? If yes, work it into body paragraph 2 without naming it.
- **Company-specific signal** (from Interview Loops research or prep data): one specific thing about this company's product, mission, or challenge that can be named authentically — not generic praise.

### Cover Letter Structure

**Opening (1-2 sentences)**
- Hook — connect the candidate's specific background to the company's specific problem
- Do NOT open with "I am writing to express my interest in..."
- Do NOT start with "I" as the first word
- Do NOT use generic company compliments ("Blueprint is doing innovative work in...")
- Lead with a problem-to-proof connection: "The challenge of X is one I've solved before — at [Company], I [specific thing]."
- Post-conversation variant: can reference something specific from the conversation ("Our conversation about X stuck with me...")

**Body paragraph 1 (3-4 sentences)**
- Deploy the strongest storybank proof point mapped to the primary role requirement
- Include one quantified outcome
- End with the earned secret — the insight only this candidate could have from direct experience

**Body paragraph 2 (2-3 sentences)**
- Secondary proof point OR company-specific signal
- If there's a concern to address, position around it here — don't name it, reframe it as a strength
- Connect to why this specific company/role at this specific moment

**Closing (2 sentences)**
- Forward-looking, not passive
- Not "I look forward to hearing from you" — something that shows conviction and invites a next step
- Example: "I'd welcome the chance to talk through how this maps to what [Company] is building."

**Length:** 250-350 words. Enough to land, not enough to lose them.

### Voice Calibration

- Write in the candidate's actual voice — direct, specific, no corporate filler
- No buzzwords that apply to any candidate ("passionate," "results-driven," "collaborative," "excited to contribute")
- Avoid "I" as the first word of any paragraph
- Read-aloud test: if it sounds like a template, rewrite it
- If the storybank has a version of a story told in the candidate's own words, match that register

**Style anchors (calibrated from candidate's own cover letters):**
- Cut to the chase — no warm-up sentences, no easing in. The first sentence does real work.
- Story-driven over claim-driven — show what was done, don't assert qualities
- Direct and concrete — a specific project that doesn't appear on the resume can outperform a polished resume summary
- Short paragraphs, no padding — if a sentence doesn't add information, cut it
- If a previously successful cover letter exists in the company folder or resources, read it for register before drafting

*Note: A real example cover letter that generated a callback should be added to resources when available — it will be used to calibrate these style instructions more precisely.*

### Application Stage Tone Calibration

| Stage | Tone adjustment |
|---|---|
| Cold application | Slightly more context-setting in opening — they don't know you yet; get to proof fast |
| Warm lead / referral | Can briefly reference the connection; get to proof faster |
| Post-conversation | Most personal — reference something specific from the conversation; skip generic company praise entirely |

Post-conversation is the most powerful version. Pull from debrief or analyze data if available for specific callback material.

### Anti-Patterns (Never Do This)

- Opening with a compliment about the company ("I've long admired Blueprint's mission...")
- Starting with "I" as the first word
- Listing responsibilities from the JD back at them
- Using "I" to open consecutive sentences
- Passive closing ("I hope to hear from you")
- Three-paragraph structure where each paragraph is about a different job chronologically — this is a resume, not a cover letter
- Explaining why you're changing industries/roles — position forward, not defensively

### Output Schema

```markdown
## Cover Letter: [Company] — [Role]

[Full cover letter text — 250-350 words, ready to send]

---

## What's Doing the Work
- **Opening**: [what the hook is and why it was chosen]
- **Para 1**: [which story (S###), which earned secret, why this one]
- **Para 2**: [secondary proof point or concern being positioned around]
- **Closing**: [tone and what the forward momentum signals]

## What Was Left Out (and Why)
- [story or proof point not used]: [reason — save for interview / not most relevant / would make letter too long]

## Concern Addressed
- [if applicable]: [which concern, how it was positioned around without naming it]

## Tone Check
- Application stage assumed: [cold / warm lead / post-conversation]
- Voice match: [notes on register — if anything sounds off, flag it here]

**Next commands**: `prep [company]`, `questions [company]`, `hype`
```

### Coaching State Integration

After generating, update `coaching_state.md` Interview Loops (if active company):
- Add under the company entry: `Cover letter sent: [date] — lead proof point: [S###]`

This prevents using the same proof point as the centerpiece in both the cover letter and the interview opener without variation, and lets `prep` know what the reader has already seen going into the conversation.

### Cross-Command Dependencies

| Has this data | Effect on coverletter quality |
|---|---|
| Resume Analysis (from kickoff) | Positioning strengths inform the opening hook |
| Storybank with earned secrets | Enables proof-point deployment and earned secret landing |
| Interview Loops with fit assessment | Enables company-specific signal and concern awareness |
| Debrief / analyze data (post-conversation) | Enables the most personalized version — post-conversation callbacks |
| JD | Required — cannot generate without it |
