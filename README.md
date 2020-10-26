# Programming Assignment 1: Antonio Campos and Edward Diaz Lopez

## ScroogeCoin
Main focus is to implement the logic used by Scrooge to process transactions and produce the ledger. What is given are Transaction.java (Class that creates transaction), UTXO.java (Class that represents an unspent transaction output aka UTXO), and UTXOPool.java (A mapping from UTXO's to their corresponding transaction).


## Deliverables
We are given TxHandler.java to complete. There are two methods that need to be completed. 
```java
public boolean isValidTx(Transaction tx)

/*
* Returns true if
* (1) all outputs claimed by tx are in the current UTXO pool,
* (2) the signatures on each input of tx are valid,
* (3) no UTXO is claimed multiple times by tx,
* (4) all of tx’s output values are non-negative, and
* (5) the sum of tx’s input values is greater than or equal to the sum of
its output values;
and false otherwise.
*/

public Transaction[] handleTxs(Transaction[] possibleTxs)

/*
*Handles each epoch by receiving an unordered array of proposed
*transactions, checking each transaction for correctness,
*returning a mutually valid array of accepted transactions,
*and updating the current UTXO pool as appropriate.
*/


```
TxHandler.java returns a mutually valid transaction set of maximal size (one that can’t be enlarged simply by adding more transactions).
