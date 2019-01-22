---
layout: post
title:  "Towards an understanding of technical debt"
---

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/widnr/6588149033/in/photolist-b3aZbr-8KScPJ-8A1VTq-eLV4ng-87UNqR-gtvGQb-biWMcv-89JjaA-pYMT8u-8pBgBb-9ZzxGH-9htL2G-74TEWQ-qQ7o5K-o3hQhD-j7iDqm-aq3FjJ-qtKEKv-nPQd5Y-aBWrzT-fLj6h-aZ3kC4-ozm7Co-dhjUrp-hYjpnY-tkQQMt-gWjC5m-AnpW4-8fJDv4-n9Y6W1-okiqfH-ynNyHR-oNnp4b-pnmsY5-psfHxo-eet1GA-e5FHQe-prE1Qi-nLgKFB-ikwLte-87XRQ5-kTbN8B-qGs2Li-wUcisw-85vF1z-ibpmcC-oUPwW2-984z9n-7MdP3H-pPQrWr" title="Somerset tire fire"><img src="https://farm8.staticflickr.com/7001/6588149033_d1b2b41cdf_b.jpg" width="720" alt="Somerset tire fire"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

I’ve spent the last few years rather flippantly stating, “Technical debt doesn’t exist.” 

What I was trying to say was, “I’m deeply uncomfortable with how our industry talks about this thing, I think it’s probably harmful, but I don’t know quite how to express what I mean.  Also, given that everyone seems to be really focused on this tech debt concept, I’m kind of worried that the problem is me, not the term or the industry”.

When I first heard Peter Norvig say, “All code is liability”, that felt closer to right.  

The other week I was sitting in the car, waiting for the baby to wake up, and bantering on Slack on the topic of tech debt when my pocket computing device died, and I was forced to finish my thoughts on paper.  These are those notes.

Technical debt exists.  But it’s relatively rare.  When you start arguing with someone about technical debt, you’ll generally encounter a definition like: Technical debt is the choices we made in our code, intentionally, to speed up development today, knowing we’d have to change them later.  Hard coding a variable because currently there is no plan to change it is a common example of technical debt.  Similarly not modularizing a function.

This is a fairly clear, succinct, and easy to reason about definition, that describes a phenomena that exists relatively rarely.  Relatively rare compared to what?  Compared to the amount of technical debt we ascribe to the codebases we work on.  How then do we explain the overwhelming prevalence of technical debt we encounter when we talk to people about code?

The term is being abused, or at least dangerously overloaded.

### “tech debt”: an overloaded term

There are _at least_ 5 distinct things we mean we say “technical debt”.

1. Maintenance work
2. Features of the codebase that resist change
3. Operability choices that resist change
4. Code choices that suck the will to live
5. Dependencies that resist upgrading

### 1. Maintenance work

As technologists we often intentionally or unintentionally use the term “technical debt” to describe to other teams (technical or otherwise) the necessary ongoing maintenance work a codebase needs.  In this case the wide recognition and acceptance of the term is useful shorthand for buying breathing room.  But it comes at a cost. We end up pathologizing something which is normal, often casting an earlier team as bumbling.  A characterization that easily returns to haunt us.

### 2. Features of the codebase that resist change

When we program we’re writing down a very explicit and exact description of a solution to our current best understanding of the problem we’re trying to solve. Over time both the problem we are trying to solve and our understanding of it will inevitably change, often dramatically.  When that happens some percentage of our very explicit and exact description is now wrong, and a liability. Taken to the logical conclusion, given time, every line of code is wrong and a liability that will need to be dealt with.

Therefore the second common meaning of “technical debt” is the features of the codebase we encounter in our work that make it resist change. Examples of features that can make a codebase resist change include: poor modularization, poor documentation or poor test coverage.  Just as easily though an abundance of modularization (and complexity) or an abundance documentation, and tests encoding the now the incorrect old behavior can apply a strong downward pressure on change. 

A little discussed and poorly understood design goal for code is disposability.  Given change, what design patterns can we follow that allow us to quickly expunge incorrect behavior from our codebase? Interestingly it is a much more tractable metric for measuring as opposed to more popular criteria like “elegance”. (a post for another day)

In my experience these features that resist change are one of the most common meanings of “technical debt”. However we often lack self-awareness about it because we don't tend to think of our work in terms of the life time of the codebase.

