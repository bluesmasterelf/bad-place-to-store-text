Characterizing ChatGPT's understanding and production of language, and how many steps are needed to make it an AGI
Inbox

John Hempfling <john.m.hempfling@gmail.com>
Jan 23, 2023, 12:08 AM
to me

Hey Ian,

In this email I'll try to characterize ChatGPT's understanding and production of language, and try to get a handle on what steps are needed to make it an AGI.

Characterizing ChatGPT's understanding and production of language
One can say that AIs are guessing effectively, or that they are understanding and producing language.

One can say that language is an extremely complex set of both syntactic rules and semantic meanings. (To demonstrate the necessity of semantic understanding to language parsing and production, I'll steal an example from Otherwords: there is no syntactic difference between "The girl drew the dog with a pencil" and "The girl drew the dog with a bone," but if you know the meaning of the words, then you can conclude the first statement indicates that the girl used a pencil to draw, while the second statement indicates that the dog in the drawing had a bone in its possession.) Talking about language in terms of meaning and understanding we could call the "realist position"; it takes language seriously as a series of signifiers that have a relationship with things that are signified. Similarly, talking about humans using language to express and understand meaning seems to take humans' use of language seriously.

One can also say that language is a set of basically arbitrary signs that occur in certain regular patterns. The patterns cause the signs to appear to have certain more-or-less well-defined relationships with each other and with other non-linguistic phenomena. The apprehension of these signs and their relationships allows for language comprehension, and the manipulation of these signs and patterns allows for language production. Talking about language in terms of signs and patterns is the "antirealist" position; from this position it is easier to regard the meaning of language as inherently tenuous, since the regularity of the patterns that give it meaning will constantly be intentionally or unintentionally disrupted. Similarly, talking about LLMs as seeing language as a series of patterns and statistical relationships that it can use to predict how a prompt would most likely be continued seems to take LLMs' use of language less seriously.

However, there's no contradiction between these two ways of regarding language, they're two sides of the same coin. Or, to speak more precisely, the meanings and understandings are a layer of abstraction that sits on top of the patterns and statistical relationships. (We could also say that the "realist position" on language is a layer of abstraction that sits on top of the "antirealist position"--this is typical of the relationship between realist and antirealist perspectives.) Meaning and understanding can be seen as emerging from patterns and regularities as long as those patterns and regularities adhere to certain assumptions, in the same way that we can recognize a computer as executing a program that contains objects with methods and properties, so long as the computer's hardware, logical operations and everything else in the lower layers of abstraction are functioning as expected.

I apologize if all of that sounded like post-structuralist nonsense, but I suspect that a certain philosophical misunderstanding of what language is may be causing certain distinctions to be drawn between LLMs' understanding and production of language and humans' understanding and production of language.

For an LLM to respond with a piece of text that it predicts is very likely to follow a prompt demonstrates a capacity to understand the prompt and respond appropriately. As the quality of responses improve and lengthen, the number of paths that would allow the AI to shortcut what we would regard as the "true understanding" with a weak facsimile of understanding eventually dwindles to zero.

I've noticed that the responses I get from GPT-3 are often vague and general enough to be compatible with several interpretations of the prompt, but ChatGPT's responses are noticeably lengthier and more specific to the point where I feel comfortable that it must have understood me correctly most of the time. Of course, humans have a somewhat greater preference for wrong-but-specific responses than LLMs, but this difference is only a matter of degree. In the end, the only way to provide a lengthy continuation of a sufficiently complicated and specific prompt is to actually understand the prompt.

Maybe I'm beating a dead horse and missing the point. Maybe we're all pragmatists that agree with the proposition that if an LLM consistently uses words meaningfully and correctly, then the LLM understands the words that it's using. In this case, I think I must be overrating ChatGPT's closeness to AGI either because:

(1) I'm missing important language use failures where ChatGPT is less fluent than the average human. Or,
(2) I'm overrating the value of understanding language, and underrating both the number of other elements necessary for an AGI, and the difficulty of adding those other elements.

I have further points I could make in favor of my characterization of ChatGPT as having a human-like grasp of language, but I'll put them down in this email's postscript. I'll move on to a discussion of the only important step necessary for ChatGPT to become an AGI--giving it sufficient memory functions. 

LARGE LANGUAGE MODELS, MEMORY AND SALIENCE
Let's imagine that we have created an ChatGPT-like LLM to work as a therapist (or we just tell ChatGPT to play the role of a therapist). It will do fine at least through the first part of the first therapy session, but pretty quickly it's going to make serious errors when it forgets the clients' therapy goals or important facts about the clients life because those things have fallen out of the chatbot's context.

Given enough computing power the problem can be solved in various ways. I'll guess at a couple possible solutions, although most likely the correct, optimal solution that doesn't blow the entire computing budget is one I can't think of. My point with these examples is to highlight that ChatGPT-like LLMs could use the same language understanding and production skills they use to continue texts to both recognize what they should remember, and to actually remember what they should remember. 

One possible solution is for temporary copies of the therapist bot to be made and yanked out of the session to chat with assistant chatbots who take notes on therapy goals, important facts about the client, and other types of things that the therapist should try to remember. Those bots keep those things in their context, observe the therapy session and intervene to help the therapist bot remember those things when the therapist bot needs to. Implementing the intervention is relatively simple, you just inject some text into the chatbots context that looks like:

Remember, the therapist thought to herself, [insert therapy goal or important fact about the client here.]

How the assistant bots know when to intervene to remind the therapist bot is the much more difficult and interesting implementation question; what can play the role of the gatekeeper to prevent unnecessary interventions polluting the therapist bot's context like a neurotic human's intrusive thoughts? Theoretically, you could have each assistant bot intervene and not intervene, and then have the therapist bot or a third bot judge whether the therapist's response was better in the presence or the absence of the intervention. Obviously this solution would be pretty expensive, but I think it's interesting as a thought experiment.

Maybe a better solution is for the therapist bot to frequently ask itself "As a therapist, what am I expected to remember from this exchange? What can I learn from this exchange that would help me better help my client?" ChatGPT-like LLMs are already able to extract the salient and relevant information from the exchange, so the therapist bot should have no problem answering its own questions, and determining what exactly it should remember.

Is it possible to use the therapist bot's understanding of what it should remember to be trained into the therapist bot so that it will remember the information when it is needed? Isn't an LLM like ChatGPT capable (or close to capable) of encoding the information as elements of a training dataset? If so, then it is only a matter letting the LLM retrain itself as many times as necessary throughout each therapy session.

This solution is much more interesting, since such a technique should be generally applicable, and should allow an LLM placed in any given role to become better and better in that role. I would argue that a program that can learn to be a better and better therapist, lawyer, or teacher is a type of AGI. (Interesting note: the changes that the LLM would apply to itself would be written in the first instance in natural language, so they would be relatively easy to monitor for AI safety purposes. Of course, this may not completely prevent the problems associated with convergent instrumental goals, especially if we take seriously the possibility of intentionally unsafe misuse of the technology.)

That's all I've got!
John Hempfling

POSTSCRIPT: Further characterizing ChatGPT's understanding and production of language
With some difficulty, I forced ChatGPT to write this argument for me. (The difficulty appeared to stem from the fact that although ChatGPT was familiar with this argument, it doesn't agree with it, so it was a bit loath to describe it fully. It was adamant that this argument is not widely accepted, and seemed to be strongly discouraging me from taking it seriously):

"The main way that brains and machine learning models process language is through the manipulation of symbols or representations, and the use of patterns and regularities." Furthermore,

Both brains and machine learning models process language as a set of symbols or representations that are associated with certain meanings or functions. For example, a word or a phrase is a symbol that is associated with a certain meaning, and the way that brains and machine learning models process these symbols is fundamentally similar in that they both use patterns or regularities to make predictions about how the symbols are likely to be used in different contexts.
 
Both brains and machine learning models can learn from experience and adapt their understanding of language over time. For example, a person who is exposed to a new language can learn and adapt their understanding of the language over time, and machine learning models also can learn and adapt their understanding of language based on the data they are trained on.
 
Both brains and machine learning models are capable of generalizing their understanding of language beyond specific examples they were exposed to, they can make predictions and understand meaning in new context and examples they haven't encountered before.
 
Both brains and machine learning models are information processing systems that use patterns and regularities to make predictions and understand the environment around them. In this sense, the arguments for the similarity of the information processing methods of brains and machine learning models can be seen as the idea that brains and machine learning models are both essentially performing computations on input data to extract meaning and make predictions.

I believe these points are highly compatible with linguistic turn philosophy. Surely, words and letters have no inherent meaning, and their meaning has to be inferred, in the first instance, from patterns, regularities and associations.

People may argue that to understand words you have to either know what objects they are referring to, or be able to imagine those objects. My favorite example of learning the meaning of words without being able to directly experience or imagine the referent is Helen Keller's understanding of color:

When I feel my cheeks hot, I know that I am red. I have talked so much and read so much about colours that through no will of my own I attach meanings to them, just as all people attach certain meanings to abstract terms like hope, idealism, monotheism, intellect, which cannot be represented truly by visible objects, but which are understood from analogies between immaterial concepts and the ideas they awaken of external things. The force of association drives me to say that white is exalted and pure, green is exuberant, red suggests love or shame or strength. Without the colour or its equivalent, life to me would be dark, barren, a vast blackness.

Obviously, Keller fully understands how color is used and what its associations are, and therefore her understanding of color is richer than that of a toddler with sight. (Of course, I mean this specifically in the context of verbal communication, which is the only context that matters for the purposes of this discussion.) To paraphrase the pragmatist philosopher Charles Sanders Peirce, the meaning of a word is fully contained in how it is used (of course, analytic philosophy takes an equivalent position).

I have one simpler, maybe dumber, maybe more important reason for why I think it can be said that ChatGPT really understands what it is saying: I can tell when I'm talking to someone who really understands what they're talking about, and one that is bullshitting, and this one understands what it's talking about.

John Hempfling <john.m.hempfling@gmail.com>
Jan 23, 2023, 1:21 AM
to me

PPS I should correct or clarify my statement about a self-retraining AI becoming, a "better and better therapist, lawyer, teacher, etc." Of course, what I meant to say is that it would become better and better at producing a facsimile of its understanding of what a therapist, lawyer or teacher would say in the conversations it is participating in. One would expect that it would still be worse than the best therapists, lawyers or teachers by default, but I don't think this should stop us from characterizing such an AI as an AGI. Once you have an LLM driving its own retraining to change itself towards the goal of performing a role more successful, and that retraining is actually successful in allowing it to behave in a consistent and coherent fashion, you have an AGI, even if it is weak or misaligned.


Ian Hogan <grandmasteroftheuniverse@gmail.com>
Jan 28, 2023, 1:08 PM
to John

"As the quality of responses improve and lengthen, the number of paths that would allow the AI to shortcut what we would regard as the "true understanding" with a weak facsimile of understanding eventually dwindles to zero."

False. What you are missing here is the scope of how many ways the system can be wrong while appearing right, probably due to the scale of the number of dimensions involved. English has 5000 words (approximately, skipping drug and chemical names, etc). The human ability to construct a concept by concatenating words vanishes after about 100 words. So we could say that there are at most 5000^100 possible meaningful constructs. Indeed, the vast majority of those combinations are fundamentally meaningless, and I estimate that we are dealing with a number closer to 5000^25. Both of these are large numbers, but the problem is that large language models have almost unfathomably many dimensions to operate in. GPT3 has 1.75 billion parameters, but they are linked as a deep network, dozens of layers, such that it is capable of modeling objects in a space with potentially trillions of dimensions, compared to English's feeble millions. To say that GPT approximates human language so well that it can't possibly be anything but a well fit model of human language, is to say that the intersection of a three dimensional shape with a plane is a square, therefore it must be a cube (and not a pyramid, bi-pyramid, finite, infinite, regular, irregular, etc, but one thing is for sure, at some axis it has a slice that is square). Comparing 2 to 3 dimensions makes the problem plain, comparing billions to trillions is often confusing. 

"In the end, the only way to provide a lengthy continuation of a sufficiently complicated and specific prompt is to actually understand the prompt." 

False. Again, the lengthy continuation of a fiddly prompt is just a subset of an n-dimensional space, like a hyper cube or a 50k dimensional star that has a different point in each cardinal direction. There are infinitely many 50,001 dimensional shapes that intersect 50k dimensional space such that the exact star I described washes out, but in the remaining dimension, anything goes. Same as expanding a square into 3-d allows infinities of possibilities, and Cube is only likely insofar as humans thinking about squares usually think about cubes. 

While I have no beef nor shade to throw at your post-structuralist sense (not, nonsense, since it is intelligible and possibly a very strong outlining of ideas, at least for humans), let's consider a very weird way to consider language. As a projection from the n-dimensional space of human thought and interaction with the world, into the space of finite collections of words. This may provide us extremely little insight into HOW the projection works for humans or computers, but it provides us a clear idea of the number of dimensions, and so makes plain the analogy I want to make. To say that because the model accurately builds projections into the space of finite collections of words, therefore it must have the same pre-image (human-understanding of the concepts being projected) is the same as to say that every object that casts a circular shadow is the same 3 dimensional shape, or up to a few variations the same: spheres and cylinders. However, a totem casts a circular shadow at noon. And indeed, there are whole classes of shapes that are rotationally projection invariant, but we cannot conclude anything much about their pre-image. 

Consider two cases, one in which we ask ChatGPT to describe the 3 dimensional shape depicted in an svg (an image file rendered in text, so it can be parsed by LLMs), let's say the image is of a cube. The response might be: "The image depicts a cube, a three dimensional regular solid, with 6 corners and sides, each side a square, the top is shaded green and the two other visible sides are red, but the bottom and back sides are not visible."

In the other case, we prompt: Repeat after me, "The image depicts a cube, a three dimensional regular solid, with 6 corners and sides, each side a square, the top is shaded green and the two other visible sides are red, but the bottom and back sides are not visible."

In this case, we can neither determine the prompt from the answer, nor whether the machine understood the prompt. 

"(2) I'm overrating the value of understanding language, and underrating both the number of other elements necessary for an AGI, and the difficulty of adding those other elements."

Yes. AGI has to be an agent that has goals in the real world. ChatGPT only has goals in the space of language, its only goal is to provide apparently meaningful and correct responses to prompts rendered in language. Being a good therapist is actually an example of something that an LLM carefully tuned and configured would do pretty easily. What it won't do at all, is operate outside that space. 

Consider that ChatGPT is loaded into a mobile robot, and given eyes and ears. Will it join you on a walk if you gesture? If so, why? Because it enjoys walks? Because it values time with us? Because it believes that we value time with it? Because someone wrote an interpreter that allows it to express some language in movement, and the movements associated with joining you on a walk are consistent with the prompt that was mapped to by the visual processors that picked up the gesture? Or because it has a fixed 1.75 billion node set of parameters that spit out cervo instructions to render walking as an output that it was trained to by gradient descent over billions of examples it was provided?

Mostly the last one, and it would take years of development to get it to work once, at this point. 

Don't forget, I trained a model on 50,000 images of noise, and it was able to guess at images from 10 categories with 30% accuracy, a statistically significantly better than chance. Does that model 'understand' what a newt is? No. It just has the result of firing thousands of shots around the images of newts into a peg-board. There's a newt-shaped void, and it has that. It's aluminum foil wrapped around meaning and squished by math until it looks the same. 


Ian Hogan <grandmasteroftheuniverse@gmail.com>
Jan 9, 2024, 8:06 AM
to John

Hi,

I've had it on my todo to write a blog about ML, Guessing and Knowledge for a couple years now. I think a lot of the material in this exchange is probably where I'd start. Would you be ok with me quoting you, or quoting you anonymously, or would you rather your content stay off the internet where it will be scraped and trained into the next large language model?

Regards,
-Ian


John Hempfling <john.m.hempfling@gmail.com>
Jan 10, 2024, 10:41 AM
to me

This draft has been sitting in my drafts for months. I think I forgot to send it?
______

Yes, yes, it seems we don't disagree regarding ChatGPT and its capabilities, just regarding human thought, language and the definition of AGI.

Your multidimensional analogy is perfect for explaining this distinction. You wrote,

"To say that GPT approximates human language so well that it can't possibly be anything but a well fit model of human language, is to say that the intersection of a three dimensional shape with a plane is a square, therefore it must be a cube (and not a pyramid, bi-pyramid, finite, infinite, regular, irregular, etc, but one thing is for sure, at some axis it has a slice that is square). Comparing 2 to 3 dimensions makes the problem plain, comparing billions to trillions is often confusing. "

I am not trying to make any statement about the 3 dimensional object, it is a matter of indifference to me whether it is a cube, a pyramid, bi-pyramid, etc. My position is that linguistic meaning and reasoning does not extend beyond the limits of the 2 dimensional object of your analogy. Essentially I'm asserting that if the intersection of a plane with a three dimensional object is a quadralateral with four right angles, then that intersection really is a rectangle, and whatever the shape of the 3 dimensional object is not particularly important. Semantic meanings in utterances are limited, and understanding the connections between the utterance and the deeper structures in the speaker's mind is probably impossible, and certainly not necessary to properly interpret the meaning of the speaker's utterances.

Before I got into linguistic turn philosophy, I studied pragmatist philosophy, a much earlier and simpler set of ideas about language and thought. The central tenant of pragmatist philosophy is that the entire meaning of a word or a sentence is contained in the ways that that word or sentence can be used. Ordinary language philosophy is based on a similar view. Post linguistic turn philosophy also likes to make statements about the limits of language, while at the same time taking the view that there is nothing that is knowable (or discussable) outside of the realm of language. The fundamental move here is to argue that there are not really deeper meanings beyond those that are accessible to the ordinary person with an ordinary grasp of language, and that gestures to such meanings are due to either some misunderstanding of ordinary language, or some philosophical mysticism. A somewhat less comfortable approach is to emphasize that we have no knowledge of real objects, and so our facts and theories can be true or false only in the sense of their practical implications for action. One of my favorite analyses from this approach is Lakatos's philosophy of the history of science, which takes the approach of evaluating the success of different scientific research projects across the history of science based on how well they are able to make novel predictions that are later proven true.

Let's return to your analogy, however. is better than any kind of misunderstanding of language or false realism. It gestures at the really existing shape of language and that that space that language fits within is obviously smaller than the space that contains the deep structures of our minds or the neural networks of LLMs. Thus, a very, very large number of different configurations of those neural networks are basically compatible with similarly adequate language uses.

I don't know what it means for a system to be wrong if its responses appear to be right consistently enough. Any possible system that produces utterances will be imperfect and produce some incorrect utterances; it is not possible to right 100% of the time. If in its everyday use the system's utterances are correct 95% of the time (a 5% fail rate), I think that system would best be described as mainly correct with a still quite significant number of flaws. I think ChatGPT has already exceeded this bar.

I don't entirely understand your "describe the shape depicted in an svg" example. If it passes 95% of svg tests, you might conclude that it understands the semantic meaning of "describe the shape depicted" and is able to parse svgs adequately, or you might conclude that it is failing at one of those elements of the task. Similarly, a battery of "repeat after me" tests can demonstrate whether the AI understands the semantic meaning of "repeat after me," but you don't otherwise shed any light on the AI's capabilities. Again, the question of whether or not it is able to pass or fail these tests is central to judging its capablities and understanding in the same way that the way people react to different tests or in different situations informs our beliefs about what the person knows, understands and is capable of. After a sufficient number and variety of tests, it is silly to continue to wonder whether a person's understanding is right or is actually wrong but simply appears to be right. Ultimately, we can't absolutely prove that other people actually understand something correctly or just got really lucky over and over. But beliefs like "the subject's performance on these earlier tests of types A, B, and C suggests that they have certain knowledge, understanding and capabilities such that we expect them to pass >95% of tests of type D" are useful because they allow us to make true, novel predictions about the behavior of the subject in the future (assuming that the evidence produced by tests of type A, B and C was adequate and appropriate, and accepting the possibility that we will sometimes misjudge the subject). Again, I don't think we disagree on any of this.

"Being a good therapist is actually an example of something that an LLM carefully tuned and configured would do pretty easily. What it won't do at all, is operate outside that space."

Yes, we agree on everything except what an AGI is. My bar for general intelligence is just lower. If you think I should call it a "weak AGI" or something, I think that is fair.

You wrote:

"AGI has to be an agent that has goals in the real world. ChatGPT only has goals in the space of language, its only goal is to provide apparently meaningful and correct responses to prompts rendered in language."

Again, we agree on everything except the definition of AGI. The goal of providing meaningful and correct responses to prompts rendered in language is extremely general. In fact most--and possibly all--tasks can be translated into a task within this space. For example, "give complete instructions on how to create an AGI" is itself a task that can be expressed in language space, and for which an adequate response could be given within language space.

The novelty limitation
Now, I don't expect ChatGPT-like LLMs to do anything like this, or anything particularly novel and innovative. They have the implicit goal of, "give a response that a human would give (i.e., a resonse that looks like the training data), and that a human would like (i.e., a response that look like the responses that have been given positive feedback, and do not look like responses that have been given negative feedback)". (Obviously, on topics where the training data contains a lot of inaccuracies, or where the AI has been given feedback that discourages correct answers and encourages incorrect answers, the LLM will pursue its goal by giving inaccurate answers.)  Developers might try to show an LLM that they like novel-seeming responses, but their ability to show this is limited by their own biases, as well as the fundamental design of this type of LLM. I expect that LLMs of this type will always be averse to novelty. This means they will be bad at certain types of tasks that require true novelty, like developing new, novel scientific theories, or new forms of literature.

I'm guessing that the only way that an AI can get around this limitation is to have a utility function or something similar. But as Robert Miles describes, utility functions are very dangerous. So, it might be for the best that we'll have weak AGIs with amazing human-like capabilities before we have AI's with goals that aren't centered on imitating humans.

John Hempfling


John Hempfling <john.m.hempfling@gmail.com>
Wed, Jan 10, 10:41 AM
to me

And, yes, you can quote me.


John Hempfling <john.m.hempfling@gmail.com>
Jan 10, 2024, 10:46 AM
to me

Lol, I guess I never finished the "Let's return to your analogy, however" paragraph. It is the weakest part of the argument, though, so I'm fine with that.
