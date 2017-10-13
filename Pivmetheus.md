![](https://www.hicgrp.net/wp-content/uploads/2016/02/work-in-progress-500x261.jpg)

  # Pivmetheus consensus-proposal 
  ### Because an advanced digital assett deserves an advanced consensus model!
 

# 1 Abstract
The proposal we wish to introduce at this time is intended as an upgrade for the current PIVX consensus/voting system used for passing proposals into community acceptance. This proposal keys significantly off of presstabs original 3 layer model. However, for mathematical reasons, it has been adapted for optimum balance. 
#### This is the only model being presented that has the ability to successfully represent and protect small investors in the voting pool.  
The issues to be balanced into the model have been chosen as follows:

* Privacy
* Simplicity for the end user
* Protection and respect for crucial subgroups of the community 
* Most particularly, successful inclusion of the general usership as a substantial voting influence. This is especially important, because of the squared relationship between number of people/nodes and network value, wheras the other factors are only single power. 
* Maximization of network value and respect for the crucial resource of people in the system rather than only respect for numbers that mean nothing without people
* Balance
* Resistance to vote gaming
* Protection against common weaknesses of voting systems such as those of "first past the post" voting. These weaknesses can often be abstracted as vote information starvation. See this video for a lay-person explanation of that: https://www.youtube.com/watch?v=s7tWHJfhiyo&list=PLPZwr9rnuY9pr4InUaLfjmX757UfE-DVY
* Aggressive system tuning and protection against feedback loop parasitics. 


The model we will present is designed to respect the fundamental value model of a cryptocurrency. N^2SI  (described in detail later) It is also designed to respect the various conundrums of voting that result from currently used voting models that are starved of information. The last challenge to be managed is to curtail the arrival of common feedback loop misbehaviors that are evident in current politics as well as common feedback systems. Some explanation for the exact choices made will be given. 

#### While this document often makes use of the traditional word "vote", it is important to understand that it only appears to be traditional voting from the users perspective. The internal maths will be in the form of weighted network feedback. This appears to be the only means of accomplishing all of the above named goals. Therefore, it is appropriate to replace the word "vote" with a phrase such as "inform" or "informing" or "information acquirement" or "decision making event". The use of the word "vote" is for mental convenience of the reader only, and the meaning of the word shall be switched to an altered state defined by this paragraph. 

One of the fundamental features of this model is that it offers leadership to large stake holders (and potentially developers) while simultaneously securing protection for small investors. This is the inspiration for the name "PIVX-metheus".  

Note that voting systems are feedback loops that can exhibit unexpected behaviors. It is unrealistic to assume that one can construct a feedback loop and have it behave optimally from the very beginning.  Therefore it is strongly suggested to hold the voting system design as experimental for the first 10 to 15 years. This suggests strongly that for that time period, a meta-voting system be enabled which allows the voting system its self to be altered with a model that does not allow for one of the layers by its self to block the voting system edit. However, such a meta-voting system should only be activated based on references to behavior tuning issues.  Such tuning issues need to be made visible by means of building a set of system measures into a system status panel similar to what we see at this site:  http://pivx.masternodes.pro/  only much more advanced and informative. The existence of such a system status panel will for many reasons be a substantial addition the value of the cryptocurrency. 
















# 2 Strategic Weight Analysis



  ## 2.1 Derivation of Approach
  
Many issues were brought up and many models and proposals considered for the purpose of achieving consensus regarding private cryptocurrency development.  We chose a model that made use of many components of other proposals that were made. Simpler models may have been desirable, but could not satisfy enough of the fundamental values needed by the system.
These values are:



The fundamental model we begin with is that of the value of a network, which is approximated by the following equation:

N^2*S*I

where N is the number of nodes and N^2 the number of possible connections, S the strength of the connections and I the intelligence of the connections. 

We can re-state these value dimensions with the terms:  
### Network effect (N^2), Network Support (S), Intelligence (I).  
The goal is to maximize the value of the network by developing a feedback model which respects and protects these dimensions of value seperately, and as accurately as possible. According to the model, clearly, the value of the network is extremely sensitive to the number of people using the network. Therefore, in deference to some earlier models suggested, this document assumes that protection of the N^2 element of the network, which is primarily represented by the small investors, can not be sacrificed. 

Because of the above privacy requirement, acquiring extremely accurate representations of these three value dimensions is not possible without choosing and using cloaked identity technologies which, while under development, are not yet proven and trustable in our estimation. Therefore, we relegate the possibility of using such identity technologies to future decision making, and strategize to make due with approximations of the three value dimensions noted above. The resulting strategy looks very similar to presstab's original 3 layer proposal, but is adjusted in order to acquire some of the other values listed above. 

It is to be noted at this point that a voting layer is just that. It is a mathematical entity (N^2, S, I ) used to calculate vote value/weight, and not to be confused with a particular type of node on the network. Simultaneously, the voting layers would have strong relationships to the types of nodes and accounts on the network because of the nature of those nodes and accounts. 

#### It is important to understand that the layers are abstract in concept, and that the goal is to approximate the abstractions  successively better with time. Therefore, the original set of parameters put forth by this document is presumed to require future adjustments.  

The Network Support value dimension is the easiest layer to represent in the system because network support data is already on-chain and strongly verifiable. Turtleflax and Veramis presented a model for this, which is close to passable, but hangs up on a few issues, therefore we will have to modify that model somewhat in order to fit it together with the other voting layers. 

For the other two layers, two approximations have been identified, which we believe should share the voting weight equally. The first approximation is the use of voting exponents. In other words, an individuals vote weight is not directly proportional to that individuals holdings, but to the individuals holdings held to an exponent power.  What this means is say for an exponent of 2, An account holding 10 pivs would get 100 votes while for an exponent of 0.5 would an account holding 10 pivs would get only 3.16 votes. The exponent effects different account sizes differently such that exponents smaller than 1 benefit small accounts while exponents greater than 1 benefit large accounts. While "quadratic voting" (exponent 0.5) is a practice of some respect historically, we can not directly follow that path for multiple reasons.  

* Most significantly, the requirement for privacy dictates that simply using square root voting to protect small investors does not work because large investors could too easily game the system and pretend to be many small investors by dividing down their accounts. Therefore, to solve this problem, we merely needed to admit that protecting only small investors is a flawed concept. Benefits given to small investors need to be balanced out by benefits given to large investors. Therefore, a square root vote accompanied by a squared vote gives both small investors and large investors benefits.  The square root vote would be a good approximation for the network effect layer.  The squared vote a good approximation for the intelligence layer, since large investors should take an interest in the development of the currency intelligence, so as to benefit the value of their holdings. Giving a squared voting layer for this purpose should eliminate most motivation for players to game the layers because optimizing ones accounts to benefit the vote count for one layer simultaneously damages ones vote count for the other layer leaving the gamer little to no net benefit for gaming. 
* The second issue with earlier quadratic voting models in circulation is that the sale of votes and redistribution of funds presents conundrums, so we simply do away with those features. 
* The third issue with earlier quadratic voting is that when we use squared voting as its counterpart for the benefit of large investors, we will likely have too small of a voting sample size for that layer because large holders will be able to outweigh too many smaller holders. Therefore, to aid the voting sample size problem in the squared layer, we suggest moving to exponents other than 0.5 and 2.  Using exponents of 0.6 and 1.66 should solve this problem.  

#### The system will be simple for the end user to use because all of the voting math is handled by computer. The voting/feedback system will not initially require massive amounts of re-coding the system because the voting math will primarily operate on data already present in the system. 

## 2.2 Three Layers
The reason for using three seperate layers for the voting system is that each layer can be designed to provide its own perspective on voting events. We would be deprived without having two eyes, two ears or multi-channel audio/video. If layers substantially disagree with one another on an event, then there is evidence that the proposals involved need deeper understanding and development. Aligning each of the layers with a legitimate dimension of value further tunes the voting apparatus to protect value in the system. It also shows us the dynamics of that value as we watch the voting play out over time. 

To exemplify the meaning and behavior of this system, we will construct some example situations. 


## 2.3 Avoiding Information Starvation

https://www.youtube.com/watch?v=s7tWHJfhiyo&list=PLPZwr9rnuY9pr4InUaLfjmX757UfE-DVY

It is a fact, observable generically, that a decision making aparatus can not make the best decisions on a dearth of information. Furthermore, a system which makes optimal use of the information available to it makes quicker and more accurate decisions. The above listed video describes problems with "first past the post" voting, which are results of information starvation. Information starvation of the algorithms makes the system gameable, because it then becomes a matter of social gaming to position ones self to inject manipulated versions of missing information into the system. This is how "Tweed voting" arises. https://www.youtube.com/watch?v=PJy8vTu66tE .  It is important to be aware that highly intelligent people set up complicated means of Tweed voting that can be highly effective, but that a system with a solid foundation of information management makes it difficult to game the voting system. 

Historical voting math analysts have studied various voting systems, but normally not under this fundamental understanding. This is evident by the fact that many models of voting systems show up in the studies which are clearly information starved. First past the post voting systems as in common use today being perfect examples.  Therefore, many attempts to create information starved voting algorithms of various flavors all result in a decision making apparatus that misbehaves as is described in the first past the post voting video above.  Furthermore, it is a first step towards Tweed voting. 

In a universe of "for every action, there is an equal and opposite reaction" for example, a voting system that does not include negative feedback (a negative vote) is not representing a fundamental truth about reality.  Reality literally insists on negative feedback, and will find it in whatever way necessary.  If negative feedback isn't explicitly on the ballot, then the ballot is information starved, and invites someone to find out how to play the role of negative feedback. In the first past the post voting system, Negative feedback naturally appears because of the natural narrowing of the party count down to 2. For a two party system, a vote for one party is identical to a vote against the opposing party, and nature's inherent requirement for negative feedback is filled, but at the cost of monopoly and near-monopoly over the candidate pool, Tweed voting style ( https://www.youtube.com/watch?v=PJy8vTu66tE ), which severely damages the voting system by simply removing choices that the voting pool may deeply desire.  Fortunately, PIVX was born with +/0/- voting. Therefore, this issue already partially solved, except that with just one option up for vote and yay or nay to go with it, the two-party system is already also born into the system. Therefore, vote option monopoly is expected. 

To solve the two party system and vote option monopoly problem, we need a combination of +/0/- voting/feedback and the possibility of multiple vote options. Vote options meaning: "I want A or B or C, but not D". Because people can't properly manage a large number of vote options in their minds, more than four vote options may begin to become unmanageable. After long discussions, it was concluded that the best vote counting algorithm available is +/0/- iterative ranked with null option.  

The voter is confronted with a list of options. "Do Nothing" is one of the options, and is automatically listed as a choice. The voter may then add additional options to a list of such choices as being ranked in the voters preferred order above or below "Do Nothing". Options above "Do Nothing" are counted as positive while those below are counted negative.  Those options not moved to a choices list are set to abstain. (0) The voter shows in this case neither preference nor deference for the option abstained and will neigher be weighed for nor against that option during any stage of the counting process. <br />
For each voting layer, (with slight tuning adjustments possible) options that are dominantly listed as negative are counted as blocked (or as requiring extreme positive votes from other layers in order to pass), and may be removed from the options list. Remaining options, always including the "do nothing" option continue to the macro-vote or total group vote where all three layers vote. Each layer providing 1/3 of the total vote weight. The algorithm removes least popular (least positive and lowest ranked) options one at a time until two possible winners remain. This vote may be tuned by adding a default percentage to the "do nothing" option. At this point, votes are counted as + if a remaining option is ranked above the other option by a voter and - if a remaining option is ranked beneath the other option. If a voter does not have both final options ranked on his/her ballot, then that voter has not expressed a preference between the two possible winners, and his/her vote can not be counted. 

A "Must Choose" vote may be implemented by means of removing the "Do Nothing" or Null option. 


## 2.4 Management of Feedback Loop Dynamic
https://www.youtube.com/watch?v=5HNmsBaVmZs  

The above video demonstrates that experts are concerned about government decision processes being influenced by special interest groups. What they blatantly fail to note is that 

* You have multi-billion dollar decisions being made by as little as 11 people. Clearly the "gain factor" is too high, (in other words, they are controlling issues that are way too much larger than themselves) and makes the 11 people susceptible to too much influence created by the heavy monetary weight of the decision. This is a standard feedback loop problem .. or a couple of them in tandem that we might call "high impedence feedback loop" and "high gain factor".  In this Scenereo, the energy in the system is so much greater than the energy in the feedback route, that the feedback information is corrupted by the system energy, creating either distortions, or parasitic patterns, both in the case of current governing practices .. Change the committee size to 110 in stead of 11, and suddenly the group is ten times more expensive, complicated, and difficult to manipulate by special interest groups. The video goes out from the assumption that the committee size can't be questioned.  This is utter nonsense. The true problem they are fighting and don't want to admit is over-centralization. 

* The tuning of the Federal Government voting feedback loop dramatically shifts with population rise because delegate to population ratio is a form of "gain factor". Feedback loop stability is extremely sensitive to loop gain factor. Roughly in the 70's they want to attribute exaggerated corporate influence on federal decisions to transparency laws. Said transparency laws may in fact benefit special interest groups more than the public because those special interest groups are able to pay lobbyists to monitor and influence committee members. However, they fail to properly note that people can't know if their delegates are representing them without transparency, and wish to set up a trusted system. This is an extremely dangerous move to make because .. remember ..  because of increased population size, the tuning of the system is no longer identical to the 1970's and we can not simply trust that the system will then reconfigure back to its 1970's behavior. They fail to consider the possibility that the rise in corporate influence on decisions is also caused by the larger and larger sums of money wielded by corporations (and other groups) doing larger and larger business with more and more people while the federal decision maker teams/committees remain the same size. Setting the federal decision body sizes in stone while the population grows exponentially is basically setting up a feedback loop that constantly re-tunes towards less and less stable numerics without apparently any voice standing up to say ... "hey, this loop is constantly de-tuning its self". We have been begging on hands and knees and praying for exactly this kind of problem to show up. These so called experts fail entirely to suggest the real solution to the problem, which is larger committes and gain factors limited to approximately dunbars number squared (22500). Interestingly, the original constitution used the number 30,000, an acceptable number, but that number was overridden when the size of congress was limited. That limitation appears from a systemstheoretical perspective to be an act of class warfare. However, it is also indistinguishable from being an act of ignorance... an accident (?) which promotes slow domination of oligarchy over time.  

https://en.wikipedia.org/wiki/United_States_congressional_apportionment  

With Current gain factors for congress members in the ballpark of 700,000 (people/representative) this is a number we would drastically reduce if at all possible in any single amplifier gain stage because of the inherent instability of that kind of gain factor. We can eradicate this entire concern with a single move.  Limit the number of accounts a delegate may represent to 30,000 ( just over dunbars number squared .. many people have multiple accounts, justifying higher numbers, but team members have argued to reduce potential powers of single delegates.)  

https://en.wikipedia.org/wiki/Dunbar's_number

 Dunbars number squared represents the concept of "a friend of a friend". If the individual representing you isn't a friend of a friend, then it's doubtful that you are being represented. 



## 2.5 Staking Nodes

Because staking is a network support function, staking node feedback will be counted into the network support layer proportionally with the number of PIVX staked. Unless there is further information to process, Staking nodes and Masternodes will each acquire 50% of this layers vote. Many have argued against using vote nodes, leaving vote nodes as a last resort for acquiring adequate vote activity in the N^2 layer. Since vote nodes are a last resort to acquiring adequate N^2 vote, this layer may shift if vote nodes are actually implemented so that vote node holders (not those whom they represent) acquire something like 7% of the total S layer vote.

## 2.6 Masternodes

Masternodes currently present us with a conundrum, because they are pre-defined to be accounts of exactly 10k PIVX. Individuals won't be holding their own preferred coin numbers in those accounts. It is known that many individuals hold quite a few masternodes, but without explicit data, this can not be directly counted into the voting scheme. Unless the community opts to link masternode accounts, masternodes can only be assumed to be components of larger holdings, therefore we reduce their network effect vote by a predefined amount, and increase their intelligence vote by the same amount. 40% decrease/increase. For exponents of 0.6 and 1.66, this equates to the assumption that masternodes will typically be held by people who have 30k PIVX total.  This is an approximation, but without better information, we can not make the approximation more correct. 



## 2.7 Vote Nodes
Because most investors won't have the time and energy to invest in making community decisions, delegation is an important option to consider. Discussions of doing delegation have had rather mixed results, leaving the option for delegation as neither popular nor unpopular. Therefore, we choose to defer the decision as to whether or not delegation is actually used to a later date when it can be elucidated as to how necessary the option is. < br />
The primary value of the concept of vote nodes is in the creation of delegates who can fill that role.  Unlike traditional governing systems, Individuals would not have delegates imposed upon them by majority rule, but will have the freedom to choose their favorite delegate. This helps to get a wealth of information into the decision making system. 

There will not be a limit on the number of delegates other than the natural behavior of a free market. Managing feedback loop dynamics does however demand a limit on the number of accounts that a single delegate can represent. There is no hard limit on that number theoretically, but we will give centralization some benefit of the doubt and use 30,000, which is somewhat higher than Dunbars Number Squared (22500).  Part of the reason for this high estimate is the assumption that many people will have multiple accounts. 

The vote of vote node holders themselves has a place in the network support layer, since they do in fact support the function of the network. The votes that they represent belong in whatever layers they would have influenced otherwise. 

Vote nodes should be allowed to implement delegated proof of stake (DPOS) or staking pools with their adherents. The efforts of those individuals can be supported by DPOS reward percentages, as well as whatever agreements they wish to make with their adherents.  



## 2.8 General Users
All users vote according to PIVX holdings in layers N^2 and I according to the powers (exponents) given to those layers. This includes all node holders. However, there will be a minimum holdings requirement which may change over time. Early suggestion for this number is 500 PIVs. If this number falls too low, it becomes too easy for large holders to steal N^2 vote as well as too easy for uninterested parties to influence decisions. If it rises too high, it becomes too difficult for small stake holders to acquire that voting power. 


## 2.9 Thresholding

### For standard votes

Historically, the concept of a democracy is "majority rule" or 51% takes it. A democracy tends to be predatory as the 3 wolves voting against 2 sheep idea demonstrates.  The concept of a republic was built up to try to alleviate the predation of the democracy. This normally implies a voting threshold of something like 60%. While this may in fact make it more difficult for predators to rule, what we interestingly see is that in this case, 3 wolves can still eat 2 sheep. In neither case have the wolves been separated from the sheep in the voting paradigm, so a wolf votes like a sheep, but eats like a wolf. 

The three layer paradigm we present has something of the ability to separate the wolves and the sheep. This only works because this three layer model projects a new set of roles. It somewhat separates large stake holders from small stake holders. Historically, the wolves tend to be the large stake holders. Interestingly however, if we switch from wolf/sheep dichotomy to sadist/masochist dichotomy then we get something probably a little more true to reality. In the sadist/masochist dichotomy, the masochist occasionally strikes out in desperation and punishes the sadist, which is what the lower class sometimes does to the upper class in political settings. Therefore, the 51% vote tends to result in sadism/masochism .. a pattern normally identified as unhealthy. 

The way these issues work is that people tend to play roles that work. So if you set up a system that disadvantages one role game for a different role game, then you effectively project the new role game onto the public mind in a long-term sort of statistical and tipping point way. So if you want a wolves and sheep game, simply set up a majority rule system. The majority will reliably prey upon the minorities. In what way the majority differs from the minorities. Separating the wolves from the sheep makes it possible to break down the sadist/masochist game. It may not always be possible to do this, in particular because there may be no easy way to make the distinction, but in a setting where the primary issue is account size, the two roles are in all probability distinguishable. Perhaps cryptocurrencies have a little advantage in this respect over other structures. 

By creating a voting layer which substantially advantages an upper class, but that can't be fully enjoyed by an individual who wishes to divide down his accounts to steal lower class protection vote, we are projecting a different role game. We are suggesting to the upper class "don't be a wolf/sadist, be a leader. Be Prometheus and bring fire to man kind! Look at the value equation and see that playing the leadership role raises the value of the system for all, and that falling back to a predator role does you no advantage because it robs from you vestige of leadership." Add to that the inconvenience and problematics of gaming the system, and we expect most large investors to opt for the leadership role because it's just as powerful, but more fun, more open, easier to maintain and more glorious.  So, simply dividing up into the three layers as defined effectively solves the predator/prey problem in this one dimensional dynamic. Therefore, the 60% vote demand for the republic becomes redundant because it's designed to solve a problem that is already solved. We can move the system more easily and safely because protection for the various layers is already built in. 

Unnoted by politicians and attorneys whith whom I have spoken, there is a second reason for a vote requirement substantially over 50%. If we go back to the intelligence equations in various AI models, we will discover that time, or number of iterations of the system, is a crucial element of intelligence algorithmic. We expect it to take more time to get a proposal substantially above 50% vote, and hence, we expect the quality of the resultant proposal to be higher. This conflicts in some cases with the need for an emergency decision, where time simply is not available.  So, what we are seeing here is that once the predator prey problem is pre-solved by layering, we can actually use the voting threshold for a different purpose. We can maximize system intelligence according to time requirement. We can impose a high vote requirement if there is plenty of time, and a lower vote requirement if there is an emergency.  Recalling that PIVX is using +/0/- voting so that >50% is net positive, I believe that reasonable sets of numbers for this are:

* Net Positive, Net Positive, Net Positive (all 3 layers) in case of emergency (such as severe bandwidth problems)
* Net Positive, Net Positive, Net Positive (all 3 layers) and 5% positive total with each layer representing 1/3 of total vote in non-emergency situations. 
* It's probably reasonable to have a vote forcing option where every 5% extra total vote outweighs a 1% layer blocking such that for example 15% total net positive in a non-emergency situation overcomes one of the layers blocking at -2%.

Because of the intention to do away with single-option voting in order to accept a stronger information variety in to the voting option pool, this set of weights does not complete the system. Multiple voting options may pass according to those criteria. In that case, we simply choose the option that has the highest total positive percentage. 

Furthermore, there is the possibility that a large percentage of the public does not deliver information. The earlier threshold of required vote power exercised for a vote to pass was 10%.  A suggestion of 5% has been made in the interim. I believe that starting with 5% is a correct model, to assure mobility, and allowing this value to be altered as history writes something to look at. It will be appropriate to include into voting code a separable matrix structure of tuning parameters which may be both retained and updated over time so as to validate old decisions as well as make new ones. 


### For Meta-votes 
Meta-votes are just votes with special thresholding for the meta-vote purpose.  These votes are allowed only to operate on the voting system or primary documents of the system its self such as the Manifesto. Any meta-vote operating on normal system decisions is invalid and not to be implemented.  Any normal vote operating on the voting system or primary system documents is similarly invalid and not to be implemented. 

In the case of meta-votes, the structure of the decision making system is in question. It's probably appropriate to have two separate meta-layers for voting.  One for the general manifesto, and a second for any other fundamental document. 




## 2.10 Meta-Consensus
It would be naive to assume the ability to anticipate all possible dynamics of a consensus system which involves complex feedback, stochastic inputs, and therefore chaotic movement. Therefore, it is prudent that there are built in procedures for adapting the consensus mechanism itself. However, since Meta-consensus is on a more abstract level, it's impact can be even more unpredictable and sensitive to change than the consensus mechanism itself. For this reason, it is necessary that controls for Meta-Consensus be even more restrictive, with high threshold (see 2.9) and limited manipulability.  






# 3. Implementation

## 3.1 Information Timing (The No-dancing Filter)
Without delaying the shift in voting power related to the movement of PIVs in the system, large players can simply move their pivs into a favorite position for each separate vote. Clearly this ruins the 3 layer model. Therefore, we enforce vote timing such that voting power takes roughly 1 year to fully transfer from one address to another. Therefore a voter must choose his favorite layer in general and not for specific votes.

It was requested for vote data and computation to be minimal. If we examine the plethora of signal processing strategies for smoothing and delaying signals, the solution that requires the least computation and memory is the single pole IIR filter of following design. IIR stands for infinite impulse response, which is the converse of finite impulse response. FIR filters are basically just as good, possibly better under circumstances, but more expensive to implement. We will call it "the no dancing filter"

W[N] = W[N-1]C + A * (1-c)

This is an extremely simple IIR filter which produces a series of vote weights W[N] given a filter constant c between 0 and 1, and a time varying account value A. The filter constant c is tuned in terms of what we call "time constants" the word time constant derives out of math/physics and the number e, but in this case, that is merely tradition. What a time constant means is that after one time constant of time, the system has settled to 63% of its final settling position.  If we decide to have a time constant of four months, then it will take about eight months for most of an accounts voting power to accrue. 

Now suppose we run the filter equation once every month. Each W[N] would then be valid for one month of time. Four months then requires 4 iterations of the equation. So to get the proper value of c for a time constant of 4 months, we set A to 1, therefore eliminating it. And tune the equation to get us a value of 0.63 after four iterations. 

W[N] = W[N-1]c + (1-c)  <br />
now set w[0] to 0 and W[6] to 0.63 <br />
W[1] = 1-c  <br />
W[2] = (1-c)*c + (1-c) = c-c^2 +1 -c = 1-c^2  <br />
W[3] = (1-c^2) * c + 1-c = c-c^3 + 1 - c = 1-c^3  <br />
W[4] = 1-c^4 = 0.63  <br />
c^4 = 0.37   <br />
c = 0.37^1/4 = 0.779920671 <br />





This would be a very inexpensive, fundamental means of dampening vote movement to foil vote hopping. It is of further interest to compare W[N] and A and choose the smaller of the two for vote weight.  This would instantly kill voting for emptied accounts which would be an important part of breaking destroy and cache-in market strategies. In other words, if you use your vote to destroy the currency, then you're still holding the currency and therefore are subject to the damage. The choose the smaller rule also foils some additional, more subtle attack vectors. 

It should not be necessary to use this filter for the S layer, but rather only for the N^2 and I layers. 


## 3.2 Additional Means Of Protecting the N^2 Vote
The N^2 voting layer is the most important voting layer, as it clearly actually represents two dimensions according to the exponent.  Simultaneously, the N^2 layer is also the most difficult layer to successfully capture because capturing it means getting vote data from individuals who are small investors, who are only minimally to moderately interested in the outcome of the system. Besides potential predation from the other layers, voter apathy threatens to weaken the effectiveness of the N^2 voting layer.  Besides the information timing section above. NOTE without adequate protection of the N^2 vote, the model collapses. some options for strengthening this layer are as described below.  Some of these options are more popular than others, so they are listed in an order of reasonable implementation priority. The idea is to implement them starting at the top, and if more N^2 protection seems to be required, then we implement further down the list. Number six is far down the list because it is both unpopular and difficult to implement.  However, early voting count results could show it to be necessary. :

1. Power voting as described above, and exponents of 0.6 and 1.66 for N^2 and I layers respectively. 
2. Easy Voting systems that provide voters an assortment of resources to minimize the effort required to vote. 
3. Slightly raising the exponent of the I layer to 1.72 or some such would additionaly curb predation by other layers without substantially damaging the system.
4. One of the most potent options is to float (make alterable) the N^2 blocking threshold and feed-back tie it to least squares approximations of the exponential function and power law visible in a snapshot of the PIVX distribution.  Significant attempts to steal N^2 vote will be visible in those least squares approximations, and if the distribution starts getting fat at the bottom, we know people are cheating and we can raise the blocking threshold appropriately.  In order to get this right, we need a small research project into identifying the correct account value distributions. Use of this option should allow partial deactivation or down-tuning of the no-dancing filter. 
5. Slight reduction (3-10%) of staking rewards for small accounts should further deter vote stealing by large account holders.
6. Use of delegates, DPOS and vote nodes to allow voters to be represented by those in the study, thereby reducing the effort required to vote.
7. Allowing exchanges to vote explicitly and only in the N^2 layer would bolster the stability of the layer without breaking the N^2SI model. Many have objected to this idea. It's possible in attempt to appease such to reduce the vote weight of the exchanges. 
8. Any other accounts or classes of accounts that can be positively identified as N^2 accounts could be factored into N^2 in order to bolster the meaning and stability of the layer.
9. Anonymous Identity Models (not under consideration at this time)


## 3.3 Data Retention
Because of the need to minimize the size of the block chain, It will be an advantage store the vote data separately from the chain. The actual vote results are crucial information and need to be on the chain.  In order to verify the legitimacy of the vote data and the chain, a hash of the vote data blocks should be stored on chain, and something like 100 of the next block creations should sign off the hash of the vote data in digital signatures. Over half of such block creation signatures chain-verifies the vote, and less than that invalidates it. The Vote data shall be retained for roughly 1 year before being archived. Vote data older than one year no longer shall be subject to scrutiny, and shall only be available from any nodes who voluntarily wish to archive the data. 

## 3.4 Examples

## 3.5 Tokens

## 3.6 Onramp
Avoiding an identity model requires extra complexity in this system, which then imposes a step-wise implementation. A reasonable ordering of the steps for implementation is as follows. This schedule should be somewhat flexible, based on the needs of other projects and availability of coding talent. 

1. Create an S layer by adding staking vote together to the currently used masternode vote.
2. Create the N^2 and I layers and options 1 and 2 from section 3.2 as well as a minimal set of measurement instruments for observing the system. Most especially, least squared exponential and power law approximations as well as vote statistics.
3. Observe the system behavior for roughly 1 year.
4. Re-tune parameters and add additional elements from section 3.2 as appears to be appropriate. Adjust system design if necessary.
5. Build more instruments for system observation and observe for another year. 
6. Add more options from 3.2 if necessary, and Re-tune parameters once again. 


# 4 Discussion and Reference


## 4.1. Options for Optimization to be Discussed These Options Are Not Necessary, but May be Advantageous. 
They have the disadvantage of making it more difficult for people to understand the voting math. 

* account snapshotting combined with exponential-curve and power law analysis and timing allows emphasizing accounts that are relatively certain to not be misrepresenting themselves

* Use of zero knowledge proofs in order to allow ZPIVs to influence voting. 

* allowing exchanges to vote in the network effect layer

* creation of defense and defense intelligence functions to play a role in network support and intelligence layers. Such defense function may be responsible for legal and memetics concerns (Public Relations). 

* use of automatic network tuning mathematics to auto-tune the voting/feedback system.

* use of private identity systems to bolster voting information

* Use of transaction fee information to bolster voting information

* use of iterative voting

* use of vote history to adjust vote weights


## 4.2 Examples of History Measures for a Sytem Guidance Instrument Panel 
Some of these measures have already been implemented. 
See:  http://www.presstab.pw/phpexplorer/PIVX/index.php,  http://pivx.masternodes.pro/

* least squares approximation of negative exponential curve distribution for account values below 10k pivs
* least squares approximation of power law curve distribution for account values above 10k pivs  
* Pivs in Masternodes vs Pivs Staked
* Number of Masternodes
* Number of Staking nodes
* Transaction volume/day
* Layer vs layer vote percentages
* Vote blocking events where a single layer blocks below the blocking threshold
* Number of Vote Nodes
* Average PIVS represented by vote nodes
* Average number of accounts represented by vote nodes
* BTC and USD prices
* rms price volatility measure
* BTC/USD price derivatives
* Estimated price shift time constant (amount of time required to make 63% of a price correction)
* Estimated current value (based primarily off of a single pole fir filter with above time constant)
* Estimated pump pool size
* Estimated dump pool size


## 4.3.  Math Reference (for mathematicians)

The network calculation used to determine a decision based on the individuals votes will take the general form of a 4 layered feed-forward network with the first three layers being non-thresholding layers while the fourth implements a complex system of interrelated thresholds. These four network math layers are not to be confused with the lay-person voting layers. They are calculation machinery, and not human-subjective function description. The input data will take the form of vectors of ternary numbers (+/0/-). 

The first network layer will be the input data.  The first set of weights is derived from chain data, and will weigh the input data into nodes of the second network layer which represents a detailed list of currency related functionalities. The form of the data at this point will be vectors of integers. They will be accompanied by additional scalars, which retain the number of original non-zero votes for each function. The scalars may be used to determine vote percentages. Those functionalities, once summed, will be weighed into the third network layer.

The third network layer will contain a list of the primary value dimensions (or lay-person voting layers). The data in that layer will be summed according to the weight scheme chosen for the three value dimensions. It consists of vectors of integers and scalars

The fourth network layer sums data from the vectors of integers and scalars from the third layer into a mutually suppressive thresholding system. The vector data is split from vectors into scalars. Each node of the fourth layer represents one of the elements of the vectors.  Each node of the fourth layer fills a thresholding function and outputs a single boolean number, all, except for one of which being 0 (not chosen)  while one of which is 1 (chosen). 


## 4.4 Other Reference:

https://en.wikipedia.org/wiki/Electoral_system <br />
https://en.wikipedia.org/wiki/Social_choice_theory  <br />
https://en.wikipedia.org/wiki/Arrow%27s_impossibility_theorem <br />
https://en.wikipedia.org/wiki/Gibbard%E2%80%93Satterthwaite_theorem <br />
https://en.wikipedia.org/wiki/Cardinal_voting <br />
https://en.wikipedia.org/wiki/Condorcet_paradox <br />
http://www.cds.caltech.edu/%7Emurray/books/AM05/pdf/am06-complete_16Sep06.pdf <br />



Contributors:
The information and ideas required to build this document come from a large number of individuals. <br /> 
Turtleflax, Veramis, Openbaringen, Nitya, Presstab, Alexanderluthor, cryptosi, Grant, derek_hansen, Trismegistus, mgshightech
