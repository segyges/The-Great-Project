# Can Language Models Think?

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

Can language models think?

We should define these terms. For our purposes, a "language model" is some computer program, running on real hardware, which produces text as its output. As of this writing, such a model is probably a descendant of the Transformer architecture (Vaswani et al, 2017). This architecture and the techniques surrounding it (gradient descent, cross-entropy loss, et cetera) are very important for recent research in the field, but the only essential characteristic of a "language model" is that it produces text as its output.

What does it mean for a language model to think? Any normal use of the word "think" does not seem like it will work here. Ultimately, what we mean when we say "think" is "able to do the sorts of things that humans do". This insight is, of course, originally from Alan Turing. There is a specific test, the "Turing test", that he proposes. This test directly measures the computer program (which he calls a "machine") against a human, such that we judge a program to be thinking if and only if the text the program outputs can pass for human.

This is a very neat solution to the problem. If we accept that humans think, and that human thought can be utilized fully in written text, then anything which cannot be discerned from a human in written text must also be thinking.

We will take as given that humans think. We may not want to take for granted that human thought can be utilized fully in written text. Much of what humans are able to do does not involve words at all, much less written text.

Considering the cases of humans with various disabilities should convince us that writing alone can express the presence of human thought. We do not doubt that people who are blind and deaf from birth experience thought because they are not able to speak or to write with conventional implements. Any of us can be paralyzed completely by injury. In cases, people have been limited to expressing themselves by well timed blinks to dictate writing. Such writings do not fail to express human thought; on the contrary, the sheer labor involved in such a thing seems almost guaranteed to mean that far more thought goes into every detail.

There are many human endeavors besides writing. Thought and care are expressed and understood in music, and movement, and all the arts we see with our eyes. Being able to write convincingly, such that no reader could ever tell that the author was not human, does not guarantee that a program is able to think in all the ways that humans think. This is also true of those who are born totally colorblind, and who seem unlikely to be able to imagine color, and true in other ways of other disabilities. It is obvious to us when the subject is human that these sorts of disabilities do not rob the person of their humanity, of their ability to think in the way that makes them human. It would require special pleading to deny the same grace to a program.

Turing's test, as originally proposed, is not perfect. In brief: An interrogator exchanges messages, entirely with text, with another human respondent and a computer program, which they know only as A and B. Eventually, the interrogator has to choose which of A or B is a computer, and which is a human. Turing does not specify many peripheral details of administering the test, such as who the humans involved are. Many purported "Turing Tests" have been devised and administered since the test was first proposed. As a general rule, they are executed in some manner that gives the program some advantage, such that some plausible research project then existing has some chance of claiming to have passed the test. In cases where they are not, the program, of course, performs poorly.

We prefer to contemplate a test that is delivered under circumstances that disadvantage the program as much as possible. We need some reasonable population of interrogators and respondents, and we consider a program to pass this test only if no method of choosing or preparing human interrogators and respondents for the test, including allowing them to perform the test many times, allowed them to discern each other from the program more than 50% of the time. This would have to apply to interrogators, respondents, and to pairs thereof. Passing information outside of the text-only test environment is the only prohibition, and for any interrogator and respondent that perform multiple sessions, their past mutual history should be available both to them and to the program. Any program passing such a test would be producing text which was indistinguishable from that produced by a human, and therefore able to think as well as humans do.

No program currently existing passes this very strict test. Unfortunately, most humans would not pass this test either. Some people are certainly more skilled at convincing the interrogator that they are human than others, and those humans that are less skilled at this would not be judged to be "thinking" by the criteria of the test if they were entered in the program's position. In order to pass this test, a program does not have to be better at most humans or a median human at seeming human; it has to seem at least as human as the most human-seeming human available.

If we accept that humans at large do think, we would like to relax this test somewhat. We will continue to assume that we are comparing only trials of the Turing test where the interrogator is the most skilled, such that in many tests between many interrogators and many human respondents, we choose whichever interrogators have the highest "win rate" for discerning humans from programs. We will require only of the human respondents that they be drawn from some reasonably sized population more or less at random, and that they sincerely be attempting to convince the interrogator that they are human during each trial. We would have to concede that a computer program was thinking as well as a human if its percentile was at least 50%. If the program had any notable disability relative to most humans, the interrogators could exploit that and its percentile would be far below 50%.

We will take for granted that there is some program which could possibly be constructed which would pass such a test. Turing's paper on the test itself helpfully addresses most of the plausible-seeming objections to the notion that some program could, in principle, think, such as that humans have souls and machines cannot have souls.