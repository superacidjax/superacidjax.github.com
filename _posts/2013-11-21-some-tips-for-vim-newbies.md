---
layout: post
title: "Some Tips for Vim Newbies"
description: "Some Tips for Vim Newbies"
category: "Vim"
tags: [vim, learning, beginners]
---
{% include JB/setup %}

As someone who tended to revert to Sublime when faced with a particularly time-sensitive editing task, learning Vim tended to go more slowly than I would have liked.

However, over the past two weeks, I've refused to allow myself to open Sublime at all, even when on a tight feature-release deadline for work. So here's a suggested strategy if you find yourself not learning as quickly as you would like.

Each morning, before you start work, your goal should be to pick up one single new thing. For me yesterday it was learning how to quickly open test file/app files in a split. So if I was in a controller, being able to instantly open the functional test in a split was a big boost. The day before, I learned about indenting.. etc. The book [Practical Vim](http://pragprog.com/book/dnvim/practical-vim) from Pragmatic is really good (you can work through it in small daily chunks.)

Then work that day using ONLY vim. Do not open Sublime or TextMate. You will be slower. You will get frustrated. That's ok. Throughout the day, use that day's technique every possible chance you get. If you get to a point where you absolutely just can't accomplish it in Vim, then look up the relevant technique. Yes, that'll slow you down for the few minutes it will take you, but you'll end up owning that technique afterwards, because you were forced to use it, and it was highly relevant.

I'm not a vim expert yet, but I've improved more in the past few weeks than I had after a year of using Vim to "learn" and then switching to Sublime to "work." The key is combining learning as you work.

This is probably common sense, but it's very effective. If you want to be even more hardcore, just delete Sublime completely. Then it would take you 5-10 minutes just to download and reinstall it that the effort wouldn't be worth it and you'll force your way through vim instead. I personally didn't do this simply because in my job I occasionally have to pair with people who don't use vim.

I also recommend Tmux and using Vim in the terminal instead of using MacVim. The reason is personal for me -- I prefer to have one screen for everything, meaning running iTerm in full screen with my vim in a vertical split over the top 80% of the screen with my command-line underneath. (Like an upside down T.) The advantage of this is I can switch almost instantly between my console/command line and vim without having to switch apps. That's just my way of working, so it might not apply to everyone, but MacVim is, to me, another app to switch into and out of, so the slight delay (and loss of mental "flow" in doing that dozens of times and hour) is costly. The very best book on Tmux is also from Pragmatic and can be found [here](http://pragprog.com/book/bhtmux/tmux).

This might not help everyone, but it worked for me. Good luck fellow newbies! We will win vim, and subsequently [win the internet](http://knowyourmeme.com/memes/you-win-the-internet).