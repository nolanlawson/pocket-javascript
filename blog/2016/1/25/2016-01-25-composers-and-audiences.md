---
layout: layouts/post.njk
title: "Composers and audiences"
date: 2016-01-25T17:33:13.000Z
---

*(Yes, this post is about JavaScript. Please indulge the analogy for a bit.)*

Imagine yourself as a young court composer in the 18th century. You've just arrived in Vienna, fresh from the academy, with one goal in mind: to improve your craft, and to learn from the old masters. You've heard the stunning operas of Mozart, the ponderous fugues of Bach, and you've dreamed of wowing audiences with your own contributions to this storied art form.

<img src="https://images.squarespace-cdn.com/content/v1/54d00072e4b0c38f7e184ee0/1453652236343-9AG7DI650WRWO4D75IS8/ke17ZwdGBToddI8pDm48kLzxjX0ewCOP-k4yiI1x\_sl7gQa3H78H3Y0txjaiv\_0fDoOvxcdMmMKkDsyUqMSsMWxHk725yiiHCCLfrh8O1z4YTzHvnKhyp6Da-NYroOW3ZGjoBKy3azqku80C789l0jG2lbcDYBOeMi4OFSYem8B3JXwsqs3UDR6lQFnfsK5UTt71u4\_-9u7ALFvJimN92w/https%3A%2F%2Fcommons.wikimedia.org%2Fwiki%2FFile%253AAdolph\_Menzel\_-\_Fl%25C3%25B6tenkonzert\_Friedrichs\_des\_Gro%25C3%259Fen\_in\_Sanssouci\_-\_Google\_Art\_Project.jpg" alt="Source: Wikimedia Commons" />

Source: Wikimedia Commons

