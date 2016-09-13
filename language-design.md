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
majority of whom were male, this quote struck me as being particularly accurate.
Sadly, it epitomizes the current state of the tech industry as a place
bifurcated into groups of "insiders" and "outsiders", one in which ability and
potential have little to do with which group one finds themselves in.

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

> "You can't please everyone, so aim to displease everyone equally" [Bloch,
2006]

We chose this quote because it is an undesirable, yet important part of
designing a language or an API.  In CS 5 and CS 60, all of our homework
assignments were very small and self-contained, and they often had "perfect"
solutions.  However, when I transitioned to working with a much larger code-base
during an internship this summer, I soon found that the real world is very
different from our ideal CS assignments.  There were many situations where
deciding a variable name was ambiguous, or when a new feature broke existing
contracts.  This quote reminds me that while you should definitely try to make
your code as clear and intuitive as possible, it is not realistic to please
everybody.
	This issue was evident in the source article about grayscale [Verou, 2014]. 
	All of the proposed names for the "graying" functions had their own drawbacks. 
Their seemed to be well-thought arguments for any of the four options.  The
designers of the language heeded the advice of not being able to please
everybody, and sensibly decided to poll users.

---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

Guy Steele gives us several traits of a good language in "Growing a Language".
According to Steele, the size of the language is one important indicator. As he
demonstrates by restricting himself to one-syllable primitive words, using a
language that is too small can be cumbersome. However, if a designer is too
ambitious with the size of the language, then it may be too slow to develop.
The danger of a large language, to Steel, is that "in a race, a small language
with warts will beat a well designed language because users will not wait for
the right thing" (Steele 6). So a small language is not good enough, but large
well-thought-out languages tend to fail. Steele's solution is to design a small
language that can easily grow. Importantly, it must be able to grow in such a
way that the users can contribute to the growth -- languages designed by one
person or by a committee tend to grow more slowly, and to alienate original
users as they grow.

All of the more specific language characteristics mentioned by Steele are in
service of this goal -- to allow growth. To name a few, a language set up to
grow should have generic types (Steele 10), operator overloading (10), and
(perhaps most importantly) the ability to add new words to the vocabulary of the
language in such a way that the new words look and act like primitive words (6).
By way of example, languages as diverse as Haskell, Lisp, and C++ satisfy these
criteria.

While Steele gives us one useful criterion for evaluating languages, we can see
a slightly different approach in Joshua Bloch's "How to Design a Good API and
Why it Matters". (Note that while Bloch's talk pertains specifically to APIs, we
have seen that APIs and languages share many traits, such as vocabulary and
fluency, so it stands to reason that many of the things that make an API good
might also make a language good). Bloch gives us many tips for how to make an
API that is user-friendly, not just in terms of growth, but also as it exists
right now. The most generally applicable is probably the "principle of least
astonishment" (Bloch 506). This necessary, though probably not sufficient,
condition for a language to be good, can be stated as follows:

>  Every method [or feature, in the case of a language] should do the least
>  surprising thing it could, given its name.
>  [Bloch, 2006]

So what is a bad language? We believe the easiest definition of a bad language
is any language that is not good, as we now have a good idea of what makes a
language good. To end with an example, we agree with Tim Smith that R is a bad
language, evidenced by the content and tone of Smith's "aRrgh: a newcomer’s
(angry) guide to R". R violates the principle of least astonishment in many
ways. Take, for example, the dot operator -- in fact, this is not an operator at
all, but simply a valid character to include in a variable name, which makes for
very astonishing names. As Bloch says, "names matter" (Bloch 506). Another
unfortunate trait of R, one not yet mentioned here, is its tendency to fail
silently or late. A good language should "fail fast" (506), and R definitely
does not.

---

**Question**

How do the themes of _Growing a Language_ relate to the "sound lab" we did this week?

**Response**

My main takeaway from _Growing a Language_ was that a good language should
provide users with a small and useful set of building blocks.  From there, the
progammer should be able to compose the available tools to suit their
specific need. We tried to use this same mentatility when adapting the Sound
library to be a more usable API.  First, we created a "Sound" class which
contained all of the methods for editing sounds.  We tried to be
consistent--each method took in a Sound (self) along with other parameters and
returned a new Sound.  This way, the user could easily compose functions using
calls like `mySound.reverse().overlay(otherSound)`.

In addition, _Growing a Language_ showed the importance of keeping a keeping an
API as contained as possible, and only including options that would be relevant
to many users.  On pages 10 and 11, Steele showed many cases of data types, each
increasingly obscure.  After describing them, Steele asked "So should we make
'x' a type in the Java programming language?"  In the ends, he concludes that
language designers should not include these rare features because "It would not
be fair to weigh down all programmers with the need to have or to learn all the
words for all niche uses" (Steele, 12).  This idea ties with the theme of making
a language/API exactly as small as it should be, and no smaller [Bloch, 2006]. 
We tried to respect this mentality when designing our API for the sound lab. 
All of the methods should perform a single task, which allows users to combine
functions effectively.  We tried to keep the methods as segmented as possible,
including options like "play", "overlay," "reverse," and "change speed".  We did
not, for example, add a method that would both divide overlay two sounds and
reverse them, as this would not have been useful for most users.

