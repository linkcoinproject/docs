# Technical Foundation: IronTX

## 4.1 The Malleability Fix

IronTX introduces canonical transaction serialization, eliminating all malleability vectors. Every transaction has exactly one valid encoding.

## 4.2 IronTxId: Stable Transaction Identifiers

IronTX introduces a secondary transaction identifier excluding signature data:

```
Standard TxId = Hash(version∥inputs∥outputs∥locktime∥signatures)
IronTxId = Hash(version∥inputs∥outputs∥locktime)
```

The IronTxId remains stable regardless of signature variations.

## 4.3 Activation Status

| Network | IronTX Height | Status |
| :--- | :--- | :--- |
| **Mainnet** | Block 12,000 | Active |
| **Testnet** | Block 12,000 | Active |
| **Regtest** | Block 0 | Active |

## 4.4 Schnorr Signatures

Linkcoin implements BIP-340 Schnorr signatures natively:

*   **Linearity**: Enables signature aggregation (MuSig2)
*   **Batch Verification**: 2-3x faster block validation
*   **Adaptor Signatures**: Building block for atomic operations
*   **Simpler Security**: Provable in random oracle model
