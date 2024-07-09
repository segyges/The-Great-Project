# Can Language Models Think?

> The Analytical Engine has no pretensions whatever to *originate* anything. It can do *whatever we know how to order it to perform*. It can follow analysis; but it has no power of anticipating any analytical relations or truths.
>
> -- Ada Lovelace, "Notes on the Analytical Engine" (1843)

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
> -- Emily M. Bender, Timnit Gebru, Angelina McMillan-Major, and Shmargaret Shmitchell, "On the Dangers of Stochastic Parrots: Can Language Models Be Too Big? 🦜" (2021)

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

Turing's test, as originally proposed, is not perfect. In brief: An interrogator exchanges messages, entirely in text, with another human respondent and a computer program, which they know only as A and B. Eventually, the interrogator has to choose which of A or B is a computer, and which is a human. Turing does not specify many peripheral details of administering the test, such as who the humans involved are. Many purported "Turing Tests" have been devised and administered since the test was first proposed. As a general rule, they are executed in some manner that gives the program some advantage, such that some plausible research project then existing has some chance of claiming to have made progress against the test. In cases where the test does not advantage the program, the program, of course, performs poorly.

## 3. A Stricter Turing Test

We prefer to contemplate a test that is delivered under circumstances that disadvantage the program as much as possible. We need some reasonable population of interrogators and respondents, and we consider a program to pass this test only if no method of choosing or preparing human interrogators and respondents for the test, including allowing them to perform the test many times, allows them to discern each other from the program more than 50% of the time. This would have to apply to interrogators, respondents, and to pairs thereof. Passing information outside of the text-only test environment is the only prohibition, and for any interrogator and respondent that perform multiple sessions, their past mutual history should be available both to them and to the program. Any program passing such a test would be producing text which was indistinguishable from that produced by a human, and therefore able to think as well as humans do. When choosing its next message, the program would be performing an operation at least as complex as the one the human performed.

No program currently existing passes this very strict test. Unfortunately, most humans would not pass this test either. Some people are certainly more skilled at convincing the interrogator that they are human than others, and those humans that are less skilled at this would not be judged to be "thinking" by the criteria of the test if they were entered in the program's position. In order to pass this test, a program does not have to be better than most humans or a median human at seeming human; it has to seem at least as human as the most human-seeming human available.

If we accept that humans at large do think, we would like to relax this test somewhat to include them. We will continue to assume that we are comparing only trials of the Turing test where the interrogator is the most skilled, such that in many tests between many interrogators and many human respondents, we measure only how successful the best interrogators are at discerning humans from programs. We will require of the human respondents only that they be drawn from some reasonably sized population more or less at random, and that they sincerely be attempting to convince the interrogator that they are human during each trial. We would have to concede that a computer program was thinking as well as a human if its percentile was at least 50% considering the best-performing interrogators. If the program had any notable shortcoming relative to most humans, the interrogators could exploit that and its percentile would be far below 50%.

## 4. Old Objections

We will take for granted that there is some program which could possibly be constructed which would pass such a test. Turing's paper on the test itself helpfully addresses most of the plausible-seeming objections to the notion that some program could, in principle, think.

Many of the objections Turing covers to the notion that a program could think are still commonly used. In many cases the modern strain of the objection adds some new detail. Any of these objections, if valid, would apply just as well to the models we actually have as it would to the general concept of a program. It will be useful to go over these objections briefly.

The first, Turing calls "The Theological Objection", and it is the assertion that humans have souls and machines cannot have souls. Modern constructions asserting that all humans have something that machines cannot have, such as 'qualia', all uniformly restate this with the choice of word changed. Disentangling all such arguments is beyond the scope of this document; the reader is invited to return when such objections no longer seem reasonable to them.

The Mathematical Objection and The Argument from Consciousness, which Turing covers, also follow this pattern. In this case, the things that humans have and machines cannot have are "mathematical completeness and consistency" and "consciousness". One of the related modern constructions asserts that human consciousness is somehow quantum mechanical; the only evidence offered seems to be that quantum mechanics is very mysterious.

The Arguments from Various Disabilities is the objection from the paper which seems to be the most common currently, and Turing's text deserves to be exerpted here:

> These arguments take the form, "I grant you that you can make machines do all the things
you have mentioned but you will never be able to make one to do X." Numerous features
X are suggested in this connexion. I offer a selection:
Be kind, resourceful, beautiful, friendly, have initiative, have a sense of humour, tell right
from wrong, make mistakes, fall in love, enjoy strawberries and cream, make some one
fall in love with it, learn from experience, use words properly, be the subject of its own
thought, have as much diversity of behaviour as a man, do something really new.

