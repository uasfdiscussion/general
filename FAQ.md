# USAF FAQ

## USAF General Questions
### Does a UASF use node count to determine activation?
A UASF does not require signaling, voting, or counting nodes. If consensus can be had by all major economic players (exchanges, major businesses, etc.), a flag date or block height would be set, at which point all economic players would begin enforcing Segwit. From that point on the economic majority would orphan any block containing an illegal Segwit spend and those that follow it. Both users and miners would be free to upgrade or not, to utilize Segwit or not, at their own leisure.

### Will a UASF cause a chain split?
All soft forks have the possibility of chain splits.  Soft forks rely on the economic incentives of the majority of miners and economic actors to reject invalid blocks based on the new ruleset.  Since the new rules are a stricter set than the old rules, any chain split presents asymmetrical risks to the chain with the old rules.  If the majority of miners enforce the new ruleset, all blocks produced that are invalid in the new ruleset will eventually become orphaned.  This economic incentive pushes miners to enforce the new rules. A User Activated Soft Fork also uses similar economic incentives.  If the majority of hashing power enforces the new rules, chain splits remain temporary as with a soley miner enforced soft fork.  
If the majority of hashpower does not enforce the rules, a malicious miner could alter the mining code to create an illegal SegWit transaction in a block.  SegWit transactions today are non-standard, are not relayed by the network, and not currently mined by any known software used by miners.  A miner would have to deliberately create an invalid block to cause a fork to the network.  In the event that the majority of hashpower does not enforce this block as invalid, the chain may split.  If the economic majority has upgraded to enforce this rule, then the blocks created by the miners on the invalid SegWit chain will not be able to be sold, as these nodes would consider the blocks invalid.  This leads to an economic incentive to remain on the chain with the stricter rules.  If the majority of miners then start enforcing the new rules, the invalid chain will then be orphaned by unupgraded nodes for having less work.

### How can miners prevent a chain split?
Miners can prevent a chain split if the majority only build on top of valid SegWit blocks and do not mine invalid SegWit blocks.  For miners that have not upgraded to support SegWit, they must filter out invalid SegWit blocks before mining on them.  This can be done by running a border node.  A border node is a node that miners interface with to the outside world.  Most miners already have this configuration present - as they often highly customize their mining software, but want to maintain compatibility with the rest of the Bitcoin ecosystem.

### Isn't a UASF a hard fork?
A hard fork is often confused with a chain split.  A hard fork is a type of chain split where the rules are loosened to allow previously disallowed blocks or transactions.  A soft fork is a tightening of rules.  A soft fork will result in a converged chain if the majority of hashpower enforces its rules.
For a more detailed explanation of types of forks and chain splits, see here: https://medium.com/@alpalpalp/chain-splits-and-resolutions-d3398bddf4ab#.2p61byx24


### How can I make sure I am protected?
This will depend on what type of wallet you use. In the case of something using a centralized service's nodes, make sure the nodes their service uses are upgraded. In the case of something like Electrum, make sure the Electrum server you are using is upgraded. Ultimately any non-fully validating wallet derives information about its balances from a fully validating node. You must take whatever steps you have to in order to ensure your wallet is connected to an upgraded node. In the case of someone running an alternative fully validating client, the method of using a border node that miners can do is equally applicable. 


### Isn't a UASF "proof of ownership of bitcoin.org"?
Absolutely not. In order to safely activate a UASF would require the support of the economic majority of the ecosystem, the exchanges and businesses. Ultimately at the end of the day the consensus rules of Bitcoin are decided upon by the consensus that the economic majority of the ecosystem enforces. This if anything would be a proof of user ownership, the antithesis to the false notion that consensus rules are dictated by miners fiat. 

### Isn't this overriding the miners vote?  Isn't this an attack on miners?
Miner activated soft forks are done to limit the risk of a chain split.  It was never intended to be a vote.  This allows the ecosystem to coordinate when to start enforcing the new rules at a time when it is unlikely to prevent a chain split.  Miners do not have a vote in deciding consensus rules. Ultimately consensus is decided by the economic actors in the ecosystem. A UASF is not overriding miners, it is the economy exerting the decision making power they have always had. A UASF in no way impedes the operation of non-upgraded miners, nor disenfranchises them in any way.  Miner always have the freedom to produce  blocks following any rules they wish, but they may have trouble selling the rewards if the economy does not recognize such coins as valid.

### Can't miners attack the minority chain in the event of a split?
Miners can always attack a chain, but must do so by exerting real and opportunity costs.  There are two main types of attacks.  The first attack would be mining empty blocks.  In the case of a chain split, this kind of attack would actually be beneficial - it would allow the chain to reach a difficulty retarget period faster.  The second kind of attack is an active 51% attack on the chain.  This type of attack requires a majority of hashpower co-operating to orphan valid blocks that have been mined.  This kind of attack is always possible in Bitcoin, but can be defeated by changing the Proof of Work.  These types of attacks are discouraged due to economic incentives- there typically is more to gain by cooperating than attacking.

### Won't blocks become very slow if there is a split?
Both sides of a chain split will produce slower than normal blocks until the difficulty period resets.  This time will be dependent on the share of the hashpower.  For example, if 25% of the hashpower was left on a chain, it would take four times as long (8 weeks) to reach a retarget period.  After this period, blocks would return to 10 minutes.  Cogestion would also likely result in higher fees, which would encourage more mining on this chain and faster blocks until equilibrium would be reached.

### What if someone tried to enforce a UASF that was a bad idea? How can we stop it?
A mining enforced soft fork without the broad support of users that negatively impacted users is a form of a 51% attack.  A sustained 51% attack can be countered with a POW algorithm change, which renders miners attacking useless.  This kind of attack is always possible with POW-based blockchains, and users must be prepared to defend themselves from a hostile mining majority.
If users proposed a soft fork, the economy could reject it by not enforcing it. This would result in a chain split with very few users following the new rules.  Such a split is always possible through a minority spin-off coin.  Bitcoin ultimately allows users the freedom to create their own spin-off whenever they choose.  However, they would no longer be part of the same network.

### What is the Worst Case Scenario for a UASF?
The worst case scenario of a UASF is a permanent chain split.  This can happen if the economy does not enforce the new rule and the value of the original chain retains value greater than the new chain.  In this case, there are two coins that result - one with the vast majority of the economy rejecting the UASF and one with the a few users using the new rules.  Users can choose to abandon their chain if they miscalculated and the economy was not truly supportive of the soft fork, or continue as a spinoff if the features of the new chain are worth more to them than the network effect of Bitcoin.

## BIP148 Questions
### How does BIP 148 differ from a pure flag-date Soft Fork?

### What are the various scenarios that could happen from BIP148?

### Why was the date of August 1, 2017 Chosen?

### How can we show support for BIP148?
