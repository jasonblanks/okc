OKCupid hacker scripts, data, etc
===

Tools for crawling OKCupid for users and their profiles.
TODO(anyone): Pull users' answers to 'Questions' as well (the multiple choice ones that they use for match percentages)
TODO(anyone): Clean up FetchProfiles.py file to use the 'requests' library and generally make it sleeker.

--- Fun Links ---
Because I'm not the only one who has thought of this:
http://www.wired.com/wiredscience/2014/01/how-to-hack-okcupid/

--- Pulling Data ---

* FindUsers.py
This will find all the usernames of current OKC users in the target location.
Results are stored in the Usernames table of the commandline-specified database.
This was recently updated and should be pretty smooth.
* FetchProfiles.py
This takes the usernames from the database produced above, and pull the profiles one at a time.
Results are stored in the Profiles table of the commandline-specified database.
This is older code and may need some help to be used.

--- Analyzing Data ---
* AnalyzeProfiles.py
Has tools to load profiles from the database, and convert each into a Profile object for easy access. It also cleans up and strips the HTML from the 'essay' fields so they can be read and processed as plain text
* ReadingLevel.py
Tools for determining the reading level of a chunk of text, as well as some useful statistics about a blob (number of words, sentences, syllables, etc). Useful function is TextScores(some_text) which makes an object with a number of useful fields.

--- Other files ---
* cmudict.0.7a.txt
This is a dictionary mapping words to their numbers of syllables. I pulled it from some CMU page on the interwebs, but I forget where. It is parsed in reading_level.py, which adds some extra logic to guess the number of syllables for unknown words.