Another point that _Growing a Language_ emphasized was that users should be able
to make their own functions that look like primitives of the language. 
According to Steele, 
> APL was designed by one man, a smart man—and I love APL—but it had a flaw that
> I think has all but killed it: there was no way for a user to grow the
> language in a smooth way (Steele, 6)

This is a very interesting and useful idea that we did not consider when
desigining our Sound API.  Our design involved creating a Sound class with two
data members, the sound samples and the sampling rate.  Our goal was to keep
these data members private and only expose users to the class's methods.  
(Bloch includes this idea in his maxim "Minimize accessibility; when in doubt,
make it private").  With this design, however, a user would not be able to
extend the Sound class.  They compose the sound methods that we defined, but
they would have no way of creating a primitive method that looked like one from
the API.  As Steele shows, this rigidness could dissuade programmers from
using our API, and suggests that we should have used a different approach.
---

**Question**

In what way is an API a language?

**Response**

In class, we talked about the specturm of DSL-ness, which included, in order
from least to most "DSL-y", libraries, APIs, and DSLs. Just from that, it should
be clear that the distinction between APIs and languages is fuzzy -- that's the
whole point of a spectrum.

This fuzziness is also evident in the similarities between the definitions of an
API and a language. In particular, we defined a language as having fluency
(vocabulary and grammar) and semantics. An API certainly has semantics. It also
has some sense of fluency -- per Bloch, "if you get an API right, code will read
like prose" (Bloch 506).

As we alluded to in an earlier response, a similiarity between APIs and
languages is what makes one good. We can get a sense of the similarities by
comparing Steele's traits of a good language with Bloch's traits of a good API.
For example, Steele makes a big point of how "a main goal in designing a
language should be to plan for growth" (Steele 7). In a similar vein, Bloch
advises API designers: "When in doubt, leave it out.... You can always add
things later, but you can’t take them away" (Bloch 506).

As another example, a good language, like a good API, should be a collaborative
endeavor. Steele describes the bazaar/cathedral metaphor, and suggests that a
language should be built like a bazaar -- the many users of the language all
play a small part in building the final product -- since "it is fine to come
up with good thoughts, but much better to know them when you see them in the
work of other persons" (Steele 8). Bloch seems to agree, writing

> API design is not a solitary activity. Show your design to as many people as
> you can, and take their feedback seriously. Possibilities that elude your
> imagination may be clear to others (Bloch 506).

To summarize, languages and APIs are adjacent on the DSL spectrum, and they
share similar definitions. Thus it is no surprise that good API is in many ways
similar to a good language.

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

There are clearly stereotypes about certain DSLs. For example, Yang and Rabkin
mention the tendency of back-end developers to look down on front-end
programmers. They mention Javascript in this context. While Javascript is
clearly a general purpose language, there are DSLs involved in web development
that also contribute to the stereotypes. For example, HTML fits our definition
of a DSL, and more generally a programming language. It has syntax and
semantics, and it allows small building blocks to be chained and composed in
ways that add to the expressiveness of the language. However, the internet is
rife with articles claiming that HTML is not a programming language. For an
example, see the top answer [here](http://stackoverflow.com/questions/145176/is-html-considered-a-programming-language).

We believe that the disdain for HTML is but an example of a more general
principle. Note that many of the comments on the StackOverflow answer linked
above discuss Turing completeness. For example,

> TeX is a Turing-complete language, so its classification as a programming
> language or markup language is a bit blurry.

> Apparently, HTML5+CSS3 is turing complete too.

What's interesting here is not whether these langauges are Turing-complete, or
if they are, well, languages. Rather, the interesting thing is that
Turing-completenes is an issue of discussion at all. There seems to be a popular
conception that Turing-completeness makes a programming language, and since we
have seen that many DSLs are not Turing-complete, it seems reasonable to believe
that programmers in general may be more wary of DSLs than they would be of
general purpose languages.

This could lead to the same kind of discrimination described in Yang and
Rabkin's article, where engineers are kept "outside" the loop based on their
familiarity with certain DSLs. It may, however, have the opposite affect: those
who are prejudiced against DSLs may be unwilling to take a job in which they
would be working with DSLs. This obviously presents problems for the hiring
managers at such companies, but we propose that it might be a blessing in
disguise, as people wont to judge on the basis of language are self-selected out
of opportunities, and those with more open minds take their place.

Unfortunately, this way of thinking presumes that there are plenty of DSLs to
begin with. Mitigating this effect may be the fact that those who are in a
position to create DSLs are likely to be the same ones who are biased against
them. This could lead to suboptimal solutions to problems where a DSL could
solve the problem more elegantly.

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

- [x] Question 1: Daniel, Jeb, Daniel
- [x] Question 2: Jeb
- [x] Question 3: Daniel
- [x] Question 4: Jeb
- [ ] Question 5: Daniel
- [x] Question 6: Jeb
- [ ] Question 7: Daniel


---
