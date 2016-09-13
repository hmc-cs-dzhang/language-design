_Fill in each this file with your responses, placing each response after its
corresponding question._

---

**Question**

Pick three quotes from the readings about language design. Good candidates 
are:

   + Something you agreed with / resonates with your own experience
   + Something you disagree with
   + Something that is interesting, a new idea or perspective you'd like to remember
   + Something you didn't understand

For each quote, describe what it was about the quote that led you pick it.

**Response**

1. From the article by Pavlus:

>"According to findings by researchers from Southern Illinois University, this
>reaction isn’t just because you’re a n00b: they found that Perl, a major
>programming language used by untold zillions of developers, is no more
>intuitive to novices than a language with a randomly generated syntax."
>[Pavlus, 2012].

We selected this quote as an example of something we disagree with.  Most
notably, the quote contradicts itself.  The quote first says that if you
have trouble intuiting code then it's not becuase you're a n00b.  However,
they go on to reference a studying that tested people who have never coded
before.  This quote does not support their point that experienced coders
struggle with syntax.

I also disagree with the sentiment that syntax should necessarily be more
intuitive to "novices".  Sure, using natural language could look more
understandable for someone who has never coded before.  However, for
more experienced coders, using natural language could feel ambiguous and
cumbersome.  Frequent users of a code would appreciate a small syntax
that they could build off of and a concise set of keywords.  Also, I think
it is more important to cater to experienced coders than the "n00bs" in the
study because they were only novices for an hour.  Typically, people spend
more time as experienced coders who understand the syntax than as beginners
trying to read off the code like a natural language.  There is certainly
a use for intuitive languages that read more like natural language for
teaching purposes.  However, once a student has learned how to code, he/she
will probably grow tired of writing less concise code.


> "While those on the outside are still struggling to prove themselves, the
> technically privileged have gone ahead to determine what the software that
> runs our lives should look like."
> [Yang and Rabkin, 2015].

Having spent the summer working in an office of 300 engineers, the overwhelming
majority of whom were male, this quote struck me as being particularly
accurate. Sadly, it epitomizes the current state of the tech industry as a
place bifurcated into groups of "insiders" and "outsiders", one in which
ability and potential have little to do with which group one finds themselves
in.

A particularly interesting point of the article, which we believe is
encapsulated in this quote, is the ambiguous direction of causality when it
comes to language-based discrimination. Do so-called "Real Programmers" look
down on Javascript or HTML users because of prejudice against those languages?
Or have industry insiders cultivated the language-based stereotypes as a means
to discriminate against those who tend to use the languages? We believe the
causality flows both ways. Those on the inside have certain prejudices about
languages, which inform their prejudices about those who use the languages.
They then utilize the language prejudice to keep the outsiders out and
themselves in. Breaking this cycle of privilege will require a dramatic
cultural shift.

"You can't please everyone, so aim to displease everyone equally"
	In the real world there is not always a perfect solution like in CS5
	There are always tradeoffs
	This was evident in the grayscale article


---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

Good language:

User-defined things act like primitive ones
A good language is one that is easily extendable.  Starts small. Allows users to grow the language.
Principle of least astonishment.  Vocabulary should be intuitive.
Easy things should be easy
Conduct a study.
Fails early and loudly.

Bad language:

Examples of poorly designed languages, R and Perl.
Astonishing
Will let you do things that you shouldn't do
Inextensible
R: Easy things not easy, like equality testing for integers
One way to tell a language is designed poorly is to conduct a study.




---

**Question**

How do the themes of _Growing a Language_ relate to the "sound lab" we did this week?

**Response**

We made it easier to compose things, and create complicated sounds out of the
building blocks.  Made it easier for the user to do complex things. All the
functions were simple, basic, primitive building blocks.  Then the user could do
what they wanted.  Made connections easier.  Better room for growth by making
connections more intuitive Connect to building blocks We didn't add to the rules
of the sound lab.  We just modified the existing ones. We didn't include complex
functions that would only be useful to a select few. Not possible for users to
add to the API and make it look like a primitive. (pg 6)  Cannot extend the
sound class. (Keep APIs free of implementation details).



---
 
**Question**


In what way is an API a language? 

**Response**

Language - semantics, vocabulary + grammar
API - semantics, vocabulary
"If you get an API right, code will read like prose": fluency

Good characteristics of languages are good characteristics of APIS
	- principle of least astonishment
	- extensible
	- start small (when in doubt leave it out, steele)
	- collaboration/open source
	- easy to evolve/pivot
	- fail fast
---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**

Example of open source/collaborating with users "If it's hard to find good names
go back to the drawing board" -- is CSS a bad language??? Sometimes every
alternative will have drawbacks You can't please everyone ... displease everyone
equally Expect API design mistakes, see article Principle of least astonishment
(see comments) Readability is an important consideration for names Would a small
change in program behavior require a lot of name changes in the code?
(extensibility/evolvability)

---

**Question**

The Yang and Rabkin article talks mainly about general-purpose languages. In 
what ways do the themes apply to the study and creation of DSLs?

**Response**

A disadvantage of a DSL is that its difficult to hire people to convince them to
work on your DSL (or maybe an advantage?) Stereotypes about specific DSLs (html)
People look down on not Turing Complete DSLs because its harder to do certain
nondomain specific tasks People might view using DSLs are cheating because it is
easier to do things. More respect for back-end than front-end (analogous) Use of
general programming language depends on your background/socioeconomic status, so
perhaps the idea to create a DSL does too. Maybe people are biased against
creating DSLs for the reasons above



---

**Question**

The Pavlus article mentions the researchers' comments that people preferred
"natural-language replacements for some of the more abstruse syntax". In other 
words, people found it easier to work with code that looks more like a human language (e.g.,
English). Consider the following quote by William R. Cook, one of the creators
of AppleScript:


> The experiment in designing a language that resembled natural languages (English
> and Japanese) was not successful. It was assumed that scripts should be
> presented in “natural language” so that average people could read and write
> them. … In the end the syntactic variations and flexibility did more to confuse
> programmers than to help them out. It is not clear whether it is easier for
> novice users to work with a scripting language that resembles natural language,
> with all its special cases and idiosyncrasies. The main problem is that
> AppleScript only appears to be a natural language: in fact, it is an artificial
> language, like any other programming language. … even small changes to the
> script may introduce subtle syntactic errors that baffle users. It is easy to
> read AppleScript, but quite hard to write it.
[[Cook 2007, page 1-20]](https://dl.acm.org/citation.cfm?doid=1238844.1238845)

Are these two experiences of natural languages at odds with one another? Would
you choose to include natural language in the design of a DSL? If so, how might
you do so? If not, why not?

**Response**

"natural-language replacements for some of the more abstruse syntax" seems to be
talking more about replacing the vocab, whereas AppleScript was more about
replacing the grammar to make it easier to read.  More about choosing good names
for things. I would include some aspects of natural language but only so far.
From Zen of Python, "there should be one, and preferably only one obvious way to
do it".  If you make it too similar to natural language then there would seem to
be more than one way. Vocab should come from natural language, but grammar needs
to be more precise. Small vocabulary set so that you can keep track and learn
relevant things. Even then we question is NL would make as much of a difference
once someone has put in the effort learn the syntax.


---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

We individually read the articles, and then we pair-programmed the outline.

Question 1:
	First quote: Daniel
	Second quote: Jeb
	Thrid quote: Daniel

Question 2: Jeb
Question 3: Daniel
Question 4: Jeb
Question 5: Daniel
Question 6: Jeb
Question 7: Daniel


---
