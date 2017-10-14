![](https://www.hicgrp.net/wp-content/uploads/2016/02/work-in-progress-500x261.jpg)
+# Disclaimers
+
+#### While this document often makes use of the traditional word "vote", it is important to understand that it only appears to be traditional voting from the users perspective. The internal maths will be in the form of weighted network feedback. This appears to be the only means of accomplishing all of the above named goals. Therefore, it is appropriate to replace the word "vote" with a phrase such as "inform" or "informing" or "information acquirement" or "decision making event". The use of the word "vote" is for mental convenience of the reader only, and the meaning of the word shall be switched to an altered state defined by this paragraph. 
 
   # Pivmetheus consensus-proposal 
   ### Because an advanced digital assett deserves an advanced consensus model!
  
 
 # 1 Abstract
-The proposal we wish to introduce at this time is intended as an upgrade for the current PIVX consensus/voting system used for passing proposals into community acceptance. This proposal keys significantly off of presstabs original 3 layer model. However, for mathematical reasons, it has been adapted for optimum balance. 
-#### This is the only model being presented that has the ability to successfully represent and protect small investors in the voting pool.  
-The issues to be balanced into the model have been chosen as follows:
-
-* Privacy
-* Simplicity for the end user
-* Protection and respect for crucial subgroups of the community 
-* Most particularly, successful inclusion of the general usership as a substantial voting influence. This is especially important, because of the squared relationship between number of people/nodes and network value, wheras the other factors are only single power. 
-* Maximization of network value and respect for the crucial resource of people in the system rather than only respect for numbers that mean nothing without people
-* Balance
-* Resistance to vote gaming
-* Protection against common weaknesses of voting systems such as those of "first past the post" voting. These weaknesses can often be abstracted as vote information starvation. See this video for a lay-person explanation of that: https://www.youtube.com/watch?v=s7tWHJfhiyo&list=PLPZwr9rnuY9pr4InUaLfjmX757UfE-DVY
-* Aggressive system tuning and protection against feedback loop parasitics. 
 
+This proposal is as an upgrade to the current PIVX consensus/voting system for passing proposals into community acceptance,  which has been adapted for optimum balance. Currently, it is the foremost consensus model for both representing and protecting the small investors in the voting pool.
 
-The model we will present is designed to respect the fundamental value model of a cryptocurrency. N^2SI  (described in detail later) It is also designed to respect the various conundrums of voting that result from currently used voting models that are starved of information. The last challenge to be managed is to curtail the arrival of common feedback loop misbehaviors that are evident in current politics as well as common feedback systems. Some explanation for the exact choices made will be given. 
 
-#### While this document often makes use of the traditional word "vote", it is important to understand that it only appears to be traditional voting from the users perspective. The internal maths will be in the form of weighted network feedback. This appears to be the only means of accomplishing all of the above named goals. Therefore, it is appropriate to replace the word "vote" with a phrase such as "inform" or "informing" or "information acquirement" or "decision making event". The use of the word "vote" is for mental convenience of the reader only, and the meaning of the word shall be switched to an altered state defined by this paragraph. 
 
-One of the fundamental features of this model is that it offers leadership to large stake holders (and potentially developers) while simultaneously securing protection for small investors. This is the inspiration for the name "PIVX-metheus".  
+The following issues to be balanced into this model have been chosen as follows:
 
-Note that voting systems are feedback loops that can exhibit unexpected behaviors. It is unrealistic to assume that one can construct a feedback loop and have it behave optimally from the very beginning.  Therefore it is strongly suggested to hold the voting system design as experimental for the first 10 to 15 years. This suggests strongly that for that time period, a meta-voting system be enabled which allows the voting system its self to be altered with a model that does not allow for one of the layers by its self to block the voting system edit. However, such a meta-voting system should only be activated based on references to behavior tuning issues.  Such tuning issues need to be made visible by means of building a set of system measures into a system status panel similar to what we see at this site:  http://pivx.masternodes.pro/  only much more advanced and informative. The existence of such a system status panel will for many reasons be a substantial addition the value of the cryptocurrency. 
 
+1.  <span>Privacy</span>
 
+2.  <span>Simplicity for the end user</span>
 
+3.  <span>Balance, protection, and respect for all groups of the
+    community</span>
 
+4.  <span>Maximation of network value. It is understood that network
+    value may have modelled by $V=N^2SI$(described in
+    detail below)</span>
 
+5.  <span>Maximization of the total utility the PIVX network provides
+    for its end users, who are the real source of its value.</span>
 
+6.  <span>Proper representiation for the general usership is of
+    particular concern, because the relationship between a social
+    networks value and the quantity\*quality of its members is
+    approximately quadratic ($N^2$).</span>
 
+7.  <span>Resistance to vote gaming, agressive system tuning, and
+    unhealthy feedback</span>
 
 
+The model presented here is designed to respect the fundamental value model of a cryptocurrency. N^2SI  (described in detail later) It is also designed to respect the various conundrums of voting that result from currently used voting models that are starved of information. The last challenge to be managed is to curtail the arrival of common feedback loop misbehaviors that are evident in current politics as well as common feedback systems. 
 
+ This document describes how a voting architecture may be capable of solving sundry known voting quandries, notably those arising from an inadequate collection of information to make proper decisions, as well as the growth of the unhealthy feedback behaviour which is already recognizable from contemporary political systems, and their tendency to extreme wealth inequality.  A major tool for handling these issues is an advanced balloting system, which allows voters to both rank their preferences, and provide negative feedback.
 
+Consensus for PIVX, however, has a new set of major restrictions arising from its architecture and privacy. Typical voting occurs by indentifying citizens, yet all PIVX voting information must come from the blockchain itself, without necessitating personal identification, for it to really have privacy. PIVX votes can only be verified with private keys, which prove ownership of  public keys, and connect the voter to  their transfers and staking. Under this architecture, it is very difficult, without sacrificing privacy, if not impossible, to prevent the wealthy, from gaining proportionally greater representation, since they can always feign the appearance of many small investors if they so desire. Therefore, in order to protect small investors from virtually being robbed by the wealthy, who can make stronger votes, it remains to provide an incentive for large investors to consolidate their holdings which is greater than their incentives to feign small investors. 
 
+One principal device for this is the provision of leadership opportunities for large stake holders and developers, with simultaneous ensurement of protection for small investors, hence the name "PIV-metheus". Said opportunities  arise from three layered voting, where large stake holders will have an upper hand in the second, 'S' layer, developers in a separate 'I' layer, and the rest in the 'N^2' layer.
 
+An important part of this strategy is to keep multiple investor groups competing. If three maligning gold hunters are coming back from the Sierra Madre, with packs full of treasure, there is far greater security than with two, because if any member of the party were to attempt a heist, he'd be outnumbered, two to one. 
+How to keep democracy between eleven sheep and thirteen wolves with a  sheeps wardrobe? One way is to keep them in two huts, with hay fed to the first, and beef to the second. The huts vote seperately, may veto decisions, and if a wolf leaves to the sheep bin, the rest get to split his beef. 
 
 
 
@@ -49,20 +58,17 @@ Note that voting systems are feedback loops that can exhibit unexpected behavior
 
   ## 2.1 Derivation of Approach
   
-Many issues were brought up and many models and proposals considered for the purpose of achieving consensus regarding private cryptocurrency development.  We chose a model that made use of many components of other proposals that were made. Simpler models may have been desirable, but could not satisfy enough of the fundamental values needed by the system.
-These values are:
-
-
+Many issues, models, and proposals have been considered for the purpose of achieving consensus regarding private cryptocurrency development.  Our model utilizes many components of these other proposals. Simpler models may have been desirable, but could not satisfy all of these important values and conditions:
 
-The fundamental model we begin with is that of the value of a network, which is approximated by the following equation:
+The fundamental model of network value:
 
 N^2*S*I
 
 where N is the number of nodes and N^2 the number of possible connections, S the strength of the connections and I the intelligence of the connections. 
 
 We can re-state these value dimensions with the terms:  
 ### Network effect (N^2), Network Support (S), Intelligence (I).  
-The goal is to maximize the value of the network by developing a feedback model which respects and protects these dimensions of value seperately, and as accurately as possible. According to the model, clearly, the value of the network is extremely sensitive to the number of people using the network. Therefore, in deference to some earlier models suggested, this document assumes that protection of the N^2 element of the network, which is primarily represented by the small investors, can not be sacrificed. 
+Having this model of network value means we can analyze the voting feedback system as an optimization problem. According to N^2SI, the network value is clearly extra sensitive to the number of people using the network. Therefore, in deference to some earlier models suggested, this document assumes that protection of the N^2 element of the network, which is primarily represented by the small investors, can not be sacrificed. 
 
 Because of the above privacy requirement, acquiring extremely accurate representations of these three value dimensions is not possible without choosing and using cloaked identity technologies which, while under development, are not yet proven and trustable in our estimation. Therefore, we relegate the possibility of using such identity technologies to future decision making, and strategize to make due with approximations of the three value dimensions noted above. The resulting strategy looks very similar to presstab's original 3 layer proposal, but is adjusted in order to acquire some of the other values listed above. 
 
@@ -88,11 +94,10 @@ To exemplify the meaning and behavior of this system, we will construct some exa
 
 ## 2.3 Avoiding Information Starvation
 
-https://www.youtube.com/watch?v=s7tWHJfhiyo&list=PLPZwr9rnuY9pr4InUaLfjmX757UfE-DVY
 
-It is a fact, observable generically, that a decision making aparatus can not make the best decisions on a dearth of information. Furthermore, a system which makes optimal use of the information available to it makes quicker and more accurate decisions. The above listed video describes problems with "first past the post" voting, which are results of information starvation. Information starvation of the algorithms makes the system gameable, because it then becomes a matter of social gaming to position ones self to inject manipulated versions of missing information into the system. This is how "Tweed voting" arises. https://www.youtube.com/watch?v=PJy8vTu66tE .  It is important to be aware that highly intelligent people set up complicated means of Tweed voting that can be highly effective, but that a system with a solid foundation of information management makes it difficult to game the voting system. 
+Optimal decisions can't be made from a dearth of the information needed to accurately represent reality. . The infamous 'Tweed' declared, "I don't care who does the electing, so long as I get to do the nominating", because in a two party decision, by the time both candidates are picked, many of the important decisions have already been made. This principle remains widely and effectively exploited in complicated ways. However, proper information management makes it difficult to play these sort of tricks. For those interested, these videos provide additional information concerning "first pass to post" and Tweed tactics, respectively https://www.youtube.com/watch?v=s7tWHJfhiyo&list=PLPZwr9rnuY9pr4InUaLfjmX757UfE-DVY  https://www.youtube.com/watch?v=PJy8vTu66tE
 
-Historical voting math analysts have studied various voting systems, but normally not under this fundamental understanding. This is evident by the fact that many models of voting systems show up in the studies which are clearly information starved. First past the post voting systems as in common use today being perfect examples.  Therefore, many attempts to create information starved voting algorithms of various flavors all result in a decision making apparatus that misbehaves as is described in the first past the post voting video above.  Furthermore, it is a first step towards Tweed voting. 
+#NOTE- Questionable paragraphs- Historical voting math analysts have studied various voting systems, but normally not under this fundamental understanding. This is evident by the fact that many models of voting systems show up in the studies which are clearly information starved. First past the post voting systems as in common use today being perfect examples.  Therefore, many attempts to create information starved voting algorithms of various flavors all result in a decision making apparatus that misbehaves as is described in the first past the post voting video above.  Furthermore, it is a first step towards Tweed voting. 
 
 In a universe of "for every action, there is an equal and opposite reaction" for example, a voting system that does not include negative feedback (a negative vote) is not representing a fundamental truth about reality.  Reality literally insists on negative feedback, and will find it in whatever way necessary.  If negative feedback isn't explicitly on the ballot, then the ballot is information starved, and invites someone to find out how to play the role of negative feedback. In the first past the post voting system, Negative feedback naturally appears because of the natural narrowing of the party count down to 2. For a two party system, a vote for one party is identical to a vote against the opposing party, and nature's inherent requirement for negative feedback is filled, but at the cost of monopoly and near-monopoly over the candidate pool, Tweed voting style ( https://www.youtube.com/watch?v=PJy8vTu66tE ), which severely damages the voting system by simply removing choices that the voting pool may deeply desire.  Fortunately, PIVX was born with +/0/- voting. Therefore, this issue already partially solved, except that with just one option up for vote and yay or nay to go with it, the two-party system is already also born into the system. Therefore, vote option monopoly is expected. 
 
@@ -109,7 +114,7 @@ https://www.youtube.com/watch?v=5HNmsBaVmZs
 
 The above video demonstrates that experts are concerned about government decision processes being influenced by special interest groups. What they blatantly fail to note is that 
 
-* You have multi-billion dollar decisions being made by as little as 11 people. Clearly the "gain factor" is too high, (in other words, they are controlling issues that are way too much larger than themselves) and makes the 11 people susceptible to too much influence created by the heavy monetary weight of the decision. This is a standard feedback loop problem .. or a couple of them in tandem that we might call "high impedence feedback loop" and "high gain factor".  In this Scenereo, the energy in the system is so much greater than the energy in the feedback route, that the feedback information is corrupted by the system energy, creating either distortions, or parasitic patterns, both in the case of current governing practices .. Change the committee size to 110 in stead of 11, and suddenly the group is ten times more expensive, complicated, and difficult to manipulate by special interest groups. The video goes out from the assumption that the committee size can't be questioned.  This is utter nonsense. The true problem they are fighting and don't want to admit is over-centralization. 
+* You have multi-billion dollar decisions being made by as little as 11 people. Clearly the "gain factor" is too high, which makes them  susceptible to too much influence created by the heavy monetary weight of the decision. This is a standard feedback loop problem .. or a couple of them in tandem that we might call "high impedence feedback loop" and "high gain factor".  In this Scenereo, the energy in the system is so much greater than the energy in the feedback route, that the feedback information is corrupted by the system energy, creating either distortions, or parasitic patterns, both in the case of current governing practices .. Change the committee size to 110 in stead of 11, and suddenly the group is ten times more expensive, complicated, and difficult to manipulate by special interest groups. The video goes out from the assumption that the committee size can't be questioned.  This is utter nonsense. The true problem they are fighting and don't want to admit is over-centralization. 
 
 * The tuning of the Federal Government voting feedback loop dramatically shifts with population rise because delegate to population ratio is a form of "gain factor". Feedback loop stability is extremely sensitive to loop gain factor. Roughly in the 70's they want to attribute exaggerated corporate influence on federal decisions to transparency laws. Said transparency laws may in fact benefit special interest groups more than the public because those special interest groups are able to pay lobbyists to monitor and influence committee members. However, they fail to properly note that people can't know if their delegates are representing them without transparency, and wish to set up a trusted system. This is an extremely dangerous move to make because .. remember ..  because of increased population size, the tuning of the system is no longer identical to the 1970's and we can not simply trust that the system will then reconfigure back to its 1970's behavior. They fail to consider the possibility that the rise in corporate influence on decisions is also caused by the larger and larger sums of money wielded by corporations (and other groups) doing larger and larger business with more and more people while the federal decision maker teams/committees remain the same size. Setting the federal decision body sizes in stone while the population grows exponentially is basically setting up a feedback loop that constantly re-tunes towards less and less stable numerics without apparently any voice standing up to say ... "hey, this loop is constantly de-tuning its self". We have been begging on hands and knees and praying for exactly this kind of problem to show up. These so called experts fail entirely to suggest the real solution to the problem, which is larger committes and gain factors limited to approximately dunbars number squared (22500). Interestingly, the original constitution used the number 30,000, an acceptable number, but that number was overridden when the size of congress was limited. That limitation appears from a systemstheoretical perspective to be an act of class warfare. However, it is also indistinguishable from being an act of ignorance... an accident (?) which promotes slow domination of oligarchy over time.  
 
@@ -125,7 +130,7 @@ https://en.wikipedia.org/wiki/Dunbar's_number
 
 ## 2.5 Staking Nodes
 
-Because staking is a network support function, staking node feedback will be counted into the network support layer proportionally with the number of PIVX staked. Unless there is further information to process, Staking nodes and Masternodes will each acquire 50% of this layers vote. Many have argued against using vote nodes, leaving vote nodes as a last resort for acquiring adequate vote activity in the N^2 layer. Since vote nodes are a last resort to acquiring adequate N^2 vote, this layer may shift if vote nodes are actually implemented so that vote node holders (not those whom they represent) acquire something like 7% of the total S layer vote.
+Because staking is a network support function, staking node feedback will be counted into the network support layer proportionally with the number of PIVX staked. Unless there is further information to process, Staking nodes and Masternodes may each acquire 50% of this layers vote, although this is a tunable quantity. Many have argued against using vote nodes, leaving vote nodes as a last resort for acquiring adequate vote activity in the N^2 layer. Since vote nodes are a last resort to acquiring adequate N^2 vote, this layer may shift if vote nodes are actually implemented so that vote node holders (not those whom they represent) acquire something like 7% of the total S layer vote.
 
 ## 2.6 Masternodes
 
@@ -148,6 +153,29 @@ Vote nodes should be allowed to implement delegated proof of stake (DPOS) or sta
 ## 2.8 General Users
 All users vote according to PIVX holdings in layers N^2 and I according to the powers (exponents) given to those layers. This includes all node holders. However, there will be a minimum holdings requirement which may change over time. Early suggestion for this number is 500 PIVs. If this number falls too low, it becomes too easy for large holders to steal N^2 vote as well as too easy for uninterested parties to influence decisions. If it rises too high, it becomes too difficult for small stake holders to acquire that voting power. 
 
+## 2.9 {No Dancing Filter}
+A consensus model deriving its voting weights simply  by what each wallet is holding at voting time would  erroneously overrepresent traders who'd only recently bought their PIVX. Value comes from those who hold their PIVs, as should the votes. A good measure for this is the 'Exponential Moving Average'.
+The EMA has a few neat properties. If the holdings on a wallet were to suddenly jump from zero to H, the EMA would steadily respond as
+
+f(t)=H(1-e^{-ct})
+
+If the wallets value jumped back to zero, it's EMA would respond at the rate
+
+f(t)=He^{-ct}
+
+Where (H(t)) is the wallet at time t. To be implemented, the EMA can be calculated by tracking the time and values between transactions. For example, suppose the last transaction occured T in the past, then:
+
+f(H(t)) = (1-e^{-cT})H(t)+e^{-cT}f(H(t-T))
+
+
+If it happens these calculations are too cumbersome to perform on every transaction, an even further simplified model can be used, which simply approximates a wallets holdings by its contents iteratively say, every two weeks, so that if $e^{-cT}=C$ and the iteration is n, then
+
+f_n=(1-C)H(n)+(C)f_{n-1}
+
+The electronics engineers know this equation as an 'IIR' filter.
+Smaller C result in faster t decay.  If C is needed to provide a specific decay rate as fractional reduction per interval T, 0<\lambda<1, the inversion is quite simple.
+
+c=ln(lambda)
 
 ## 2.9 Thresholding
 
@@ -171,52 +199,72 @@ Because of the intention to do away with single-option voting in order to accept
 
 Furthermore, there is the possibility that a large percentage of the public does not deliver information. The earlier threshold of required vote power exercised for a vote to pass was 10%.  A suggestion of 5% has been made in the interim. I believe that starting with 5% is a correct model, to assure mobility, and allowing this value to be altered as history writes something to look at. It will be appropriate to include into voting code a separable matrix structure of tuning parameters which may be both retained and updated over time so as to validate old decisions as well as make new ones. 
 
+## 2.10 Meta-Consensus
+It would be naive to assume the ability to anticipate all possible dynamics of a consensus system which involves complex feedback, stochastic inputs, and therefore chaotic movement. Therefore, it is prudent that there are built in procedures for adapting the consensus mechanism itself. However, since Meta-consensus is on a more abstract level, it's impact can be even more unpredictable and sensitive to change than the consensus mechanism itself. For this reason, it is necessary that controls for Meta-Consensus be even more restrictive, with high threshold (see 2.9) and limited manipulability.  
 
 ### For Meta-votes 
 Meta-votes are just votes with special thresholding for the meta-vote purpose.  These votes are allowed only to operate on the voting system or primary documents of the system its self such as the Manifesto. Any meta-vote operating on normal system decisions is invalid and not to be implemented.  Any normal vote operating on the voting system or primary system documents is similarly invalid and not to be implemented. 
 
 In the case of meta-votes, the structure of the decision making system is in question. It's probably appropriate to have two separate meta-layers for voting.  One for the general manifesto, and a second for any other fundamental document. 
 
 
+# 3. Implementation
 
+## 3.1 Ballots and Counting
 
-## 2.10 Meta-Consensus
-It would be naive to assume the ability to anticipate all possible dynamics of a consensus system which involves complex feedback, stochastic inputs, and therefore chaotic movement. Therefore, it is prudent that there are built in procedures for adapting the consensus mechanism itself. However, since Meta-consensus is on a more abstract level, it's impact can be even more unpredictable and sensitive to change than the consensus mechanism itself. For this reason, it is necessary that controls for Meta-Consensus be even more restrictive, with high threshold (see 2.9) and limited manipulability.  
 
+The main issue is that voters should have no need for 'insincere voting'. Rather, they should be prompted to include enough information in their ballot that the voting algorithm can always signify their vote in the most preferable way. First 'pass to post', or basic voting, suffers because its minimal information only really supports a two party system. I expect the  many of you are already familiar with the problems of first pass to post, and may be familiar with the apparent alternatives of both 'iterative ranked' voting, and +,0,- voting, and so may wish to skip some of the following text.
 
+The idea behind iterative ranked is that each ballot consists of an ordered list of the voters preferences. After the first pass, ballots may be counted up, and for each voter whose top pick was for a losing option, his vote gets to be redistributed to his next favored option on a second iteration. 
 
+With +,0,- voting, each option on the ballot recieves a +, -, or nothing. There are two versions of this, since the + and - options may or may not be mutually ranked. The rest of this document will consider only mutually ranked +,0,-. Once the ballots are filled, the +,0,-1 counts are first added together, and as before, votes for the least desired option will be removed from the ballots before an iterated recount. If, at any point, each -1 option is removed from a voters ballot, it is reasonable that said voter gets an implicit -1 count on his least preferred of the +1 options, and similarly if all +1 options are eliminated. Implicit -1 to +1 and reverse should not, of course, be taken in comparison to the null vote
+	
+However, there is a subtle relation between the two systems.
+	PIVX doesn't intend to rely on elections, if they  even choose to have them at all. The sources of analysis many of the folks on PIVX governance have been considering are for picking candidates for a particular role, say 'king', or what have you. However, the PIVX community will be voting on  proposals and ammendments directly, which is uniquely different from an election, in that the 'null' option, to change nothing, is present. OK, so now you may be thinking, sure, all that means is we simply need to include null within the ranks, so that a ballot for three competing options may look something like this: 
 
+  
+  1.  <span>B</span>
 
+2.  <span>A</span>
 
-# 3. Implementation
+3.  <span>null</span>
 
-## 3.1 Information Timing (The No-dancing Filter)
-Without delaying the shift in voting power related to the movement of PIVs in the system, large players can simply move their pivs into a favorite position for each separate vote. Clearly this ruins the 3 layer model. Therefore, we enforce vote timing such that voting power takes roughly 1 year to fully transfer from one address to another. Therefore a voter must choose his favorite layer in general and not for specific votes.
+4.  <span>C</span>
 
-It was requested for vote data and computation to be minimal. If we examine the plethora of signal processing strategies for smoothing and delaying signals, the solution that requires the least computation and memory is the single pole IIR filter of following design. IIR stands for infinite impulse response, which is the converse of finite impulse response. FIR filters are basically just as good, possibly better under circumstances, but more expensive to implement. We will call it "the no dancing filter"
+This voter would rather see nothing get passed than Option C, because it
+is ranked below null. Infact, the same voter could have identically
+represented his opinions on this +,0,- style ballot:
 
-W[N] = W[N-1]C + A * (1-c)
+1.  <span>B +1</span>
 
-This is an extremely simple IIR filter which produces a series of vote weights W[N] given a filter constant c between 0 and 1, and a time varying account value A. The filter constant c is tuned in terms of what we call "time constants" the word time constant derives out of math/physics and the number e, but in this case, that is merely tradition. What a time constant means is that after one time constant of time, the system has settled to 63% of its final settling position.  If we decide to have a time constant of four months, then it will take about eight months for most of an accounts voting power to accrue. 
+2.  <span>A +1</span>
 
-Now suppose we run the filter equation once every month. Each W[N] would then be valid for one month of time. Four months then requires 4 iterations of the equation. So to get the proper value of c for a time constant of 4 months, we set A to 1, therefore eliminating it. And tune the equation to get us a value of 0.63 after four iterations. 
+3.  <span>C -1</span>
 
-W[N] = W[N-1]c + (1-c)  <br />
-now set w[0] to 0 and W[6] to 0.63 <br />
-W[1] = 1-c  <br />
-W[2] = (1-c)*c + (1-c) = c-c^2 +1 -c = 1-c^2  <br />
-W[3] = (1-c^2) * c + 1-c = c-c^3 + 1 - c = 1-c^3  <br />
-W[4] = 1-c^4 = 0.63  <br />
-c^4 = 0.37   <br />
-c = 0.37^1/4 = 0.779920671 <br />
 
+  
+	Since C is -1 here, it is implicit that it is less preferred than null. There is little meaning as to which of these two is better because, infact, they contain identical  identical information, and are 'Isomorphic'. My preference is for, +,0,-1 ballots, as they strike me as cleaner, but it's not a major concern because in the end, there isn't much difference. At the end remains the task of counting up the votes. In our example here- if the C and NULL options are eliminated after the first iterated passes, the algorithm should automatically set preference for B, with +1, against A, with -1. 
+	
+	 Some PIVX members have cited the 'Condorcet Paradox' and its various derivatives as arguments against ranked systems. However, if you look at them carefully, you may notice that the real problem amounts to the fact that items can get symmetric voting. Objectively, these theorems are not paradoxes at all, but trivial; when all the options get the same number of votes, in any system, obviously that's a problem. 
+	 
+	 Another concern is how this system could be integrated into more complex macro-model, with multiple layers and so forth. Although I can't specify which is best until the actual full voting algorithm is specified, there are a few very effective ways to integrate votes from different layers:
 
 
+-   <span>Perhaps the simplest solution is just to add all the votes
+    from different voting layers into one pool, differentiating them
+    only by the algorithms that determine their weighting</span>
 
+-   <span>A specialized tactic would be to rank the canditates into a
+    macrovote, by progressively removing the previous winner from the
+    ballots, in order to determine the next most preffered option. You
+    could even keep track of the precise margin each winner recieved,
+    but then again, if we wanted that functionality we’d have just used
+    the first option listed here.</span>
 
-This would be a very inexpensive, fundamental means of dampening vote movement to foil vote hopping. It is of further interest to compare W[N] and A and choose the smaller of the two for vote weight.  This would instantly kill voting for emptied accounts which would be an important part of breaking destroy and cache-in market strategies. In other words, if you use your vote to destroy the currency, then you're still holding the currency and therefore are subject to the damage. The choose the smaller rule also foils some additional, more subtle attack vectors. 
+-   <span>it may be strategic to allow layers to block ammendments that
+    they have a negative opinion about, meaning the option ranks bellow
+    null</span>
 
-It should not be necessary to use this filter for the S layer, but rather only for the N^2 and I layers. 
 
 
 ## 3.2 Additional Means Of Protecting the N^2 Vote
@@ -236,7 +284,6 @@ The N^2 voting layer is the most important voting layer, as it clearly actually
 ## 3.3 Data Retention
 Because of the need to minimize the size of the block chain, It will be an advantage store the vote data separately from the chain. The actual vote results are crucial information and need to be on the chain.  In order to verify the legitimacy of the vote data and the chain, a hash of the vote data blocks should be stored on chain, and something like 100 of the next block creations should sign off the hash of the vote data in digital signatures. Over half of such block creation signatures chain-verifies the vote, and less than that invalidates it. The Vote data shall be retained for roughly 1 year before being archived. Vote data older than one year no longer shall be subject to scrutiny, and shall only be available from any nodes who voluntarily wish to archive the data. 
 
-## 3.4 Examples
 
 ## 3.5 Tokens
 
@@ -251,10 +298,59 @@ Avoiding an identity model requires extra complexity in this system, which then
 6. Add more options from 3.2 if necessary, and Re-tune parameters once again. 
 
 
-# 4 Discussion and Reference
+## 4 Examples
+There are quite a few roles the people who involve themselves with PIVX
+may play. Whether it is one or many, these roles will determine their
+interests and how they’ll vote. A few of the important ones are listed
+below:
+
+**Whales** 
+
+	Fat cats who move large volume, sometimes making visible splashes in the markets. 
+	Some are just wealthy people, but 
+	others come from financial institutions who trade with other peoples money. 
+
+**Traders** 
+
+	From the exchanges, mostly. They like predictable volatility, often use
+	backtested tradebots, may be leveraging borrowed currency (margin), and
+	mercurially may be either bullish or bearish, depending on if they plan to 
+	buy or sell, respectively.
+
+**Investors**
+
+	Separate from the traders, because they buy and hold long term. Since they are 
+	healthy to the system, PIVX incentives 	
+	them with  staking and masternode rewards, which lands them in the S layer. 
+	
+**Developers**
+
+	The ones who design improvements. You, presumably, in the I layer.
+	
+**Suppliers/Customers**
 
+	Using cryptos to trade either goods or services,
+	these people will mostly need low transaction fees, stable currency 
+	values, and quality representation in the N^2 layer.
 
-## 4.1. Options for Optimization to be Discussed These Options Are Not Necessary, but May be Advantageous. 
+
+	
+Whale traders often proactively push currency value towards the
+direction they think it’s already headed. If they are bulls, they may
+publically declare it diamonds, and will vote accordingly. If they are bearish, however, whale
+traders will be most likely trying to push the price down.
+## 4.1 Scenario 1
+Suppose some whales from JP Morgan and other financial institutions decide PIVX has potential, although it hasn't been doing all that well lately. First, they act as bears, spreading 'FUD' and doubt, possibly even borrowing PIVX on margin, and selling them. However, as the price dips a bit further, they then buy up a few million $ worth of undervalued PIVX. Some of the bots and traders, seeing how the market has suddenly picked up momentum, following common indicators and technical analysis, also buy in, which drives the price up further. 
+
+Now the price is up, but if the whales tried to sell right then, so would the other traders, and besides, they bought PIVX  because they thought it had potential. Even if they did sell soon, they still wouldn't get a vote because of the EMA. Now they wait, and play the role of investors, slowly buying more pivs, as if they were blowing on a feather, until they decide they would finally like to sell. If PIVX is really growing like investors thought, whales are likely to hold their assets long enough to build a vote on the EMA, a likely to st
+
+Suppose now, the devs from the I layer 
+
+
+# 5 Discussion and Reference
+
+
+## 5.1. Options for Optimization to be Discussed These Options Are Not Necessary, but May be Advantageous. 
 They have the disadvantage of making it more difficult for people to understand the voting math. 
 
 * account snapshotting combined with exponential-curve and power law analysis and timing allows emphasizing accounts that are relatively certain to not be misrepresenting themselves
@@ -276,7 +372,7 @@ They have the disadvantage of making it more difficult for people to understand
 * use of vote history to adjust vote weights
 
 
-## 4.2 Examples of History Measures for a Sytem Guidance Instrument Panel 
+## 5.2 Examples of History Measures for a Sytem Guidance Instrument Panel 
 Some of these measures have already been implemented. 
 See:  http://www.presstab.pw/phpexplorer/PIVX/index.php,  http://pivx.masternodes.pro/
 
@@ -300,7 +396,7 @@ See:  http://www.presstab.pw/phpexplorer/PIVX/index.php,  http://pivx.masternode
 * Estimated dump pool size
 
 
-## 4.3.  Math Reference (for mathematicians)
+## 5.3.  Math Reference (for mathematicians)
 
 The network calculation used to determine a decision based on the individuals votes will take the general form of a 4 layered feed-forward network with the first three layers being non-thresholding layers while the fourth implements a complex system of interrelated thresholds. These four network math layers are not to be confused with the lay-person voting layers. They are calculation machinery, and not human-subjective function description. The input data will take the form of vectors of ternary numbers (+/0/-). 
 
@@ -311,7 +407,7 @@ The third network layer will contain a list of the primary value dimensions (or
 The fourth network layer sums data from the vectors of integers and scalars from the third layer into a mutually suppressive thresholding system. The vector data is split from vectors into scalars. Each node of the fourth layer represents one of the elements of the vectors.  Each node of the fourth layer fills a thresholding function and outputs a single boolean number, all, except for one of which being 0 (not chosen)  while one of which is 1 (chosen). 
 
 
-## 4.4 Other Reference:
+## 5.4 Other Reference:
 
 https://en.wikipedia.org/wiki/Electoral_system <br />
 https://en.wikipedia.org/wiki/Social_choice_theory  <br />
@@ -325,4 +421,7 @@ http://www.cds.caltech.edu/%7Emurray/books/AM05/pdf/am06-complete_16Sep06.pdf <b
 
 Contributors:
 The information and ideas required to build this document come from a large number of individuals. <br /> 
-Turtleflax, Veramis, Openbaringen, Nitya, Presstab, Alexanderluthor, cryptosi, Grant, derek_hansen, Trismegistus, mgshightech
+Turtleflax, Openbaringen, Nitya, Presstab, Alexanderluthor, cryptosi, Grant, derek_hansen, Trismegistus, mgshightech
+
+
+
