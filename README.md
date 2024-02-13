Facilitating the search of publicly available databases of academics accused of misconduct, with a focus on sexual misconduct.

With many thanks to the diligant team at ASMD who have spent hundreds of hours collecting the database: <ins>https://academic-sexual-misconduct-database.org</ins>

By using the package, users agree to the following:

I understand that this package provides a probabilistic match between names found in my .bib file and publicly available lists of individuals accused of, or convicted of sexual harassment and/or other academic misconduct. It is my responsibility to verify the information provided in these databases, to ensure that the match is accurate, and I am entirely responsible for any action I take, including choosing not to cite the person matched, as a result of learning of the match. I acknowledge that the package authors guarantee neither the accuracy of the lists, nor the accuracy of the match between .bib files and the list. I am aware that the lists can be found here: <ins>https://academic-sexual-misconduct-database.org</ins>


**Getting Started**
tldr; creeps is currently only available on overleaf. A minimum working example is here: https://www.overleaf.com/read/hnkxprbnnjfv#db093a

**Expected behaviour**

If you do not cite someone who is matched to an individual in the database, **nothing will happen, this is expected**. If an author is matched to someone in the database, a message will be printed, showing you who it is, which articles you're citing in which they're an author, and a link to the case providing details on why they were sanctioned by their institution.


1. In your overleaf project, create a new file, select 'From External URL', copy and paste the following url: https://raw.githubusercontent.com/alistaircameron/creeps/main/asmd.csv

NB. by default, the file created will be named "asmd.csv". DO NOT CHANGE THIS!

2. Repeat for the following url: https://raw.githubusercontent.com/alistaircameron/creeps/main/creeps.sty 

NB. by default, the file created will be named "creeps.sty". DO NOT CHANGE THIS!

3. Load creeps as you would any other package (`\usepackage{creeps}`), then scroll to the place in your .tex file where you put your bibliography. In the line above this (or, wherever you want the names of the offenders to be displayed), put the following: `\creeps{path_to_my_bibfile}`

`\creeps{}` takes two optional arguments, the first is a comma-separated string of .bib entries you wish to exclude from being flagged. Set the second to 'false' if you do not want a reminder to update your link to the offenders database if you have not done so in the preceding 100 days. Options included, it looks like: `\creeps{mybibfile}[exception1, exception2][false]`

**Roadmap**

Unfortunately, creeps is currently only available on overleaf. A package is in the works which will be available for all users (creeps uses a python script to scrape a publicly available database of convicted offenders. I am currently working on a parsimonious, offline version with a focus on ease of use. For those comfortable incorporating python in their latex lives, the .py file is available in this repository.)