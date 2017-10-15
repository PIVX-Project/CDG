# Basic Weighted Vote Voting System

## Abstract

A voting system that makes use of weighted voting.

## Introduction

This proposal focuses on the following key components of a voting system:

1. Who can vote., i.e. holders, stakers, voting node owners, masternode owners.
2. Voting weights, if any, i.e. 0.25 weight per PIV for holders, 0.5 weight per PIV for stakers, 1.0 weight per PIV for masternode owners.
3. How many “voting layers” there are, i.e. single layer, separate layers for each group.
4. The vote thresholds for passing/failing proposals, and whether thresholds are different for some categories, i.e. higher threshold required to modify transaction fee burning.

Although there are many other governance features which can be implemented into this voting system, if any of these features are desirable, they can be adapted into the voting system, so there is no need to further complicate this proposal that is focused on a few key components.

## Goals

This proposal presents a weighted voting system that seeks to allow as many people to vote as possible, while still incentivizing larger holdings of PIV. The voting system is designed with the assumption that those with the most PIV have the most to lose by voting incorrectly, and the most to gain by voting correctly, and should thus be given relatively higher voting power than those with less stake in PIVX. But still, the thresholds for passing/failing proposals must be defined to optimally combat the passing of bad proposals, the failing of good proposals, and development gridlocking, in order to address the possibility that bad actors, whose goals are not aligned with the growth of PIVX, accumulate significant amounts of PIV in order to harm PIVX.

The proposal also seeks to illustrate how different options in the above key components affect voting “fairness”, resilience to foul play, and incentive for people to hold/accumulate more PIV.

The author believes that many voting systems can work well for PIVX, but that PIVX would benefit most from one which is very resilient to foul play without unduly negatively impacting the utility of the coin. Many potential voting systems will not be presented by the deadline for submitting proposals for Community Designed Governance, October 16th, 2017, so readers are asked to please not exclude other voting systems from consideration simply because they are not presented in a proposal at this time.


## Implementation

### Who can vote

Anyone with any amount of PIV can vote. But in case this may pose network congestion or attack issues, a minimum amount of PIV inside  a wallet required to vote can be implemented, and/or implement a nominal fee to vote that will apply when the minimum threshold to avoid that fee is not met, but the minimum threshold to still vote is met. This nominal fee amount should be chosen to effectively deter network issues only, and not used to unduly punish those who do not meet some arbitrarily-decided amount of PIV required to vote without a nominal fee applying.

### Voting weights

There are four different voting weights, ranging from 50% voting power per PIV for Holders to 100% per PIV for Masternode Owners. The voting weight gap between the different groups can be gradually reduced or eliminated via proposals, if and when it seems prudent to do so.

The reason that a voting weight percentage as low as 50% is used, is that as of now, currently it is only Masternode Owners who have any voting power, while all other groups have none, and it was only through the voting of Masternode Owners that it was unanimously voted to redistribute voting power to the PIVX community at large. This unanimous vote, along with a consistent history of high voter concordance and no foul play, have shown that current Masternode Owners have been highly responsible in governance. The author believes it is only prudent to gradually redistribute voting power with the voting weight percentages presented in this proposal, and to bridge the gap only as the other groups prove themselves able to responsibly vote without causing any passing of bad proposals, failing of good proposals, or gridlocking of proposals.

1. Masternode owners can vote with 1.0 vote weight per PIV. Up to 9,999 additional coins can be “assigned” to a Masternode so that these additional coins can benefit from the 1.0 vote weight per PIV. But any such additional coins would still only receive staking rewards, as currently happens, so Masternode Owner minting rewards remain the same.
2. Stakers with at least 1,000 PIV staked can vote with 0.8 vote weight per PIV. The purpose of this voting weight group is to incentivize people to accumulate and hold onto larger quantities of PIV, even if they can’t or don’t want to buy enough PIV to own a masternode. This can also have a positive effect on PIVX price by locking up PIV.
3. Stakers can vote with 0.65 vote weight per PIV. The purpose of this voting weight group is to incentivize people to contribute to the PIVX network with additional voting power over those who do not contribute to the PIVX network.
4. Holders can vote with 0.5 vote weight per PIV. The purpose of this voting weight group is to incentivize people to buy, use, and hold onto PIV by giving them some voting power, and to allow participation in governance regardless of how much PIV a person owns.


