---
layout: post
title: The Sound of the Library at Work
excerpt: "Experiments with data sonification and library data"
modified: 7/26/2016, 9:17
tags: [data]
comments: true
category: blog
---

Originally posted as ["The Sound of the Library at Work"](https://library.gwu.edu/scholarly-technology-group/posts/sound-library-work) on the GW Libraries Scholarly Technology Group blog. 


At the Access Conference in Toronto in September 2015, I attended an all-day hackfest on data sonification, led by William Denton of York University and Katie Legere of Queen’s University. Data sonification is the translation of data into sound, much as data visualization transforms data into a graph or image. You can read about the workshop and see some examples of data sonification at [Music, Code and Data: Hackfest and Happening at Access 2015](https://www.miskatonic.org/music/access2015/).

In brief, it was a fast, fun, and practical introduction to both data sonification and the freely available [Sonic Pi](http://sonic-pi.net/) synthesizer software. Everyone who attended made some kind of music using a data file they brought with them or from provided sample files. The fact that we were able to get so far in a day speaks to both the skill of our hackfest leaders and the ease with which you can make sound with Sonic Pi.

I’d like to describe a few experiments, one from this workshop and another more recently, that have me excited about data sonification.

### Music from the circulation desk

I brought to the hackfest a csv file with the number of circulation transactions each day for a year--July through June--created from our Voyager system’s circulation transactions logs. The values ranged from roughly 100-1000. With such a broad range, I chunked up the values into a smaller set from 10-100 corresponding to Sonic Pi’s numbering of notes as on a piano keyboard. However, the pitches were so wildly dispersed, that while it was easy to hear outliers, the arc of activity through the semester was hard to perceive. The notes just didn’t make sense to my ears.

To provide a more listenable-- and I’m hoping, more meaningful--line, I assigned the chunks of values to specific notes in the C major scale, across two octaves. This is a much smaller range than the first version, and the notes feel more coherent, being in the same key. 

Thinking there may be patterns in the volume of activity within the week, I added underlying drum beats to emphasize the first day of each week, Sunday. Finally, lighter beats accompany each note during the semester, underscoring the quiet in library activity during semester breaks.

You can listen to it here:
<iframe frameborder="no" height="150" scrolling="no" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/222953127&amp;auto_play=false&amp;hide_related=false&amp;show_comments=true&amp;show_user=true&amp;show_reposts=false&amp;visual=true" width="100%"></iframe>


##Github beats

More recently, I worked with my colleague Dan Chudnov to make visible to the library staff the activity of our team, the Scholarly Technology Group. The steady work of creating and maintaining software to help our user community often simply looks like us working away on our computers with our heads down. Dan created [a visualization of our team’s work](https://www.youtube.com/watch?v=tCFPp97tw4w) as expressed in commits to our projects’ repositories on Github. We also wondered what our team’s work might sound like.

I focused on one software project, an interface to our catalog data and other APIs for discovery; we call it “Launchpad” internally. It’s something quite a number of us have worked on over the past three years. I started with a file which listed one Github commit per line, including the name of the file changed and the person making the change. I then assigned a pitch to each person on the team, all within the same key, giving the initial project manager (Dan) and current project manager (Michael Cummings) the tonic note to provide some centering. To add a sense of time passing, I added drum beats, with a sound sample for the two major rollouts of Launchpad to our user community.

You can listen to it and watch the supplementary logging within Sonic Pi on [YouTube](https://www.youtube.com/watch?v=_GKkaXPOK78) (best viewed fullscreen):

<iframe allowfullscreen="" frameborder="0" height="400" src="https://www.youtube.com/embed/_GKkaXPOK78" width="600"></iframe>


You can hear how the project started with three core developers, who worked intensively on the project through its first roll-out. Over time, participation broadened to a larger group, and each new person’s entry to the project is audible. It bears acknowledging that we’re hearing only a slice of the activity in the creation of Launchpad; this project had considerable contributions from others who represented end users, participated in testing, wrote documentation, conducted usability testing, and performed analyses to inform feature development.

##A few observations

In each of these experiments, the first few iterations were not pleasant to listen to. I struggled to make sense of the noise, lacking anything to latch onto, the audible equivalent of X and Y axes. A little knowledge of music goes a long way in providing some structure that our ears are trained to recognize: rhythm, key, tempo.

As in creating a visualization, aesthetic choices in sonification can interfere with accuracy. Even in these small experiments, I wrestled with choices that mute, in a sense, aspects of the data and could mislead a listener trying to understand the data. For example, in the Github sonification, I chose to represent the activity across time uniformly, one beat per commit. Obviously, the work was not evenly distributed across three years; the pace and changes in work intensity don’t come across in this sonification. 

When it comes to coding, Sonic Pi was an easy entry point to making music from data, particularly when you don’t have a live orchestra at hand. The tips in William Denton’s blog post about reading csv files helped get me started, along with Sonic Pi’s built-in tutorial. Beyond Sonic Pi, there are many other software and tools to support data sonification; I’d be interested to hear what others have tried and found useful.

I'd also like to explore the growing cross-disciplinary literature on data sonification. Other examples of applying data sonification to library data include [Denton's STAPLR experiment](http://staplr.org/) and Legere's research on using sonification to inform real-time library management decisions. In the end, these pieces were fun to create and made my colleagues’ work apparent in a new way.  There’s something satisfying about hearing your work turned into music.

