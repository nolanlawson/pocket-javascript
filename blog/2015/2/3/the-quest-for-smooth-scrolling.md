---
layout: layouts/post.njk
title: "The quest for smooth scrolling"
date: 2015-02-16T16:45:20.000Z
---

Back in 2012, when Facebook famously ditched HTML5 for fully native apps, [the main problem they cited](https://lists.w3.org/Archives/Public/public-coremob/2012Sep/0021.html) was a lack of smooth scrolling:

> “This is one of our most important issues. It’s typically a problem on the newsfeed and on Timeline, which use infinite scrolling. \[...\] Currently, we do all of the scrolling using JS, as other options were not fast enough (because of implementation issues).”
>
> — Tobie Langel

It should be clear why this was a dealbreaker for Facebook. If you want people to stay glued to their timelines, then you need a scrolling list that doesn't break a sweat. Otherwise the user's attention starts to drift pretty fast.

This affects more than just Facebook, though. As any mobile developer knows, the "ginormous scrolling list" is a common UI pattern across a wide variety of apps. Even if you're not Facebook, you probably have some kind of list – of notes, tasks, beers, Pokémon, whatever – that figures heavily into your app's presentation.

Recently Flipboard caused quite a stir by unveiling their [scrolling list implementation](http://engineering.flipboard.com/2015/02/mobile-web/), which renders to canvas in order to achieve 60 FPS. My reaction was: "neat!" The reaction of the web intelligentsia [was](http://www.broken-links.com/2015/02/13/flipboard-com-idealism-vs-pragmatism/) [a](http://farukat.es/journal/2015/02/708-how-flipboard-chose-form-over-function-their-web-version) [bit](https://twitter.com/jaffathecake/status/566129048972431360) [more](https://twitter.com/Charlotteis/status/565821393489891328) [mixed](https://twitter.com/codepo8/status/566572801445097473).

> Achieve 60 FPS easily by rendering your sites with node.js and imagemagick as static images!
>
> — Christian Heilmann (@codepo8) [February 13, 2015](https://twitter.com/codepo8/status/566199581416112128)

As an Android developer who only recently learned the web stack, I can see where Flipboard is coming from. I've heard for years that HTML5 was the equal of native platforms, and yet every time I've tried to write a PhoneGap or AppCache-powered web app, I've always had fun, but ended up feeling a little disappointed.

For instance, I recently built a prototype app using [Ionic](http://ionicframework.com/). Overall I found it to be a great developer experience, but getting a scrolling list to perform at 60 FPS [turned out to be impossible](http://nolanlawson.s3.amazonaws.com/www/ionic_list_perf/index.html). And this was despite the admirable efforts of the Ionic team, who developed [some very clever tricks](http://ionicframework.com/blog/collection-repeat/) to achieve even 45-50 FPS.

So the Flipboard approach starts to look pretty attractive by comparison. The cry of the web advocates, however, is that we shouldn't sacrifice accessibility, copy-paste, "find in page," "open in new tab," or other classic browser features at the altar of 60 FPS.

My point of comparison, however, is with native apps. And when, exactly, was the last time you used a native app that let you "find in page"? Or even copy-paste? Sometimes you can "share," but such functionality is usually hobbled in comparison to the web experience.

Native apps have long abandoned the kind of built-in DOM features that web advocates swoon over (with the exception of accessibility, which works out-of-the-box with TextViews). And yet, native apps are the [reigning champions](http://cdixon.org/2014/04/07/the-decline-of-the-mobile-web/) of user attention, especially when it comes to "ginormous scrolling list"-style apps. That speaks volumes about what people really value when they're flicking through tweets at the bus stop.

The truth is that for a largely consumptive experience – which is what infinite scrolling embodies – 60 FPS is much more valuable than the interactive features like "find in page" or copy-paste. Admittedly, accessibility is harder to justify throwing under the bus, which is why even Flipboard acknowledged that [they need to fix it](https://github.com/flipboard/react-canvas#accessibility).

But amidst all the hand-wringing from web apologists, as well as [some gleeful jabs from the web's detractors](http://daringfireball.net/linked/2015/02/10/flipboard-web), I found the most insightful response to the Flipboard fiasco to be Jacob Rossi's:

> Apple's "animation triggers" proposal would enable the [@flipboard](https://twitter.com/Flipboard) scroll UX at 60FPS w/o throwing out accessibility [http://t.co/FDEjTMb6pV](http://t.co/FDEjTMb6pV)
>
> — Jacob Rossi (@jacobrossi) [February 11, 2015](https://twitter.com/jacobrossi/status/565348172793667585)

In other words, the web can solve the problem of slow scrolling in the same way that it solved the problem of [slow animations](http://www.pocketjavascript.com/blog/2015/2/2/smooth-animations-in-css). Just as CSS animations allowed us to achieve native-level performance by moving rendering off the main thread (where it blocks the DOM) and onto a background thread or the GPU (where it hums along nicely), the [animation triggers proposal](https://lists.w3.org/Archives/Public/www-style/2014Sep/0135.html) would move the responsibility for scrolling squarely to the browser.

Trying to re-implement the browser's scrolling in JavaScript, as Ionic and other frameworks do, is simply a non-starter if we want to achieve 60 FPS. JavaScript blocks the DOM, and as Flipboard says, "if you touch the DOM in any way during \[JavaScript\] animation, you’ve already blown through your 16ms frame budget."

Flipboard's solution was to replace the DOM with GPU-powered canvas. But the real solution is to replace JavaScript scrolling with GPU-powered scrolling.

For the time being, though, JavaScript scrolling is the best we've got, unless we want to dip into canvas or WebGL experiments like Flipboard's. Personally I think their approach is pretty exciting, especially if it spurs browser vendors to finally solve the sorts of scrolling problems that Facebook identified way back in 2012.

Of course, now Facebook has an even bolder experiment in [React Native](http://blog.reactnative.com/introducing-react-native/), based on the presumption that, even at 60 FPS, WebViews just "feel" wrong. But that will have to wait for a future blog post.
