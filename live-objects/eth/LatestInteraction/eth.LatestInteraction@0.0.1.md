# Latest Interaction

Represents the latest "interaction" between 2 addresses on ethereum. 
Currently, only transactions are represented (traces will be included later),
with each interaction categorized as either `wallet --> wallet` or `wallet --> contract`. 

* **Namespace:**  `eth`<br>
* **Name:**  `LatestInteraction`<br>
* **Version:**  `0.0.1`<br>

## Interface

```typescript
export interface LatestInteraction {
    // Address this transaction was sent from.
    from: string

    // Address this transaction was sent to.
    to: string

    // Specifies whether the sender or recipient is either a wallet or a contract.
    interactionType: LatestInteractionType

    // The transaction hash.
    hash: string

    // Timestamp of when this interaction occurred (i.e. block timestamp).
    timestamp: string

    // The hash of the block this interaction occurred in.
    blockHash: string

    // The number of the block this interaction occurred in.
    blockNumber: number
}

export enum LatestInteractionType {
    WalletToContract = 'wallet:contract',
    WalletToWallet = 'wallet:wallet',
}
```

## Constraints

**Unique By:** `(from, to)`<br>

## Associated Events

[eth.NewInteractions@0.0.1](/events/eth/NewInteractions/eth.NewInteractions@0.0.1.md)