An example of maintenance work might be dealing with data that accumulates over time.  An example of inevitable change might be that at some point that data that accumulates over time no longer fits on a single physical device. And the resistance will come from how straightforward it is to add a more sophisticated storage solution.

### 3. Operability choices that resist change

Related to the code choices we’ve made that resist change: what are the operability choices we’ve made in the design of our systems that put downward pressure on change?

If the site goes down every time you make a change, you stop making changes. If you don’t have metrics you can’t deploy changes confidently.  Similarly if your tests are flakey, if extensive coordination is required for a release, if you don’t have staging environments, if you can’t run product and operational experiments, if people don’t have access to the information they need to make decisions, if incentives are misaligned etc, etc.

Attempting to improve an environment either under conditions of constant crisis, or in the face of inertia often leads to the energy drained state that programmers attribute to working on systems with large amounts of technical debt.  These are failings of operability.


### 4. Code choices that suck the will to live

Operational inertia and/or crisis isn’t the only phenomena that can lead us to feeling tired and drained. A significant percentage of what gets referred to as technical debt are the decisions that don’t so much discourage change but rather discourage us from even wanting to look at the code. The aspects of the code that suck our will to live as it were. 

We often describe this code with the suck-the-will-to-live quality as messy (spaghetti), unmaintainable, or amateurish. Often what we’re describing under the surface is fear and confusion. We don’t understand the code, and when we don’t understand things, as human, we tend to get scared, tired, and angry.  Often we find this pattern in teams who’ve inherited a codebase. The code that was originally written by a small tight knit team with a clear vision of the problem is now being worked on by (often much more senior) separate teams working in some degree of silo. What was a productive lack of indirection to the code becomes a poorly considered lack of abstraction resisting change.

Hence the paradox: how is it that a team of brilliant senior engineers need 6 months to clean up after that one early programmer’s weekend kludge job?

It makes no sense, unless you factor in and address the emotional impact of working on certain types of code. (and to be clear different types of code have this impact on different types of people, just another reason to be thinking about having a diverse team)

The other time I see teams struggling with this scared-tired-angry experience is when they’re asked to work on technology that runs counter to their identity politics.  I struggle to describe this phenomena with an empathic view point and so I’ll defer, but this recent post on [contempt culture](http://blog.aurynn.com/86/contempt-culture) is a good starting point.


### 5. Dependencies that resist upgrading

Finally we use technical debt to describe technical decisions that bind a codebase to a technology that due to the passage of time has become a liability: it has stopped receiving updates, expertise are difficult to find, upgrade paths become convoluted. Often a single dependency pegged to an older technology cascades across your infrastructure holding back important upgrades.

Archaic dependencies are often a symptom that we weren’t able to prioritize ongoing investment and maintenance of the codebase (see #1), and is the thing most reasonable to refer to as technical debt. Even in this often both clear cut and debilitating situation it is still a mistake to characterize the technical debt as a failing, moral or otherwise. We _may_ be in this situation due to a failure of planning, foresight, or expertise. Or maybe someone made a very correct choice to focus on delivering business value knowing that building for the future is only worth worrying about if you’re actually going to survive. 

This is an area where focusing on a small number of well known technologies, and being diligent about your new technology adoption process can really pay off.

### Why it matters

The first step to addressing any problem is understanding it. When we conflate these 5 different phenomena we confuse ourselves about possible solutions.  When we take it a step further and turn these conflations into a judgement on the intellect, professionalism, and hygiene of whomever came before us we inure ourselves to the lessons those people learned. Quickly we find ourselves in a situation where we’re undertaking major engineering projects without having correctly diagnosed what caused the issues we’re trying to solve (making recapitulating those issues likely) and having discarded the iteratively won knowledge that had allowed our organization to survive to date.

The two most common solutions both often make the problem worse:

 1. Declaring bankruptcy and rewriting from the ground up.
 2. Papering over the issue with a layer of indirection/proxy/wrapper

Rather if you are addressing a problem you understand and have correctly diagnosed you can put together a reasonable strategy for iterating and measuring your way to improvement. (and if you aren’t measuring when making changes you aren’t doing engineering, but that’s an essay for a different day)

And finally you should especially worry if your team believes they’re “fixing” or “paying off” technical debt.  All code is technical debt. All code is, to varying degrees, an incorrect bet on what the future will look like.  You can address issues that are damaging to productivity, operability and morale, but only way to “fix technical debt” is “rm -rf”.
