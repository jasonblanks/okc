okc
===

OKC hacker scripts, data, etc

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
