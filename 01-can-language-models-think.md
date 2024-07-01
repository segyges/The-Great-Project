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

What does it mean for a language model to think? Any normal use of the word "think" does not seem like it will work here. Ultimately, what we mean when we say "think" is "able to do the sorts of things that humans do". This insight is, of course, originally from Alan Turing. There is a specific test, the "Turing test", that he proposes. This test directly measures the machine against a human, such that we judge a machine to be thinking if and only if the text the machine outputs can pass for human.

This is a very neat solution to the problem. If we accept that humans think, and that human thought can be utilized fully in written text, then anything which cannot be discerned from a human in written text must also be thinking.

We will take as given that humans think. We may not want to take for granted that human thought can be utilized fully in written text. Much of what humans do are able to do does not involve words at all, much less written text.

Considering the cases of humans with various disabilities should convince us that writing alone can express the presence of human thought. We do not doubt that people who are blind and deaf from birth experience thought because they are not able to speak or to write with conventional implements. Any of us can be paralyzed completely by injury. In cases, people have been limited to expressing themselves by well timed blinks to dictate writing. Such writings do not fail to express human thought; on the contrary, the sheer labor involved in such a thing seems almost guaranteed to mean that far more thought goes into every detail.

There are many human endeavors besides writing. Thought and care are expressed and understood in music, and movement, and all the arts we see with our eyes. Being able to write convincingly, such that no reader could ever tell that the author was not human, does not guarantee that a machine is able to think in all the ways that humans think. This is also true of those who are born totally colorblind, and who seem unlikely to be able to imagine color, and true in other ways of other disabilities. It is obvious to us when the subject is human that these sorts of disabilities do not rob the person of their humanity, of their ability to think in a way we believe makes them human. It would require special pleading to deny the same grace to a machine.
