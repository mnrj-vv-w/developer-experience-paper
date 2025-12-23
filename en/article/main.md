![cover image](/assets/images/cover_en.png)

# The 40-Year Mystery: Why TRON Stays Stable While My Dev Tools Change Every Month

**A Structural Solution to VC-Driven Instability**

---

### Scope and Methodology Note

This paper distinguishes clearly between:
- **Documented facts** (based on public documentation and observable changes),
- **Developer experience** (based on the author’s direct experience),
- **Structural interpretation** (analytical hypotheses).

References to specific platforms or tools in the paper
are based on publicly observable behavior or personal experience,
and are not intended as factual claims about internal intent,
competence, or organizational quality.
This paper aims to contribute constructively to discussions
on improving developer experience across the industry.

---

## Again

App Store Connect has changed again.

The UI I just learned last month has moved to a different location. Button placements have changed, workflows have changed, and the documentation hasn't caught up.

I ask ChatGPT, but it only returns outdated information. Same with Bing AI. Google Search too. **There is no single source of information that has caught up with the latest UI changes.**

In the end, I have to contact support again.

This gets resolved in a day or two. But **it keeps repeating**.

Expo's EAS. The command options that worked a few months ago have changed again. Was it `--clear-cache` or `--no-cache`? Even looking at the documentation, the descriptions differ by version. Stack Overflow answers from six months ago no longer work.

RevenueCat's dashboard. The settings screen that was there last week has changed entirely, along with the menu structure.

Every time, relearning.  
Every time, reset.

**What a waste of time.**

I want to solve fundamental problems. I want to implement new features. I want to deliver value to users.

But in reality, **I'm forced to spend time "relearning" every single time**.

---

Is this really progress?  
Or is it just chaos?

And I suddenly thought:

"Is this just my problem?"

---

## Not Just Me

When I looked into it, I saw the same pattern.

**Apple App Store Connect**: UI changes almost monthly. Button positions, workflow redesigns.

**Expo EAS**: Command options change every few months. Was it `--clear-cache` or `--no-cache`? Even the documentation has different descriptions depending on the version.

**RevenueCat**: The settings screen that existed last week has changed this week, along with the entire menu structure.

**Three things in common**:

1. **No advance notice** of changes
2. **Documentation doesn't keep up**
3. **Even AI can't catch up with yesterday's UI changes**

Result: **The only option is to contact support every time**.

---

This phenomenon isn't limited to specific apps. **It's happening structurally to all developers.**

---

## Hidden Costs

This instability isn't just about irritation.  
**When you quantify it, it's much more serious.**

**Assumptions**:
- Total mobile/web developers worldwide: **27 million**  
  (Source: Stack Overflow Developer Survey 2023)
- Those affected by platform changes: **10%** = 2.7 million
- Time spent responding to platform changes: **1 hour/month**

**Calculation**:
```
2.7 million × 1 hour/month × 12 months
= 32.4 million hours/year

At $50/hour (¥7,000):
= $1.62B (approximately ¥220 billion) /year
```

Note that this is a **conservative estimate**.  
In reality, most people spend more than 1 hour per month.

**This is an "unmeasured hidden cost".**

It doesn't appear in VC KPIs:
- ❌ MAU (Monthly Active Users)
- ❌ Revenue growth rate  
- ❌ Engagement

**What isn't measured doesn't exist.**  
**So no one measures it, and no one improves it.**

![ figure 2: hidden cost ](/assets/images/fig2_en.png)

---

## The Question

Is this "progress"? Or is it "chaos"?

Are these monthly UI changes really for users?  
Or are they for someone else?

To find the answer, let's look at a contrasting world.

---

## A Contrasting World

Around the same time, I had an opportunity to use **TRON/μT-Kernel** in an embedded system.

I was amazed.

**Code from 20 years ago runs almost unchanged.**

Old documentation still works. No need to relearn. **A consistent design philosophy** runs through it.

**Why is it so different?**

---

## 40 Years of Stability

**The TRON Project** (1984~):

