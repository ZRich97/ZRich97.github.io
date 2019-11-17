---
layout: post
title:  "The Rap-alyzer"
date:   2019-11-09 11:05:36 -0700
categories: jekyll update
---

<iframe controls='true' type='video/mov' allow="fullscreen" src="https://drive.google.com/file/d/1zhhEbwY7Xur_TFbsBCTmjnYjqGpAqlE1/preview" width="716" height="378"></iframe>

After seeing quite a few 'rhyme scheme analysis' breakdowns such as [this one](https://www.youtube.com/watch?v=k2ah9CtlaEs)
on Instagram, Reddit, and YouTube, I decided to try my hand at automating the process. The result is the aptly named the Rap-alyzer
(or 'Rap Analyzer'). 

The webapp is hosted on AWS. The frontend is written in React (my first foray into web development!) and the backend is a Flask app served using Gunicorn.
Lyrics are scraped using the [Genius API](https://docs.genius.com/) and the rhymes are found using the [CMU Proncouncing Dictionary](http://www.speech.cs.cmu.edu/cgi-bin/cmudict).

While it's a fun toy, it's definitely not perfect. Some future things I'd like to implement are:

- Rhyme groups should be confined to a single verse.
- Genius' lyrics sometimes contain cruft that should be cleaned more thoroughly. 
- The colors used to indicate rhyme groups are randomly generated, making it possible that two groups have the same color. 
- Many rappers bend rhymes using unusual pronounciation (example: [Eminem](https://www.youtube.com/watch?v=lPcR5RVXHMg)). It may be possible to use speech-to-text to more accurately pick up rhymes.

Try it out at [rap.zrich.dev](https://rap.zrich.dev). Thanks!