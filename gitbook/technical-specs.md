# Technical Specifications

## A.1 Network Parameters

| Parameter | Mainnet | Testnet |
| :--- | :--- | :--- |
| **P2P Port** | 7200 | 72555 |
| **RPC Port** | 7200 | 72555 |
| **Address Prefix** | L | l |
| **IronTX Height** | 12,000 | 12,000 |

## A.2 Proposed Opcodes

| Opcode | Hex | Purpose |
| :--- | :--- | :--- |
| **OP_CHECKLNCEDUTXO** | 0xc0 | Verify linked UTXO in same TX |
| **OP_CHECKUTXOSPENT** | 0xc1 | Verify UTXO has been spent |
| **OP_CHECKUTXOSPENTBY** | 0xc2 | Verify UTXO spent by pubkey |