### How many voting layers

One.

Some prefer multiple layers, but the author believes multiple layers are game-able and more prone to gridlock attacks, while a single layer is the most resilient to such foul play. The author is under no illusion that any form of governance can be immune to harm or takeover, but also believes that such issues should be dealt with by methods other than multiple layers, such as higher voting threshold requirements in general, or higher voting threshold requirements to alter key features of PIVX. The facts that PIVX voting history has high voter concordance and no signs of foul play since its inception, and Masternode Owners have unanimously voted to reduce their own voting power, are compelling evidence that the current Masternode Owners can be trusted to establish higher voting threshold requirements for removing/altering the key features of PIVX right now, so that it would require a significantly larger investment by bad actors to ever successfully harm or take over PIVX years or decades into the future.

Even if attempts are made to add coin age to adjust voting weight of coins based on how long they have stayed put in a layer, malicious actors can simply wait out the coin age time requirement to attain full/near-full voting weight. Additionally, multiple layers will invite complicated forms of gaming such as malicious actors pretending to move between layers, or choosing which layers to move to for different types of proposals which they believe will be passed/failed by some layers but not other layers.

Coin age-based voting weight will not just cripple the voting power of malicious actors when moving funds between layers, but it would also cripple the voting power of good actors attempting to counteract the actions of the malicious actors by also moving funds between layers. Considering such good actors can only move between layers in reaction to the malicious actors and can be deceived by false movements between layers by the malicious actors, malicious actors can simply wait out their coin age time requirement to vote while good actors trying to counter them are still waiting for their coin age time requirement to expire, so bad actors may actually be advantaged by coin age while good actors disadvantaged.

Finally, any coin age-based voting weight will punish people who transfer PIV around, such as people who actually use PIV to buy and sell things, by reducing their voting power. It is the author’s belief that multiple layers would only end up offering significant advantages to malicious actors attempting to harm or orchestrate takeover of PIVX, who would then be able to do so with relatively less holdings of PIV than would be required if there was only one layer.

### The voting thresholds for passing or failing proposals, and whether thresholds are different for some categories

Currently, in order for a proposal to pass, it requires more than 50% of the votes to be “Yes”, with at least 5% of the total voting pool voting “Yes”.

With the inclusion of holders and stakers in the voting pool, it will be possible for those with less than 10,000 PIV invested to help chart the course of PIVX development. These smaller holders have less to lose than Masternode Owners by voting improperly, whether intentionally or due to accident/lack of understanding. Although it would take a significant amount of coins owned by bad actors and/or many very uninformed voters for a bad proposal to pass or for a good proposal to be gridlocked, it is best to determine the optimal thresholds at the start to make the voting system as resilient to foul play as possible.

The author recommends that the threshold required for a proposal to pass be increased slightly, from 50% to 55-65%, to make it more difficult for bad proposals to pass. This will also make gridlock attacks easier, but the author believes that the passing of bad proposals is more dangerous than the gridlocking of good proposals, especially if a method is implemented to protect existing key features with higher voting thresholds.

In this voting system, the following voting rules apply:

1. For a proposal to pass, at least 5% of the total possible votes (after adjusting for voting weights) must vote “Yes”.
2. For a proposal to pass, at least 60% of the votes on the proposal must be “Yes”. The proposal will fail if at least 40% of the votes on the proposal are “No”. Although this proposal uses 60% as the threshold, the actual number used should be determined only after much consideration, since this threshold will determine how resilient the voting system will be to different types of voting attacks.
3. If a proposal is not submitted at least 168 hours (1 week) before the end of the current cycle, it will be rolled over to the next voting cycle (next 30-day period), and any existing votes will persist over both cycles to avoid needing to revote. The purpose of this rule is to prevent bad proposals from being submitted and voted in towards the end of a voting cycle, and to allow the percentage threshold of rule #1 to be low.
4. The community can vote on proposals to add one or more existing features to a “PIVX Constitution”. When an existing feature is successfully added to the “PIVX Constitution”, it will gain the benefit of a new voting threshold requirement to either remove, modify in what ways, or modified to the amounts/degrees, as specified in the proposals. Any “PIVX Constitution” proposal must clearly specify in what way an existing feature is to be protected and conditions under which the protection should apply, i.e. not to be removed, not to be modified to specific degrees, indefinitely, for a specific period of time, becoming null and void under certain circumstances such as during periods of time PIVX is above a specific market cap, etc. If a “PIVX Constitution” proposal is not submitted at least 504 hours (3 weeks) before the end of the current cycle, it will be rolled over to the next voting cycle (next 30-day period), and any existing votes will persist over both cycles to avoid needing to revote. The voting threshold requirement is equal to whatever voting percentage was achieved minus 15%, and any “PIVX Constitution” proposal that does not pass with at least 75% “Yes” votes will not pass (75% minus 15% equals 60%, the normal threshold for passing proposals).

Example A: PIVX Constitution proposal “Do not remove transaction fee burning” to apply “Indefinitely” passes with 98% “Yes” votes. Transaction fee burning feature of PIVX can only be removed now if at least 83% of votes are “Yes” (98% minus 15%).

Example B: PIVX Constitution proposal “Do not reduce transaction fee burning by more than 50%, or increase transaction fee burning by more than 175%” to apply “So long as coins are not burned faster than coins are minted as measured over a one year period” passes with 86% “Yes” votes. Transaction fee burning feature of PIVX can only have fee reduced by more than 50%, or increased by more than 175%, if a proposal to do either passes with at least 71% “Yes” votes (86% minus 15%), unless the condition of "So long as coins are not burned faster than coins are minted as measured over a one year period" is no longer met, in which case the feature is no longer protected by the PIVX Constitution proposal threshold of 71%.

Example C: PIVX proposal “Do not let Verge head dev join PIVX team” to apply “Until he publicly admits Verge has wrongly slandered PIVX” passed because someone was bored. The attempt to make this proposal a PIVX Constitution proposal failed, because during the PIVX Constitution proposal, only 73% of the votes were “Yes”, when a minimum of 75% of the votes must be “Yes” for a PIVX Constitution proposal to pass.

Although minus 15% is used here, the exact number should be determined after much consideration. Slight changes in this number can have drastically different effects on how effectively PIVX Constitution proposals can deter malicious actors, and how likely PIVX Constitution proposals may cause gridlock issues. The author believes it is desirable to have the percentage not too high in order to make Constitution proposals effective, but at the same time not too low that if it ever becomes desirable to amend a feature protected by a Constitution proposal (technology and opinions change all the time!), that bad actors are effectively deterred from gridlocking the overturning of a Constitution proposal.

5. The community can vote on a proposal to overturn an existing “PIVX Constitution” proposal. In order for the proposal to succeed, “Yes” vote % must meet the threshold for overturning the proposal, as determined by rule #4. If a proposal to overturn a “PIVX Constitution” proposal is not submitted at least 504 hours (3 week) before the end of the current cycle, it will be rolled over to the next voting cycle (next 30-day period), and any existing votes will persist over both cycles to avoid needing to revote.

## Disadvantages