You're excited by recent advances to improve the sonority of instruments – after all, the violin's [F-hole](https://en.wikipedia.org/wiki/F-hole) was only perfected in your lifetime. You're also intrigued by the strange note systems described by explorers to the Far Orient, completely unlike the 12-note chromatic scale you learned in school. You've even heard of the complex rhythms practiced in Africa, far more intricate than the lock-step percussion of standard European fare.

So your first day on the job, you approach your [Kapellmeister](https://en.wikipedia.org/wiki/Kapellmeister) and excitedly ask: what new techniques are being developed in the court of today? What musical innovations will amaze and delight opera-goers in the coming years?

The master sighs and places a hand on your shoulder. The landscape of modern composition, he explains, is an arduous one. The raging debate among composers today is on the proper use of sheet music.

"You see," he says, "we realized some time ago that annotations like *Pizzicato* and *Allegro* are too difficult for non-Italian speakers to understand. Furthermore, they clutter up the page, and they take too much time for the musicians to sight-read. So we are gradually replacing them with symbols that explain the same concept."

<img src="https://images.squarespace-cdn.com/content/v1/54d00072e4b0c38f7e184ee0/1453743297981-LH85OF31WDJ3CH5FMHWR/ke17ZwdGBToddI8pDm48kK\_WYW-CmAZvywtR8MY4S497gQa3H78H3Y0txjaiv\_0fDoOvxcdMmMKkDsyUqMSsMWxHk725yiiHCCLfrh8O1z4YTzHvnKhyp6Da-NYroOW3ZGjoBKy3azqku80C789l0hveExjbswnAj1UrRPScjfBxETrsn4xj0\_v2LvZpRX0W9-2nrtx2XF86c3Na1SQeDw/image-asset.jpeg" alt="" />

"Ah," you say, a bit surprised at the dull subject matter. "That does make sense. Musicians should be able to perform at their peak potential, in order to better please audiences."

"Yes yes," the master waves his hand dismissively. "But unfortunately this creates an additional problem, which is that our existing scores need to be laboriously migrated over to the new system. Furthermore, not all composers agree on which system to use, so there are many competing and incompatible standards."

"That would certainly create problems for the musicians!" you admit. "And the composers as well."

"Indeed," the master says. "It also causes headaches with the newly-invented musical typewriter. Every year, there are updates to the typewriter design, and every year composers need to learn the new system, or hold steadfastly to their familiar one." He shakes his head. "As a community, we are suffering from tool fatigue."

"But what about the music?" you say impatiently, despite yourself. "All of this is well and good for composers, but how are we improving the experience for audiences? They don't care a bit how we create the music, only how it sounds."

"My child," the master says with a smile, "you have much to learn. The more efficiently we can *create* our music, the better it will be in the end for audiences. The most important thing is to learn the *purest* system for note-writing, which I will deign to teach you. Here, let me show you my typewriter, which is of course the most advanced on the market today…"

## Composing JavaScript

The analogy is a bit labored, but this is how I feel about web development today.

Every day, I'm bombarded by tweets and articles touting one framework over another, always in terms of the tooling and the developer experience, with little regard for the *user* experience. From reading Hacker News or EchoJS, you'd think the most important parts of JavaScript were the tools, patterns, and philosophies. The fact that someone, somewhere, is actually interacting with pixels on a screen feels like a side effect.

Of course, [tool fatigue](https://medium.com/@ericclemmons/javascript-fatigue-48d4011b6fc4) is a well-worn topic, but I'm not just talking about that. I'm also talking about the endless discussion – especially in vogue in the React/Redux community – about "action creators" and "subreducers" and "sagas" and abstractions that are so complex you need [a cartoon version](https://code-cartoons.com/a-cartoon-intro-to-redux-3afb775501a6) to understand it. All of this mental overhead is deemed necessary to keep our app code from growing into an unreadable spaghetti mess (or so it's argued). [\[1\]](#footnotes)

Then of course, there are the competitor frameworks that [boast about their own ideological purity](http://staltz.com/why-react-redux-is-an-inferior-paradigm.html) compared to the prevailing model. The more I read, the more it starts to sound like a game of intellectual one-upsmanship: "Oh, I only use *immutable data*." "Oh, I only use *pure functions*." "Oh, I only use *organic shade-grown npm modules* ." With all this highfalutin terminology, I can't tell sometimes if I'm reading about a JavaScript framework or the latest juice cleanse.

## Forgetting about the user

Of course, tools and patterns are important, and we should be talking about them. Especially when working with junior developers, it's good to enforce best practices and teach difficult concepts. None of this discussion would bug me, except that it seems like the experience of the users (you know, those weird non-programmers who actually *use* your app) is getting lost in the shuffle.

Paul Lewis has already written about this in ["The Cost of Frameworks,"](https://aerotwist.com/blog/the-cost-of-frameworks/) but it bears repeating. Your user does not give a damn how you built your app; they only care that 1) it works, and 2) it works quickly. I'm disappointed that so much of this topic gets shoved under the umbrella of "performance," and that we have to hammer home the point that ["perf matters"](https://twitter.com/search?q=%23perfmatters), because in fact "performance" is just the closest translation we have in developer-speak to what users would call "good experience." [\[2\]](#footnotes)

I spend a lot of time harping on performance – in my work at Squarespace, at JavaScript meetups, and in my blog – and it never ceases to amaze me that "performance" is such a dark art to so many developers. The truth is that you can discover most performance problems by simply testing on slower hardware.

For instance, I'm shocked at how many developers (newbies and experts alike) are still using CSS `top` and `left` rather than `transform` to animate movement, even though the framerate difference is [crystal-clear](https://youtu.be/zrkCr1FThn0) once you test on something other than an 8-core MacBook Pro. (My personal favorite workhorses are a janky 2011-era [Galaxy Nexus](http://amzn.com/B005ZEF01A) and a cheap [Acer laptop](http://amzn.com/B00P6FM23W).)

Note that I'm not saying newbies should feel guilty for making this mistake; `top`/`left` is much more intuitive than `transform`. However, that's exactly why we (the experts) should be making an effort to learn and pass on these sorts of optimization techniques to them, rather than the petty minutia of the framework-of-the-week.

## A lost art

It'd be understandable if performance tricks like `transform` were arcane due to their novelty, but a lot of it is well-established stuff that seems to be willfully ignored. For instance, offline tools like IndexedDB, WebSQL, and AppCache have been around for years ([2010](https://hacks.mozilla.org/2010/06/beyond-html5-database-apis-and-the-road-to-indexeddb/comment-page-1/), [2007](https://webkit.org/blog/126/webkit-does-html5-client-side-database-storage/), and [2009](http://googlecode.blogspot.com/2009/04/gmail-for-mobile-html5-series-using.html) respectively), yet most web developers I talk to are barely aware of them. The same goes for WebWorkers, which have made parallelism possible [since 2010](http://www.html5rocks.com/en/tutorials/workers/basics/), though you wouldn't know it from browsing most web sites.

These are technologies that can *vastly* improve the user experience of your webapp, either by reducing server round-trips (offline) or increasing UI responsiveness (parallelism). And yet it feels like many of us are more eager to learn about some hot new framework that improves our own *developer* experience, rather than existing technologies that empower users.

If I sound bitter about the lack of progress in these areas, it's because I am. Just last week I published [pseudo-worker](https://www.npmjs.com/package/pseudo-worker), a WebWorker polyfill, because I could not find a decent one anywhere on npm or Github. (Yes, for WebWorkers: a six-year-old technology!) I've also spent the last few years working on [PouchDB](http://pouchdb.com) and related IndexedDB/WebSQL projects, and the most surprising part of my experience has been realizing just how little work is being done in this field. Often I find myself [filing bugs on browsers](https://gist.github.com/nolanlawson/11672431f0d219b96335) for implementation flaws that should have been uncovered years ago, if people were actually using this stuff.

I keep waiting for web developers to "discover" these techniques (as [Ajax was "discovered"](http://adaptivepath.org/ideas/ajax-new-approach-web-applications/) in 2005), but I barely heard a peep from the blogosphere this year, except in my own niche circles. Instead, one of the most heralded web technologies of 2015 was [hot loading](http://gaearon.github.io/react-hot-loader/), a tool that allows you to ignore the slow loading time of your app in order to increase your own developer efficiency. If there's a better example of a tool that privileges developers at the expense of users, I can't think of one.

## Looking forward

There's still hope that we can reverse this trend. I am encouraged by the burgeoning excitement over [ServiceWorkers](https://ponyfoo.com/articles/serviceworker-revolution), and the fact that my ["Introducing Pokedex.org"](http://www.pocketjavascript.com/blog/2015/11/23/introducing-pokedex-org) post actually drew some attention to the potential of [progressive webapps](https://medium.com/@slightlylate/progressive-apps-escaping-tabs-without-losing-our-soul-3b93a8561955). I'm even more excited that Malte Ubl, the head of the [AMP project](https://www.ampproject.org) at Google, has declared 2016 to be [the year of concurrency on the web](https://medium.com/@cramforce/2016-will-be-the-year-of-concurrency-on-the-web-c39b1e99b30f).

These are all efforts to improve the experience of web users, even if they add a bit of complexity to our app code and build processes. And in fact, the two aren't mutually exclusive; we can build tools that help both developers and users – projects like [Hoodie](http://hood.ie/) and [UpUp](https://www.talater.com/upup/) are making great strides in this area. I also love the performance feats that React and Ember (especially [Glimmer](http://emberjs.com/blog/2015/05/05/glimmer-merging.html)) have managed to pull off, which are being pushed even further by [Angular 2](https://docs.google.com/document/d/1M9FmT05Q6qpsjgvH1XvCm840yn2eWEg0PMskSQz7k4E).

Some of these problems, though, can only be improved with education. Developers need to make more of an effort to learn the web platform itself, and not rely on some framework's abstraction of it. Luckily, there are plenty of folks doing great work to increase developer awareness around topics of performance and user experience, and to show what the web is capable of today: [Paul Lewis](https://youtu.be/obtCN3Goaw4?list=PLNYkxOF6rcIBz9ACEQRmO9Lw8PW7vn0lr), [Rachel Nabors](https://youtu.be/GxOq1bnlZXk), [Tom Dale](https://youtu.be/puOrC7cfjRI), [Jason Teplitz](https://youtu.be/Kz_zKXiNGSE), and [Henrik Joreteg](https://youtu.be/okk0BGV9oY0) are some names that spring to mind. (All of the above links are videos, and all of them are worth watching!)

Overall, I'm hoping that web developers in 2016 will spend a bit less time navel-gazing over our processes, philosophies, and abstractions. These things are important for the day-to-day task of building and maintaining code, but they shouldn't distract us from the needs of the people we ultimately serve: the users.

#### Footnotes

***\[1\]** I meant no offense to Dan Abramov, Lin Clark, André Staltz, or anybody else trying to make our applications' wiring easier to manage. This stuff is hard-hitting, computer-sciency work, and fun to think about! It's just not the whole story, which is why I wrote this piece.*

***\[2\]** "Design" is another good translation, although I think design and performance are inextricably linked (e.g. 60FPS animations, smooth transitions between related screens, etc.).*

*Thanks to Nick Colley, Jan Lehnardt, André Miranda, and Garren Smith for feedback on a draft of this blog post.*

#### Update 26/Jan/2016

I was super harsh on React, Redux, and Cycle.js folks in this post, and got [rightfully called out for it](https://twitter.com/dan_abramov/status/691976015594311680). So I should clarify: I know plenty of folks in those communities do care about performance, and that the end-user experience [motivated a lot of these tools in the first place](https://medium.com/swlh/the-case-for-flux-379b7d1982c6).

React pioneered things like isomorphic rendering, which is absolutely *huge* for performance. Webpack made code-splitting easier. All of these things are awesome! I even think hot-loading is nifty. (As long as you're still sure to test the actual load time of your app.)

We all want to write great software. That's why we got into this business in the first place. My point was just that I don't feel like I'm hearing nearly enough discussions about the capabilities of the web platform, and how webapps can be pushed in interesting directions.

It sometimes feels like we've concluded there are no more worlds to conquer, and that we just need to figure out how to perfect the process of writing websites as they were written in ~2012. That would be a shame. There are some wild possibilities in the web today (not just around offline and parallelism; Jenn Simmons has [an awesome talk](https://youtu.be/ZNpn7FBp_9U) about CSS layouts that nobody's using). I just don't want our tools and abstractions to distract us from that.
