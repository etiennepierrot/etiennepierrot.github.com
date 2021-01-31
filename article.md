# Scientific method and Software Engineering


## We need to build **predictable** systems.

What's the thing we hate the most about software? Unpredictable behavior. When developers begin to be surprised by how their software behaves, big troubles start. When teams hope that it will work, organizations will think that developers lose control. Sometimes, developers know how the system behaves, but they do not understand the exact initial requirement. And, even in these conditions, companies can make revenue and grow. Backoffice report bugs, but no way these tiny bugs replace in the next sprint; this brand new feature that the sales team needs to onboard new clients. After all, the users can use some workaround. That's not a blocker. So, people deal with it until the day where the workaround became the official process that people teach to the new hiree. ** It's not a bug. It's a feature**. So, our first duty it's to deliver software that behaves as **client** expect. So we need to use the best methodology to achieve that.

## Two theories that make predictions: quantum physic and astrology

understand quantum physics (I didn't), or I trust scientists because they're looking serious. Or because I think it's impossible that the position of stars in space can affect our lives. Quantum physics told us things way more crazy than that. I don't know astrology well, but I'm pretty sure that astrology is built around principles that are coherent between them.  I trust Quantum physic because this theory makes actual predictions, and these predictions are very accurate, and the accuracy of this theory has allowed us to build incredible technology. When we heard about Heisenberg's uncertainty principle, some people could think that quantum mechanics is not very reliable. That's the opposite. The theory of quantum mechanics is the physics domain where the p-value (level of accuracy of studies, lower is better)  is the lower (and from very, very far). On the other hand, astrology didn't perform so well in terms of prediction. Sometimes, that's work. Sometimes not. Like bad software.


## The method

So if we need to build predictable systems, maybe you need to look to which method uses scientists to produce such a powerful model. And stay away from the way of working of an astrologer. And by the way, even people that believe in astrology didn't make critical decisions based on this prediction. They will not buy an expensive car based on fact than astrology predicts they will earn a lot of money. As developers, we are not scientists, but we should still looking their way of working.  But if we look closely, most of the good practices raised in the 20 last years are an adaptation of the scientific method. Obvious example : Peer reviewing

## Searching failure

When an astrologer spends time to find confirmation about these successful predictions, the scientist spends his time so search errors in existing theory. When an experience didn't have the behavior that the best theory of its time predicts,  when theory didn't work, the scientist has an opportunity to make a discovery. He's going to try to reproduce it, and he's going to try to find a better theory that can explain this unexpected result. That's how science progress. Instead of trying to prove that theory is accurate, scientists use methodical doubt to build knowledge. And this methodical doubt is at the heart of my favorite development method: **Test-Driven Development**. When the non-TDD practitioner tries to confirm that he has done a correct implementation by writing his test after, the TDD practitioner starts by proving the system's deficiencies. Once that done, you are allowed to write the simplest solution to a problem that you have established. That's a fantastic way to have a substantial safety net against confirmation bias. By writing tests after implementation, a developer is highly influenced by his implementation. Implementation detail that leaks into tests suits make maintenance and refactoring complicated.

## Occam's razor or the law of parsimony: Entia non sunt multiplicanda praeter necessitatem.

The Occam's razor allows scientists to choose which theory to choose between both to explain something. Maybe the less parsimonious is the good one. But until you prove that the more parsimonious is wrong, you should stick to it.   
The third law of TDD is just an adaption of Occam's razor for code : "You can't write more production code than is sufficient to pass the currently failing unit test."  That's another great advantage of TDD. he prevents you from falling into the worst plague of Software Engineering: over-engineering. Because it's very complicated to find a relevant test that justified an over-complicated choice.  It's easy to find complex solutions to simple problems, but it's more complicated to find a relevant use case that justified complex design.

## Backward compatibily (not sure to add this part)

<!-- A major problem in Science is when you have two theories that are capable to make great predictions in different field but are not compatible between them. Classic example : the nature of the light. For Newton, light was a corpsucule that has infinite speed. For Maxwell, light was electro magnetic wave with limited speed. Scientists was kind of stuck with that. Because they couln't reject one of those theory, because separately theses gave incredible results. So scientist's communauty agreed on an Ad-Hoc hypothesis around the concept of "Ether"; a kind of matter that was supposed the medium of propagation of light. Something not really proven, but this ether allow scientist to have a concept that make both great theories compatible. In 1887, Michelson and Morley try to make an experiment to prove the existence of ether. The result of the experience was quiet different from what was expected. Instead of proving the ether existence, this experence bring more confusion. So, the problem remain : two great theories incompatible between them. Until 1905, where a guy in the Patent office in Bern publish a paper called "On the Electrodynamics of Moving Bodies". In this paper, the author, Albert Einstein propose a new way to explane how light behave and gave explanion to the strange result of the Michelson and Morley. This paper was in fact a new theory that redefine our understanding of time and space : The special relativity. -->

When a scientist prove with experience that a theory is wrong. Scientist need to elaborate a new theory that explain the previous experience and all other experience that the old theory explain. If not, not way that scientific community will adapt your theory if the new one is not at least as good as the previous one. Interesting anecdote about that, when Einstein start to think about a better theory that explain gravitation than Newton's theory, other scentist like Max Plank, tried to discourage Einstein to that path. Scientists was aware that they are some very tiny drawback in the Newton's theory like she's not performing so well to predict mercury trajectory. But except that, Newton theory was so great that he seem to be impossible to propose something better. But Einstein has the deep conviction that there are something wrong at the heart of Newton gravitation theory. So from 1907 to 1915, Albert Einstein work very hard to bring a new theory that was "backward compatible" with Newton theory but perform also in some domain where Newton was wrong : The General Relativity. 

So we have already in our set of good practices, something that allow us to not deliver software that are not inline with previous requirement : Continuous Integration. We can see CI like a cheap way to check if our new model/theory is compatible with all tests/experiences that has been made in the past. That a luxary that scientists didn't have. Tests are cheap to execute. With computing capabilities on demand that cloud platform offer us, we have the abilities, to check in couple of minutes if our brand new refactoring is align with requirements from the past. 

## Outcome of science is useful too

One interesting thing, this last decade is the powerfull come back of functional programming. Even if the most popular languages are almost all Oriented Object, this languages do their best to offer funcational way of doing things (great video about that to link). The last releases of C# give me the feeling that microsoft are trying to bring F# feature to C#. Why a lot of developers appreaciate to code in functional style? In my opinion, it's because you have trust in the properties of your function. By sitting on a top if well-estasblish formalism, you can be sure that if you're following some rules (pure function, immutability, closure of operation ...), you can use all mathematican theoreme that apply to this. A great example of that is Monoid (link to Cyrille talk at SC London)
The other big trend of this last decade is microservices. It's well know that going to microservices is not that easy. A lot of companies fall into the trap of Distributed Monolith. Lot of coupling of between. 

Conway's law
Any organization that designs a system (defined broadly) will produce a design whose structure is a copy of the organization's communication structure.

— Melvin E. Conway

That law give us a big hint that a developer we will need to understand very well how organization are structured. On top of that, most of our system are build to be used at large scale. Even if each person is different, sociology is a science that's trying to understand how group of people behave. Nerver work with trading system, but I'm pretty sure that understanding about how traders behave should be useful to build this kind of system.

## Bayesian thinking

Let's be honest, all our decisions cannot be choose by just following a method. Very often, we should make trade off and sometime we make some "bet" about the future. Eg,  


## Conclusion

Even, if software engineering is relatively new field, we are sitting on giant's shoulder. 