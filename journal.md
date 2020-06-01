# Reflection Four
This week left me feeling untethered. Partially because I was dealing with new material, but also because this week, more than in all the previous weeks, I had the sense that I was barely scratching the surface of something massive. I think that this can best be exemplified when, in [_Big Data for Dead People_](https://historyonics.blogspot.com/2013/12/big-data-for-dead-people-digital.html), Tim Hitchcock (2013) discussed the potential of using macro/micro analytics tools to “ask questions we know computers can answer” that do only confirm our current historical knowledge. This perspective was also [supported by Matthew Lincoln]( https://matthewlincoln.net/2015/03/21/confabulation-in-the-humanities.html) (2015).  For example, during my Voyant analysis of Dr. Melodee Beels’ data, one of the words I chose was “Indians” ¬because – based on the time and location of the text we were analyzing – it would be a word that would get an interesting distribution. And I was right, but I didn’t learn anything new from it. In short: _**it was not surprising**_.  Hitchcock (2013) asserts that reading text, even massive amounts of text at once, is the “vanilla sex” of digital history. I suppose, then, that all the text analysis I did this week is the equivalent of looking lovingly at my partner while we assume a missionary position. Overall, this analogy really only supports my feeling that I’m dipping my toes into deep waters. Because this feeling stuck with me all week, I wanted to honour it here. I am not yet sure how I can move beyond it, besides spending more time in this field. 

Like I did last week, I think that it’s important to acknowledge that history cannot be positivist, and is in actuality something that we reconstruct after the fact with our own modern biases. Thus, the narratives we create will also naturally be influenced by how we create them. I have therefore been thinking about how the affordances of digital work – specifically the ability to jump in between the micro and the macro – can both enable and discourage particular narratives within historical work. Often everything was both a giant mass of text and a tiny snippet of a phrase. It simultaneously felt too big ¬_and_ too small to be understood as a cohesive narrative. I couldn’t find a balance, and so I frequently found myself struggling this week to determine how I would tell a story with the text I analyzed. There was one occasion, however, where I saw the possibility for a narrative. While working with AntCont, I saw the phrase “[dear honey](https://github.com/sidxi/week-four/blob/master/antconc_results_dear%20honey.txt)” by chance. Because it caught my attention, I searched for it and found that it appeared 315 times. From all of these words, I had chanced on something that, to me, felt remarkably tender. While I don’t have the time or the knowledge to continue down that thread at the moment, the emotion it spurred in me was powerful. Hitchcock (2013) believes (and I agree) that a common thread between “normal” history and digital history is the telling of stories. To do any history, one must engage with the material openly, imaginatively, and empathetically. I am starting to see how digital history can help create new kinds of narratives.

Lastly, these new narratives – the ones that can only be generated through digital history – must be taken seriously. A [whitepaper published by the Roy Rosenzweig Center for History and New Media]( https://rrchnm.org/wordpress/wp-content/uploads/2017/11/digital-history-and-argument.RRCHNM.pdf) (2017) asserts that for historians, digital collections are overlooked in favour of printed knowledge. In particular, we still promote text – and by this, I mean linear, printed words – above all other forms of knowledge. Digital history work is deemed disruptive and unpredictable, partially because its methods aren’t easily intelligible to an untrained person, and also because it forces the reader to consider new perspectives that may deprioritize text in favour of images, sounds, and data. Despite the fact that the practices of digital history are still done by historians to the same rigor, this fact is often discarded because of its unfamiliarity. Hopefully, as digital history work starts to become more prominent, it will be better understood as just another set of tools that can be used to tell the stories of the past. 

# Reflection: Errors

The first error I encountered was a Voyant error that most of the class seemed to be dealing with. Luckily, I was able to implement the fix in the discord with no issues.

![voyant error](https://github.com/sidxi/week-four/blob/master/Week4%20Voyant%20Error%20-%20Failed%20Attempt%20to%20Create%20a%20Corpus.PNG)

My next series of errors all occurred while I was trying to topic model. It started out with more innocuous errors such as 

![zip](https://github.com/sidxi/week-four/blob/master/Question%20-%20zip%20issue.PNG)

which I was able to fix quite easily. I even helped a fellow classmate with the error, which is _so_ nice to be able to do! 

![zip fix](https://github.com/sidxi/week-four/blob/master/Week4%20Topic%20Modelling%20Zip%20Fix.PNG)

My next set of errors all had to do with topic modelling - this was definitely the area I had the most trouble with this week. First, I had a few errors that seemed to be fairly common: 

![no tm package](https://github.com/sidxi/week-four/blob/master/Week4%20TM%20error%20no%20package%20called%20'tm'.PNG)

![no topicmodels package](https://github.com/sidxi/week-four/blob/master/Week4%20TM%20error%20no%20package%20topicmodels.PNG)

Luckily, both were discussed within the discord also. For the first one, I had to do the following:

![no tm fix](https://github.com/sidxi/week-four/blob/master/Week4%20TM%20FIX%20no%20package%20called%20'tm'.PNG)

For the second, I had to install the topic models package. In fact, I had to install a few packages that r told me were missing, including one called 'pals'. This package ended up causing me some trouble a bit later on, when I got the following error:

![alphabet error 1](https://github.com/sidxi/week-four/blob/master/Week4%20Error%20could%20not%20find%20function%20alphabet.PNG)

When I tried fixing it by installing alphabet(20) the same way I had tried to install other packages (hey - it had worked up until now!), I got this error

![alphabet error 2](https://github.com/sidxi/week-four/blob/master/Week4%20Error%20alphabet(20)%20not%20available%20for%20version%204.0.0.PNG)

When I asked about it in the discord, Dr. Graham was an enormous help - he figured out that I could fix it by ignoring ```scale_fill_manual(values = paste0(alphabet(20), "FF"), name = "decade") +``` in the code (by putting a # in front of it). Dr. Graham also figured out what the issue had been!

![alphabet error cause](https://github.com/sidxi/week-four/blob/master/alphabet%20error%20cause%20-%20pals.PNG)

One error that occurred which contributed to my learning but I ultimately didn't fix was this one:

![masked](https://github.com/sidxi/week-four/blob/master/Week4%20error%20Reshape2%20masked.PNG)

Once I figured out what was actually happening, I decided that since only one package was being ignored, I’d press on without fixing it and if everything broke then I’d try the [fix I found](https://stackoverflow.com/questions/39137110/what-does-the-following-object-is-masked-from-packagexxx-mean). 

I also had a few "whoops!" errors where I definitely made the mistake. For example, I would forget to run a line of code individually, or skip a few lines of code.

![ran together](https://github.com/sidxi/week-four/blob/master/Week4%20Error%20A%20moment%20where%20I%20forgot%20to%20run%202%20lines%20separately%20and%20tried%20to%20run%20them%20together.PNG)

![skipped 3 lines](https://github.com/sidxi/week-four/blob/master/Week4%20accidentally%20skipped%203%20lines%20of%20code.PNG)
1[skipped 3 lines fixed](https://github.com/sidxi/week-four/blob/master/Week4%20when%20including%20the%203%20lines%20I%20skipped.PNG)

Ultimately, these were good for me to take stock of the fact that I really needed to pay attention to my work!
