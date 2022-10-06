---
layout: post
title:  "How to plan?"
---

I was in a job interview the other day when I got asked about planning, and so I decided I'd turn the question into another "plucked from the interviews" blog post.  To be clear this is significantly expanded answer based on what I rattled off from the top of my head, but I think the themes are roughly the same. There isn't a one true way to plan, and this post won't tell you how to do it. Instead these are some things to think about in why planning is often so awful, often useless, and what you can do about it.

Interview Question:

> Have you been involved in annual planning? How did you handle it? Do you prefer top down or bottom up? Is thinking about tradeoffs something you've done? 

This interview was for one of those jobs leading product and engineering which are coming back into vogue, sometimes called a GM, or CPTO, or just a VP of something or other. As an industry we've gotten pretty clear on the downsides of matrix management and the pendulum has started to swing the other way.  Though as Andy Grove said when deciding between organizing functionally and organizaing along business units the right answer is always the other one.

Let's set aside the question of tradeoffs for the moment, except to say, tradeoffs are the very heart of engineering and engineering leadership. Software as a medium is so malleable that functionally anything can be made to work. Any language, architecture, approach, style, process, etc can be made to work given sufficient effort. Meaning we find ourselves not asked to choose between right and wrong answers, but between tradeoffs. 

Planning is a bit like software in that with enough effort anything can be made to work.  Consequently we aren't looking for the Right Way to Plan, as much as trying solve for a set of constraints and things we've learned the hard way about how humans work. (Also like software: planning is easier the smaller your team is)

The first challenge we need to navigate about planning is we're usually using a single process (or small set of processes) to attempt to solve a bunch of different problems:

* Communicate a shared goal and vision for everyone to pull towards. Our vast and endless sea to yearn for.
* List the projects that teams are going to work on, and the metrics they plan to move.
* Equip the business to estimate whether the projects and impacts are sufficient to meet the organization's targets (growth, revenue, capabilities, etc)
* Solicit insights from the organization on what are the critical and high impact projects to undertake.
* Give leadership a venue to provide feedback, set direction and course correct.
* Project plan, tile work, and evaluate utilization.
* Identify and manage dependencies.
* Headcount planning and allocation. 
* And a dozen other things in any given iteration.

As you can see we're a long way from Do One Thing Well.

### Some guidance as you set out to build a planning process to satisfy the above constraints

### 1. Bottom up processes don't work. 

There are a ton of critical insights we need from the people on the frontlines doing the work, but bottom up planning isn't how to get it. Bottom up planning starts at the squad/team level, the leaves of the hierachy, and aggregates and synthesizes the plans at each level as they move up the hierarchy.  We see a few predictable failure modes with bottom up:

* Individual teams, almost definitionally, aren't in posession of the information and perspective to understand what is most important for the whole organization, and perforce will make locally optimal choices based on the information they do have. 
* Individual teams during planning will the answer the question of what it would take _them_ to accomplish a given goal, without awareness of what other teams will accomplish.

The above two tendencies are a recipe for an organizaiton that grows larger every year, but is largely maintaining the status quo.  Ben Horowitz has written a take about this in [How to Ruin Your Company with One Bad Process](https://a16z.com/2014/07/22/how-to-ruin-your-company-with-one-bad-process/) His take isn't most charitable, but even people with the best intentions will walk into these traps.

Finally

* Bottom up processes fall victim to anchoring. In a bottom up process you ask people to spend time and energy advocating for what they think the right thing to do is, and what resources they need to do it. They naturally emotionally invest in that outcome.  This now becomes the floor for their expectations.

### 2. Planning isn't the time to introduce anything new

Most organizations have a formal period of time annually (or quarterly or every 13 weeks) when they "Do Planning".  This period is usally called Planning. The implicit or explicit ask of Planning is often tell us about all your exciting new ideas. We need your creativity to achieve our goals. Swing for the fences! Throw big rocks!  This is a mistake.  Look at that list of problems from earlier in the post we're already trying to solve with Planning, does this look like the time to also get creative? Similarly leadership often feels like Planning is their opportunity to introduce the new direction they'd like to see the company move in. All this does is create a low quality scramble and shallow thinking.

Once we get past project management in our planning and start trying to plan how to make meaningful progress towards our goals and missions, we're going to need to coordinate with people across the organization. Building a new product without thinking about how it's going to be sold and marketed, or what infrastructure it needs to support it, or even finding out the history of previous attempts at the company to build similar products is how tech companies fail, over and over.  But during Planning everyone is too busy to have those conversations. (and probably too emotionally keyed up as they contemplate their budget for the coming year)

Start work on new things when you aren't planning. Document what you want to do/build/etc. Share the proposal with people. Get their explicit buy in to support the new thing.  Test your assumptions and estimates with people in your organization with expertise that are different than yours. Get feedback from leadership about whether your idea is aligned with the direction of the organization (or if they're willing to change directions). Tell people how much it's going to cost: in terms of people assigned to it, to iterate on it, to break through the noise in the market and educate your target customers, etc. Solicit internal interest for people who would be interested to join the effort if it gets approved.  This is a Funding Proposal.

