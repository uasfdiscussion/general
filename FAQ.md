# USAF FAQ

## USAF General Questions
### Does a UASF use node count to determine activation?
A UASF does not require signaling, voting, or counting nodes. If rough consensus can be had by major economic players (exchanges, major businesses, etc.), a flag date or block height would be set, at which point all economic nodes would enforce the rules of the UASF.  Users that decide to enforce the new rules will only follow blocks that conform to the existing rules.  A UASF could be enforced by any number of economic nodes, although miners may only choose to follow such rules if there was significant economic weight behind it.

### Will a UASF cause a chain split?
All soft forks (both miner signaled and user activated) have the possibility of chain splits.  Soft forks rely on the economic incentives of the majority of miners and economic actors to reject invalid blocks based on the new ruleset.  Since the new rules are a stricter set than the old rules, any chain split presents asymmetrical risks to the chain with the old rules.  If the majority of miners enforce the new ruleset, all blocks produced that are invalid in the new ruleset will eventually become orphaned.  This economic incentive pushes miners to enforce the new rules. A User Activated Soft Fork also uses similar economic incentives.  If the majority of hashing power enforces the new rules, chain splits remain temporary as with a soley miner enforced soft fork.  
If the majority of hashpower does not enforce the rules, a chain split would occur.  If there is a greater demand for the blocks produced by the soft fork enforcing miners, then profit-driven miners would eventually flock to this chain, leading to the orphaning of the pre-soft-fork chain.  If the demand is less for the soft-fork chain, then both chains may co-exist indefinitely.

### How can miners prevent a chain split?
Miners can prevent a chain split if the majority of miners enforce the UASF rules.  Miners typically have an economic incentive to avoid a chain split.  Provided that the UASF changes are reasonable, the economic actors support the soft fork, it can be reasonably enforced by miners, and miners are given sufficient time to upgrade their systems, then a chain split is unlikely.

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
If users proposed a soft fork, the economy could reject it by not installing software that enforces it. This would result in a chain split with very few users following the new rules.  Such a split is always possible through a minority spin-off coin.  Bitcoin ultimately allows users the freedom to create their own spin-off whenever they choose.  However, they would no longer be part of the same network.

### What is the Worst Case Scenario for a UASF?
The worst case scenario of a UASF is a permanent chain split.  This can happen if the economy does not enforce the new rule and the value of the original chain retains value greater than the new chain.  In this case, there are two coins that result - one with the vast majority of the economy rejecting the UASF and one with the a few users using the new rules.  Users can choose to abandon their chain if they miscalculated and the economy was not truly supportive of the soft fork, or continue as a spinoff if the features of the new chain are worth more to them than the network effect of Bitcoin.

## BIP148 Questions
### How does BIP148 Work?
BIP 148 works by setting a flag date for mandatory signalling of SegWit.  After this date (August 1, 2017), miners must signal readiness for SegWit by creating blocks with the version bit 1.  Miners do NOT need to support SegWit or even produce blocks that contain SegWit transactions.  Miners must also check blocks prior to their own and ensure that they also signal for SegWit, and only build on those blocks.

### What is the effect on users with Segwit aware clients?
BIP148 was created to avoid having to force most users to upgrade their software.  A vast majority of the nodes currently deployed are aware of the BIP9 signalling for SegWit.  BIP148 is designed to motivate miners to signal for SegWit so that it is activated in a way that even users who are not running the UASF will get the benefits of the activation of SegWit.

### What do miners need to do to enforce BIP148?
At a minimum, miners should make sure they have a border node that enforces BIP148 (and eventually filters out invalid SegWit blocks).  They should also update their software to produce blocks with version bit 1 enabled prior to the flag date.  Miners do not need to create SegWit blocks or make any other changes.

### What do users need to do to enforce BIP148?
Users should use clients that enforce BIP148.  Users that run full nodes would upgrade to one that enforces BIP148, or run behind a border node.  Users of light clients should check with each vendor to see their support for BIP148.  We plan on detailing any public responses from wallets regarding BIP148 support.

### What are the various scenarios that could happen from BIP148?
The best case scenario is if the majority of miners enforce BIP148, then all users if Bitcoin (including all light-clients) will converge upon a single chain.  After 2016 blocks are mined on this chain (which would take between 2 and 8 weeks, depending on when an activation period starts, and how many miners enforce the rule), SegWit would become locked in.  After another 2016 blocks (roughly 2-4 weeks), SegWit will become activated.  Users who do not enforce BIP148 may see blocks that are occasionally orphaned.  Depending on the hashpower mining BIP148 invalid blocks, these chains may be significant in length.  In an ideal situation, very few of these blocks will be mined.

In a worst case scenario, a majority of miners will not enforce BIP148.  Users that do not enforce BIP148 will follow that chain, and users that follow BIP148 will follow a separate chain.  If the BIP148 chain does not have significant economic value, it will likely die.  If it does have significant economic value, then miners will have a chance to join this chain.  It may eventually become the majority and a reorganization would occur for non-BIP148 enforced users.

A final scenario is no miners enforce BIP148, and no blocks are mined for any BIP148 users after a certain point.  At this point, users would have to decide the best way to proceed.  Options may include a POW change or simply setting a flag date in the future that requires enforcement of SegWit (but not signalling).

### Why was the date of August 1, 2017 Chosen?
Version Bit 1 for SegWit expires on Nov 15, 2017.  To guarantee activation of BIP9 compatible clients, they would need to see a full activation period with BIP148 enforced.  This could take up to 4 weeks (assuming the majority of hashpower enforces it).  However, a signalling period may not line up exactly with Nov 15.  In the worst case scenario, one completes immediately after Nov 15.  This would mean you would need 8 weeks before Nov 15 to enforce it.  This would require enforcement to start at least by Sep 20, 2017. By moving it back to August 1, it gives an extra buffer in case there is an initial slow enforcement period, followed by increased enforcement if miners determine that it is more economical to follow BIP148 than not.


### How can we show support for BIP148?
The best way to show support is to champion it through social media (Twitter, Facebook, etc...) and petition businesses and wallets to support it.
