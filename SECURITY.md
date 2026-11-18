# Security policy

Damper is unaudited software that runs on Stellar testnet. It must not be used with real funds. We still want to hear about anything that would be a vulnerability if it were.

## Reporting a vulnerability

Please do not open a public issue.

1. Open the **Security** tab of the affected repository.
2. Choose **Report a vulnerability** and describe the problem privately.

Include what you found, how to reproduce it, and what an attacker could do with it. For the oracle contract that usually means a sequence of calls or a price path, which a failing test makes unambiguous.

We will acknowledge a report within 5 days and tell you what we plan to do about it. Please give us reasonable time to fix a problem before discussing it publicly.

## What is in scope

- The guarded oracle contract: anything that lets a caller move a quote further or faster than its policy allows, call a keeper- or admin-only function, make the oracle return a price it should refuse, or stop it returning a price it should give.
- The keeper and scanner: anything that leaks the keeper's signing key, signs something unintended, or makes the keeper move an anchor it should hold.
- The repositories' CI and dependency configuration.

## What is not

- Behaviour of upstream oracles (Reflector, issuer-run feeds) or of Blend itself. Those belong to their maintainers. We do want to hear when an upstream weakness changes what Damper should defend against.
- Findings that need a compromised admin or keeper key. Both are trusted roles by design and are documented as such.
- The testnet mock feed, which anyone with its admin key can set to any price. It exists only for tests.
