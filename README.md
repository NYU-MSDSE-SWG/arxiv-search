# arXiv Author Search
------
This is a python program to search arXiv’s paper given an author. 
It can also do institution verification and subject verification to find the paper published by 
this author with a specific affiliation.

# Dependencies
feedparser, urllib, numpy, pandas, pyprind, pdfminer

# Usage
If we want to find papers authored by Yann Lecun, we can use author = arxiv(Lecun_Yann) to initialize. 
Then use author.parse() to query arXiv and parse the returned data. 

- author.count: number of papers
- author.arxiv_id: paper’s arxiv id
- author.time: paper’s submission time
- author.title: paper’s title
- author.category: paper’s category
- author.pdf: paper’s pdf link 
- author.subject: subjects of all of author’s papers 
- author.contributor: paper’s contributors

If we also want to find paper by Yann Lecun submitted with affiliation in NYU, we can use 
author.institution_verify(save=False, institution=[‘nyu’, ‘new york university’])
If save=True, it will download all papers and save them to local.

# Note
institution_verify() will download all papers returned by searching query, and please do not use this 
as a robot to get all available papers from arXiv! ‘Indiscriminate automated downloads from arXiv are not premitted’.
See more information about this: http://arxiv.org/help/robots

