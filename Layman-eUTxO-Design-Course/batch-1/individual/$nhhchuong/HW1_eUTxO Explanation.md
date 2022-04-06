**Summary about eUTXO**

Firstly, about UTXO [1] 
* UTXOs are locked up box full of coins.
* The lock can be opened by providing the right key.
* When you spend some coins, you create a transaction (or the wallet does it for you) that consumes some old UTXOs (old UTXO becomes spent) and creates a bunch of new UTXOs. 
* UTXOs are always consumed as a whole, and change UTXO is created automatically by your wallet to get back the balance.

UTXO model has some flaws including lack of Turing-completeness, value-blindness, lack of state which basically requires introduction of more complex logic (smart contracts) [2].

The Extended UTxO Model (eUTXO) preserves UTXO’s structure while adding support for more expressive smart contracts
* Instead of restricting locks to public keys and keys to signatures, addresses in the EUTXO model can contain arbitrary logic in the form of scripts [3]
* outputs in eUTXO can carry (almost) arbitrary data in addition to an address and value. This makes scripts much more powerful by allowing them to carry state information [3]

References:
[1] https://medium.com/bitbees/what-the-heck-is-utxo-ca68f2651819
[2] https://ergoplatform.org/en/blog/2021-07-23-ergo-utxo-model-the-evolution-from-bitcoin-to-ergo/
[3] https://docs.cardano.org/plutus/eutxo-explainer
