---
title: "The 40-Year Mystery: Why TRON Stays Stable While My Dev Tools Change Every Month"
published: false
description: Analyzing VC-driven instability in developer tools and proposing a structural solution through the "cushion layer"
tags: devtools, vc, architecture, programming
cover_image: https://github.com/mnrj-vv-w/developer-experience-paper/raw/main/assets/images/cover_en.png
canonical_url: https://github.com/mnrj-vv-w/developer-experience-paper
series: Developer Experience
---

## TL;DR

- **Problem**: Developer platforms (App Store Connect, Expo, RevenueCat) change UI/APIs constantly
- **Root Cause**: VC's 5-7 year exit pressure & quarterly KPIs
- **Hidden Cost**: $1.62B/year in developer time
- **Contrast**: TRON/Linux maintained 40-year stability
- **Solution**: "Cushion Layer" - Developer Experience Council + DX Certified
- **Inspiration**: Applying Clean Architecture principles to social systems

⏱️ **Reading time**: ~15 minutes

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

**Expo EAS**: Command options change every few months. Documentation has different descriptions depending on the version.

**RevenueCat**: The settings screen changes weekly along with the entire menu structure.

**Three things in common**:

1. ❌ **No advance notice** of changes
2. ❌ **Documentation doesn't keep up**
3. ❌ **Even AI can't catch up with yesterday's UI changes**

Result: **The only option is to contact support every time**.

---

This phenomenon isn't limited to specific apps. **It's happening structurally to all developers.**

---

### 💰 Hidden Costs

This instability isn't just about irritation.  
**When you quantify it, it's much more serious.**

**Assumptions**:
- Total mobile/web developers worldwide: **27 million** (Stack Overflow Developer Survey 2023)
- Those affected by platform changes: **10%** = 2.7 million
- Time spent responding to platform changes: **1 hour/month**

**Calculation**:
```
2.7 million × 1 hour/month × 12 months = 32.4 million hours/year

At $50/hour: = $1.62B (¥220 billion) /year
```

> Note: This is a **conservative estimate**. Most people spend more than 1 hour per month.

**This is an "unmeasured hidden cost".**

It doesn't appear in VC KPIs:
- ❌ MAU (Monthly Active Users)
- ❌ Revenue growth rate  
- ❌ Engagement

**What isn't measured doesn't exist.**

---

## 🏛️ A Contrasting World

Around the same time, I had an opportunity to use **TRON/μT-Kernel** in an embedded system.

I was amazed.

**Code from 20 years ago runs almost unchanged.**

Old documentation still works. No need to relearn. **A consistent design philosophy** runs through it.

**Why is it so different?**

---

### 40 Years of Stability

**The TRON Project** (1984~):

Since its inception in 1984, the TRON Project has **maintained the stability of its basic interface through a consistent design philosophy**.

The main reason embedded device manufacturers continue to adopt it is the reliability that **"the same assets (code) and know-how can be utilized even 20 years later"** because specifications don't change due to platform convenience.

> **Philosophy**: "Social infrastructure should not be broken"

TRON is not just a technical standard. It was designed with the philosophy that social infrastructure should not be broken.

---

**Linux Kernel** (2004~):
- User space API unchanged for 20 years
- Linus Torvalds' iron rule: **"No breaking userspace"**

> **"If it breaks things, we don't need new features"** - Linus Torvalds

This is Linus's principle. As a responsibility to developers.

---

**FreeBSD**: Similar emphasis on stability and backward compatibility obsession.

---

### In Contrast, Modern Platforms

| Platform | Change Frequency |
|----------|------------------|
| App Store Connect | Weeks to months |
| Expo EAS | Every few months |
| RevenueCat | Monthly |

---

**The Question**: Why are technologies from 40 years ago more stable?

**The answer lies in the flow of money.**

---

## 💸 Follow the Money

When I looked into it, the funding structures were completely different.

---

### The Reality of VC Money

**Expo** (EAS development):
- Raised **$27M** from Amplify Partners (2019)
- Condition: **5-7 year Exit** (IPO or acquisition)

**RevenueCat**:
- Raised **$56.5M** total from Index Ventures
- Same: **5-7 year Exit**

**Apple**:
- **65%** held by institutional investors
- Major shareholders: Vanguard, BlackRock, Berkshire Hathaway
- What they look at: **Quarterly earnings**

---

### 📊 Structural Constraints of VC Funds

**Why 5-7 years?**

