BitShare Dividend Algorithm
---------------------------

Dividends are generated with each new block as 50% of the transaction fees and mining rewards.

Because Dividends are generated via mining, they cannot be confirmed nor spent for 120 blocks. If
we were to attempt to pay out dividends sooner than that then a chain split would invalidate
all transactions on the bad chain and the dividends could generate a lot of 'dust' (aka: outputs to small to spend).

As a result the following algorithm will be used to claim dividends:

1) Whenever an output is spent, it may claim all dividends from blocks with more than 120 confirmations as
part of the balance.

2) All dividends from blocks less than 120 confirmations become part of the transaction fee.  This will
serve to aggregate all of these 'unconfirmed' dust dividends into a single fee that will be 'recycled' once
the next block reaches 120 confirmations.

3) The end result is that high-frequency transactions generate more dividends for those who hold! 

4) 'inter-day-trading' by rapidly minting will result in 0 dividends and thus no profit opportunity. 

5) For high-speed trading, do that off chain where you can speculate with sub-second timing if you like.


Dealing with Dust
-----------------
A challenge with paying Dividends is that they generate 'dust' as a result of dividing a
small number (25 BitShares in fees) by a large number (21,000,000) in total BitShares which
generates a dividend payment of .0000012 per BitShare or given the minimum transaction fee
of 0.00005 a dividend payment of 0.00000000006 for very small balances.  The result is that
rounding errors will accumulate and could slowly destroy the currency through use. As a result, 
all dividends will be rounded down to the nearest satashi and to compensate for this 'lost'
dust the mining reward will never reach 0, but will always produce at least .001 a BitShare reward. 

This reward is never paid to the miner, but instead always paid out as dividends and thus does
not constitute debasement of the currency but a means of recovering value lost as dust in a manner
that has a slight bias toward larger balances over small balances.   Small transaction outputs will
have a larger percentage of their dividend lost to 'dust'.  



