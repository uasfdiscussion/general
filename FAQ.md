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


### Isn't a UASF just developers controlled?
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
There are three main scenarios that can occur from BIP148.

The first scenario is when a majority of hashpower immediately complies with BIP148.  In this scenario, any non-compliant blocks (blocks that do not signal for SegWit) will be orphaned.  All Bitcoin nodes will follow this chain as well, and any SegWit aware nodes (0.13.1 and higher) will detect the activation of SegWit.  If the majority of the economy is behind BIP148, then economically motivated miners will enforce BIP148 and this scenario will be likely. 

In a second scenario, if none of the hashrate enforces BIP148, all nodes that enforce BIP148 will see no blocks mined after a single non-SegWit signalling blocks is mined.  In this case, BIP148 users will have to revert back to non-BIP148 nodes.

In a third scenario, if the economic majority enforces BIP148 and a majority of hashpower ignores BIP148, but a significant minority does enforce it (15% of the original hashrate at the time of a split), all nodes that have upgraded to BIP148 will follow a separate chain than the nodes that have not upgraded.  Miners will, however, find difficult to sell their coins.  This would lead economically motivated miners to switch to enforcing BIP148, leading to SegWit activation for both BIP148 nodes and SegWit aware nodes.

The final scenario is when the economic majority is not behind BIP148.  While BIP148 should not be run when the economic majority is not supportive of it, there is no way to guarantee this ahead of time.  In this scenario, a chain split would occur similar to the third scenario, but miners on the BIP148 chain would have difficulty selling coins.  This would eventually lead to a potential split coin scenario, but in all likliehood it would lead to a complete abandoning of the BIP148 chain.

### Why was the date of August 1, 2017 Chosen?
BIP148 allows for the possibility of up to 85% of the hashpower to exit mining and still successfully activate SegWit.  If the hashpower after the flag date of Aug 1, 2017 drops by 85%, it may take 13 weeks to complete an activation period.  In this scenario, SegWit will activate for all BIP148 compliant nodes.

### How can we show support for BIP148?
The best way to show support is to champion it through social media (Twitter, Facebook, etc...) and petition businesses and wallets to support it.  Many users are also altering their node's user agent string to include BIP148.

### How can custodians and receivers of Bitcoins mitigate a potential chain split on Aug 1, 2017?
Awareness is the first key.  Users should pay attention to chain splits and require extra confirmations when accepting payments.  If the majority of hashpower enforces BIP148, there still may be re-organizations that occur on the non-BIP148 chain.  Extra caution should be used.  In the event that the majority of hashpower does not enforce BIP148, users will need to decide the best course of action.  The safest course would be to run both BIP148 and non-BIP148 compliant nodes and ensure receiving payment on both chains.  Users that receieve payment only on the non-BIP 148 chain should be extremely cautious that their chain has a strong possibility of being re-organized and merged with the BIP148 chain.  Users should be extremely cautious when sending coins to custodians around this time to better control their money.  Particularly vulnerable will be wallets and custodians that do not enforce BIP148.  A list of BIP148 supporting businesses and wallets will be made available when possible.

Custodians should be cautious when accepting payments during this time.  For extreme safety, they should only accept payments that reach both the BIP148 chain and non-BIP148 chain.  Custodians that only accept payment on the non-BIP148 chain risk re-organization and possible liability for lost funds.  Until the market is able to properly price the value of the two chains, miners may not have clarity on what rules to enforce.  Once that clarity is provided, custodians can determine which chain is best to follow moving forward.  So long as the economic majority does support BIP148 and it is proven through the market, this would likely be exclusively the BIP148 chain.

### Can BIP148 be cancelled?
In the event that the economic majority does not support BIP148, users should remove software that enforces BIP148.  A flag day activation for SegWit and/or a POW change would be the next logical steps and require coordination of the community.
