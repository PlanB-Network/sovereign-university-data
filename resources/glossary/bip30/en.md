---
term: BIP30
---

Proposal for improvement involving a soft fork implemented on March 15, 2012, to solve the problem of duplicate transaction identifiers. Before BIP30, it was technically possible to have two different transactions with the same transaction identifier (TXID) in the blockchain. This notably happened twice for coinbase transactions: the one in block 91,880 has the same TXID as the coinbase of block 91,722, and the one in block 91,842 has the same TXID as the coinbase of block 91,812. BIP30 resolved this flaw by imposing a new simple rule: no new transaction can have the same TXID as a previously recorded transaction unless the original transaction had been completely spent (i.e., all its outputs had been used). This soft fork was activated using the flag day method. Thus, it is one of the first UASFs.