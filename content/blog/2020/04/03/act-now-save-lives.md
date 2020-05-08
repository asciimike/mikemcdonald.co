---
title: "Act Now. Save Lives."
slug: "act-now-save-lives"
date: 2020-04-03T11:58:09-06:00
---

[Max](https://www.linkedin.com/in/maxhenderson/) and [James](https://www.linkedin.com/in/jamest/)
pulled me into [Covid Act Now](https://covidactnow.org) to help with product strategy. This post
has a brief overview of the problem space, as well as how we're approaching the products.

Briefly, with COVID-19, we're facing a few potential scenarios:

  1. We get extremely lucky and it turns out to be less deadly than we think (or pharmaceutical interventions come faster than previously thought)
  2. We resort to authoritarian tactics and have lockdowns/martial law
  3. A lot of people die
  4. We follow a reasonable Non-Pharmaceutical Intervention (NPI) plan

 Briefly, an NPI plan would include the following:

  1. Convince decision makers to issue "stay at home" orders, which buys us time
  2. Provide up-to-date data to those decision makers about how well their interventions are working
  3. Provide citizens contact tracing, telemedecine, and testing (or access to those)
  4. Provide an offramp to NPIs as other interventions come online

At the same time, we must ensure that the cure isn't worse than the disease: how do we balance
the economic consequences with the interventions chosen.

We've already built [the website](https://covidactnow.org) to help with item 1 above, and are
working on mobile apps, APIs, and other products. We're a fast moving organization responding to
a quickly growing problem, so I'm sure that by the time you read this post, there's a good chance
this is outdated. I'll do my best to keep this post updated, but if you're wondering why reality
is different than this site, it's because reality is quickly moving and full of
[a surprising amount of detail](http://johnsalvatier.org/blog/2017/reality-has-a-surprising-amount-of-detail).

Here's an example of one of the products we're building to solve #2 and #3:

## Embeds

We provide a simple embed that you can provide on your website that highlights current
intervention as well as case load and mortality. Given that it's an embed, over time it will
be updated to include other information, such as the projection charts.

Here's an example of the embed, set to my current state:

<iframe src="https://covidactnow.org/embed/us/co" title="CoVid Act Now" width="350" height="700" frameBorder="0" scrolling="no"></iframe>

You can quickly add it to your website via an `iFrame`:

```
<iframe 
    src="https://covidactnow.org/embed/us/co"
    title="CoVid Act Now"
    width="350"
    height="700"
    frameBorder="0"
    scrolling="no"
></iframe>
```

Or via a `script` include:

```
<div class="covid-act-now-embed" data-state-id="CO"/>
    <script src="https://covidactnow.org/scripts/embed.js"></script>
</div>
```

Make sure to swap out the state code from `co` above to whatever your desired state is.

<div class="covid-act-now-embed" data-fips-id="08031"/>
    <script src="https://covidactnow.org/scripts/embed.js"></script>
</div>

We also provide county embeds, referenced via [FIPS codes](https://en.wikipedia.org/wiki/FIPS_county_code) in an `iFrame`:

```
<iframe 
    src="https://covidactnow.org/embed/us/county/08031"
    title="CoVid Act Now"
    width="350"
    height="700"
    frameBorder="0"
    scrolling="no"
></iframe>
```

Or via a `script` include:

```
<div class="covid-act-now-embed" data-fips-id="08031"/>
    <script src="https://covidactnow.org/scripts/embed.js"></script>
</div>
```

Make sure to swap out the FIPS code above to whatever your desired state/county is.

For more info, visit [covidactnow.org](https://covidactnow.org). If you're interested
in helping out, [let us know](https://docs.google.com/forms/d/e/1FAIpQLSfQkdwXsbDbwLHhWwBD6wzNiw54_0P6A60r8hujP3qnaxxFkA/viewform)!