VC funds are legally **liquidated in 10 years** (Limited Partnership agreement).
```
Year 0: Fund formation
Year 1-3: Investment period
Year 4-7: Growth period
Year 7-10: Exit & repayment
Year 10: Forced termination ⏰
```

**You must Exit by Year 7 to make it in time.**

---

### 📈 Quarterly KPI Pressure

Metrics VCs demand:

**✅ Measured**:
- MAU growth: Min **30-50%/quarter**
- Revenue growth: Min **50-100%/quarter**
- Next fundraising prep (every 18-24 months)

**❌ NOT Measured**:
- Developer learning costs
- Documentation quality
- Support inquiry volume
- Community burnout

**What isn't measured doesn't exist.**

---

### 💬 Board Meeting Reality
```
VC: "What's this quarter's growth rate?"
CEO: "Up 30% from last quarter"
VC: "Not enough. Need 50% or valuation drops"
CEO: "Understood... new features it is..."
  ↓
Result: Changes for the sake of changes
```

---

### Contrast: TRON/Linux

| Aspect | VC-backed | TRON/Linux |
|--------|-----------|------------|
| Funding | VC rounds | Membership fees, consortium |
| Exit deadline | 5-7 years | None |
| Evaluation | Quarterly KPIs | Annual (relaxed) |
| Time horizon | Short-term | 10-30 years |

---

### 🎯 Conclusion

**There are no "bad people" here.**

**What's bad is the "algorithm" that optimizes everything for short-term profits.**

- VCs must repay in 10 years
- So they demand 5-7 year Exits
- So companies must show "growth"
- So they change things frantically
- So developers get whipsawed

Everyone is acting rationally. But the system is broken.

> **What we lose every day isn't numbers, but "quiet time".**  
> Time to learn. Time to create. Time to think.

---

## 🤔 A Question to VCs

To VCs,

**We share the same goal**: Creating better services and generating sustainable value.

I want to pose one question:

**"Does the same model fit all sectors?"**

---

### Differences by Sector

✅ **Consumer apps (SNS)**: Short-term Exit works. Trends change quickly.

❌ **Developer tools**: Infrastructure. Used for 10-20 years.

**The mismatch**:
- Developers want: 10-year tools
- VCs want: 5-year Exit

---

### Long-term Risks

Short-term change frenzy creates:
- Developer attrition
- Trust erosion
- Technical debt

These appear as **valuation losses** in the next round.

A reputation as "unstable" **lowers Exit valuation**.

---

### 💡 Proposal

**How about 15-20 year long-term funds?**

History proves infrastructure investments work:
- Power grids
- Telecommunications
- Roads

"Low return, long-term, stable" → **Most reliable returns**

Developer tools = Same infrastructure.

---

## 📢 A Call to Developers

To developers,

**You're not alone.**  
**You just want to do your work.**

**Let's speak up.**

---

### Concrete Actions

1. **📝 Send feedback** (Apple, etc.)
   - "I lost X hours due to this change"
   - With data and constructive suggestions

2. **⏱️ Record time costs**
   - Track platform change response time
   - Visualize hidden costs

3. **🐦 Speak up on social media**
   - Constructively, with data
   - #DeveloperExperience

---

### 🔬 Join the Data Collection

I'm starting: **`developer-experience-observatory`** on GitHub

**"A place to turn anger into data"**

- Record platform changes
- Measure developer satisfaction
- Share best practices

**1,000 voices are 1,000× stronger than one.**

---

## 🏗️ The Solution: "Cushion Layer"

So what should we do?

**This article proposes: A structural solution through a "cushion layer".**

**This is not a demand. It's a framework for cooperation.**

---

### 💡 Clean Architecture Meets Social Systems

This applies **Clean Architecture principles** from software design to social systems.

Developers should intuitively get this.

---

### Current: Tightly Coupled 🔴
```
LP (Pension Funds)
  ↓ "Quarterly returns!"
VC
  ↓ "Growth!"
Startup
  ↓ "UI changes!"
Developer
  ↓ "Whipsawed..."
```

**Problem**: Pressure hits developers directly. Developer voices don't reach VCs.

---

### Proposal: Loosely Coupled 🟢
```
LP (Pension Funds)
  ↓ "Quarterly returns!"
VC
  ↓
┌─────────────────────┐
│ Developer Experience │
│      Council         │ ← Developer voices
│   (Cushion Layer)    │
└─────────────────────┘
  ↓ "Follow standards"
Startup
  ↓ "Get DX Certified"
Developer
  ↓ "Not whipsawed!"
```

---

### Three Functions

The cushion layer provides:

1. **🛡️ Pressure absorption**: Shield VC→Developer impact
2. **🔄 Information translation**: Quantitative Developer→VC feedback
3. **🤝 Action synchronization**: Market pressure aligns behavior

---

## 🎖️ Developer Experience Council + Certification

### Organization

- Independent non-profit
- 3 VC reps + 3 developer reps + 3 neutral experts

### Roles

1. Review platform changes
2. Measure developer satisfaction
3. Award **"DX Certified"**

---

### Certification (3 Levels)

**Level 1 (Basic)** 🥉:
- ✓ Docs updated simultaneously
- ✓ 1-week advance notice
- ✓ Support system

**Level 2 (Standard)** 🥈:
- ✓ Level 1 +
- ✓ 1-month beta period
- ✓ Migration guide
- ✓ Developer NPS 60+

**Level 3 (Excellent)** 🥇:
- ✓ Level 2 +
- ✓ Voting on breaking changes
- ✓ 6-month old version support
- ✓ Developer NPS 80+

---

### Market Mechanism
```
Company displays "DX Certified Level 3" badge
  ↓
Developers choose certified companies (market pressure)
  ↓
VCs prioritize certified companies (risk avoidance)
```

**Result**: No "force", but everyone "must comply"

---

## ✅ Proven Success Models

This isn't fantasy. Proven in other industries:

**🔐 PCI DSS** (Payment):
- Self-regulation
- Can't process payments without compliance
- Dramatically improved security

**📋 ISO 9001** (Quality):
- International certification
- Brand value for certified companies
- Industry-wide improvement

**🌱 B Corporation** (Social):
- Third-party certification
- Patagonia, Ben & Jerry's certified
- Stakeholder-focused proof

**Developer tools can do this too.**

---

## 🗓️ Roadmap

**Phase 1 (0-6 months)**: Data collection
- Launch `developer-experience-observatory`
- Record changes, measure satisfaction
- Build community of 1,000

**Phase 2 (6-18 months)**: Standards
- Form Working Group
- Draft "Developer Experience Standards v1.0"
- Public comment period

**Phase 3 (18-36 months)**: Certification
- Establish non-profit
- 10-20 initial certified companies
- Media exposure

**Phase 4 (3-5 years)**: Standardization
- Apple, Google, Microsoft join
- Become de facto standard

---

5 years? Yes.  
**But feasible.**  
**And you can start today.**

---

## 🎬 Finally

What will this article change?

Immediately? Maybe nothing.

**But change always starts quietly.**

---

One PM might hesitate to change UI.  
One VC might consider long-term funds.  
100 developers might speak up.

**That's enough.**

---

## 🚀 I've Already Started

**`developer-experience-observatory`** - Launched on GitHub

**Goals**:
- 6 months: 1,000 community
- 18 months: Standards
- 3 years: Certification

**This is the first step to Developer Experience Council.**

---

5 years from now, I want to say: **"That was the beginning."**

---

## 💬 Jobs's Words

> "You've got to start with the customer experience and work backwards to the technology."  
> — Steve Jobs, WWDC 1997

He was right.

But Apple in 2025 seems to have forgotten.

**So let's remind them.**

---

> "The people who are crazy enough to think they can change the world are the ones who do."  
> — Steve Jobs

Right now, I'm a little crazy.

**Will you get crazy with me?**

**Those "slightly crazy people" quietly move the world.**

---

## 🙏 Acknowledgments

In writing this paper, I received valuable feedback from
**Prof. Ken Sakamura**, 
leader of the TRON Project.

His detailed comments on the technical descriptions of TRON
were extremely helpful in revisiting and refining the explanations
presented in this article.

I am deeply grateful.

---

## 📚 Further Reading

- 📄 [Full Paper (GitHub)](https://github.com/mnrj-vv-w/developer-experience-paper)
- 🔬 [developer-experience-observatory](https://github.com/mnrj-vv-w/developer-experience-observatory)
- 📖 [Citation Guide](https://github.com/mnrj-vv-w/developer-experience-paper/blob/main/docs/CITATION.md)

---

## 💬 Discussion

What do you think?

- Have you experienced the same frustration?
- Do you think the "cushion layer" could work?
- What would you add to the DX Certified standards?

**Let's discuss in the comments! 👇**

---

## 🏷️ Tags

#devtools #vc #cleanarchitecture #developerexperience #tron #linux #softwarearchitecture #productmanagement #startup #innovation

---

*Cross-posted from [GitHub](https://github.com/mnrj-vv-w/developer-experience-paper)*
```
