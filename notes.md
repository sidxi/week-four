# Quick Links
* 1
* 2
* 3

# New terms, alphabetical order:
* AntConc: A freeware corpus analysis toolkit for concordancing and text analysis (key terms as follows)
  *	Collocates: Clusters show us words which _definitely _appear together in a corpus; collocates show words which are statistically likely to appear together. 
  *	Clusters: This view shows you words which very frequently appear together. 
  *	Concordance: This will show you what’s known as a Keyword in Context view (abbreviated KWIC, more on this in a minute), using the search bar below it. 
  *	Concordance Plot: This will show you a very simple visualization of your KWIC search, where each instance will be represented as a little black line from beginning to end of each file containing the search term. File View: This will show you a full file view for larger context of a result. 
  *	Keyword List: This will show comparisons between two corpora.
  *	Word list: All the words in your corpus. 
*	Corpus analysis: a form of text analysis which allows you to make comparisons between textual objects at a large scale (so-called ‘distant reading’)
*	Imj: a tool for creating a rapid visualization of a corpus of images, so that you can determine whether or not you might like to look into more complex tools for deeper analysis. Imj works in a web browser with your computer’s memory.
*	MALLET: *MAchine Learning for LanguagE Toolkit*; a Java-based package for statistical natural language processing, document classification, clustering, topic modeling, information extraction, and other machine learning applications to text
*	Project (in R): having a ‘project’ in R means that R knows where to look for data, and where to save your work or restore from.
*	set.seed: enables the machine to generate the same sequence of random numbers every time we do these calculations (used for topic modelling in R)
*	Voyant: Voyant Tools is an open-source, web-based application for performing text analysis. It supports scholarly reading and interpretation of texts or corpus, particularly by scholars in the digital humanities, but also by students and the general public. It can be used to analyze online texts or ones uploaded by users
*	Topic modelling: a method for finding and tracing clusters of words (called “topics” in shorthand) in large bodies of texts

# Resources that helped me this week
* https://craftingdh.netlify.app/week/4/instructions/
* https://craftingdh.netlify.app/week/4/excel/
* https://craftingdh.netlify.app/week/4/voyant/
* https://craftingdh.netlify.app/week/4/antconc/
* https://craftingdh.netlify.app/week/4/topic-models/
* https://craftingdh.netlify.app/week/4/bonus/
* https://programminghistorian.org/en/lessons/corpus-analysis-with-antconc
* https://www.laurenceanthony.net/software/antconc/
* http://mallet.cs.umass.edu/
* http://miriamposner.com/blog/very-basic-strategies-for-interpreting-results-from-the-topic-modeling-tool/
* https://stackoverflow.com/questions/39137110/what-does-the-following-object-is-masked-from-packagexxx-mean
* http://www.zachwhalen.net/posts/imj-a-web-based-tool-for-visual-culture-macroanalytics/
* Our class Discord


# Other notes and random thoughts
*	I feel like I need to spend more time with Excel
*	You can already see the “Edinbugh” error before the chart in the count

 insert image here
 
  *	I would fix this error by cleaning my data in OpenRefine – merging Edingbugh with Edinburgh
*	Another mistake I found in the graph is that it only goes up to 150, when Edinburgh goes above 180
*	**_When reviewing data, ask yourself: are my findings an artefact of the data, or of my collection methods?_**
*	(Some of) the R code I created to find more data visualizations:
```r
titles <- table(documents$Newspaper.Title) 
barplot(titles, main="Publication Titles", xlab="Newspaper Titles", ylab="Number of Articles")
```

Insert image here

```r
keywords <- table(documents$Keywords)
barplot(keywords, main="Common Keywords", xlab="Keywords", ylab="Number of Articles")
```

insert image here

_Note: this data visualization is really funny to me, because it’s highly generic_


```r
type <- table(documents$Article.Type)
barplot(keywords, main="Types of Articles", xlab="Article Type", ylab="Number of Articles")
```

Insert image here


_Note: this was also wildly generic (in fact, it’s basically the same graph)_

  *	In terms of patterns – the first one would be worth investigating. The second two, not so much.

