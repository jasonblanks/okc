OKCupid hacker scripts, data, etc
===

Tools for crawling OKCupid for users and their profiles.

Pulling Data
---
* FindUsers.py - This will find all the usernames (with age and gender) of current OKC users in the target location, dumping out a csv.
* FetchProfiles.py - This takes the usernames csv from FindUsers.py and pulls the profiles one at a time, writing to a new csv.

Analyzing Data
---
* ReadingLevel.py
Tools for determining the reading level of a chunk of text, as well as some useful statistics about a blob (number of words, sentences, syllables, etc). I have used it to compute reading levels for essay responses, plot them, etc, though I don't have any of that code checked in.
* cmudict.0.7a.txt - Used by ReadingLevel.py, this is a dictionary mapping words to their numbers of syllables. I pulled it from some CMU page on the interwebs, but I forget where.
* 2012-06-30_profiles.csv.zip
.zip file of .csv file containing profile information (from their public profiles on 2012/06/30) for n=59,946 users who 
	* were members on 2012/06/26
	* were living within 25 miles of San Francisco
	* were online in the last year
	* had at least one photo in their profile
* Analysis.R
R script to read in profiles.20120630.csv and 
	* produce a mosaicplot cross-classifying gender and sexual orientation
	* produce a histogram of heights split by gender

Fun Links
---
Because I'm not the only one who has tried this kind of thing:
* http://www.wired.com/wiredscience/2014/01/how-to-hack-okcupid/
* http://jonmillward.com/blog/attraction-dating/cupid-on-trial-a-4-month-online-dating-experiment/

TODOs (anyone)
---
* Pull users' answers to 'Questions' as well (the multiple choice ones that they use for match percentages)
