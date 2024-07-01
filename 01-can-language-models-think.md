# Can Language Models Think?

> The Analytical Engine has no pretensions whatever to *originate* anything. It can do *whatever we know how to order it to perform*. It can follow analysis; but it has no power of anticipating any analytical relations or truths.
>
> -- Ada Lovelace, "Notes on the Analytical Engine", (1843)

> I propose to consider the question, "Can machines think?" This should begin with definitions of the meaning of the terms "machine" and "think." The definitions might be framed so as to reflect so far as possible the normal use of the words, but this attitude is dangerous, [...]
>
> -- Alan Turing, "Computing Machinery and Intelligence" (1950)

> As we discuss in §5, LMs are not performing natural language understanding (NLU), and only have success in tasks that can be approached by manipulating linguistic form [...]
>
> [...]
>
> [...] no actual language understanding is taking place in
LM-driven approaches to these tasks [...] Furthermore, as Bender and Koller [14]
argue from a theoretical perspective, languages are systems of
signs [37], i.e. pairings of form and meaning. But the training data
for LMs is only form; they do not have access to meaning. Therefore,
claims about model abilities must be carefully characterized.
>
> -- Emily M. Bender, Timnit Gebru, Angelina McMillan-Major, and Shmargaret Shmitchell, "On the Dangers of Stochastic Parrots: Can Language Models Be Too Big? 🦜", (2021)

## 1. The Question

Can language models think?

We should define these terms. For our purposes, a "language model" is some computer program, running on real hardware, which produces text as its output. As of this writing, such a model is probably a descendant of the Transformer architecture (Vaswani et al, 2017). This architecture and the techniques surrounding it (gradient descent, cross-entropy loss, et cetera) are very important for recent research in the field, but the only essential characteristic of a "language model" is that it produces text as its output. We will start with this general definition, and then work our way towards the specifics of the types of models that exist today.

What does it mean for a language model to think? Any normal use of the word "think" does not seem like it will work here. Ultimately, what we mean when we say "think" is "able to do the sorts of things that humans do". This insight is, of course, originally from Alan Turing. There is a specific test, the "Turing test", that he proposes. This test directly measures the computer program (which he calls a "machine") against a human, such that we judge a program to be thinking if and only if the text the program outputs can pass for human.

This is a very neat solution to the problem. If we accept that humans think, and that human thought can be expressed fully in written text, then anything which cannot be discerned from a human in written text must also be thinking.

## 2. The Turing Test

We will take as given that humans think. We may not want to take for granted that human thought can be expressed fully in written text. Much of what humans are able to do does not involve language at all, much less written text.

To rephrase the assertion: to master human language as well as a human does suffices to demonstrate human equivalent thinking. Seemingly the simplest and most direct argument for this is that nothing humans ever do is categorically more complex than language. There are an astronomical number of possible things to say; choosing one of them as well as a human does simply cannot be done without having human-equivalent thinking.

Considering the cases of humans with various disabilities should also convince us that writing alone can express the presence of human thought. We do not doubt that people who are blind and deaf from birth experience thought because they are not able to speak or to write with conventional implements. Any of us can be paralyzed completely by injury. In cases, people have been limited to expressing themselves by well timed blinks to dictate writing. Such writings do not fail to express human thought; on the contrary, the sheer labor involved in such a thing seems almost guaranteed to mean that far more thought goes into every detail.

There are many human endeavors besides writing. Thought and care are expressed and understood in music, and movement, and all the arts we see with our eyes. Being able to write convincingly, such that no reader could ever tell that the author was not human, does not guarantee that a program is able to think in all the ways that humans think. This is also true of those who are born totally colorblind, and who seem unlikely to be able to imagine color, and true in other ways of other disabilities. It is obvious to us when the subject is human that these sorts of disabilities do not rob the person of their humanity, of their ability to think in the way that makes them human. It would require special pleading to deny the same grace to a program.

Turing's test, as originally proposed, is not perfect. In brief: An interrogator exchanges messages, entirely with text, with another human respondent and a computer program, which they know only as A and B. Eventually, the interrogator has to choose which of A or B is a computer, and which is a human. Turing does not specify many peripheral details of administering the test, such as who the humans involved are. Many purported "Turing Tests" have been devised and administered since the test was first proposed. As a general rule, they are executed in some manner that gives the program some advantage, such that some plausible research project then existing has some chance of claiming to have made progress against the test. In cases where the test does not advantage the program, the program, of course, performs poorly.

## 3. A Stricter Turing Test

We prefer to contemplate a test that is delivered under circumstances that disadvantage the program as much as possible. We need some reasonable population of interrogators and respondents, and we consider a program to pass this test only if no method of choosing or preparing human interrogators and respondents for the test, including allowing them to perform the test many times, allows them to discern each other from the program more than 50% of the time. This would have to apply to interrogators, respondents, and to pairs thereof. Passing information outside of the text-only test environment is the only prohibition, and for any interrogator and respondent that perform multiple sessions, their past mutual history should be available both to them and to the program. Any program passing such a test would be producing text which was indistinguishable from that produced by a human, and therefore able to think as well as humans do. When choosing its next message, the program would be performing an operation at least as complex as the one the human performed.

