OKCupid hacker scripts, data, etc
===

Tools for crawling OKCupid for users and their profiles.

Pulling Data
---
* FindUsers.py - This will find all the usernames (with age and gender) of current OKC users in the target location, dumping out a csv. This was recently updated and should be pretty smooth.
* FetchProfiles.py - This takes the usernames csv and pulls the profiles one at a time. This is older code and may need some help to be used.

Analyzing Data
---
* ReadingLevel.py
Tools for determining the reading level of a chunk of text, as well as some useful statistics about a blob (number of words, sentences, syllables, etc). I have used it to compute reading levels for essay responses, plot them, etc, though I don't have any of that code checked in.
* cmudict.0.7a.txt - Used by ReadingLevel.py, this is a dictionary mapping words to their numbers of syllables. I pulled it from some CMU page on the interwebs, but I forget where.

Fun Links
---
Because I'm not the only one who has tried this kind of thing:
* http://www.wired.com/wiredscience/2014/01/how-to-hack-okcupid/
* http://jonmillward.com/blog/attraction-dating/cupid-on-trial-a-4-month-online-dating-experiment/

TODOs (anyone)
---
* Pull users' answers to 'Questions' as well (the multiple choice ones that they use for match percentages)
