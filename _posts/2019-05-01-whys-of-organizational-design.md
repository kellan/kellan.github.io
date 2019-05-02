---
layout: post
title:  "The 5 Whys of Organizational Design."
date:   2019-05-01 01:02:45 -0500
---

Recently I wrote about [sizing engineering organizations](/notes/on-team-size), and how you can think about it as an exercise in managing concurrency.  In un org size I talk about the mental exercise of thinking about how the number of concurrent work streams you're taking on as a team applies upward pressure on the needs of your organization (e.g. you need more managers, who need more directors, who need a more senior CTO, etc) The inverse exercise is also useful. 

As is so often the case with conversations about organizational design the problem statement usually starts like, "we need a new engineering leader".  Should we hire a new VPE and move all our managers there (except of course for that one team)? Should we hire a CTO to own architectural conversations but maybe not have anyone report to them? Maybe this half of our team could report to the CPO? 

I spend a lot of time trying to convince teams that this is the wrong way to think about organizational design.  You can't solve questions of organizational design by shuffling responsibilities around the board like so many chips on the roulette table. (or memorably once like so many stacks of Starburst candy on the floor of the CEO's office)  And you can't solve your team's problems by slicing more thinly the responsibilities at the top, no matter how often someone tells you the hoary distinction that the VPE is there to manage people and the CTO is there to make technical decisions. (a distinct that is not only bad, and wrong, but will eventually leave your company a pile of burning rubble).  These are the wrong questions.  So what are the right questions?

### Get Curious

When faced with these problems I find it useful to walk the stack down to the front line of work to understand what are the pressures on this complex system.  Call it the "5 (possibly rhetorical) Whys of Organizational Design". 

Q1: Why can't your CTO/VPE/Head of Engineering create the context where these problems are getting solved?

A: Well they're just spread really thin

Q2: So why aren't your directors helping take the load off?

A: Well they're spread really thin as well (or we don't have them)

Q3: So why aren't your eng managers taking load off the directors?

A: They're spread really thin as well, we just promoted one of them from being a senior engineer, etc

Q4: So why aren't your tech leads taking load off your managers?

A: They're spread really thin (or we don't have them)

Q5: So why aren't your senior engineers taking load off your tech-leads?

And by now we often get to the interesting actionable answers. 

### Some common discoveries along the way:

- your head of engineering doesn't have anyone they can delegate organizational work to ⇒ you need directors.
- your directors are spending all their time managing and can't contribute to organizational capacity ⇒ you need managers.
- your managers are spending all their time dealing with the fact that their team is comprised of humans ⇒ they either need fewer direct reports or to be managing people in a less drama inducing work place.
- your managers are spending all their time tech leading ⇒ you need tech leads.
- your managers are spending too much time reviewing PRs ⇒ stop being a control freak and trust your team. you're hiring smart people to make good decisions. if you can't trust them that's a leadership failure.
- your managers are spending too much time coding ⇒ you need more engineers or to do less.
- you don't have tech-leads because every team is super small, maybe one engineer per team ⇒ you're doing too many things. also you like failing.
- your tech-leads spend all their time reviewing PRs ⇒ seriously, stop it.
- your tech-leads and/or senior engineers spend all their time coding ⇒ your definition of senior doesn't include leadership.  you need to fix that.  likely as far back as your hiring process.
- your senior engineers are busy working on less important things ⇒ it's *possible* communication has broken down.  or maybe prioritization isn't as clear as you thought it was?
- your senior engineers are spending all their time firefighting ⇒ likely you've created insufficient slack in the system to allow for training and tool building.
- your senior engineers don't have anyone to mentor/train, they're discouraged by the constant firefighting, they've become cynical about your lack of ability to plan, and they'd like to wander off and just build something shiny to give their brain a rest ⇒ did you do that thing where you "only hire seniors", because that's what it sounds like.  alternately, did you do that thing where you spent a lot of energy selling your "hard technical problems" during your interview loop, but having those problems was a bit ... aspirational?
- your CTO/VPE/HoE doesn't actually want to think about any of these problems. ⇒ are you sure?  have you asked them? if so, you're right, you need a new head of engineering.