# Examples

## Table of content

5.1. [Example Voting Math](#51-example-voting-math)

5.2. [Scenario 1](#52-scenario-1)

## 5.1 Example Voting Math

For vote options A,B,C,D, null and public keys labelled 1,2,3 ...  consider the following data matrix:

| ID  | Status | PIVS | Filter |S%     | I vote | I%   | N<sup>2</sup>  |N<sup>2</sup>%| Rank Vector|% total|
|-----|--------|------|--------|-------|--------|------|------          |------        |------------|-------|
|     |        |      | Output |       |/1000   |      | Vote           |              | Top First  |       |
| 1   | none   | 550  | 500    | 0     | 30     | 2.14 | 42             | 3.5          | ABDNC      | 5.64  |
| 2   | none   | 5000 | 4000   | 0     | 954    | 6.83 | 145            | 12.1         | ACBND      | 18.93 |
| 3   | staker | 20k  | 14k    | 41.17 | 7631   | 54.61| 307            | 25.6         | BADNC      | 121.38|
| 4   | none   | 3000 | 2000   | 0     | 302    | 2.16 | 96             | 8            | BCNDA      | 10.16 |
| 5   | staker | 3000 | 3000   | 8.83  | 592    | 4.24 | 122            | 10.2         | ADBNC      | 23.27 |
| 6   | none   | 2000 | 1000   | 0     | 95     | 0.68 | 63             | 5.3          | DNACB      | 5.98  |
| 7   | m-node | 10k  | 8000   | 50    | 4069   | 29.32| 163            | 13.6         | ABDNC      | 92.92 |
| 8   | none   | 1000 | 900    | 0     | 80     | 0.58 | 59             | 4.92         | BADCN      | 5.5   |
| 9   | none   | 800  | 700    | 0     | 53     | 0.379| 51             | 4.25         | CABDN      | 4.629 |
| 10  | none   | 600  | 500    | 0     | 30     | 0.215| 42             | 3.5          | ABCND      | 3.715 |
| 11  | none   | 700  | 600    | 0     | 41     | 0.293| 46             | 3.83         | ACBDN      | 4.123 |
| 12  | none   | 1200 | 1000   | 0     | 95     | 0.680| 63             | 5.3          | ABDNC      | 5.98  |
|total|        |      | 36400  | 100   | 13972  | 100  | 1199           | 100          |            |       |


The intended effect of power voting is clearly functioning, as visible in the differing vote percentages between I and <sup>2</sup>.

Notice that some of the system criteria don't make sense with this small of a sample size, so we will omit the 4% single account cap on the I layer. In a real vote, single account vote percentages would of course be much smaller. Also, recall that the m-node gets extra I vote and diminished <sup>2</sup> vote while checking. The vote weights are calculated from the filter output. For the S layer, the vote weights are the filter output for stakers and masternodes. Note that the filter output can not be higher than the PIV holding.

Interpretation:
Option C is eliminated by the S layer because it gets 50% negative (below N) from the only masternode and both stakers also placed it below N, therefore giving it another 50% negative for that layer. No other options are blocked, so the remaining options continue to the macro-vote.

Inspection reveals that N will be the obvious first loser. Therefore we can reduce our further considerations to the options A,B, and D. To simplify the calculation of the weighted copeland scores, we will combine percentages into a single percentage (% total) so that the equation looks like (W-L) * %total  where W is compare wins and L is compare losses.

The weighted copeland scores clearly reveal b as the next loser, leaving only A and B in the struggle for the second weighted copeland score. A eeks out as the winner with 28.147 positive.

|ID     | A (WCS)| B (WCS)| D (WCS)| A (WCS2) | B (WCS2) |
|---    |-----   |-----   |-----   |----------|----------|
| 1     | 11.28  | 0      | -11.28 | 5.64     | -5.64    |
| 2     | 37.86  | 0      | -37.86 | 18.93    | -18.93   |
| 3     | 0      | 242.76 | -242.76| -121.38  | 121.38   |
| 4     | -20.32 | 20.32  | 0      | -10.16   | 10.16    |
| 5     | 46.54  | -46.54 | 0      | 23.27    | -23.27   |
| 6     | 0      | -11.96 | 11.96  | 5.98     | -5.98    |
| 7     | 185.84 | 0      | -185.84| 92.92    | -92.92   |
| 8     | 0      | 11     | -11    | -5.5     | 5.5      |
| 9     | 9.258  | 0      | -9.258 | 4.629    | -4.629   |
| 10    | 7.43   | 0      | -7.43  | 3.715    | -3.715   |
| 11    | 8.246  | 0      | -8.246 | 4.123    | -4.123   |
| 12    | 11.96  | 0      | -11.96 | 5.98     | -5.98    |
| total | 298.094| 215.58 | -513.67| 28.147   | -28.147  |



## 5.2 Scenario 1

There are quite a few roles the people who involve themselves with PIVX
may play. Whether it is one or many, these roles will determine their
interests and how they’ll vote. A few of the important ones are listed
below:

**Whales**

	Fat cats who move large volume, sometimes making visible splashes in the markets.
	Some are just wealthy people, but
	others come from financial institutions who trade with other peoples money.

**Traders**

	From the exchanges, mostly. They like predictable volatility, often use
	backtested tradebots, may be leveraging borrowed currency (margin), and
	mercurially may be either bullish or bearish, depending on if they plan to
	buy or sell, respectively.

**Investors**

	Separate from the traders, because they buy and hold long term. Since they are
	healthy to the system, PIVX incentives
	them with  staking and masternode rewards, which lands them in the S layer.

**Developers**

	The ones who design improvements. You, presumably, in the I layer.

**Suppliers/Customers**

	Using cryptos to trade either goods or services,
	these people will mostly need low transaction fees, stable currency
	values, and quality representation in the <sup>2</sup> layer.



Whale traders often proactively push currency value towards the
direction they think it’s already headed. If they are bulls, they may
publically declare it diamonds, and will vote accordingly. If they are bearish, however, whale
traders will be most likely trying to push the price down.

Suppose some whales from JP Morgan and other financial institutions decide PIVX has potential, although it hasn't been doing all that well lately. First, they act as bears, spreading 'FUD' and doubt, possibly even borrowing PIVX on margin, and selling them. However, as the price dips a bit further, they then buy up a few million $ worth of undervalued PIVX. Some of the bots and traders, seeing how the market has suddenly picked up momentum, following common indicators and technical analysis, also buy in, which drives the price up further.

Now the price is up, but if the whales tried to sell right then, so would the other traders, and besides, they bought PIVX  because they thought it had potential. Even if they did sell soon, they still wouldn't get a vote because of the EMA. Now they wait, and play the role of investors, slowly buying more pivs, as if they were blowing on a feather, until they decide they would finally like to sell. If PIVX is really growing like investors thought, whales are likely to hold their assets long enough to build a vote on the EMA, a likely to st

Suppose now, the devs from the I layer

[vote Scenereo to be finished by Trismegistus or later deleted]