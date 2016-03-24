---
inFeed: true
hasPage: true
inNav: false
inLanguage: null
starred: false
keywords: []
description: 'For Christmas, my wife and I gave our family the gift of a puzzle to solve.'
datePublished: '2016-03-24T00:00:59.774Z'
dateModified: '2016-03-24T00:00:34.937Z'
title: ''
author: []
authors: []
publisher:
  name: null
  domain: null
  url: null
  favicon: null
sourcePath: _posts/2016-03-24-for-christmas-my-wife-and-i-gave-our-family-the-gift-of-a-p.md
published: true
url: for-christmas-my-wife-and-i-gave-our-family-the-gift-of-a-p/index.html
_type: Article

---
**For Christmas, my wife and I gave our family the gift of a puzzle to solve.**

Everyone in the family received a similar handmade Christmas card from us, staggered throughout Christmas Eve and Day.
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/b9b5a34f-ef29-4ef2-9082-645ace2ec7fc.jpg)

Prior to Christmas Eve, we had been keeping the name of our upcoming baby a state secret, which of course drove many in our family crazy. So right off the bat, this Christmas card was huge news: they suddenly knew how many letters the baby's name had. It only took a few minutes for the most puzzle-minded people in the room to figure out the next part: the cards contained partially-played games of Hangman. Seconds later, I heard the first instance of a question I would hear several more times before the puzzle was solved: "What letters did you get??"

By combining the 9 cards that different groups of people got, the family would have the information they needed to figure out the baby's name. The day after Christmas, I got to experience the joy of being on an email thread with my entire family, each of them putting forth effort to solve the puzzle. The engineers in the family immediately found data from the Social Security Administration of the most common names in the US over the past 100 years, and used that list to programmatically start narrowing down the list. Some time was spent calling up remote family members to verify their letters. 41 emails later, the family had what they believed to be the most probable name based on the list, and they got it right: my soon-to-be-born son's name is Finn.
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/8dd8f019-39fb-4567-9653-e00245cfd768.png)

As a programmer, creating the puzzle was great fun. I wrote a Node.js program to come up with combinations of letters in the alphabet that could be excluded using similar SSA name data that my family ended up using. The goal of the puzzle design was to make it so that no single card would eliminate too many possibilities. Once I figured out the total list of letters I wanted to give to the family (my list ended up being 19 letters, out of the 23 I could have given them) I wrote a second script that checked to ensure that no combination of cards short of the full set could solve the puzzle. It was a fun hastily-thrown-together programming exercise that I am certain I approached from the entirely wrong direction, but it worked! I [tossed the code up on GitHub][0], even though it is a horrible mess of a Node.js script that nobody should ever use.

_[Source code on GitHub][0]_

Anyway, the whole thing was a giant success. If you're looking for a fun way to reveal the name of your baby to family, and have a family full of puzzle-minded people, consider a hangman puzzle!

[0]: https://github.com/OverloadUT/baby-name-puzzle