That's can seem like a heavy process. It can take weeks or months. That is what it takes to write a plan to do a new thing. It isn't something you can do meaningfully within the constrains of a company's annual Planning process. 

The is another option that also works well for a large class of ideas: just try them. Don't ask for resources, don't ask for support from other teams, do the quick and dirty test to validate or disprove your idea, build knowing that you'll probably fail and be ready to back out your changes.  That's the alternative to doing a real plan. 

Not using Planning to introduce new things has a bunch of benefits. Much like everyone is too busy running around like crazy people during Planning to give you meaningful engagement with your plan, these hectic planning processes make it difficult to keep even close partnerships, like engineering and product, in sync, and result in frustration and hurt feelings. 

Finally, addressing the CEOs who feel like it is expected of them to roll out a new exciting direction each Planning is a topic for a different post.  Ideally however we're not rewriting our 3 and 5 year plans annually and so continunity flows naturally from gaining increased confidence in our multi-year vision.

### 3. Provide frameworks and constraints

This is how you do the top down planning, without micro-managing your team. Ben's post touches on the importance of telling teams what the budget they have to operate in is, and holding back a buffer (20%) both to encourage teams to be creative and ambitious, and to perserve option.  Those are useful constraints, but there are so many others that teams need.

Frameworks can be a useful way to introduce constraints. 

* "Even overs" can be a useful framework. Our goal is to be multi-product company, prefer net dollar retention even over new customers. Ship new features even over multi-platform consistency.

* An investment portfolio approach is a framework. 20% of our effort should be going to brand new efforts that are high risk and high reward. The number of people it takes to operate our mature produdcts should decrease 20% YoY.

* Capabilities models: we need to be able to X so we can unlock Y opportunity.

Metrics (and by extension OKRs) are perennially popular constraints. Revenue, churn, sign ups, availability, etc are the bread and butter of many companies planning processes. Consider pairing them with metrics that shape a narrative (storytelling metrics) about what you think is important: customers who used us both on desktop and mobile, % of the company who uses a product, etc.

