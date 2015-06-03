# Notes_6.3.15
Final Class Meeting Notes

Roadkill Example.

Richard's advice:

Think about: what processes could generate data like these?  Form hypotheses, and simulate data.  If you can write the algorithm (monks & manuscripts example from Richard’s course) that simulates similar data, you have your stats model.  It's possible to estimate the parameters from the data.

Misspecification testing - you know linear regression is inappropriate for this context, but what would happen if you used it?  Simulate data under all these assumptions that they violate, and see what happens.  Report your misspecification value with the rest of the model description.

Logistic regression might be unreasonably effective for this particular case even though in principle it shouldn’t work.

There's a series of sequential events before the data are entered.  Start w/ prevelance of the sp. at the site (real abundance, or density/unit area).  Then there's a probability the animals go on the road, which is a function of all the things that would lead the animal to get onto the road.  If you're not on the road, we don't detect.  Once you're on the road, you're either hit or you cross  If you get hit, someone sees you or they don't (could add other possibilities).  So there are really 3 probability models: detection, risk of getting hit, and risk of getting on the road (p1, p2, p3, which can all be logit-link linear models.  Could be three Bernoulli trials).  Can add cars/day as a parameter of both p1 and p2.

Could do partial pooling - every species gets its own intercept for each component.  Could also do guilds - get a lot of good pooling that way.  

How many animals are exposed per unit length of the road?
log(lambda sub s) = habitat + species + time of day + traffic + ..include some context.... + gaussian process that depends on the location
logit(p2) = traffic + species + 





