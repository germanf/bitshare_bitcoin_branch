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


