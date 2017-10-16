# Votes-For-All (VFA) Consensus Proposal




## 0 Foreword
This proposal does not include technical descriptions and instead focuses on the concepts and philosophies of Governance. This model hopes to establish a system that gives every single Pivian some share of the vote, keeps things relatively simple, and avoids long development times. Ultimately any system chosen will be heavily modified over the years as new technologies and revelations come to pass. We must start with creating the best we can with what is currently available to us.






## 1 Abstraction
The following Governance model is one potential candidate to replace the current Governance model. It does offer a wealth of additional features that can help further define the voting process, but at its core it is attaching one vote to each PIV in existence. This enables all users, regardless of how large or small their holdings are, to have a say in the future of PIVX. 


The goals of the VFA model are as follows:


1. Allow every Pivian to vote
2. Ensure more involved users hold more weight
3. Eliminate First-Past-The-Post (FPTP) voting
4. Prevent voter fraud
5. Ease of use
6. Establish variable pass requirements






## 2 The Current Governance System
Currently we operate within a system that only allows Masternode holders to vote. Each Masternode is worth one vote and much of the vote is actually only controlled by a few people as they have dozens, if not hundreds of Masternodes each. PIVX is fortunate that these people who control all the power are believers in the PIVX cause and have voted to dilute their power and give some to the masses. At its current state, PIVX is essentially under the rule of benevolent dictators. Thus the goal is to give enough power to the masses, so that if the dictators of the future are less benevolent, the smaller investors are protected from what would have been ultimate power. 


In addition, it is worth noting that the current method of voting is through the Debug Console in the wallet. This is also how proposals are created and it has proven to be a hassle for the few people that actually do use it. If mainstream voting is to become a thing, we will need to rework the system to be more user-friendly as it currently discourages voting. To create a proposal also costs 50PIV and if it passes, it costs another 50PIV, totalling 100PIV to put a proposal through. At the time of creating this cost, 1PIV was worth far less than it is now. It was put in place to prevent junk proposals, but as PIVX’s budget grows, it will become an increasingly large portion of the budget to refund those costs to successful proposals. It is likely worth revisiting this fee while Governance is being reviewed. 






## 3. Features
### 3.1 One Piv = One Vote
This feature is fairly self explanatory at face value. For each PIV you hold, even fractional quantities, you get an equivalent number of votes. It is a common belief that those that support the network and hold a lot of stake in PIVX should have more voting power per capita than those who hold less or are much less involved. There is no need for complex systems to enable this as it is already solved with this model. Those who are most invested already have things weighted to give them more control as they have more votes. The top-most investors hold more than a large segment of the bottom-most. To do anything else to shift the balance in their favour will strip the smaller investors of their ability to band together to demonstrate the will of the Pivians. 

This is likely the simplest way to give power to the people. You are essentially converting each Masternode to 10,000 votes, but also giving each holder with 500, 50, 5, or 0.5PIV an equivalent number of votes in proportion to their holdings. This way the thousands of people who are not as wealthy as the Masternode holders can band together to prevent proposals that can harm them. It is important when considering the balance between large and small investors to remember that neither group is a monolith. At different points of PIVX’s lifespan, who holds more weight may shift, but not all people in each group will vote as one big block. Proposals will have to garner the support of the majority of the whole to pass.


Why a three-tier system is not used in this proposal. It is the author’s belief that the three-tier system’s division of the voting blocks increases the risk of vote manipulation and gridlock. With voting being in one block where there is nothing that you can do to increase your weight or shrink another’s, there is nothing that can be done to manipulate the vote. It simply comes down to which option has more backing. In one scenario of three-tier voting, you have ⅔ blocks required to pass. This is problematic because a coalition of incredibly wealthy investors only now needs to tip the balance of ⅔ of the vote in their favour. They can ignore the block that is most inhabited by their opponents. This will inevitably be whichever block has the cheapest barrier to entry. Simply put this means that you no longer need 60% to pass a proposal, you only need 40% because you’ve eliminated ⅓ of the competition. Some believe that the financial incentives in different blocks will prevent movement, but this is unlikely. As an example, staking earns roughly 5% a year at the current balance. PIVX in just the last couple months has doubled in value. This means that the 5% is a nice bonus for holders, but is a weak incentive to deter those who would like to game the system. The other option of consensus with three-tier voting is having a requirement of all three blocks to agree to pass a proposal. This is also a non-starter because the risk of gridlock is immense. It would be very likely that even core requirements like development and marketing would fail to pass at one point or another. This would effectively kill PIVX if it ever happened.


