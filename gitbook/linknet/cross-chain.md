# Cross-Chain Links

## 5.3 Cross-Chain Links

Trustless connections to other UTXO blockchains via adaptor signature atomic swaps.

### Adaptor Signature Atomic Swap

1.  Alice generates secret `s`, publishes `T = s · G`
2.  Both create adaptor signatures locked to `T`
3.  Alice reveals `s` by claiming on Chain B
4.  Bob extracts `s` from published signature, claims on Chain A

**Result**: Trustless, atomic, no intermediary

### 5.3.1 Supported Chains

| Chain | Signature | Support |
| :--- | :--- | :--- |
| **Bitcoin (Taproot)** | Schnorr | Native |
| **Litecoin (MWEB)** | Schnorr | Native |
| **Bitcoin (SegWit)** | ECDSA | Via 2P-ECDSA |
| **Ethereum** | ECDSA | Via 2P-ECDSA |