Since its inception in 1984, the TRON Project has **maintained the stability of its basic interface through a consistent design philosophy**.

The main reason embedded device manufacturers continue to adopt it is the reliability that **"the same assets (code) and know-how can be utilized even 20 years later"** because specifications don't change due to platform convenience.

This consistency is the greatest value. Knowledge gained through updates doesn't become obsolete, and education is easy. This is at the heart of why TRON continues to be supported by industry.

Reason: **The philosophy that "social infrastructure should not be broken"**

TRON is not just a technical standard. It was designed with **the philosophy that social infrastructure should not be broken**.

---

**Linux Kernel** (2004~):
- User space API unchanged for 20 years
- Linus Torvalds' iron rule: **"No breaking userspace"**  
  (Don't break user space)

**"If it breaks things, we don't need new features"**

This is Linus's principle. As a responsibility to developers.

---

**FreeBSD**:
- Similar emphasis on stability
- Obsession with backward compatibility

---

## In Contrast, Modern Platforms

**App Store Connect**: Changes every few weeks to months  
**Expo EAS**: Changes every few months  
**RevenueCat**: Monthly changes

---

## The Question

**Why are technologies from 40 years ago more stable?**

Newer technologies are more chaotic.

Is this a technical problem?  
Or is it something else?

**The answer lies in the flow of money.**

---

## Follow the Money

When I looked into it, the funding structures were completely different.

---

## The Reality of VC Money

**Expo** (EAS development):
- Raised **$27M** from Amplify Partners (2019)
- Condition: **5-7 year Exit** (IPO or acquisition)

**RevenueCat**:
- Raised **$56.5M** total from Index Ventures
- Same: **5-7 year Exit**

**Apple**:
- **65%** held by institutional investors
- Major shareholders: Vanguard, BlackRock, Berkshire Hathaway
- What they look at: **Quarterly earnings numbers**

---

## Structural Constraints of VC Funds

**Why 5-7 years?**

VC funds are legally **liquidated in 10 years** (Limited Partnership agreement).
```
Year 0: Fund formation (fundraising from LPs)
Year 1-3: Investment period
Year 4-7: Growth period
Year 7-10: Exit & repayment period
  ↓
Year 10: Forced termination
```

In other words, **you must Exit by Year 7 to make it in time**.

---

## Quarterly KPI Pressure

Metrics VCs demand from portfolio companies:

**Measured**:
- ✅ MAU growth rate: Minimum **30-50%/quarter**
- ✅ Revenue growth rate: Minimum **50-100%/quarter**
- ✅ Next fundraising preparation (every 18-24 months)

**Not measured**:
- ❌ Developer learning costs
- ❌ Documentation quality
- ❌ Number of support inquiries
- ❌ Community burnout

---

## The Reality of Board Meetings
```
VC: "What's this quarter's growth rate?"
CEO: "Up 30% from last quarter"
VC: "Not enough. Without 50%, valuation will drop in the next round"
CEO: "Understood... I'll add some new features..."
  ↓
Result: Changes for the sake of changes
```

---

## In Contrast, TRON/Linux

**TRON**:
- Funding source: Membership fees, corporate consortium
- Exit deadline: **None**
- Evaluation cycle: Yearly (relaxed)
- Time horizon: **10-30 years**

**Linux**:
- Funding source: Linux Foundation (corporate membership fees)
- Exit deadline: **None**
- Evaluation metrics: Stability, compatibility
- Time horizon: **Long-term**

![ table 1: VC structure vs Long term project ](/assets/images/table1_en.png)

---

## Conclusion

**There are no "bad people" here.**

**What's bad is the "algorithm" that optimizes everything for short-term profits.**

- VCs must repay in 10 years
- So they demand 5-7 year Exits from portfolio companies
- So portfolio companies must continuously show "growth"
- So they frantically make changes
- So developers get whipsawed

Everyone is acting rationally.  
But the system as a whole is broken.

**What we lose every day isn't numbers, but "quiet time".**

Time to learn. Time to create. Time to think.

That's being silently stolen away in the shadow of KPIs.

---

## A Question to VCs

To VCs,

**We share the same goal.**

The goal of "creating better services and generating sustainable value."

With that said, I want to pose one question:

---

I have no intention of denying your investment strategy.

Aiming for Exit in 5-7 years is rational given the structure of funds. And this strategy has greatly contributed to accelerating innovation.

But I want to ask:

**"Does the same model fit all sectors?"**

---

## Differences by Sector

For consumer apps (SNS, etc.), short-term Exits may be fine. Trends change quickly.

But **developer tools are different**.

These are infrastructure. They're used for 10, 20 years.

Developers want tools they can use for 10 years.  
You want Exit in 5 years.

**Are you aware of this fundamental mismatch?**

---

## Long-term Risks

Long-term costs created by short-term change frenzy:

- Developer attrition and burnout
- Loss of community trust
- Accumulation of technical debt

These appear as **"valuation losses"** in the next fundraising round.

Furthermore: A reputation as an "unstable tool" **lowers valuation at Exit**.

In other words, short-term growth appeals may be undermining long-term value.

---

## Proposal

**How about experimenting with 15-20 year long-term funds?**

You might think "low returns."

But look at the history of infrastructure investment:
- Power grids
- Telecommunications networks
- Roads

These were "low return, long-term, stable," but ultimately **generated the most reliable returns**.

Developer tools are the same infrastructure.

---

**Do short-term capital really fit developer tools?**

---

## A Call to Developers

To developers,

Have you experienced the same thing?

**You're not alone.**

**You just want to do your work, too.**

Do you think this is "normal"?

**Let's speak up.**

---

## Concrete Actions

**① Send Apple Feedback**
- Specifically: "I lost X hours due to this change"
- With data: "Number of support inquiries"
- Constructively: "This is how it could be improved"

**② Record time costs**
- Time spent responding to platform changes
- Time spent relearning
- This visualizes "hidden costs"

**③ Speak up on social media**
- Not emotionally, but constructively
- With data
- With #DeveloperExperience tag

---

## Shall We Collect Data Together?

I'm starting to record on GitHub:

**`developer-experience-observatory`**

**This is "a place to turn anger into data".**

Here:
- Record platform changes
- Measure developer satisfaction
- Share best practices

1,000 voices are 1,000 times stronger than one.

---

## A Viable Solution: Designing the "Cushion Layer"

So what should we do?

**What this article ultimately proposes is  
a structural solution through a "cushion layer".**

**This is not a demand.  
It's a framework for cooperation.**

---

## The Idea of Clean Architecture

This is an attempt to apply the idea of **"Clean Architecture"** from software design to social systems.

Developers should intuitively understand this.

---

## Current State: Tightly Coupled System

**To put the essence of the problem in one sentence,  
it's a structure where "short-term pressure directly hits frontline developers".**
```
    LP (Pension Funds)
        ↓
   "Quarterly returns!"
        ↓
       VC
        ↓
   "Increase growth rate!"
        ↓
   Startup
        ↓
    "UI change frenzy"
        ↓
      Developer
        ↓
    "Whipsawed..."
```

**Problem**: VC's short-term pressure reaches developers directly. Developers' voices don't reach VCs.

---

## Proposal: Loosely Coupled System
```
    LP (Pension Funds)
        ↓
   "Quarterly returns!"
        ↓
       VC
        ↓
  ┌─────────────────┐
  │ Developer Experience │
  │      Council         │← Developer voices
  │   (Cushion Layer)    │
  └─────────────────┘
        ↓
   "Please follow standards"
        ↓
   Startup
        ↓
   "Get DX Certified"
        ↓
      Developer
        ↓
    "Not whipsawed!"
```

**The cushion layer produces three things:**

1. **Pressure absorption** (Shield direct damage from VC→Developer)
2. **Information translation** (Quantitative feedback from Developer→VC)
3. **Action synchronization** (Market pressure makes it easier for both companies and developers to move)

![ figure 3: cushion layer design ](/assets/images/fig3_en_3.png)

---

## Concrete Proposal: Developer Experience Council + Certification System

**Organization**:
- Independent non-profit organization
- 3 VC representatives + 3 developer representatives + 3 neutral experts

**Roles**:
1. Review platform changes
2. Measure developer satisfaction
3. Award **"DX Certified" certification**

---

## Certification Standards (3 Levels)

**Level 1 (Basic)**:
- ✓ Documentation updated simultaneously
- ✓ 1 week advance notice of changes
- ✓ Support system

**Level 2 (Standard)**:
- ✓ Level 1 + 
- ✓ Beta period (1 month)
- ✓ Migration guide provided
- ✓ Developer NPS 60+

**Level 3 (Excellent)**:
- ✓ Level 2 +
- ✓ Advance voting on breaking changes
- ✓ Old version coexists for 6 months
- ✓ Developer NPS 80+

---

## Market Mechanism

**Display "DX Certified Level 3" badge on company site**
  ↓
Developers choose certified companies (**market pressure**)
  ↓
VCs prioritize certified companies (**reputational risk avoidance**)

**Result**: No one "forces" it, but everyone "must comply"

---

## Existing Success Models

This isn't fantasy. It's proven in other industries:

**PCI DSS** (Payment industry):
- Self-regulatory standard
- Can't process payments without compliance
- Dramatically improved security

**ISO 9001** (Quality management):
- International certification system
- Certified companies gain brand value
- Improved quality across the industry

**B Corporation** (Social enterprises):
- Third-party certification
- Obtained by Patagonia, Ben & Jerry's, etc.
- Proof of stakeholder focus

**The developer tools industry can do it too.**

---

## First Step: You Can Start Today

**Phase 1 (0-6 months)**: Data collection
- Launch `developer-experience-observatory`
- Record platform changes
- Measure developer satisfaction
- Build community of 1,000

**Phase 2 (6-18 months)**: Standards development
- Form Working Group
- Draft "Developer Experience Standards v1.0"
- Collect public comments

**Phase 3 (18-36 months)**: Launch certification system
- Establish non-profit organization
- Initial 10-20 certified companies
- Media exposure, create brand value

**Phase 4 (3-5 years)**: Industry standardization
- Apple, Google, Microsoft, etc. participate
- Become de facto standard

---

It might take 5 years.

But **it's feasible**.

And **the first step can be taken today**.

---

## Finally

What will change by writing this article?

Immediately, nothing may change.

**But change always starts quietly.**

---

One PM might hesitate to change the UI.  
One VC might consider a long-term fund.  
100 developers might start speaking up.

That's enough.

---

## I've Already Started Taking Action

**`developer-experience-observatory`**

Launched on GitHub.

**Goals**:
- **6 months**: Community of 1,000
- **18 months**: Standards development
- **3 years**: Certification system establishment

This is the first step toward Developer Experience Council.

---

5 years from now, when I read this article again, I want to be able to say, "That was the beginning."

---

## Jobs's Words

Steve Jobs said at WWDC in 1997:

*"You've got to start with the customer experience and work backwards to the technology."*

He was right.

But Apple in 2025 seems to have forgotten that.

So let's remind them.

---

Another Jobs quote:

*"The people who are crazy enough to think they can change the world are the ones who do."*

Right now, I'm a little crazy.

**Will you get crazy with me?**

**Those "slightly crazy people" quietly move the world.**

---

## Acknowledgments

In writing this paper, I received valuable feedback from
Prof. Ken Sakamura, 
leader of the TRON Project.

His detailed comments on the technical descriptions of TRON
were extremely helpful in revisiting and refining the explanations
presented in this article.

I am deeply grateful.

---

## Metadata

- **Version**: 1.1
- **Word Count**: ~6,000
- **Created**: November 2025
- **License**: CC BY 4.0（Creative Commons）
- **Contact**: [GitHub: developer-experience-observatory]

---