This passage has aged very nicely. It is especially amusing to see "make mistakes" on the list; most of the time when we see the Arguments from Various Disabilities made now, they concern some current category of common mistakes from LLMs. (To wit: They are bad at arithmetic, they rhyme poorly, they cannot count letters well, they are prone to odd spelling errors, they repeat themselves, they have no long term memory, they are often poor conversationalists, and they confabulate completely made up facts with complete abandon.)

Turing's remarks state, it seems correctly, that all such assertions are made out of induction, that is, because people have never seen such a thing happen, they think it is natural that it never could. This reasoning is categorically incorrect; it was incorrect in 1950 when Turing was stating that it was used to argue that no program could use words properly, and it is incorrect now.

To abuse induction the other way: Since Turing wrote in 1950, many such arguments regarding various disabilities have been made and proven wrong. Chess and Go were popular such objections; natural language comprehension was another, and Turing cites it directly. Turing had to die and half a century had to pass before he was definitively proven right about computer programs being able to use words properly. We have no idea how long it will be before any given argument is proven wrong, but it would not seem wise, given past progress, to assume that the trend will reverse itself.

Simply to be contrary: If language models are still bad at math, rhyming, counting letters and spelling, and it is the year 2034 or later, I should be mocked as thoroughly as possible for my naivete here.

We note that we are passing over Lady Lovelace's Objection here. We do this not because it is less interesting than the others, but because it is the most interesting objection and the most modern. Alan Turing could not possibly have anticipated the types of things we say concerning it now. This objection deserves its own discussion, and benefits immensely from a modern context.

The objection is this:

> The Analytical Engine has no pretensions whatever to *originate* anything. It can do *whatever we know how to order it to perform*. It can follow analysis; but it has no power of anticipating any analytical relations or truths.

This very modern and subtle argument was written in 1843.

After the arguments from various disabilities, this is the argument that is the most commonly repeated today. Saying that a language model is a "stochastic parrot" or saying they "only have success in tasks that can be approached by manipulating linguistic form" are simply ways of restating it. Sometimes, these arguments are made cautiously. When made cautiously, these statements state that some category of language model, X, cannot be original, but that perhaps some other category of language models, Y, might. More often, there is no Y; the statement is only that the types of models we actually use cannot be original. Frequently, these types of arguments have no qualifiers and seem to state that no program can ever be original.

The core dispute about whether modern language models can think is, fundamentally, whether we think Ada was right about this in general or whether this applies specifically to the models we have now. I would answer no to both. It is enduringly impressive that she managed to ask the question at all nearly two centuries early.

## 5. New Objections

Before we return to Lady Lovelace's objection, we will go over objections to current-generation systems that could not have been proposed in the 1800s. Many of these have similar flavors to those that Turing covered. Turing put Lady Lovelace's objection late in his paper, and it would seem he did so wisely. Before you address such an objection directly, it is better to address the many similar objections that often are often hidden in it.

### The Argument from Unimpressive Components

This model is "only" "X", therefore neither it nor anything like it can think (or demonstrate any other property I do not think X can have).

X is variously: Math, matrices, statistics, electricity, training data. I am sure there are many more.

We can also make this argument against people, where X can be: atoms, chemicals, electricity, molecules, carbon compounds, enzymes, burning sugars, electricity, random mutations.

Human beings are "just" apes retrofitted with some extra fatty tissue loaded with ion pumps. We call this "brain matter". Each individual part is perhaps unimpressive, or can at least be described so it sounds unimpressive. In aggregate, they are a person.

Complex things can have many simple parts. In fact: It is difficult to think of any complex thing that does not have many simple parts. One sound is noise; many sounds can be music. Visual art is just lines, or brushstrokes; books are just letters.

Anything can be made to sound trivial if it is described as "just" what it is made of. Everything is made of something, and whatever it is made of will generally be some reasonable number of reasonably simply things.

This argument is bad; people should not be persuaded by it. People will continue to be persuaded by it because it is good rhetoric. X, whatever X is, is unimpressive or boring. Therefore, anything made of X must also be unimpressive or boring.

If we want to be correct, we should avoid falling for such arguments. We have many counterexamples, so we know that they are not always true.

### Argument from Architecture

Some category of program, X, can never do X. Therefore, it cannot think. (Possibly we mean to imply that no model of any kind can think).

