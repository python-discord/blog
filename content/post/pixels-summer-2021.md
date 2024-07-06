---
title: "Python Discord Pixels: Summer 2021"
description: "Python Discord Pixels was our collaborative canvas event that we held between 25th May to the 14th June 2021 providing a beginner-friendly API to paint pixels on a virtual canvas."
author: Joe Banks, Chris Lovering
date: 2021-07-18
featured_image: /post/pixels-summer-2021/cover.png
---

## What was Pixels?

Python Discord Pixels was our collaborative canvas event that we held between
25th May to the 14th June 2021 providing a beginner-friendly API to paint
pixels on a virtual canvas.

We built an API with FastAPI, Redis and PostgreSQL that would allow users to
paint a single pixel on a virtual canvas, with rate limits so they could only
do so a few times a minute.

Painted pixels would then be returned to the API as well as posted every minute
into a channel in our Discord server so folks could keep up with the current
state of the canvas.

The final state of the Pixels canvas:
![](./final-state.png)

## Project motives

The main goal for this project was for it to be a learning tool for those that
may not have ever interacted with an API before. By adding in a fun twist,
where users could see their actions reflected in an image displayed on our
server, we found users of all backgrounds participated.

By giving participants a space to discuss implementation within our server, we
found that many of the more experienced users mentored those who were having
difficulties getting started.

Many times throughout the event users were overjoyed when their first ever API
project finally worked, and they could see their first pixel on our canvas!

## Participation statistics

Across the 20 days that the event ran we saw 2,395,667 total pixel placements
from 414 distinct users.

![](./participation-statistics.svg)

## A look at the pixels

You can see a timelapse [on our YouTube channel](https://www.youtube.com/watch?v=obC-l9JWx2M).

## Colours

Of the 2,395,667 placed pixels, there were 119,992 unique colours used, the
most popular being shown below:

![](./most-popular-colors.png)

## Active Hours

The most active hour for placing pixels was 16:00 UTC with 115,312 pixels being
placed between 16:00–17:00 across the event.

![](./active-hours.png)

## Users

The top 10 users by pixel placement are as follows:

![](./top-10-users.svg)

## Pixels Data

We've made available the whole pixels dataset, with the majority of placed
pixels (pixels from banned users were not included).

You can download the data at [this
link](https://cdn.discordapp.com/attachments/563594791770914816/858706547110838292/history.csv.gz?ref=blog.pythondiscord.com)
or [view it on
Kaggle](https://www.kaggle.com/joebanks/python-discord-pixels?ref=blog.pythondiscord.com).


## Source code

We open sourced Pixels during the event so people could understand how the API
worked, we'll be writing a subsequent blog post to talk about the engineering
behind Pixels, and how we use tools such as PostgreSQL, Redis and more to
ensure reads and writes are as fast as they can be.

You can find some of the documentation we used during the event
[here](https://pythondiscord.notion.site/Python-Discord-Pixels-99e3058855a94f6cab69853d6e2c355b?ref=blog.pythondiscord.com).
The repository can be found at
[python-discord/pixels](https://github.com/python-discord/pixels/?ref=blog.pythondiscord.com).

## Future of Pixels

Python Discord Pixels was a huge success, and outperformed our expectations in
terms of user participation. Due to the success we plan to bring back Pixels in
the future with different twists. Make sure to stay focused on our
#announcements channel in
[Discord](https://discord.gg/python?ref=blog.pythondiscord.com) and [our
Twitter](https://twitter.com/PythonDiscord?ref=blog.pythondiscord.com) to stay
up to date with future event announcements.
