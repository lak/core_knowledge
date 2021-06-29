# A productivity company?
What would it look like to start a productivity company? What would it even mean? Can you help productivity generically? Is there any value if you can't?

A bit like Mara's idea of having a community-focused incubator, I could almost see a meta-company that spawned companies building productivity tools for individual industries. You're building a bunch of niche businesses but not requiring that a given company be able to be all things to all people.

It would be awesome to be able to do the opposite, build a generic productivity product. Trello is one, but it's not powerful enough.

Do you have to give up reach if you do this?

Excel wasn't powerful at first but certainly became so over time. Same with Photoshop and Autocad.

Maybe I should research how these products evolved.

They all have this kind of spiky usage distribution -- deep usage by an industry or three, and shallow usage by a huge portion of people.

Trello seems different - no deep usage, because you can't really.

Hmm. Except... For all that Photoshop has become incredibly powerful, most of that power is actually tied up in people's heads -- functionality that isn't understood isn't accessible, but inaccessible functionality didn't hurt these tools, so maybe I'm putting too much importance on the progressive disclosure and such.

Changing tacks:

A big part of what matters to me, and how I see the opportunity, is that productivity is an understandable thing, a thing that can be observed, studied, dissected. No current productivity tool believes that. 

People have goals. They can measure progress against those goals.

More importantly, there is such a thing as expertise in productivity, and most people don't have it. Building something that encapsulated that expertise could and should have real value.

Maybe the way to describe this is operational tooling? That moves it away from project management, which is probably helpful and hurtful.

In other words, I think there's a broad opportunity in creating software that makes people more productive, but the opportunity that excites me is in creating something that helps make productivity a thing on its own. A bit like Puppet: Yes, it was about making sysadmins more productive, but it was also about making automation a separate industry.

Let's go back to basics.

# What do I believe?

Productivity is a form of expertise

Expertise in productivity is not widely distributed

We cannot and should not expect people to become productivity experts

The work is not done in productivity tools, merely tracked by them

There is no fundamental "right" visualization of work, so any product must provide multiple options

There are many tightly related operational systems

We can build a single tool that with minor changes can handle different systems (e.g., pipelines, Kanban, decision-making)

Effective productivity requires assessment loops, not just execution

A tool's helping you accomplish your goals requires that you be able to express them to it

Within a team or a person's time, effort spent on system design and optimization is and should be segregated from effort spent on execution

# What would I build?

We should build a single platform that enables creation of problem-specific workflows (e.g., pipelines), with automatic productivity metrics for a given workflow.

It should connect to where the work is, enable people to track the work automatically, or track it directly in the tool where appropriate.

Even within a workflow, it should provide multiple views (e.g., list of lists, grid of text boxes, grid of pictures).

Each card should be an instance of a card type, which itself is configurable.

Workflow instances can define which cards they work with.

# Post-script
If we take the below -- that we're really talking about another kind of project management tool -- then we need to make explicit some necessary beliefs.

Project management tools in general seem useless for the kind of work people actually do. People do not build comprehensive plans, people do not estimate time, they do not write down dependencies except in extreme cases, and they do not view the world through the lens of project.

Also, project management tools seem generally built for executing individual plans, vs ongoing operation of systems.

Taken together -- this lack of comprehensive plans, and need for ongoing operation vs one-time plans -- we get a sense of what's really different about what we need.

Strangely, searching for 'project management tools' does not provide a list of products, implying there's no active market here. Weird.

There's also a ton of good info on lean project management, including the 7 (or 8) wastes.

I like [this separation][1] between operation and process, pointing out that in general operation (i.e., human action) is waste. That's a scary way of looking at things, right?

Productivity as a goal looks very different when viewed from the lens of team vs from the lens of company. From the company's perspective, we're trying to use the fewest people to solve the biggest problems. From the team's perspective, we have a fixed allocation of resources (to an extent) and are trying to get the highest quality work done.

# Fin
One of the obvious dangers here is trying to make something so generic that it's not actually useful to people, and at the same so powerful that no one can use it.

I still think Trello is wrong, that it's too simplistic and will stay that way.

What do I think about teams?

Productivity does seem to usually include them. Any solution here must support and enable them. And any business model likely includes selling to companies, not just individuals.

That being said, it is also important that it work for individuals.

I think Puppet has shown that distributing expertise across time is analogous to doing so across people. That is, a person might spend a couple of days setting up a system, then an hour a week assessing, or a large team might have one person devoted to system design and optimization.

Aren't I fundamentally positing a difference in tools that is not currently recognized?

*There are tools in which work is done, and there are those in which work is managed.*

In truth, the former is generally called a productivity tool: Word, Excel, Photoshop, etc. Let's call the latter a 'meta' tool for now.

Is this rational? Do people do work in Trello? If I build a large enough list, aren't I working there? If all of my comments, my actual typing, my organization, all takes place in Trello, am I now doing the work in it? Or is all of that work really just reflecting work done elsewhere, such that to some extent I'm duplicating effort or understanding?

Aren't these meta tools just project management tools?

Maybe? Certainly Trello and Asana would qualify as that, even if both companies would argue against that. They don't want to be dropped into that bucket.

So really, it might be that what I'm hypothesizing is that there's an opportunity for a better project management tool, recognizing:

* 'Project' is too limited a view on the world
* Our workflows should be optimized to the problem
* People can and do work in a more agile, on-demand way
* Our tools should tell us how we're doing against our goals (most of which are not just timelines, and certainly not interim timelines)
* It should help with ongoing work, not just one-time

[1]:	https://en.m.wikipedia.org/wiki/Muda_(Japanese_term)