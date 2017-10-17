## 3.1 Derivation of Approach

Many issues, models, and proposals have been considered for the purpose of achieving consensus regarding private cryptocurrency development.  Our model utilizes many components of these other proposals. Simpler models may have been desirable, but could not satisfy all of these important values and conditions:

The fundamental model of network value:

N^2*S*I

where N is the number of nodes and N^2 the number of possible connections, S the strength of the connections and I the intelligence of the connections.

We can re-state these value dimensions with the terms:
### Network effect (N^2), Network Support (S), Intelligence (I).
Having this model of network value means we can analyze the voting feedback system as an optimization problem. According to N^2SI, the network value is clearly extra sensitive to the number of people using the network. Therefore, in deference to some earlier models suggested, this document assumes that protection of the N^2 element of the network, which is primarily represented by the small investors, can not be sacrificed.

Because of the above privacy requirement, acquiring extremely accurate representations of these three value dimensions is not possible without choosing and using cloaked identity technologies which, while under development, are not yet proven and trustable in our estimation. Therefore, we relegate the possibility of using such identity technologies to future decision making, and strategize to make due with approximations of the three value dimensions noted above.

A voting layer is a mathematical entity (N^2, S, I ) used to calculate vote value/weight, and not to be confused with a particular type of node on the network. Simultaneously, the voting layers would have strong relationships to the types of nodes and accounts on the network because of the nature of those nodes and accounts.

#### It is important to understand that the layers are abstract in concept, and that the goal is to approximate the abstractions  successively better with time. Therefore, the original set of parameters put forth by this document is presumed to require future adjustments.

The Network Support value dimension is the easiest layer to represent in the system because network support data is already on-chain and strongly verifiable. Turtleflax and Veramis presented a model for this, which is close to passable, but hangs up on a few issues, therefore we will have to modify that model somewhat in order to fit it together with the other voting layers.

For the other two layers, two approximations have been identified, which we believe should share the voting weight equally. The first approximation is the use of voting exponents. In other words, an individuals vote weight is not directly proportional to that individuals holdings, but to the individuals holdings held to an exponent power.  What this means is say for an exponent of 2, An account holding 10 pivs would get 100 votes while for an exponent of 0.5 would an account holding 10 pivs would get only 3.16 votes. The exponent effects different account sizes differently such that exponents smaller than 1 benefit small accounts while exponents greater than 1 benefit large accounts. While "quadratic voting" (exponent 0.5) is a practice of some respect historically, we can not directly follow that path for multiple reasons.

* Most significantly, the requirement for privacy dictates that simply using square root voting to protect small investors does not work because large investors could too easily game the system and pretend to be many small investors by dividing down their accounts. Therefore, to solve this problem, we merely needed to admit that protecting only small investors is a flawed concept. Benefits given to small investors need to be balanced out by benefits given to large investors. Therefore, a square root vote accompanied by a squared vote gives both small investors and large investors benefits.  The square root vote would be a good approximation for the network effect layer.  The squared vote a good approximation for the intelligence layer, since large investors should take an interest in the development of the currency intelligence, so as to benefit the value of their holdings. Giving a squared voting layer for this purpose should eliminate most motivation for players to game the layers because optimizing ones accounts to benefit the vote count for one layer simultaneously damages ones vote count for the other layer leaving the gamer little to no net benefit for gaming.
* The second issue with earlier quadratic voting models in circulation is that the sale of votes and redistribution of funds  presents conundrums, so we simply do away with those features.
* The third issue with earlier quadratic voting is that when we use squared voting as its counterpart for the benefit of large investors, we will likely have too small of a voting sample size for that layer because large holders will be able to outweigh too many smaller holders. Therefore, to aid the voting sample size problem in the squared layer, we suggest moving to exponents other than 0.5 and 2.  Using exponents of 0.6 and 1.66 should solve this problem.

#### The system will be simple for the end user to use because all of the voting math is handled by computer. The voting/feedback system will not initially require massive amounts of re-coding the system because the voting math will primarily operate on data already present in the system. 