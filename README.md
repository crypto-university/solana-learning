# solana-learning
Learnings on Solana

## Setup

### Local Test Validator

https://docs.solana.com/developing/test-validator

This ships with solana cli and can be started with 

```bash
solana-test-validator
```

### Solana Commands

```
solana config get
```

## RPC

LocalNet
```bash
solana config set --url http://127.0.0.1:8899
```

Devnet url 
```bash
solana config set --url https://api.devnet.solana.com
```

Mainnet URL 
```bash
solana config set --url https://api.mainnet-beta.solana.com
```



## Terminology

### Lamports

1 lamport = 10^-9 Sol. Smallest Unit in Solana

## Special Programs

* Systems Program - `11111111111111111111111111111111` 
* Token Program - `TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA`
