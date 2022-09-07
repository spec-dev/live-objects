# New Interactions

Publishes the latest interactions between addresses for each new block.

* **Namespace:**  `eth`<br>
* **Name:**  `NewInteractions`<br>
* **Version:**  `0.0.1`<br>

## Data

An array of [`eth.LatestInteraction@0.0.1`](/live-objects/eth/LatestInteraction/eth.LatestInteraction@0.0.1.md) objects.

## Example

```javascript
{
    id: 'fNkxgHAXu9wMNqigTcAEZN',
    nonce: 1,
    name: 'eth.NewInteractions@0.0.1',
    origin: {
        chainId: 1,
        blockNumber: 15486604,
        eventTimestamp: '2022-09-06T22:10:29.165Z'
    },
    data: [
        {
            from: '0x6036bc771ef0e3049ff7f6bc70a9b67654064f49',
            to: '0x17293fad6ac8d74071578ff276f95e7c48a16258',
            interactionType: 'wallet:wallet',
            hash: '0xa530c2de47b1842c28c52c89d380c359f3273e6e8bfc2271f9b917305550894b',
            timestamp: '2022-09-07T03:10:07.000Z',
            blockHash: '0x1ace11243c721cb88fb5c5e8a8511ff197faede50f1c7901d0ade88e02da9582',
            blockNumber: 15486604
        },
        {
            from: '0x52b3ff6258345d97f65335ce5fee478b63f80c73',
            to: '0x17293fad6ac8d74071578ff276f95e7c48a16258',
            interactionType: 'wallet:wallet',
            hash: '0xd5d8ffe037a4f2069b3ed9fa9364d2785853ec8619b6fdaa8fedb0424798f74c',
            timestamp: '2022-09-07T03:10:07.000Z',
            blockHash: '0x1ace11243c721cb88fb5c5e8a8511ff197faede50f1c7901d0ade88e02da9582',
            blockNumber: 15486604
        },
        // ...
    ]
}
```