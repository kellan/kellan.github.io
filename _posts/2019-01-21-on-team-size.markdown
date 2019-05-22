---
layout: post
title:  "On Sizing Your Engineering Organizations"
date:   2019-01-21 17:02:45 -0500
---
One of the most frequent conversations I have with teams is how to think about organization size.  Or rather we have a conversation that goes something like, "We need to double/triple/quadruple our engineering team next year, and now we need to hire a leader who has done it before."  And to have that conversation well you need a theory of organization size.

In the abstract it seems obvious that you don't grow a team to grow a team. Rather growth is a tool to solve some other pressing issues.  In practice, across conversations with hundreds of engineering leaders and CEOs, facing a variety of challenges, the belief, "We don't have enough engineers (and we don't have the right engineers)" has nearly universal coverage.  And while I'm on record saying [that most teams don't spend enough time on hiring](/notes/faqs-from-coaching), this model of growing the team as a percentage (or multiplier) of headcount is fatally flawed.  

Hiring is often proposed as a solution to a number of thorny tensions that arise when building and operating a product.  Not enough getting done? Hire more people.  Too many bugs? Hire people to work on bugs.  Stability issues? Hire senior/infra/sre/backend type people. Tech debt slowing down important work? Hire a new team to build features while your core team pays down tech debt.  Growth slowing? Hire a growth team.  What's great about this model is no one has to compromise on their priorities.  What's less great about this model is it doesn't work. 

Setting aside hiring for the moment, which is a deeply linked but separate topic, there are 3 key ideas you should have in your mind when you think about team size, e.g. when you're being asked to forecast an annual (or even multi-year!) hiring plan.

### 1. Momentum Is a Function of Concurrency; Teams Are Your Units of Concurrency

Effective software development is performed by small, focused, cross functional teams (4-12) with a high degree of autonomy and ownership of outcomes.  These teams should have a goal.  A singular goal.  Call them squads, call them scrum teams (please don't), call them working groups, you're even welcome to confuse cause and effect and call them micro-services, but in 2019 this is well understood, if not widely practiced.  In particular small focused teams exhibit two key benefts in context of predictable, sustained momentum.  The first is they tend to be less impacted by outcome randomizers, e.g. the infamous "engineer rat holing". The second is they're more likely to deliver software that solves the business objective vs conforms to a spec.  More about working groups in a future post.

What are your teams top goals and priorities?  The inability to answer this question with clarity across your company is the most common cause of "moving too slow". There is a perception that the default state of a tech team is entitled engineers run amok, working on whatever they want.  My experience is that most teams arrive, over time, through some application of "agile processes" to a default top priority of, "Do the Tickets Assigned to Me in the Groomed Backlog." This largely subconscious attempt to do software development via industrial era conveyor belt metaphors is doomed to failure.  It does have one nice upside: it requires a very low degree of management skill.  You get to manage each individual individually rather than as part of a cohesive larger team. Unfortunately its a terrible way to build software. (side note: "velocity" in software engineering is misnamed and actively harmful as it measure how fast you're spinning your wheels irrespective of how fast you're moving towards your goals) ((side side note: yes, you definitely are paying your engineers way too much if you're going to be asking them to perform as assembly line workers))

Once you understand that small teams are your unit of concurrency the answer to how large your engineering organization should be becomes: How many concurrent top priorities do you want to be able to work on simultaneously?

### 2. Larger Organizations Need Upgraded Infrastructure

Coordination swamps all other costs in the development of software.  If concurrency is the limit on your momentum, then highly effective engineering organizations are characterized by how effectively they manage communication and coherence.

The difficulty of managing groups of engineers (and by abstraction groups of humans in general) exhibits step functions based on group size.  Below 8-12 people almost anything works. 12-25 people require better tools. This happens again at ~40-50, again at ~100, again at ~150 (a number suspiciously close to the Dunbar number, despite the wide misuse of Dunbar in popular culture), again at ~250, again at ~400-500, etc. 

These better tools include: better management, richer culture, clear hierarchies, technical standards, job levels, decision making frameworks, CI and linting tools, monitoring and observability, production testing facilities, shared goals and definitions of success, employee directories, etc.

Let's choose "better management" as an example, and take a deeper look at what it means to upgrade this tool as your organization hits these step functions.

Generally an organization of less than 12 has a well understood implicit hierarchy based on personal relationships and there is a very little need to establish formal roles and responsibilities.  Once you start getting over 12 folks, you need managers, who are increasingly specialized in how they spend their time.  Additionally those managers will find that the implicit trust and shared context that made coordination easy with a small group now requires explicit work. 

In organizations of 40-50 knowing everyone's name much less what they're all about is no longer safe to assume.  At this size you need directors.  Directors are organizational specialists responsible for making sure that coordination is happening within your organization.  They accomplish this using a wide variety of tools including putting processes in place, making speeches, offsites, on-boarding, culture reinforcing practices, performance management, teaching, etc.  In some organizations directors and above may work with specialists that support them including learning and development coaches, recruiters, HR business partners, project managers, technical writers, compensation specialists, executive assistants, etc.  These people fill a similar role to the engineering specialists you hire as your organization grows: your dedicated DevOps, infra or devtools teams. They're specialists tasked with upgrading your organizational infrastructure to support your team's increased complexity.

As we internalize that larger organizations need to be upgraded we can start to understand how critical the question of simultaneous top priorities become.  To tackle 4 top priorities simultaneously we need somewhere between 16-40 engineers.  We need between 2-5 qualified engineering managers.  We may need a qualified engineering director. We may need 4-5 additional specialist staff. We may be looking at as many as 60 people.  And to make that jump we've had to go from playing on the easiest level to playing with a very high degree of professional sophistication.  It's also worth calling out the unfortunate reality that software engineering has underinvested in training managers for long enough that our preferred method for acquiring them is the well known failure mode of "promote" a high functioning engineer and hope they figure it out. A practice with anecdotal failure rates in the new manager's first year in the 80-90% range.

You can think about the insight that you need to be incredibly disciplined with how many goals you're tackling organizationally as a version of the Toyota/Kanban/Lean insight regarding controlling work in progress.

There are two common degenerate cases we see in teams that don't invest in better tooling as the complexity grows.

Many teams start out trying to tackle a huge number of priorities by spreading their team thinly across all of them (like butter scraped over too much bread).  This predictably leads to a high failure rate of projects either not delivering, delivering on timelines that fail a cost-benefit analysis, or delivering solutions that don't address the underlying business need.  

Over time teams tend to identify the failure mode of "too little wood behind too many arrows" and bulk up the teams working on each initiative.  In this model the hiring is perceived to be the key investment and the investment in organizational tooling neccessitated by team growth doesn't happen.  This pattern leads to a common industry truism in medium sized and up teams that, "you have to hire 20% year over year just to run in place." (which leads to cost and complexity spiraling out of control until the next great re-org and/or layoff)


### 3. Turn Over, Thrash and On-boarding

No theory of calculating team size could be complete without thinking about 3 randomization factors which are only somewhat under your control.  

Most well run teams (below a certain size) don't have an expected attrition rate, each departure is surprising.  This runs somewhat counter to what we know about software engineering careers: that average company tenure has hovered around 18 months for years.  That said most teams try to have some slack in the system that can absorb surprises, like a departure.  We sometimes refer to this as "bus numbers" or "having a bench". (oddly enough the "bus number" is a metaphor usually used for ICs while "having a bench" is usually used for managers).  We know we can't immediately hire and train a replacement if someone leaves, needs to take an extended leave, switches careers or is fired, and so we try to get ahead of it.

Most well run teams try to plan. Most still do it poorly.  The most common planning failure is overstating your level of certainty with the current plan. When plans are stated with high confidence it is rational to invest heavily in laying a foundation for the plan, e.g. investing in new technologies, hiring specialists, and a thorough design and architecture phase.  When plans that were stated with high confidence change frequently the team loses their large upfront investments, and also starts underinvesting in future projects.  We usually experience this pattern of fluctuating over/under investment as thrash.  It is a key driver of technical debt, not to mention cynicism. (see also [Technical Debt Doesn't Exist](/notes/towards-an-understanding-of-technical-debt))

We have some control over how quickly new team members can become proficient members of our organization. Investment in on-boarding is one of those scaling investment costs that comes with increased organizational complexity.  Done right the cost is amortized across the much larger team.  If you underinvest in on-boarding then attrition and thrash hit you harder, and you need to plan accordingly.  Engineers who spend 6 frustrating months working at half capacity, get much less done than engineers who've been explicitly told to expect to spend their first 30-60 days coming up to speed and then achieve team average productivity in months 3-6.  Also those engineers who spent 6 frustrating months are both more likely to quit and more likely to get fired. When thinking about attrition in your team size model the root cause of why the person isn't on the team anymore is less important than what you can do to improve next time.

### Simpler Than What You're Currently Doing

The above may feel complicated, or it may feel simplistic.  It intentionally moves the complexity of thinking about team size up the chain and requires the company to get better at planning and communicating goals, and being disciplined about prioritization.  This can feel like a heavy lift, and in some organizations it is.  However it is universally easier than trying to succeed in the face of poor planning, poor communication, and rule of thumb percentage increases of people.  Or you could just plan to grow 20% next year. 


