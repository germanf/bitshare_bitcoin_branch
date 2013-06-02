BitShares - A dividend paying crypto-currency
================================

BitShares is an new crypto-currency that improves upon BitCoin by offering
the olders of BitShares dividends while providing a new hashing algorithm
that will keep the blockchain decentralized and help prevent 51% attacks.

BitShares is committed to decentralization of the money system and therefore
aims to take every measure possible to defend against the forces that are
already starting to centralize the Bitcoin / Litecoin economies. 

Dividends
------------
The defining feature of BitShares is that it pays you dividends from half the
mining reward and transaction fees.  These dividends make it equally as profitable
to mine as to 'own' BitShares as in the long-run the profit from mining will
approach the profit from owning. 


Proof of Work
-------------
Both BitCoin and LiteCoin use a proof of work system that is easily accelerated
by specialized ASIC or even GPUs.   If LiteCoin ever becomes as popular as Bitcoin
then it will be no more secure against ASIC centralization than Bitcoin.

To be truly secure against specialized hardware, the hash function must require
the use of many transistors in a configuration that is already as optimized as 
possible and widely distributed across all computers in the industry.  Transistors
are the building blocks of all ASICs and specialized ASICS gain their performance
advantage by optimizing the use of transistors.  

  - RAM (or Cache) is already the single largest consumer of transistors in modern CPUs.  
  - RAM is already as optimized as possible, specialized ASIC will not be able to improve upon it.
  - RAM access is already the bottleneck on modern GPUs and CPUs.  
  - RAM is everywhere and widely distributed.
  - RAM is 'power-hungry' and thus ASICs would not gain much power savings.
  
As a result BitShares will use a new hash algorithm that uses psuedo-random access to 128 MB
of RAM per hash.  It would require 1 GB of RAM to do 8 hashes in parallel and therefore GPUs
would have no advantage over CPUs with 8 cores. GPUs gain most of their performance using
multi-layer caching and if your dataset does not fit in one of the local memory areas then
there is a significant performance hit.

Another way to prevent specialized ASICS from optimizing the hash is to require a lot of
branching (mis-predictions) and to design the algorithm such that each step depends upon
the result of a prior step.  The more potential branches and variations on 'instructions'
used the less well suited the hash function will be to GPU use and ultimately a 'specialized'
ASIC would have to be as complex as a CPU.   

All of that said, it is always possible to build specialized hardware to optimize some
opperations.  The goal is to make such 'optimization' only apply to parts that do not
represent the bottleneck and therefore even a 10x increase in the performance of those
operations would result in only marginal over-all gains. 


Limited Bandwidth / Storage Requirements
----------------------------------------

If there are no defined limits on block-size then eventually the network will be
concentrated in the hands of high-end servers.  These servers will ultimately have 
complete control over what transactions can get into blocks. This combined with 
colored-coins and following of transactions through history would give Governments
even more power than they have today.

As a result, BitShares will place a limit on BlockSize growth and bandwidth usage to
be 1 MB per block sustainable today over common DSL connections and in years ahead should become a
trivial amount of bandwidth that every cellphone could handle.

The side effect of this that space in the blocks becomes a scarce resource which will
bid up transaction fees.  Unlike other block chains, high transaction fees are not 
much of a problem so long as you leave your money parked long enough to earn some
dividends.  The higher the transaction fees become, the more valuable it will be 
to buy and hold BitShares because half of all transaction fees are paid out as
dividends.

High Transaction fees will also push people to use off-chain services like 
OpenTransactions which can handle high-speed anonymous transactions without any
transaction history.  Generally speaking it is far better to conduct banking on
an OpenTransactions server than through the block-chain.   OpenTransactions 
destroys the transaction history which will provide much better security.

BitShares should be used for savings while OpenTransaction's is used for checking.


Blockchain Compression
----------------------
Bitshares will free clients from having to store the complete transaction history.  Each
block a hash of all unspent outputs is included in the merkel root and therefore allows
a client to use this much smaller database as equally authoratative as the complete
transaction history.   Each client could decide for itself how much history it needs 
to protect against double spends.



