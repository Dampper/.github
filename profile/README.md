<p align="center">
  <img src="https://raw.githubusercontent.com/Dampper/.github/main/profile/damper-wordmark.png" alt="Damper" width="420">
</p>

**Damper keeps lending pools on Stellar from being drained by a bad price.**

A lending pool is only as safe as the price it reads. In February 2026 one trade on a market with almost no volume moved USTRY from about $1.06 to $106.74, and the YieldBlox pool on Blend lent about $10.2M against collateral that was never worth it.

Damper is a SEP-40 price oracle that sits between a pool and its upstream feeds. It takes the median of several fresh sources, limits how fast a collateral price may rise away from a stored anchor while letting real crashes through so liquidations keep working, and is watched by a keeper that reports what the pool cannot see for itself.

| Repository | What it does |
| --- | --- |
| [damper-contracts](https://github.com/Dampper/damper-contracts) | Rust / Soroban guarded oracle: median over fresh feeds, per-asset anchor clamp, keeper-only anchor updates, and a replay of the YieldBlox exploit |
| [damper-backend](https://github.com/Dampper/damper-backend) | TypeScript pool scanner and keeper: traces every Blend reserve to its price source, scores how cheaply it could be manipulated, and keeps anchors current |
| [damper-frontend](https://github.com/Dampper/damper-frontend) | Pool risk dashboard: which pools could be drained through a manipulated price, how cheaply, and where each price comes from. [Live](https://dampper.github.io/damper-frontend/) |

### Contributing

Start with the CONTRIBUTING guide in the repository you want to work on. Issues are labelled by complexity (`trivial`, `medium`, `high`) and `good first issue` where they exist, and each one states what to do and how it will be checked.

### Status

Damper runs on Stellar testnet and has not been audited. Please do not use it with real funds. To report a vulnerability, see [SECURITY.md](https://github.com/Dampper/.github/blob/main/SECURITY.md).
