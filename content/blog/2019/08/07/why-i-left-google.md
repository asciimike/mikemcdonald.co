---
title: "Why I Left Google"
date: 2019-08-07T11:30:00-07:00
---

__Update 10/5/19:__ I've started looking around for something new and
[published a post](/blog/2019/10/05/selection-criteria/) on a framework
for making such a decision as well as what I'm looking for.

After five years working on Firebase and Google Cloud Platform, I left Google
on July 12, 2019. In an effort to avoid,
["Why did Jacob Wenger leave Microsoft for Firebase?"](https://www.quora.com/Why-did-Jacob-Wenger-leave-Microsoft-for-Firebase),
I'll take a stab at explaining why and (ideally) preempt any pointless Quora
questions. But first, a bit of history...

# How I got to Firebase

I first heard of Firebase in October 2013 while a senior at Rose-Hulman, when
[Andrew Lee](https://startupandrew.com) came back to demo the product and
recruit. At the time, I had just spent nine months attempting to build a
collaborative document annotation application, and hated databases (and really
anything backend). My friend (and future Firebase employee) Alex dragged me to
his demo and after watching him go through the drawing, chat, and Tetris demos,
I was blown away. Firebase gave regular developers superpowers.

I met Andrew that night in a coffee shop in Terre Haute to chat about startup
culture and life in the bay area, and the conversation turned into an interview.
Later I met with [James Tamplin](https://tamplin.net/), and eventually the whole
team in San Francisco at Firebase HQ 2.0, and was given an offer to join the team.

I arrived at Firebase HQ 3.0 on July 1, 2014. Remenants of [Pineapple Day](https://startupandrew.com/posts/how-i-started-pineapple-day-holiday/)
littered the office (cans of pineapples, a bottle of pineapple juice, a
pineapple with a chef's knife embedded in it...) and I was excited to start
doing whatever working at a startup meant.

Turns out, neither James nor I had any idea what that meant. I distinctly
remember our second 1:1 where I was struggling with some "hard problem" and
wanted "the answer" to which James said, "nobody knows what the **** they're
doing" and that everyone basically made it up along the way. Shocking for a
kid who spent the past four years thinking he knew the answers, but great
advice for someone just entering the workforce.

During that summer, I ended up working on developer relations, talking with
customers, playing corporate counsel (we didn't want to pay $800/hour for
actual lawyers, so I negotiated sales contracts myself), understanding our
funnel, writing sample apps and documentation, and learning how the business
worked. Towards the end of the summer we were told of the potential
acquisition, and worked harder to grow the product in both users and revenue.
It was also a period of tremendous growth for myself, and every day was
invigorating.

# Growing Firebase

We started at Google on October 18, 2014. We all showed up at Firebase HQ 3.0
bright and early and got on a bus down to Mountain View for orientation where
we got fancy badges, shiny new laptops, and a pile of paperwork to fill out.

The first year at Google was full of growth: learning new tools, understanding
a new business model and figuring out where we fit in, and doing out best to
leverage the resources of a large organization without getting crushed. I
continued to do a mix of things before eventually transitioning to the product
management ladder, as I had been doing that job all along, I just didn't know
it.

By the summer of 2015 we had found our niche within Google, and by late 2015
the effort to transform Firebase from three products to 15+ was well underway.
I took on the role of leading [Firebase Storage](https://firebase.google.com/docs/storage)
(now Cloud Storage for Firebase) and worked with three engineers to launch that
by I/O 2016. It was the hardest I've worked in my life, but also something
I'm immensely proud of. It culminated with the first attempt at "Zero to App",
where we pulled off live coding three apps on stage in 40 minutes: 

{{< youtube xAsvwy1-oxE >}}

After successfully re-launching the platform, I dove head first into integrating
Firebase with Google Cloud: striving for first class integrations with Cloud Storage
and eventually Datastore (now Firestore) and Cloud Functions.

# Transitioning to Cloud

At the end of 2017 James and Andrew left Google, and I felt like the work I had
done to integrate Firebase into Cloud meant that I'd be better suited to working
lower in the stack, so I joined the App Engine and Cloud Functions team,
working primarily on strengthening their security posture and improving control
plane usability.

In early 2018, we started work on [Knative](https://knative.dev/), and I dove
into understanding how Kubernetes worked and how we could replicate functionality
while reducing complexity. From that came [Cloud Run](https://cloud.google.com/run),
a product I'm extremely happy exists, as I now deploy number of my personal
projects on it.

# Leaving Google

Five years in, things were much different than when I first started at Firebase.
There are many excellent things about Google: the people are generally smart
and thoughtful (the vast majority of folks I worked with would pass the airport
test with flying colors), the work is technically complex and fascinating, and
(of course) the perks are excellent.

However, despite the perks and excellent coworkers, I felt my personal growth
had slowed significantly, and more and more of my day was soaked up with the
workings of a large company (status meetings, planning meetings, planning for
status meetings, etc.). I felt like I was devoting less energy towards solving
customer problems, and more time to solving internal problems.

Attempts to change issues I saw that were affecting customer adoption were
therefore slow. It took more than a year to get [Cloud Functions IAM](https://cloud.google.com/functions/docs/securing)
from Alpha to Beta. Even simple docs changes took days to weeks. It felt like
the organization had calcified, and I was restless to ship (that's what good PMs
do, right?).

But ultimately, I was burnt out. I traveled for most of 2018 and early 2019 
visiting developers and speaking at conferences (thanks in part to the slow
development cycle), and all that time meant a lack of stability in my personal
life. I couldn't keep up a workout schedule (even though there was a Google gym
directly below me), and finding time for friends or a relationship was nearly
impossible.

# What's next

Five years went by in the blink of an eye, and it's time for a break. As
mentioned above, I'm taking some time off to recover from the big tech co
life (I don't know if I eat healthier, but I certainly eat less), and work
on personal projects (some of which are software, some of which are not),
get back in shape, and carve out time for my personal life.

I still plan on doing something product related in the future, so as I get
a little further from work expect some product strategy blog posts as well
as fun tweets about the personal projects I'm working on. At some point,
I'll be searching for what's next, so if you've got interesting positions
open I'm all ears. And as always, I'd love to hear what's on your mind!