Why weighting votes was not used. This was talked about briefly previously, but it is worth stating more directly. At this time, it is actually quite hard to tell what the wealth distribution is within PIVX. There are stakers out there that can compete in volume with large Masternode holders, but they don’t open Masternodes because it would imbalance the Seesaw algorithm. Users can also hold their PIV in multiple counts effectively making them appear as multiple people. With PIVX focus on maintaining the privacy of users, it is unlikely we’ll ever have metrics that can tell us exactly how distributed wealth is within PIVX. With that in mind, how do we know which side to weight towards? Simply, we don’t. Instead we just implement a system where simply having more PIV equals more weight to vote with. Then we also make sure there are no barriers to entry that affect small holders.


To clarify something that may be confusing in this section. Many proposed systems only allow Stakers, Masternodes, or the proposed Votenodes to vote. The VFA proposal would have ALL PIVX holders able to vote. Having PIVX in your wallet would give you tickets to vote with. The ticket concept is detailed in the following 3.2 section.


### 3.2 Separate Chain Ticket Voting
The issue of network load has been tossed around a fair bit. For the VFA model, the method of voting should be a ticket system on a separate Blockchain. The initial idea for using a voting ticket system is borrowed from @turtleflax and adapted to fit VFA’s needs. To prevent the drag on the network caused by voting, we need to move the voting process onto a chain of its own. This isn’t horribly hard to do, but how do we vote with our PIVX on this new chain. If each vote cycle, we mirror PIV onto the separate chain and have the wallet software manage both the PIV holding and our new vPIV (votePIV) than we can ensure tickets fall into the hands of those who were meant to get them. A ticket system would prevent voter fraud as the main foreseeable culprit of voter fraud is moving PIV around to get multiple votes. If all tickets in a voting cycle are handed out at one specific moment, this will eliminate that risk. 

It is important to note that the author of VFA is not a developer of any kind. These conclusions were derived from knowledge of blockchain and discussions with more knowledgeable individuals. The author concluded that this method is viable, but will not attempt to lay out the details. The decisions on methodology would need to be left to developers to plan according to what they know will work best.


### 3.3 Ranked Selections
For most proposals we put through, they will amount to fund or don’t fund. In some cases, like with these governance proposals, it would be handy to be able to vote on multiple options. Thus as part of a Governance overhaul, we must come to a decision on how best to achieve this. 


The traditional method of selecting a winning candidate or option in democratic nations is the First-Past-The-Post (FPTP) method. This is where the option with the most votes, wins. It is a simple and straightforward method that isn’t fundamentally terrible, but it does have a major weak point. People tend to fall into larger categories before they get subdivided into smaller groups. For instance, politically people tend to be predominantly left or right wing, but they are then divided into specific parties that more accurately define them in many countries. This can become a problem when there are more subcategories on one side of the spectrum than the other. There could be more left-wing support overall, but if there are twice as many left-wing parties, one of the right-wing parties will likely win. To counter this, people will avoid the smaller parties and vote for the biggest in their larger category to avoid losing to the complete opposite to their desires. This means that smaller parties can’t establish themselves and political systems get forced into two party systems. 

The counter to this is a system where voters don’t choose just one party, but instead rank them based on their appeal to the voter. As an example, imagine there are three parties, the two main ones and a newcomer. The voter could mark the small party as their favourite and one of the main parties as their backup. If the small one has the least votes, it is disqualified and that voter’s vote goes to their backup. This way the new party can garner support from voters without them being afraid they are wasting a vote on a nobody who can’t win. 


