---
title: "Embrace, Extend, Extinguish"
date: 2020-02-17T20:00:00-06:00
---

GitHub [just released](https://github.blog/2020-02-12-supercharge-your-command-line-experience-github-cli-is-now-in-beta/)
their `gh` CLI, with initial support for issues and pull requests. While it's
complimentary to `git`, `gh` squashes a bunch of otherwise confusing `checkout`
and `pull` commands and makes the interface much cleaner.

It's a slick experience that I'm sure will continue to see growth, and at
some point `gh` commands will start making an appearance on GitHub docs and
eventually on the main site, for example in the "clone or download" tab on a
repo, the default could be `gh clone org/repo` instead of using `git` over
SSH.

As I was reading the [HN commentary](https://news.ycombinator.com/item?id=22313874),
I stumbled upon a great question, "why doesn't GitHub just use files in
a `git` repo to add issues, pull requests, etc.?" I shared these thoughts
in our group chat with the joke "embrace, extend, extinguish" added on,
a reference to the Justice Department's description of mid 90's Microsoft's
strategy ([many examples](https://en.wikipedia.org/wiki/Embrace,_extend,_and_extinguish#Examples)).
Given GitHub's ownership, I was poking fun at what the future might hold,
as several others on the original thread did.

To be clear, I'm not calling the death of `git`, nor am I particularly mad
that people are building more user friendly tooling on top of it, but it did
get me thinking about building good products with defensible business models.
This post aims to condense those thoughts, as well as point out a few other
areas this seems to be happening in.

## Embrace + extend = extinguish?

As discussed in [week 3](https://docs.google.com/presentation/d/19XXKTibLyNNZdK1TsC3offY67-pTPwMDBp6FLaKCue8/edit#slide=id.g6169143110_0_118)
of [my PM course](/pm-course), companies with good business models usually have
certain advantages: the founders are best in class, their products are 10x better
(or cheaper), they have a distribution network that lowers their customer acquisition
costs, or they've built up moats that keep competition at bay. Embrace, extend,
extinguish is one of the easiest moat building techniques companies to implement.
Here's how I'd go about building a company with a good moat.

First off, you need a protocol that is mature enough to have significant usage,
but also crufty enough that features can't be easily added to it.

Some examples:

 - `git` (version control)
 - `smtp` (email)
 - `sms` (text messaging)
 - `sftp` (file transfer)
 - `rss` (content aggregation)

Next, you need a layer of abstraction to cover the implementation, that you can
also run your proprietary API alongside. Email and SMS clients have done this
forever, though they typically don't deviate too heavily from what's provided
in the standard. I say typically, because the truly great ones do.

Once your product has sufficiently abstracted the underlying protocol, people
slowly forget how the original worked, where the warts are, etc. and become
increasingly reliant on the higher level of abstraction and backwards
incompatible new functionality.

In the case of `gh`, once they have commands that take the 80% of `git` actions
that involve multiple commands that nobody remembers, and wraps them in more
relatable GitHub termed actions, people will forget the ancient ways.

This lays the groundwork for the final step: replacing the legacy protocol with
your new one, and eventually removing it altogether. Once your tool has subsumed
all that functionality, there's no reason to keep the old one around. You don't
even need to consciously extinguish anything: your users effectively did that
work for you.

## More than just Microsoft

Examples of this are happening all over right now, and it's not just large
tech companies (though, most of the examples of it working only happen at
certain scale).

### iMessage: the 🐐 GOAT 🐐

As we reach the top of the S-curve of cell phone adoption, Apple has switched
to accessories (e.g. AirPods) as well as services. Apple TV is an obvious
play as is Apple Arcade, but so is the less obvious "Sign in with Apple."
The fact that it is *required* to be included when an app includes a
NASCAR login screen is a move I'm surprised hasn't been challenged. Once
you sign in with Apple on one website or app, it becomes basically impossible
to use the same account on a non-Apple device, because no Android app is even
able to support signing in with Apple. These services all work to keep users
buying Apple devices, as they only work on Apple hardware, and each add a new 
layer to the moat around that core business. And of all of them, iMessage is
the best example, in part due to strong social pressure and network effects.

I remember seeing a presentation about how "green bubbles" (Android
users) get dropped from group chats because iMessage functionality breaks.
There are similar anecdotes about people refusing to date someone without
an iPhone, or breaking up when someone gets an Android. I think a lot of
it comes down to elitism, but it's the software walled garden that got us
there.

Google has tried to fend this off with RCS (its own extension of SMS, sort
of backed by the telecom industry), but while that brings certain Android
devices up to feature parity ("darker blue bubbles", read receipts,
typing indicators, etc.), it doesn't solve the fact that non-iMessage folks
will always be green bubbles in iMessage.

FaceTime is another great example. Remember in 2010 when Steve Jobs (pour
one out) promised it would become an industry standard?

> Now, FaceTime is based on a lot of open standards — H.264 video, AAC audio,
  and a bunch of alphabet soup acronyms — and we’re going to take it all the way.
  We’re going to the standards bodies starting tomorrow, and we’re going to
  make FaceTime an open industry standard.

Well, here we are a decade later, and I can't use FaceTime on the machine
I'm writing this blog post on. And I'm not surprised: the deep integration
and walled garden of the Apple ecosystem keep selling hardware, and at the
end of the day, as much as Apple wants to be a software (or now, a services)
company, it's still in the phone business.

### Spotify: the home of podcasting

Podcasts are typically distributed via RSS feed to podcast clients, which are
able to aggregate supply, provide the listener with useful functionality beyond
playing, and also handle ad injection, etc.

Spotify, providing a client as well as an owner of several podcast groups,
is able to aggregate both supply and demand, while adding additional
functionality (e.g. better demographic information for ad targeting).

[The worry here](https://mattstoller.substack.com/p/will-spotify-ruin-podcasting)
is that Spotify gains control of the ecosystem and forks from that standard (or
the standard is otherwise rendered useless), and lots the hallmark diversity of
the podcast ecosystem is lost.

### Superhuman: coining the term "luxury software"

Superhuman is the iMessage to Gmail's Android (though it actually uses Gmail's
APIs under the hood!). While Superhuman currently lags Gmail (and many email
clients) in features (for example, formatting is very difficult/non-existent:
try monospace fonts!), but they've critically added the blue bubble to Gmail's
green: `Sent from Superhuman` below the fold.

Users on Superhuman also have a "user since 201X" in their contact card, and it's
only a matter of time before they start adding Superhuman-to-Superhuman only
functionality (e.g. reaction emoji to email threads or realtime chat). In effect,
Superhuman becomes the online equivalent of The Battery, and those not present on
the tool get left out of the real world dealflow.

That's a powerful enough incentive to keep paying $30/month, especially since Bloomberg
charges just over $2000/month for the finance equivalent (chat, meaning access
to the network, being a huge component of the worth). I won't write any more about
Bloomberg, but if you're interested I highly recommend ["You Can't Kill the Bloomberg Terminal"](https://marker.medium.com/why-its-hard-to-kill-the-bloomberg-terminal-61073482e496).

## Replacing moats full of money

The past several years have seen startups use cash as the moat: e-scooters, food
delivery, mattresses (and almost every other DTC vertical). All of these
are commodity goods, with zero defensibility: the motto was, "the best defense is
a pension funded offense."

Given the high profile dumpster fires that have come out of that and lackluster IPO
performance of the ones that made it that far, I hope we'll see more startups picking
defesible positions and having moats grounded in high quality experiences and engineering
choices that result in faster, better, or cheaper products.

As always, I'm interested to hear your thoughts, and if you know of any
other good examples of this, especially among early stage startups, definitely
[reach out](mailto:hello@mikemcdonald.co) and let me know!