*	You can really see how Voyant encourages its users to first take a broad (macro) view and then dig into the (micro) context of the text/document/data being analyzed _through the infrastructure of the site_ (word cloud (& other macro visualization tools) AND being able to quickly click to see all the instances of a word in context in your bottom right panel)
  *	“the pleasure of seeing text differently” – what a great quote from Stefan Sinclair
  *	Corpus ID: fb23e8e883a177174bd134553d41a0c5
    *	Full URL: https://voyant-tools.org/?corpus=fb23e8e883a177174bd134553d41a0c5
  *	Entering into a dialogue with the text – context: 
    *	History is a “composite of the sources and not merely a retelling of any one of them” (Whitepaper p. 3 – https://rrchnm.org/wordpress/wp-content/uploads/2017/11/digital-history-and-argument.RRCHNM.pdf)
*	Ask yourself (re: Voyant)
  *	What is this about? What words would I expect to see as describing the text?
  *	What does this text say about something that matters to me like “friendship”?
  *	What words in the Cirrus word cloud make sense, and what words are anomalous?
  *	How does the language of the text change over the span of the text? Are some words more important in the beginning and some at the end? Could there be framing words?
* Some words in the Voyant exercise:
  *	South
Insert image

    * HTML for south: 
<!--	Exported from Voyant Tools (voyant-tools.org).
The iframe src attribute below uses a relative protocol to better function with both http and https sites, but if you're embedding this into a local web page (file protocol) you should add an explicit protocol (https if you're using voyant-tools.org, otherwise it depends on this server. Feel free to change the height and width values or other styling below: -->
<iframe style='width: 424px; height: 296px;' src='https://voyant-tools.org/tool/Trends/?query=south&corpus=fb23e8e883a177174bd134553d41a0c5'></iframe>

    *	There seems to be a major increase in the importance of “New South Wales”
  *	Indians
    *	Clustered preoccupation with “Indians”
Insert image
    *	HTML for Indians: 
<!--	Exported from Voyant Tools (voyant-tools.org).
The iframe src attribute below uses a relative protocol to better function with both http and https sites, but if you're embedding this into a local web page (file protocol) you should add an explicit protocol (https if you're using voyant-tools.org, otherwise it depends on this server. Feel free to change the height and width values or other styling below: -->
<iframe style='width: 424px; height: 296px;' src='https://voyant-tools.org/tool/Trends/?query=indians&corpus=fb23e8e883a177174bd134553d41a0c5'></iframe>

*	My own Voyant exercise: Kentucky Newspapers in 1921 with the words “derby winner” on the page: https://voyant-tools.org/?corpus=e07880a44bb35ae172b2653ccf75d4a7
  * I had some issue trying to grab data for this, so eventually I just pasted the plain text URLs into Voyant. When I have the time, I'd like to go back and try and figure out what I've been missing
  *	Unrelated, but I also found this neat article while I was trying to narrow down what might be an interesting year to look at: https://www.history.com/news/the-kentucky-derbys-forgotten-black-jockeys
*	AntConc Search Operator wildcard settings
  *	** * ** = zero or more characters
  *	** + ** = zero or one character
  *	? = any one character
  *	@ = zero or one word
  *	# = any one word
  *	! = search term OR search term
*	AntConc wom?n vs m?n results (showing a whole lot of sexism - yikes)
  *	Wom?n = 6099 lines
  *	M?n = 30204 lines
* Topic Modelling thoughts 
  *	I picked 10 topics because it was the default
  *	Following Wallace, I tried identifying my own topics
  *	Something I really appreciated this week was how you would ask us to find spots in the code and encourage critical thinking about how the code was constructed
    *	Ex: “we’ll rearrange things just so that we get the top say 5 terms per topic; these 5 words will give us a sense of what the topic is about. Do you spot where you might change that to say 10 terms?”
    *	Answer is here: top5termsPerTopic <- terms(topicModel, 5)

*	Bonus Thoughts
  * https://www.buzzfeed.com/andyneuenschwander/can-you-guess-the-disney-movie-based-on-its-barcode This was fun to try out! (found here: http://www.zachwhalen.net/posts/imj-a-web-based-tool-for-visual-culture-macroanalytics/)
  * Initial thoughts on the Popular Science Monthly covers
    *	Lots of WW2 content – makes sense based on the years covered
    *	Mostly drawings, so the occasional picture is quite striking (such as these ones: 1941 May; 1941 October) 
    *	You can really see the racist stereotypes in 1945 January
  *	Some of the images I got!
Insert
Images
Here

# Errors I had
-	Voyant error
-	Topic modelling errors (zip, no tm, no topicmodels)
-	“Whoops” errors – I would forget to run a line of code, or skip a few lines of code
o	Example: *insert image*
-	The following package is masked. Once I figured out what it was, I figured that since only one package was being ignored, I’d press on without fixing it and if everything broke then I’d try the fix I found
-	So many errors with the last step of topic modelling. Thank you Dr. Graham for helping with my last one!

# Questions I asked
* First topic modelling error
* Alphabet(20) error
