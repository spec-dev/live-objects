# Latest Interaction

Represents the latest "interaction" between 2 addresses on ethereum. 
Currently, only transactions are represented (traces will be included later),
with each interaction categorized as either `wallet --> wallet` or `wallet --> contract`. 

---

**Namespace:** `eth`
**Name:**  `LatestInteraction`
**Version:**  `0.0.1`

---

## Interface

```typescript
export interface LatestInteraction {
    // Address this transaction or trace was sent from.
    from: string

    // Address this transaction or trace was sent to.
    to: string

    // Specifies whether the sender or recipient is a wallet or a contract.
    interactionType: LatestInteractionType

    // The transaction or trace hash.
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
    ContractToWallet = 'contract:wallet',
    ContractToContract = 'contract:contract',
}
```