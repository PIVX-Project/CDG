# Implementation


## Table of content

4.1. [Ballots and Counting](#41-ballots-and-counting)

4.2. [Additional Means Of Protecting the N<sup>2</sup> Vote](#42-additional-means-of-protecting-the-n2-vote)

4.3. [S layer](#43-s-layer)

4.4. [I layer](#44-i-layer)

4.5. [Data Retention](#45-data-retention)

4.6. [Onramp](#46-onramp)


## 4.1 Ballots and Counting

The main issue is that voters should have no need for 'insincere voting'. Rather, they should be prompted to include enough information in their ballot that the voting algorithm can always signify their vote in the most preferable way. First 'pass to post', or basic voting, suffers because its minimal information only really supports a two party system. I expect the  many of you are already familiar with the problems of first pass to post, and may be familiar with the apparent alternatives of both 'iterative ranked' voting, and +,0,- voting, and so may wish to skip some of the following text.

The idea behind iterative ranked is that each ballot consists of an ordered list of the voters preferences. After the first pass, ballots may be counted up, and for each voter whose top pick was for a losing option, his vote gets to be redistributed to his next favored option on a second iteration.

With +,0,- voting, each option on the ballot recieves a +, -, or nothing. There are two versions of this, since the + and - options may or may not be mutually ranked. The rest of this document will consider only mutually ranked +,0,-. Once the ballots are filled, the +,0,-1 counts are first added together, and as before, votes for the least desired option will be removed from the ballots before an iterated recount. If, at any point, each -1 option is removed from a voters ballot, it is reasonable that said voter gets an implicit -1 count on his least preferred of the +1 options, and similarly if all +1 options are eliminated. Implicit -1 to +1 and reverse should not, of course, be taken in comparison to the null vote

However, there is a subtle relation between the two systems.
	PIVX doesn't intend to rely on elections or must-pass-something votes, if they  even choose to have them at all. The PIVX community will be voting on  proposals and ammendments directly, which is uniquely different from an election, in that the 'null' option, to change nothing, must be present.  To solve this, we simply need to include null within the ranks. To operate a must-choose vote, we need only to remove the null option. A ballot for three competing options may look something like this:


  1.  <span>B</span>

2.  <span>A</span>

3.  <span>null</span>

4.  <span>C</span>

This voter would rather see nothing get passed than Option C, because it
is ranked below null. Infact, the same voter could have identically
represented his opinions on this +,0,- style ballot:

1.  <span>B +1</span>

2.  <span>A +1</span>

3.  <span>C -1</span>



	Since C is -1 here, it is implicit that it is less preferred than null. There is little meaning as to which of these two is better because, infact, they contain identical information, and are 'Isomorphic'. Some of the pivmetheus groups preference is for, +,0,-1 ballots, but in the end, there isn't much difference. At the end remains the task of counting up the votes. In our example here if the C and NULL options are eliminated after the first iterated passes, the algorithm should automatically set preference for B, with +1, against A, with -1. A different voter ranking A above B would be counted as A with +1 and B with -1.

	 Some PIVX members have cited the 'Condorcet Paradox' and its various derivatives as arguments against ranked (ordinal) systems. Ranked voting tends to promote insincere voting where an individual ranks an option higher because the individual believes higher ranking means stronger vote weight, and its chances to win are higher, and other rankings will have no impact.  Iterative ranked voting however denies actual ordinality in that a higher ranked vote is not weighed more strongly than a lower ranking vote. If a voter has a preference between the two top candidates, then the voters vote is counted + or - according to the preference. Otherwise, the voters vote never had a chance of influencing the election to begin with.  In this model, there is no advantage in showing a different order of preference than what is true.

	 In order to implement layered voting, the final vote will follow the above strategy after each layer is given the chance to reject choices out of and prior to the macro-vote by attributing to them an excess of negative (below null) votes (after calibration/tuning constants and weights are calculated in).

To eliminate losers one at a time, we will make use of the copeland score, modified by the vote weights ouput by the no dancing filter.  https://www.researchgate.net/publication/235766330_Restricted_Manipulation_in_Iterative_Voting_Convergence_and_CondorcetEfficiency Each time a loser is eliminated, the copeland score will be re-calculated while ignoring the existence of the losing option.

"Copeland: The score of candidate c is the number of pairwise comparisons she wins (i.e., contests
between c and another candidate a such that there is a majority of voters preferring c to a) minus
the number of pairwise comparisons she loses. The candidates with the highest score win."



## 4.2 Additional Means Of Protecting the N<sup>2</sup> Vote
The N<sup>2</sup> voting layer is the most important voting layer, as it clearly actually represents two dimensions according to the exponent.  Simultaneously, the N<sup>2</sup> layer is also the most difficult layer to successfully capture because capturing it means getting vote data from individuals who are small investors, who are only minimally to moderately interested in the outcome of the system. Besides potential predation from the other layers, voter apathy threatens to weaken the effectiveness of the N<sup>2</sup> voting layer.  Besides the information timing section above. NOTE without adequate protection of the N<sup>2</sup> vote, the model collapses. some options for strengthening this layer are as described below.  Some of these options are more popular than others, so they are listed in an order of reasonable implementation priority. The idea is to implement them starting at the top, and if more N<sup>2</sup> protection seems to be required, then we implement further down the list. Number six is far down the list because it is both unpopular and difficult to implement.  However, early voting count results could show it to be necessary. :

1. Power voting as described above, and exponents of 0.6 and 1.66 for N<sup>2</sup> and I layers respectively.
2. Easy Voting systems that provide voters an assortment of resources to minimize the effort required to vote.
3. Slightly raising the exponent of the I layer to 1.72 or some such would additionaly curb predation by other layers without substantially damaging the system.
4. One of the most potent options is to float (make alterable) the N<sup>2</sup> blocking threshold. We may then adjust it according to least squares approximations of the PIVX account distribution curve at the time of voting.  Significant attempts to steal N<sup>2</sup> vote will be visible in those least squares approximations, and if the distribution starts getting fat at the bottom, we know people are cheating and we can raise the blocking threshold appropriately.  In order to get this right, we need a small research project into identifying the correct account value distributions. Use of this option should allow partial deactivation or down-tuning of the no-dancing filter.
5. Slight reduction (3-10%) of staking rewards for small accounts should further deter vote stealing by large account holders.
6. Use of delegates, DPOS and vote nodes to allow voters to be represented by those in the study, thereby reducing the effort required to vote.
7. Allowing exchanges to vote explicitly and only in the N<sup>2</sup> layer would bolster the stability of the layer without breaking the N<sup>2</sup>SI model. Many have objected to this idea. It's possible in attempt to appease such to reduce the vote weight of the exchanges.
8. Any other accounts or classes of accounts that can be positively identified as N<sup>2</sup> accounts could be factored into N<sup>2</sup> in order to bolster the meaning and stability of the layer. An interesting option for implementing this would be to offer additional N<sup>2</sup> vote to public keys that show large amounts of trading.  Accomplishing this would require some careful management of network calculation math. An adequate mathematics solution could potentially raise the priority of this option.
9. Anonymous Identity Models (not under consideration at this time)

## 4.3 S layer

The S layer is unique amongst the layers because holding PIVX is not proof of network support function.  Proper proof of network support function can only be acquired by evidence of masternode or staking rewards. Therefore, rather than using current PIVX holdings, we propose counting the PIVX rewarded to an address within a period of time, probably 2 weeks. Then we run that number through the same no dancing filter, or exponential moving average as the other two layers to acquire vote weight so as to substantiate that an account is participating actively over a period of time. We then offer 50% of the vote power of the S layer to masternodes and 50% of it to staking nodes.  While some discussion of creating a concept of “tokens” for accounting vote weights for this layer, we see this as unnecessary at the time, but possibly valuable for future projects.

If vote nodes become a necessity because of voter apathy, then the vote node holders would acquire 10% of the S layer such that the percentages become 45/45/10.  That 14% would not belong to accounts being represented by vote nodes, but rather to the vote node accounts themselves.  In this case, every vote node representing more than a threshold number of accounts (start with 20) and also  (start with) over 5000 PIVs would share equally with other qualifying  vote nodes the 14% of S layer vote.

## 4.4 I layer
The I layer has the weakness of a relatively small sample size. To help alleviate this problem, we shall limit all accounts to not more than 4% total vote (tunable at after observation).  This also blocks some attack vectors, such as single, large I account vote blocking attack.


## 4.5 Data Retention
Because of the need to minimize the size of the block chain, It will be an advantage store the vote data separately from the chain. The actual vote results are crucial information and need to be on the chain.  In order to verify the legitimacy of the vote data and the chain, a hash of the vote data blocks should be stored on chain, and something like 50 of the next block creations should sign off the hash of the vote data in digital signatures. Over half of such block creation signatures chain-verifies the vote, and less than that invalidates it. The Vote data shall be retained for roughly 1 year before being archived. Vote data older than one year no longer shall be subject to scrutiny, and shall only be available from any nodes who voluntarily wish to archive the data.

If the coders however prefer, it should be acceptable to create a second chain, which maintains the vote data separately from the transaction data.



## 4.6 Onramp
Avoiding an identity model requires extra complexity in this system, which then imposes a step-wise implementation. A reasonable ordering of the steps for implementation is as follows. This schedule should be somewhat flexible, based on the needs of other projects and availability of coding talent.

1. Create an S layer by adding staking vote together to the currently used masternode vote.
2. Create the N<sup>2</sup> and I layers and options 1 and 2 from section 3.2 as well as a minimal set of measurement instruments for observing the system. Most especially, least squared exponential and power law approximations as well as vote statistics.
3. Observe the system behavior for roughly 1 year.
4. Re-tune parameters and add additional elements from section 3.2 as appears to be appropriate. Adjust system design if necessary.
5. Build more instruments for system observation and observe for another year.
6. Add more options from 3.2 if necessary, and Re-tune parameters once again.
