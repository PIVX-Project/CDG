# Strategic Weight Analysis

## Table of content

3.1. [Derivation of Approach](#31-derivation-of-approach)

3.2. [Three Layers](#32-three-layers)

3.3. [Avoiding Information Starvation](#33-avoiding-information-starvation)

3.4. [Management of Feedback Loop Dynamic](#34-management-of-feedback-loop-dynamic)

3.5. [Staking Nodes](#35-staking-nodes)

3.6. [Masternodes](#36-masternodes)

3.7. [Vote Nodes](#37-vote-nodes)

3.8. [General Users](#38-general-users)

3.9. [The No Dancing Filter](#39-the-no-dancing-filter)

3.10. [Thresholding](#310-thresholding)

3.11. [Meta-Consensus](#311-meta-consensus)

## 3.1 Derivation of Approach

Many issues, models, and proposals have been considered for the purpose of achieving consensus regarding private cryptocurrency development.  Our model utilizes many components of these other proposals. Simpler models may have been desirable, but could not satisfy all of these important values and conditions:

The fundamental model of network value:

N<sup>2</sup>*S*I

where N is the number of nodes and N<sup>2</sup> the number of possible connections, S the strength of the connections and I the intelligence of the connections.

We can re-state these value dimensions with the terms:
### Network effect (N<sup>2</sup>), Network Support (S), Intelligence (I).
Having this model of network value means we can analyze the voting feedback system as an optimization problem. According to N<sup>2</sup>SI, the network value is clearly extra sensitive to the number of people using the network. Therefore, in deference to some earlier models suggested, this document assumes that protection of the N<sup>2</sup> element of the network, which is primarily represented by the small investors, can not be sacrificed.

Because of the above privacy requirement, acquiring extremely accurate representations of these three value dimensions is not possible without choosing and using cloaked identity technologies which, while under development, are not yet proven and trustable in our estimation. Therefore, we relegate the possibility of using such identity technologies to future decision making, and strategize to make due with approximations of the three value dimensions noted above.

A voting layer is a mathematical entity (N<sup>2</sup>, S, I ) used to calculate vote value/weight, and not to be confused with a particular type of node on the network. Simultaneously, the voting layers would have strong relationships to the types of nodes and accounts on the network because of the nature of those nodes and accounts.

#### It is important to understand that the layers are abstract in concept, and that the goal is to approximate the abstractions  successively better with time. Therefore, the original set of parameters put forth by this document is presumed to require future adjustments.

The Network Support value dimension is the easiest layer to represent in the system because network support data is already on-chain and strongly verifiable. Turtleflax and Veramis presented a model for this named Tango, which is compatible with PIVmetheus.

For the other two layers, two approximations have been identified, which we believe should share the voting weight equally. The first approximation is the use of voting exponents. In other words, an individuals vote weight is not directly proportional to that individuals holdings, but to the individuals holdings held to an exponent power.  What this means is say for an exponent of 2, An account holding 10 pivs would get 100 votes while for an exponent of 0.5 would an account holding 10 pivs would get only 3.16 votes. The exponent effects different account sizes differently such that exponents smaller than 1 benefit small accounts while exponents greater than 1 benefit large accounts. While "quadratic voting" (exponent 0.5) is a practice of some respect historically, https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2264245 we can not directly follow that path for multiple reasons.

* Most significantly, the requirement for privacy dictates that simply using square root voting to protect small investors does not work because large investors could too easily game the system and pretend to be many small investors by dividing down their accounts. Therefore, to solve this problem, we merely needed to admit that protecting only small investors is a flawed concept. Benefits given to small investors need to be balanced out by benefits given to large investors. Therefore, a square root vote accompanied by a squared vote gives both small investors and large investors benefits.  The square root vote would be a good approximation for the network effect layer.  The squared vote a good approximation for the intelligence layer, since large investors should take an interest in the development of the currency intelligence, so as to benefit the value of their holdings. Giving a squared voting layer for this purpose should eliminate most motivation for players to game the layers because optimizing ones accounts to benefit the vote count for one layer simultaneously damages ones vote count for the other layer leaving the gamer little to no net benefit for gaming.
* The second issue with earlier quadratic voting models in circulation is that the sale of votes and redistribution of funds  presents conundrums, so we simply do away with those features.
* The third issue with earlier quadratic voting is that when we use squared voting as its counterpart for the benefit of large investors, we will likely have too small of a voting sample size for that layer because large holders will be able to outweigh too many smaller holders. Therefore, to aid the voting sample size problem in the squared layer, we suggest moving to exponents other than 0.5 and 2.  Using exponents of 0.6 and 1.66 should solve this problem.
* The fourth issue is that extending power voting too close to the 0 line makes it extremely easy for large investors to steal small investor vote. Therefore, 0.6 power voting is for PIV holdings over 400 PIV.  To extend vote below 400 pivs, we slice 5% of the 0.6 power vote out and give it to PIVX dust between 50 PIVs and 400 PIVs, normalized to the rate of 1 piv = 1 vote. 

#### The system will be simple for the end user to use because all of the voting math is handled by computer. The voting/feedback system will not initially require massive amounts of re-coding the system because the voting math will primarily operate on data already present in the system.

## 3.2 Three Layers
If layers substantially disagree with one another on an event, then there is evidence that the proposals involved need deeper understanding and development. Aligning each of the layers with a legitimate dimension of value further tunes the voting apparatus to protect value in the system. It also shows us the dynamics of that value as we watch the voting play out over time.


## 3.3 Avoiding Information Starvation


Optimal decisions can't be made from a dearth of the information needed to accurately represent reality. . The infamous 'Tweed' declared, "I don't care who does the electing, so long as I get to do the nominating", because in a two party decision, by the time both candidates are picked, many of the important decisions have already been made. This principle remains widely and effectively exploited in complicated ways. However, proper information management makes it difficult to play these sort of tricks. For those interested, these videos provide additional information concerning "first pass to post" and Tweed tactics, respectively https://www.youtube.com/watch?v=s7tWHJfhiyo&list=PLPZwr9rnuY9pr4InUaLfjmX757UfE-DVY  https://www.youtube.com/watch?v=PJy8vTu66tE

#NOTE- Questionable paragraphs- Historical voting math analysts have studied various voting systems, but normally not under this fundamental understanding. This is evident by the fact that many models of voting systems show up in the studies which are clearly information starved. First past the post voting systems as in common use today being perfect examples.  Therefore, many attempts to create information starved voting algorithms of various flavors all result in a decision making apparatus that misbehaves as is described in the first past the post voting video above.  Furthermore, it is a first step towards Tweed voting.

In a universe of "for every action, there is an equal and opposite reaction" for example, a voting system that does not include negative feedback (a negative vote) is not representing a fundamental truth about reality.  Reality literally insists on negative feedback, and will find it in whatever way necessary.  If negative feedback isn't explicitly on the ballot, then the ballot is information starved, and invites someone to find out how to play the role of negative feedback. In the first past the post voting system, Negative feedback naturally appears because of the natural narrowing of the party count down to 2. For a two party system, a vote for one party is identical to a vote against the opposing party, and nature's inherent requirement for negative feedback is filled, but at the cost of monopoly and near-monopoly over the candidate pool, Tweed voting style ( https://www.youtube.com/watch?v=PJy8vTu66tE ), which severely damages the voting system by simply removing choices that the voting pool may deeply desire.  Fortunately, PIVX was born with +/0/- voting. Therefore, this issue already partially solved, except that with just one option up for vote and yay or nay to go with it, the two-party system is already also born into the system. Therefore, vote option monopoly is expected.

To solve the two party system and vote option monopoly problem, we need a combination of +/0/- voting/feedback and the possibility of multiple vote options. Vote options meaning: "I want A or B or C, but not D". Because people can't properly manage a large number of vote options in their minds, more than four vote options may begin to become unmanageable. After long discussions, it was concluded that for the macro-vote (the combined multi-layer vote) the best vote counting algorithm available is +/0/- iterative ranked with null option. Before the macro-vote, the individual layers act only on the +,0 and - constituents of the ballots in order to reject excessively negative options from the vote. The counting of such votes shall be described in "Ballots and Counting".



## 3.4 Management of Feedback Loop Dynamic
https://www.youtube.com/watch?v=5HNmsBaVmZs

The above video demonstrates that experts are concerned about government decision processes being influenced by special interest groups. What they blatantly fail to note is that

* You have multi-billion dollar decisions being made by as little as 11 people. Clearly the "gain factor" is too high, which makes them  susceptible to too much influence created by the heavy monetary weight of the decision. This is a standard feedback loop problem .. or a couple of them in tandem that we might call "high impedence feedback loop" and "high gain factor".  In this Scenereo, the energy in the system is so much greater than the energy in the feedback route, that the feedback information is corrupted by the system energy, creating either distortions, or parasitic patterns, both in the case of current governing practices .. Change the committee size to 110 in stead of 11, and suddenly the group is ten times more expensive, complicated, and difficult to manipulate by special interest groups. The video goes out from the assumption that the committee size can't be questioned.  This is utter nonsense. The true problem they are fighting and don't want to admit is over-centralization.

* The tuning of the Unite States Federal Government voting feedback loop (for example) dramatically shifts with population rise because delegate to population ratio is a form of "gain factor". Feedback loop stability is extremely sensitive to loop gain factor. Roughly in the 70's they want to attribute exaggerated corporate influence on federal decisions to transparency laws. Said transparency laws may in fact benefit special interest groups more than the public because those special interest groups are able to pay lobbyists to monitor and influence committee members. However, they fail to properly note that people can't know if their delegates are representing them without transparency, and wish to set up a trusted system. This is an extremely dangerous move to make because .. remember ..  because of increased population size, the tuning of the system is no longer identical to the 1970's and we can not simply trust that the system will then reconfigure back to its 1970's behavior. They fail to consider the possibility that the rise in corporate influence on decisions is also caused by the larger and larger sums of money wielded by corporations (and other groups) doing larger and larger business with more and more people while the federal decision maker teams/committees remain the same size. Setting the federal decision body sizes in stone while the population grows exponentially is basically setting up a feedback loop that constantly re-tunes towards less and less stable numerics without apparently any voice standing up to say ... "hey, this loop is constantly de-tuning its self". We have been begging on hands and knees and praying for exactly this kind of problem to show up. These so called experts fail entirely to suggest the real solution to the problem, which is larger committes and gain factors limited to approximately dunbars number squared (22500). Interestingly, the original constitution used the number 30,000, an acceptable number, but that number was overridden when the size of congress was limited. That limitation appears from a systemstheoretical perspective to be an act of class warfare. However, it is also indistinguishable from being an act of ignorance... an accident (?) which promotes slow domination of oligarchy over time.

https://en.wikipedia.org/wiki/United_States_congressional_apportionment

With Current gain factors for congress members in the ballpark of 700,000 (people/representative) this is a number we would drastically reduce if at all possible in any single amplifier gain stage because of the inherent instability of that kind of gain factor. We can eradicate this entire concern with a single move.  Limit the number of accounts a delegate may represent to 30,000 ( just over dunbars number squared .. many people have multiple accounts, justifying higher numbers, but team members have argued to reduce potential powers of single delegates.)

https://en.wikipedia.org/wiki/Dunbar's_number

 Dunbars number squared represents the concept of "a friend of a friend". If the individual representing you isn't a friend of a friend, then it's doubtful that you are being represented.



## 3.5 Staking Nodes

Because staking is a network support function, staking node feedback will be counted into the network support layer proportionally with the number of PIVX staked. Unless there is further information to process, Staking nodes and Masternodes may each acquire 50% of this layers vote, although this is a tunable quantity. Many have argued against using vote nodes, leaving vote nodes as a last resort for acquiring adequate vote activity in the N<sup>2</sup> layer. Since vote nodes are a last resort to acquiring adequate N<sup>2</sup> vote, this layer may shift if vote nodes are actually implemented so that vote node holders (not those whom they represent) acquire something like 7% of the total S layer vote.

## 3.6 Masternodes

Masternodes currently present us with a conundrum, because they are pre-defined to be accounts of exactly 10k PIVX. Individuals won't be holding their own preferred coin numbers in those accounts. It is known that many individuals hold quite a few masternodes, but without explicit data, this can not be directly counted into the voting scheme. Unless the community opts to link masternode accounts, masternodes can only be assumed to be components of larger holdings, therefore we reduce their network effect vote by a predefined amount, and increase their intelligence vote by the same amount. 35% decrease/increase. For exponents of 0.6 and 1.66, this equates to the assumption that masternodes will typically be held by people who have 30k PIVX total.  This is an approximation, but without better information, we can not make the approximation more correct.


## 3.7 Vote Nodes
Because most investors won't have the time and energy to invest in making community decisions, delegation is an important option to consider. Discussions of doing delegation have had rather mixed results, leaving the option for delegation as neither popular nor unpopular. Therefore, we choose to defer the decision as to whether or not delegation is actually used to a later date when it can be elucidated as to how necessary the option is. < br />
The primary value of the concept of vote nodes is in the creation of delegates who can fill that role.  Unlike traditional governing systems, Individuals would not have delegates imposed upon them by majority rule, but will have the freedom to choose their favorite delegate. This helps to get a wealth of information into the decision making system.

There will not be a limit on the number of delegates other than the natural behavior of a free market. Managing feedback loop dynamics does however demand a limit on the number of accounts that a single delegate can represent. There is no hard limit on that number theoretically, but we will give centralization some benefit of the doubt and use 30,000, which is somewhat higher than Dunbars Number Squared (22500).  Part of the reason for this high estimate is the assumption that many people will have multiple accounts.

The vote of vote node holders themselves has a place in the network support layer, since they do in fact support the function of the network. The votes that they represent belong in whatever layers they would have influenced otherwise.

Vote nodes should be allowed to implement delegated proof of stake (DPOS) or staking pools with their adherents. The efforts of those individuals can be supported by DPOS reward percentages, as well as whatever agreements they wish to make with their adherents.



## 3.8 General Users
All users vote according to PIVX holdings in layers N<sup>2</sup> and I according to the powers (exponents) given to those layers. This includes all node holders. However, there will be a minimum holdings requirement which may change over time. Early suggestion for this number is 500 PIVs. If this number falls too low, it becomes too easy for large holders to steal N<sup>2</sup> vote as well as too easy for uninterested parties to influence decisions. If it rises too high, it becomes too difficult for small stake holders to acquire that voting power.

## 3.9 The No Dancing Filter
A consensus model deriving its voting weights simply  by what each wallet is holding at voting time would  erroneously overrepresent traders who'd only recently bought their PIVX. Value comes from those who hold their PIVs, as should the votes. A good measure for this is the 'Exponential Moving Average'.
The EMA has a few neat properties. If the holdings on a wallet were to suddenly jump from zero to H, the EMA would steadily respond as

f(t)=H(1-e<sup>-ct</sup>})

If the wallets value jumped back to zero, it's EMA would respond at the rate

f(t)=He<sup>-ct</sup>}

Where (H(t)) is the holdings of a public key at time t. To be implemented, the EMA can be calculated by tracking the time and values between transactions. For example, suppose the last transaction occured T in the past, then:

f(H(t)) = (1-e<sup>-cT</sup>)H(t)+e<sup>-cT</sup>f(H(t-T))


If it happens these calculations are too cumbersome to perform on every transaction, an even further simplified model can be used, which simply approximates a wallets holdings by its contents iteratively say, every two weeks, so that if $e<sup>-cT</sup>=C$ and the iteration is n, then

W[N]=(C)W[N-1] + (1-C)H[N]

where W and H are 2 series denoted with array indices. W the filter output weights and H the holdings of a PIVX public key at snapshot intervals.  C is a filter constant between 0 and 1. PIVX will use 2 week intervals if coders choose the interval option in order to avoid colliding with the common monthly financial rhythm. It will also use a "time constant" of 4 months, meaning that 63% of a holders voting power will accrue in 4 months regardless of whether the coders choose to calculate at every transaction or at intervals.   

The electronics engineers know this equation as an 'IIR' filter.
For 2 week intervals, Four months then requires 8 iterations of the equation. So to get the proper value of c for a time constant of 4 months, we set H to 1, therefore eliminating it. And tune the equation to get us a value of 0.63 after eight iterations.

W[N] = W[N-1]C + (1-C)   <br />
now set w[0] to 0 and W[6] to 0.63 <br />
W[1] = 1-C <br />
W[2] = (1-C)*c + (1-C) = C-C<sup>2</sup> +1 -c = 1-c<sup>2</sup> <br />
W[3] = (1-c<sup>2</sup>) * C + 1-C = C-C<sup>3<sup> + 1 - C = 1-C<sup>3</sup>  <br />
. <br />
. <br />
. <br />
 W[8] = 1-C<sup>8</sup> = 0.63 <br />
C^8 = 0.37 <br />
 C = 0.37<sup>1/8</sup> = 0.883131174 <br />


## 3.10 Thresholding

### For standard votes

Historically, the concept of a democracy is "majority rule" or 51% takes it. A democracy tends to be predatory as the 3 wolves voting against 2 sheep idea demonstrates.  The concept of a republic was built up to try to alleviate the predation of the democracy. This normally implies a voting threshold of something like 60%. While this may in fact make it more difficult for predators to rule, what we interestingly see is that in this case, 3 wolves can still eat 2 sheep. In neither case have the wolves been separated from the sheep in the voting paradigm, so a wolf votes like a sheep, but eats like a wolf.

The three layer paradigm we present has something of the ability to separate the wolves and the sheep. This only works because this three layer model projects a new set of roles. It somewhat separates large stake holders from small stake holders. Historically, the wolves tend to be the large stake holders. Interestingly however, if we switch from wolf/sheep dichotomy to sadist/masochist dichotomy then we get something probably a little more true to reality. In the sadist/masochist dichotomy, the masochist occasionally strikes out in desperation and punishes the sadist, which is what the lower class sometimes does to the upper class in political settings. Therefore, the 51% vote tends to result in sadism/masochism .. a pattern normally identified as unhealthy.

The way these issues work is that people tend to play roles that work. So if you set up a system that disadvantages one role game for a different role game, then you effectively project the new role game onto the public mind in a long-term sort of statistical and tipping point way. So if you want a wolves and sheep game, simply set up a majority rule system. The majority will reliably prey upon the minorities. In what way the majority differs from the minorities. Separating the wolves from the sheep makes it possible to break down the sadist/masochist game. It may not always be possible to do this, in particular because there may be no easy way to make the distinction, but in a setting where the primary issue is account size, the two roles are in all probability distinguishable. Perhaps cryptocurrencies have a little advantage in this respect over other structures.

By creating a voting layer which substantially advantages an upper class, but that can't be fully enjoyed by an individual who wishes to divide down his accounts to steal lower class protection vote, we are projecting a different role game. We are suggesting to the upper class "don't be a wolf/sadist, be a leader. Be Prometheus and bring fire to man kind! Look at the value equation and see that playing the leadership role raises the value of the system for all, and that falling back to a predator role does you no advantage because it robs from you vestige of leadership." Add to that the inconvenience and problematics of gaming the system, and we expect most large investors to opt for the leadership role because it's just as powerful, but more fun, more open, easier to maintain and more glorious.  So, simply dividing up into the three layers as defined effectively solves the predator/prey problem in this one dimensional dynamic. Therefore, the 60% vote demand for the republic becomes redundant because it's designed to solve a problem that is already solved. We can move the system more easily and safely because protection for the various layers is already built in.

Unnoted by politicians and attorneys whith whom I have spoken, there is a second reason for a vote requirement substantially over 50%. If we go back to the intelligence equations in various AI models, we will discover that time, or number of iterations of the system, is a crucial element of intelligence algorithmic. We expect it to take more time to get a proposal substantially above 50% vote, and hence, we expect the quality of the resultant proposal to be higher. This conflicts in some cases with the need for an emergency decision, where time simply is not available.  So, what we are seeing here is that once the predator prey problem is pre-solved by layering, we can actually use the voting threshold for a different purpose. We can maximize system intelligence according to time requirement. We can impose a high vote requirement if there is plenty of time, and a lower vote requirement if there is an emergency.  Recalling that PIVX is using +/0/- voting so that >50% is net positive, I believe that reasonable sets of numbers for this are:

* Net Positive, Net Positive, Net Positive (all 3 layers) in case of emergency (such as severe bandwidth problems)
* Net Positive, Net Positive, Net Positive (all 3 layers) and requirement to beat the null option, which is given 5% up front advantage for the macro-vote in non-emergency situations.
* It's probably reasonable to have a vote forcing option where every 5% extra total vote outweighs a 1% layer blocking such that for example 15% total net positive in a non-emergency situation overcomes one of the layers blocking at -2%.
* If must-chose votes are required, the layer vote would  fall out of scope, the null option would be eliminated, and the macro-vote would simply choose the highest ranked option according to iterative ranked voting with null option.


Furthermore, there is the possibility that a large percentage of the public does not deliver information. The earlier threshold of required vote power exercised for a vote to pass was 10%.  A suggestion of 5% has been made in the interim. I believe that starting with 5% is a correct model, to assure mobility, and allowing this value to be altered as history writes something to look at. It will be appropriate to include into voting code a separable matrix structure of tuning parameters which may be both retained and updated over time so as to validate old decisions as well as make new ones.

## 3.11 Meta-Consensus
It would be naive to assume the ability to anticipate all possible dynamics of a consensus system which involves complex feedback, stochastic inputs, and therefore chaotic movement. Therefore, it is prudent that there are built in procedures for adapting the consensus mechanism itself. However, since Meta-consensus is on a more abstract level, it's impact can be even more unpredictable and sensitive to change than the consensus mechanism itself. For this reason, it is necessary that controls for Meta-Consensus be even more restrictive, with high threshold (see 2.9) and limited manipulability.

### For Meta-votes
Meta-votes are just votes with special thresholding for the meta-vote purpose.  These votes are allowed only to operate on the voting system or primary documents of the system its self such as the Manifesto and consensus model. Any meta-vote operating on normal system decisions is invalid and not to be implemented.  Any normal vote operating on the voting system or primary system documents is similarly invalid and not to be implemented.

In the case of meta-votes, the structure of the decision making system is in question. It's probably appropriate to have two separate meta-layers for voting.  One for the general manifesto, and a second for any other fundamental document.  In both cases, the layer blocking option falls out, and macro-vote (combined vote) dominates entirely.  However, the null option receives 15% advantage for changes in the manifesto, and 10% advantage for changes in the core documents.

Because the consensus model is assumed to be in a tuning phase for the first 8 years however, the 10% advantage for the null option shall be reduced to 5% for those 8 years.

