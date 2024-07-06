---
title: Advent of Code from a community event organizer's perspective
description: "A look into what went on under the hood to pull off the Python Discord celebration of Advent of Code 2020."
author: "Janine (Kutiekatj9)"
date: 2021-03-24
featured_image: "/post/advent-of-code-from-a-community-event-organizers-perspective/cover.png"
---


## What is Advent of Code?

Advent of Code is one of Python Discord's favorite events that happens each
year. An [Advent
Calendar](https://en.wikipedia.org/wiki/Advent_calendar?ref=blog.pythondiscord.com)
of small programming puzzles that are released each day from December 1st to
December 25th. The puzzles can be solved in any language, although we're
obviously partial to the python solutions. The problems are designed for a
variety of skill sets and skill levels, but it overall it gets harder as it
goes on. If you want to find out more about the event, you can take a look
here: https://adventofcode.com/about

## How Python Discord participates

All of us at Python Discord love Advent of Code. It's a great event that gets
people to learn, improve, and/or flex their coding skills with a community
event. We see a lot of people learn about new ways to accomplish fun and
interesting puzzles. Regex? Vim shortcuts and macros? Brute forcing with
powershell? All different solutions our server members have come up with.

Part of how we engage our server is by having a community leaderboard that can
be viewed in server. It pulls the data from the Advent of Code leaderboard
itself, creates a fun and engaging environment.


## The Curse and Blessing of Server Growth

I stepped into the Event Lead role 3 weeks before December 1st. Not a whole lot
of time, but we've run the event before so the prep shouldn't be too bad. I
spent the first week just getting acquainted with how the previous Advent of
Code was run and reading through any of the feedback we received. I also spent
some time getting familiar with Advent of Code itself! This was the first time
I had ever heard of it, nevermind participated.

Fun fact about Advent of Code: an individual leaderboard has a limit of 200
people. I was curious about how many people we had the previous year. After
some digging in archived channels and pestering our admins, I found out that
the 2019 Python Discord leaderboard had 177 people on it. The server in
December 2019 had 30,000 people in it. At the time of planning the 2020 AoC
event, we had over 100,000 members.

Time for some back-of-the-envelope math! 2019 had 177 participants with 30,000
people. Let's assume the % participation rate (0.0059 participants/server
member) stays the same year to year. From that ratio and applying it with our
current server size, we should expect roughly 590 people who want to join the
Python Discord leaderboard for the 2020 event. Ah, here lies the rub:
leaderboards are capped at 200 people.

## Plan A

I contacted the wonderful Advent of Code organizers to see if we could get an
increase for our leadboard. I asked (2 weeks away from the event) if they could
increase it and unfortunately it wasn't technically feasible at that time.

... Time for Plan B!

## Plan B

It's clear we need multiple leaderboards. One thing the admin team and I agreed
on was that we still wanted one combined leaderboard for the server as a whole.
Having a cohesive and non-fragmented community is important to us, especially
for events that we encourage beginners to join. But we can't get really not
have multiple leaderboards, so the next step was to hack together the
leaderboards into one combined one. We knew we needed to update `@Sir Lancebot`
to grab the information from all the the various leaderboards we have (which
all have different session cookies that are required to access information
through the API), combine it into one leaderboard, and then *re-score the
entire leaderboard*. This has to happen everytime we need an update to the
leaderboard.  (AoC organizers, if you're reading this don't worry! We had a
cooldown for when we would actually query the API.)

Also, we realized we had to do all this a week before the event: code it, test
it, review it, and deploy it. Not a great start for the first event I was
officially leading.

One of our wonderful owners Sebastiaan stayed up late several nights to get the
code working with caches, cooldowns, re-scoring logic, and the actual
displaying of the leaderboard. December 1st, midnight Eastern US time, we saw
our leaderboard go live! Overall the event was a great success. 447 people in
the server completed at least one day and a substantial amount completed all
the puzzles as well. I don't think we would've seen such great engagement
throughout the event without the combined leaderboard. A lot of the
1-hour-after-puzzle-release conversation was comparing positions on the
leaderboard, solutions, and talking about different approaches to the puzzle.


## Takeaways

- You can never start planning too early!
- Advent of Code is a great experience and a great event to help strengthen
  community. Definitely try it out in the future if you haven't.
- Sebastiaan is a fantastic human being who deserves cookies~
- Server growth is awesome, but you've got to be prepared for what that brings.
