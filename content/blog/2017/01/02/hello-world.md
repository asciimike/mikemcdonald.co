+++
date = "2017-01-02T16:00:00-08:00"
title = "Hello, World 👋🏻"
slug = "hello-world"

+++

One of my new years resolutions was to make a website. Inspired by today's
["Ask HN: Excluding WordPress, what is your favorite for blogs or small stores?"](https://news.ycombinator.com/item?id=13300024)
I finally pushed myself to get a site together.

![Ryan Reynolds But Why GIF](images/but-why.gif)

I've [made](https://fir-cloudvisiontest.firebaseapp.com/)
[lots](https://sanichat.firebaseapp.com/) [of](https://zerotoapp-ccd8d.firebaseapp.com/)
terrible (mostly chat) apps to showcase various Firebase/Google features, but
never had time to build a personal site.

I love tech, but I also try to have hobbies outside of work: among them cooking,
mixology, travel, and the outdoors. I've had some unique experiences, and I'd
love to share them with others.

Anyways, as is custom when an IT professional creates a personal site, here's
the nitty-gritty details on how it was built!

## Static Site Generator
The [old Firebase site](https://www.firebase.com) used [Jekyll](https://jekyllrb.com)
(and claimed to be the largest such site in existence at the time), but I had
mixed feelings about using it. Build times were pretty long, gems were often
updated from under me causing things to break, and I was annoyed by the quirks
of running Ruby.

After a [short amount of research](https://www.smashingmagazine.com/2015/11/static-website-generators-jekyll-middleman-roots-hugo-review/)
I opted to go for [Hugo](https://gohugo.io), primarily because of the fast build
times, straightforward content model, and a clean toolchain. Many of the listed
negatives (lack of an asset pipeline, lack of extensions) also don't bother me:
I'm fine with vanilla `js` and `css`, and I don't think I'm yet at the point
where I need tons of extensions.

Additionally, Go and Swift are two languages I'm hoping to work with more
often in 2017. I figured this would be a good way to get started with Go,
[after my brief foray into Swift](https://github.com/mcdonamp/kitura-flex)
at the end of 2016.

I followed the [Hugo quickstart](https://gohugo.io/overview/quickstart/), which
was generally pretty helpful, though they did the annoying thing of making you
fail, then explaining how to fix it vs explaining how to get things set up
correctly in the first place (see Steps 4 and 5). I picked the
[Cocoa](http://themes.gohugo.io/cocoa/) theme, though I plan on forking it in
the future and customizing it further.

## Web Hosting
Since I work for Firebase, I opted to use
[Firebase Hosting](https://firebase.google.com/docs/hosting/). Getting it set
up with Hugo was as easy as:

```shell
firebase init                                # initialize firebase hosting
env HUGO_BASEURL="http://localhost:5000" \   # set the base URL as localhost
hugo --theme=cocoa \                         # build the site
&& firebase serve                            # test locally
```

Otherwise, just use `hugo server --theme=cocoa` to test using the build in Hugo
server. I wanted to ensure that it would work with Firebase Hosting, hence the
extra step of setting the `baseURL` before building the site.

Maybe, someday when I'm more adventurous, I'll explore using
[Google Cloud Storage](https://cloud.google.com/storage/docs/hosting-static-website)
directly. But for now, free web hosting + SSL + custom domain support combined
with a dead simple deployment story has me hooked.

## Domain

After a quick hunt on [domai.nr](https://domai.nr), I bought `mikemcdonald.co`
on [Namecheap](https://namecheap.com) for around ~$25/year. Came with a free
year of [whoisguard](http://www.whoisguard.com/), and was about $10 cheaper than
[Google Domains](https://domains.google).

Setting up the domain with Firebase Hosting is straight forward, though adding
the `TXT` records on Namecheap took a quick search to find the right places.
I've copied images that show how to select the right domain (click "manage"):

![Select the right domain](images/namecheap-domain-verify-1.png)

And how to add the correct `TXT` records:
![Add the appropriate TXT records](images/namecheap-domain-verify-2.png)

The one thing left to do is hook up an email address, though I haven't decided
if I want to go the [gSuite](https://gsuite.google.com) route, or
[hack it together with Zoho](https://medium.com/@gobudgie/how-to-set-up-a-free-custom-domain-email-address-with-gmail-inbox-7e8cb8574c3e) or
[Mailgun](https://simplyian.com/2015/01/07/Hacking-GMail-to-use-custom-domains-for-free/).
The former looks more scalable (10k email/month limit with Mailgun), but the
latter has way fewer steps.

## Publish and track!

After that, I hooked up [Google Analytics](https://www.google.com/analytics),
committed everything to a `git` repo, and launched:

```shell
hugo --theme=cocoa && firebase deploy     # 🚢
```

All in all, it took about three hours, $25, and a bit of motivation. Overall, a
great learning experience that I'm looking forward to sharing with you all!