In some limited cases this is true. A single layer neural network cannot compute the XOR function, for one famous example. Certainly, human thought is at least as complex as XOR, so anything which cannot compute XOR cannot think. This is a good argument against a single-layer perceptron being able to think.

Generally speaking this is untrue of any broad category of architectures still in use in 2024, the most common of which is the transformer. They are turing-complete, or as close to turing-complete as anything which has finite memory can be. (For any unfamiliar: This means that it can perform any computation.) There are a few theoretical arguments pertaining to the complexities of the circuits they can learn, but most of them do not seem to make them less general than a human being, which also have only a finite ability to deal with complexity.

It is very difficult to be sure, given that current architectures are turing-complete and that they are often modified in many ways, that they categorically cannot do any particular thing. It is plausible that no current version of a transformer can some specific thing efficiently enough to make doing that thing feasible on any hardware we can make. However, architectures are varied upon constantly; our efficiency at completing the same task has increased by several orders of magnitude in recent years. To state that a given architecture, exactly as it currently exists, cannot do any particular thing efficiently is not an argument not to use that architecture at all. It is an argument to modify it, as we can and have done many times.

As we generalize the approach: Either some architecture can think, or no architecture can. If some architecture can think, any specific disability you can find in a current architecture will give you a hint about what must be true of an architecture that could think.

Generally speaking, the principle of "stacking an arbitrary number of matrices in some clever way" has consistently proven that it solves any problem we can find a way to use it on. It is a general method, the same way writing is a general method of conveying meaning and computer programs are general purpose methods of doing math. Arguing against a specific architecture is either arguing in favor of some alternative architecture or failing to consider that alternatives could exist.

### Argument from Training Modality

From our opening, we know the argument that "languages are systems of signs [37], i.e. pairings of form and meaning. But the training data for LMs is only form; they do not have access to meaning."

This was not even true when that paper was published. Models already existed (e.g. CLIP, and much earlier, YOLO) which directly paired signs (words or sentences) with their meanings (pictures of objects). Image generation already existed as a field, where the generation task is always to pair sign (the prompt) to meaning (the output image). We currently have models which mix audio, video and text freely in input and output. They are still, compared to pure text models, a work in progress; it is not really disputed whether they work at all. As a general rule, they do.

You could claim that a model that could identify you from a picture did not know the "meaning" of who you were, but then you would have to claim the same thing of another person who recognized you in a picture. What is the person doing, in identifying you, that the model is not?

The answer is nothing; the task of recognition is the same. We can claim that "meaning" is somehow impossible to put into any form whatsoever, that digital data coming from video cameras and microphones is somehow "less meaningful" than the sense inputs of our eyes and ears. This seems like a way of smuggling in the Theological Objection again; that when a person does something it is imbued with a soul, or with meaning, but when a machine does the same task it is not. Data in a computer is "just" electricity, but our thoughts are made of electricity too. If we assume that humans are special and distinguished, and only human acts can have "meaning", then of course machines cannot think; but the argument is circular.

We can also restate this as an argument from disability: if a human had some disability (sight, hearing) but still had language, we would not say that they did not understand meaning.

We can narrowly give the argument this: It is possible that some tasks are prohibitively difficult to learn from scratch without certain types of data. Humans with disabilities still have human brains, and human brains were formed under the requirements imposed on them by all the senses that humans typically have. Models trained to produce audio of human speech, but not given any text to help them learn what words are, typically produce a babble of disconnected syllables and voice sounds. The same model, when given text to learn from along with audio of someone speaking the words, can learn to produce speech from written text. For many years, and possibly still today, the first such well-known model was the voice of the Google Assistant, which comes built into every Android phone. [cite wavenet, probably]

This is not an argument against models in general being able to think, or understand language. At most, this applies strictly to models with only written text as training data. Even there it is empirically questionable; we know that models trained strictly on language data can sometimes produce mostly reasonable answers to questions about the physical world, such as: "Here we have a book, 9 eggs, a laptop, a bottle and a nail. Please tell me how to stack them onto each other in a stable manner." [cite the thing]

Text is rich with meaning. As humans, we are always trying to find new ways to condense our thoughts, to condense meaning, into words. Training a language model is the task of extracting as much meaning from that text as possible. It is possible that some things cannot be learned, or learned well, or learned efficiently, only from text; but it is strange to assert that the text itself has no meaning. Of course it has meaning. It is perhaps the densest form of human meaning, where a person can put the residue of a lifetime of thoughts and feelings into less space than a phone background.

### Lady Lovelace's Original Objection

### Lady Lovelace's Objection, Revisited