For similar reasons to what we discussed in points 1 & 2, these constraints can't be uncovered by the planning process, they need to be constraints people know going into Planning. As an example, a popular constraint is: we'd like to do a marketing event to celebrate our new features this year. It can be tempting to let the teams tell you when they'll be ready and then plan the event, but that's circular. They can only tell you what will be ready when they know when the event is. (and knowing when the event is informs if this is a quick and dirty or a thorough and thoughtful implementation we'll be building)

The most important constraint that frequently gets lost in planning is what is the cost of the work we've already committed to:
* what is our KTLO?
* what is needed to finish the migrations we have underway
* what did we already promise customers
* what is it going to cost to deprecate the pieces of the system that aren't working
* in general, what does it cost us to maintain the status quo

These are things you should be tracking throughout the year, but if you aren't, setting aside some time before planning to get these answers is important.

One reason we see some leaders shy away from providing the constraints and frameworks is that while they can't be uncovered by Planning, they can be invalidated.  You need to be comfortable finding out your wrong.

### 4. Project planning has an inflection point

There is a time in the life of many companies in which they are single threaded, or close to it. Either everyone is working towards The One Important Thing, or everyone is working either on The One Important Thing or they're working on something unimportant.  At this stage most of the key coordination problems you're trying to solve with Planning take care of themselves.  Instead Planning will focus on the steps neccessary to acheive The One Important Thing: milestones, blockers, risks, launch plans, have we broken the big thing down into smaller things that deliver value incrementally. This is project planning and it's perfectly reasonable to do at this stage.

As the complexity of what you're trying to accomplish increases and Planning becomes more about coordination and communication, project planning is no longer appropriate to do at the company level.  It's too fine grained. More importantly it leads you to make overly detailed commitments about _how_ you solve a problem to people outside your team. You should be commiting to the impact of solving the problem. Once you have people outside your team monitoring your approach to solving a problem it becomes much harder to change your plan as you learn new things. (and if you aren't learning new things when you're building software and especially products, you're doing something wrong, but that is also another post)

Many organizations miss this critical inflection point and go sailing off into Strategic Planning with the expectations of project planning still firmly in place. Companies operating in this mode are the ones whose frustration with not getting the strategic results they were hoping for leads them to push for more and more fine grained planning as the antitdote: an attempt to achieve greatness by optimizing for predictability.

### 5. Minimize dependencies

Dependencies are another area where Planning's attempt to serve many goals leads to problems. In Planning, as we've said, we are often being asked to think big, take risks, make big impactful bets. We're also being asked to contribute to a financial plan that needs to be accurate. These two conflicting messages meet at Dependencies. I will be able to launch a new multi-billion dollar business in the fiscal new year, but I will need everyone in the company to stop what they're doing and work on my plan instead, plus the additional thousands of people I've put in my plan that we'll need to hire.  I may even be able to convince (bully?) some of those teams into agreeing to work on one of my dependencies. (or maybe I don't even ask?)   This sounds ridiculous and yet you see it over and over again in Planning.

The problem with there being a significant number of dependencies between teams, especially those that are critical to strategic plans, is you are tightly coupling those teams to the point where they are functionally the same team. Either they _should_ be the same team, at least for the span of this project/plan/intiative/etc or you should minimize the dependencies on the critical path. 

As the person designing Planning, encourage people to build their plans on the foundation of things that are already working and shipped. New capabilities, and building support and excitement for them should be done via Funding Proposals.

### 6. Headcount planning

It seems logical that Planning would inform Headcount Planning. After all once we know what the highest impact work is next year, we should put what is probably our most expensive resource against delivering that work. It however inevitably raises the stakes. People who want to grow their teams are often portrayed as empire builders, but growth and hiring are part of a healthy team. We are now motivated to navigate/game Planning to keep our team healthy.

We can start shifting the high stakes nature of Planning by moving towards off cycle funding proposals as to discussed in "2. Nothing new during planning". Team growth, and growth projects for the people on the team have then already been discussed and planned off cycle. 

Quantifying the cost of the work we're already committed to avoids the pressure to generate new projects just to keep the team funded.  Similarly reducing dependencies simplifies the sometimes 3-card monte of who is asking for headcount to fund the dependency and how that will be allocated (and are those headcount of people currently working for the company, or the people we'll hire in 6 months?)

Finally headcount is an area where you just need to be comfortable with ambiguity. Planning processes that try to be precise will backfire creating thrash and anxiety. I was once at a company that was very concerned about in-year cash flow, and rolled out a headcount planning process that closely modeled in what weeks we could hire people (because if someone starts in week 26 of the year, only half the salary cost lands in year). There was a spreadsheet produced that showed you what percentage of a headcount had vested for your team, and allowed you to borrow against future headcount. The formula for calculating the cost of borrowing was sufficiently complex that it required a Windows version of Excel, and so all senior engineering leadership had to get a 2nd laptop to figure out hiring.

After you've removed as much of the headcount budgeting pressure from your planning process, your second goal should be to roll out something simple knowing it will always be fuzzy and inexact.
Something like an end of year "Not to Exceed" number, i.e. have this many people on your team or less by the end of the year. (why will the process by fuzzy and inexact? Most companies struggle to have an accurate view of how people map to teams, how many people have been hired but not yet started, interns, etc) Hiring requires a healthy pipeline of candidates. A simple system allows you to keep the pipeline up and running, without having a stop-start interruption as you try to hit some complex intra-year target with predicted attrition curves, etc.

How do we solve for that need of healthy teams to grow and why do we care? First we care, because new people joining a team means new ideas, new skills, new backgrounds, new opportunities for mentorship, fresh energy, and team continuity when someone (or a set of someones) leaves.  To enable a team to see growth without having to game Planning, it's important to keep a significant percentage of your budget in reserve, say 20%, that teams can propose to use. Holding back a significant percentage can be painful if you're looking at a sea of bottom up proposals that already add up to 200% of your allocated budget.  Instead following some of these guidelines we've created 3 different pathways to get funding for a teams growth as appropriate for different types of work: a funding proposal for net new work, a planning process for run of the mill growth, and an exceptions process to access the reserve for opportunistic and organic hiring that keeps a team healthy.

### 7. So why do we even plan?

If we go into Planning already knowing many of the new projects we'll be tackling, what we think the impact of that work will be, with a majority of our budgets already allocated, and with the goal of introducing nothing new, why do we plan at all?

Planning serves two key purposes in this model. 

The first is it acts as a point in time to synchronize are multi-threaded company.  All year ($time_period) we run loosely coupled between different teams and functions. Having a moment in time when we all agree we want to collate as comprehensive a view of what we're doing as possible is an important investment to keep us from drifting too far apart.  That's what Planning is, a time to all get on the same page before we all start running fast again.

The second is it's a forcing function.  We're all busy and sometimes things just don't get done without a deadline and a person asking for them. 