This voting system is essentially a plutocracy, and is, on the surface, more plutocratic with its distribution of voting power than the other currently presented voting systems, even though a plutocracy can exert just as much if not more power over voting systems by manipulating a multiple layer voting system. With a plutocracy, there is always the possibility that malicious actors will gain enough power to control the voting system of any currency, to either harm the currency outright, or to cyclically create market fears and buy and sell accordingly to gradually take over an increasing portion of the currency. The author does not believe the other currently considered voting systems are any more resilient to such manipulation, but if ever in the future it becomes cost-effective to and we can reliably prove the identities of voters, then it becomes conceivable to move more towards a democracy, which can in theory result in governance of PIVX which is more beneficial to small PIVX holders by giving them more voting power per PIV than large PIVX holders. Then it becomes a question of whether or not it is desirable to disempower large PIVX holders in this manner. It is the author’s opinion that although greater vote equality is highly desirable for the governance of nations, it is not necessarily desirable for the governance of open-source digital currencies, since the primary goal of the large asset holders of self-gain should be in perfect alignment with the primary goal of PIVX of development and adoption as a digital currency, with the exception of bad actors.

This voting system rewards, incentivizes, and protects larger PIVX holders, and marginalizes smaller PIVX holders. But it should be noted, that right now Masternode Owners control 100% of the voting power, and with the voting numbers used in this proposal and the current number of Masternode Owners relative to the total coin supply, they would transfer at least 25% of their voting power to the other groups. The author believes that the voting weight numbers in this proposal are more than fair at the beginning, and if and when it seems suitable, the voting power gap between the different groups can be reduced. And if and when the other groups have also proven themselves to be highly responsible voters, and that no voting issues like gridlocks have occurred and do not seem likely to occur, the voting weight differences can be removed.

This voting system isn’t anywhere as marketable as 1 PIV 1 Vote. Some people may even be offended by how disingenuously it tries to incentivize people to hold and accumulate PIV, even though it could be argued that those with larger PIV holdings have the most to lose if foul play happens and the most to gain by becoming and staying knowledgeable and aware of what’s going on and guiding the development of PIVX by voting properly.

This voting system does not incentivize staking nearly as well as Turtleflax’s Voting Ticket System, where people get voting rights whenever they earn staking rewards.

This voting system may require some method of preventing multiple voting with one coin. Turtleflax’s Voting Ticket System rewards voting tickets inherently wouldn’t have to implement any method of preventing multiple voting with one coin. An example of a method to prevent multiple voting with one coin, would be to assign voting weight to PIV that have been used to vote based upon the group/groups of voting power of PIV, and only if those PIV still remain within the same wallet. This method would allow people to vote on proposals and have their voting weight visibly factored into ongoing vote results, but ultimately, the amount of voting power the coins will have will depend upon whether or not the voters still have the coins at the end of the voting cycle and what group/groups of voting power the PIV in their wallet fit under.

## Clarifications of a few things

Masternode owners can vote with 1.0 vote weight per PIV. Any PIV they own in excess of 10,000 locked in a Masternode and located within the same wallet will also benefit from the 1.0 vote weight per PIV up to a total of 19,999 PIV (10,000 normal cost to run a Masternode, up to 9,999 additional PIV assignable to that Masternode). Any PIV beyond the original 10,000 locked in a Masternode that is assigned to a Masternode, would still only be able to receive staking rewards instead of Masternode minting rewards, as currently happens. Any PIV in excess of 19,999 PIV total assigned to a Masternode, will only have the same voting weight as stakers with at least 1,000 PIV staked. This will reward Masternode Owners who hold onto/accumulate PIV in excess of increments of 10,000 by giving such PIV the same voting power, while at the same time the 9,999 excess limit to receive the same voting power, encourages Masternode Owners to create more Masternodes by disincentivizing assigning more PIV to one Masternode when he has enough PIV to create an additional Masternode.

Stakers with at least 1,000 PIV staked can vote with 0.8 vote weight per PIV. It may be desirable to raise or decrease this 1,000 PIV minimum in relation to the value of a stable fiat currency, so that it remains an effective incentivize for people to attempt to accumulate more PIV in order to qualify for the higher vote weight per PIV.