Thanks to @mgshightech for expressing the need for a ranked system to have this next piece to properly show the will of the people. If a system does not have a “do nothing” voting option, than it forces a choice that makes most people unhappy down their throats. In a ranked system, whether there is 2, 3, or 6 options, there should always be a “do nothing” option added on top of the proposed options. A voted can choose this as their first choice, the last, or anything in the middle. This option can’t be disqualified for low votes like the others. Instead it accumulates votes at each round of disqualification from those who no longer think the remaining options suit them. If at any point, the “do nothing” vote exceeds 40% of the population (being that 60% is needed for a proposal to pass) than the proposal is rejected with insufficient support for any option. This is essentially a no-confidence vote. 


### 3.4 Variable Pass Requirements
To show that a proposal has a clear majority support, it would be best for standard proposals to need a 60% yes vote to pass. This can be a wide range of proposals that even includes important regular funding requirements. The dev and marketing budgets would be standard proposals along with long and short term projects. Sensitive proposals should have a 75% yes requirement. This shows that 3/1 support in favour of the proposal which is an overwhelming majority. What is sensitive is something that itself would need to be voted on. What it should be confined to is things like changing important code, governance, and the manifesto. Essentially, everything that is core to PIVX values. Things that shake confidence if they are changed back and forth without strong thought and reasoning. If you have 75%+ support, the change is likely desperately needed.


### 3.5 Wallet Integration
For the regular user to join in on the voting process requires a simpler method of voting. Using the Debug Console is not something the majority of people are comfortable with. To deal with this, a voting tab will need to be added to the desktop wallet. In future we can try to get voting on mobile wallets, but for now the focus should be on desktop only. From this tab users should be able to view proposal summaries, links to the full information, and manage their voting tickets. They should also be able to create proposals or add an option to existing ones from this tab or a secondary one if that becomes too cluttered. 


### 3.6 Proposal Cost Reduction
As the budget grows, so does the number of proposals. If the price of PIV goes up, we reduce the number of PIV paid to each person, since the dollar value is proportionately higher. This gives us the ability to hire more people and do more projects. This has an undesirable side effect unfortunately. With each proposal comes 100PIV in cost. Most proposals include this as part of the payment to recoup those losses. If proposals shrink in PIV volume and we add more proposals to use the budget, then we incur more fees to waste budget money on. The fees are to prevent proposal spam, but when they were created, 100PIV was worth far less. 

As a result, I propose we reduce these fees to being 10PIV on proposal submission and 10PIV on completion. Thus reducing the burden by 80%. When in the future, there are twenty proposals on the board, this would save the budget 1600PIV or 7.4% of the total monthly budget. Give or take the generous contributor who doesn’t need a refund.  






## 4 Implementation
Instead of rolling out all features at once, it may be more advisable to divide the proposal into more bite-size pieces. What follows is a prioritized list of features based on importance and ease of implementation.


### 4.1 Easy High Impact Change
3.6 Proposal Cost Reductions should probably be the first thing completed. Not because it is extremely core to the governance of PIVX, but because it should be the simplest thing on this proposal by a great deal. Furthermore, it has a great impact considering how small a change it is. 10PIV is more than enough to deter spam votes that won’t pass and even at this point it should save somewhere in the ballpark of 500-800 PIV in fees. In the event this fee proves inadequate to prevent spam, we can raise it to a level that will counter the problem. 


### 4.2 First Core Steps
3.1 One Piv = One Vote, 3.2 Separate Chain Ticket Voting, and 3.5 Wallet Integration should all be completed and released together. The Wallet Integration is key to simplifying the process for users to actually get involved and the other two are the foundations of the process. Without the first three core features, the other features can't function, and these core features can work without the other features being implemented yet.


### 4.3 Later Core Steps
3.3 Ranked Selections and 3.4 Variable Pass Requirements are important features, but they aren’t imminently necessary. We need to have the vote system include more people first and foremost. All other time consuming features need to take a back seat to that goal. With that in mind, we should separate these features and begin them after the 4.2 First Core Steps are completed. Is is important for Devs to keep in mind that the system will eventually go in this direction and make sure they don’t write the initial version in a way that will require rewriting to make these steps happen. 






## 5. Special Thanks
I would like to thank @mgshightech and @turtleflax for their contributions and discussions which directly affected my proposal. I would also like to thank all participants in the Governance channel where the magic has been happening for their hard work. Every person in that channel deserves a pat on the back for their invaluable contributions. I also thank the readers who took the time to read all of these proposals. That is a valuable contribution in itself.