No program currently existing passes this very strict test. Unfortunately, most humans would not pass this test either. Some people are certainly more skilled at convincing the interrogator that they are human than others, and those humans that are less skilled at this would not be judged to be "thinking" by the criteria of the test if they were entered in the program's position. In order to pass this test, a program does not have to be better than most humans or a median human at seeming human; it has to seem at least as human as the most human-seeming human available.

If we accept that humans at large do think, we would like to relax this test somewhat to include them. We will continue to assume that we are comparing only trials of the Turing test where the interrogator is the most skilled, such that in many tests between many interrogators and many human respondents, we measure only how successful the best interrogators are at discerning humans from programs. We will require of the human respondents only that they be drawn from some reasonably sized population more or less at random, and that they sincerely be attempting to convince the interrogator that they are human during each trial. We would have to concede that a computer program was thinking as well as a human if its percentile was at least 50% considering the best-performing interrogators. If the program had any notable shortcoming relative to most humans, the interrogators could exploit that and its percentile would be far below 50%.

## 4. Old Objections

We will take for granted that there is some program which could possibly be constructed which would pass such a test. Turing's paper on the test itself helpfully addresses most of the plausible-seeming objections to the notion that some program could, in principle, think.

Many of the objections Turing covers to the notion that a program could think are still commonly used. In many cases the modern strain of the objection adds some new detail. Any of these objections, if valid, would apply just as well to the models we actually have as it would to the general concept of a program. It will be useful to go over these objections briefly.

The first, Turing calls "The Theological Objection", and it is the assertion that humans have souls and machines cannot. Modern constructions asserting that all humans have something that machines cannot have, such as 'qualia', all uniformly restate this with the choice of word changed. Disentangling all such arguments is beyond the scope of this document; the reader is invited to return when such objections no longer seem reasonable to them.

The Mathematical Objection and The Argument from Consciousness, which Turing covers, also follow this pattern. In this case, the things that humans have and machines cannot have are "mathematical completeness and consistency" and "consciousness". One of the related modern constructions asserts that human consciousness is somehow quantum mechanical; the only evidence offered seems to be that quantum mechanics is very mysterious.

The Arguments from Various Disabilities is the objection from the paper which seems to be the most common now, and Turing's text deserves to be exerpted here:

> These arguments take the form, "I grant you that you can make machines do all the things
you have mentioned but you will never be able to make one to do X." Numerous features
X are suggested in this connexion I offer a selection:
Be kind, resourceful, beautiful, friendly, have initiative, have a sense of humour, tell right
from wrong, make mistakes, fall in love, enjoy strawberries and cream, make some one
fall in love with it, learn from experience, use words properly, be the subject of its own
thought, have as much diversity of behaviour as a man, do something really new.

This passage has aged very nicely. It is especially amusing to see "make mistakes" on the list; most of the time when we see the Arguments from Various Disabilities made now, they concern some current category of common mistakes from LLMs. (To wit: They are bad at arithmetic, they rhyme poorly, they cannot count letters well, they are prone to odd spelling errors, they repeat themselves, they have no long term memory, they are often poor conversationalists, and they confabulate completely made up facts with complete abandon.)

Turing's remarks state, it seems correctly, that all such assertions are made out of induction, that is, because people have never seen such a thing happen, they think it is natural that it never could. This reasoning is categorically incorrect; it was incorrect in 1950 when Turing was stating that it was used to argue that no program could use words properly, and it is incorrect now.

To abuse induction the other way: Since Turing wrote in 1950, many such arguments regarding various disabilities have been made and proven wrong. Chess and Go were popular such objections; natural language comprehension was another. Turing had to die and half a century had to pass before he was definitively proven right about computer programs being able to use words properly. We have no idea how long it will be before any given argument is proven wrong, but it would not seem wise, given past progress, to assume that the trend will reverse itself.

Simply to be contrary: If language models are still bad at math, rhyming, counting letters and spelling, and it is the year 2034 or later, I should be mocked as thoroughly as possible for my naivete here.

We note that we are passing over Lady Lovelace's Objection here. We do this not because it is less interesting than the others, but because it is the most interesting objection, and the most modern. Alan Turing could not possibly have anticipated the types of things we say concerning it now. This objection deserves its own discussion, and benefits immensely from the modern context.

The objection is this:

> The Analytical Engine has no pretensions whatever to *originate* anything. It can do *whatever we know how to order it to perform*. It can follow analysis; but it has no power of anticipating any analytical relations or truths.

This very modern and subtle argument was written in 1843.

After the arguments from various disabilities, this is the argument that is the most commonly repeated today. Saying that a language model is a "stochastic parrot" or saying they "only have success in tasks that can be approached by manipulating linguistic form" are simply ways of restating it. Sometimes, these arguments are made cautiously and with reference to some alternative category of programs than the ones being discussed which would be capable of originality; more often, there is no alternative offered; frequently, this is stated categorically, as if it applies to all possible programs.

The core dispute about whether modern language models can think is, fundamentally, whether we think Ada was right about this in general or it applies to the models we have now. I would answer no to both. It is enduringly impressive that she managed to ask the question at all nearly two centuries early.
