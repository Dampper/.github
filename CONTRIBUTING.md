# Contributing to Damper

Thanks for looking. Each repository has its own CONTRIBUTING guide with setup and test commands; this page is what they share.

| Repository | Guide |
| --- | --- |
| damper-contracts | [CONTRIBUTING.md](https://github.com/Dampper/damper-contracts/blob/main/CONTRIBUTING.md) |
| damper-backend | [CONTRIBUTING.md](https://github.com/Dampper/damper-backend/blob/main/CONTRIBUTING.md) |
| damper-frontend | [CONTRIBUTING.md](https://github.com/Dampper/damper-frontend/blob/main/CONTRIBUTING.md) |

## Picking something to work on

Look for issues labelled `good first issue` or `help wanted`. Every issue has a context paragraph, what to do, acceptance criteria and where to look. Comment on the issue to get assigned before you start, so two people do not build the same thing.

Issues carry a complexity label: `complexity: trivial` (a typo, a small fix), `complexity: medium` (a standard feature or an involved bug), `complexity: high` (a new integration, a refactor, or anything that touches how prices are computed).

If you have an idea that is not an issue yet, open one first and describe the problem. For anything that changes how the oracle decides a price, we would rather agree the behaviour in the issue than review a large pull request.

## Making a change

1. Fork the repository and branch from `main`.
2. Keep each pull request to one change, with tests. For the oracle, a behaviour change needs a test that fails without it.
3. Make the repository's checks pass locally (the guide lists the commands). CI runs the same ones.
4. Open a pull request using the template: what it changes, the related issue, and how you tested it.

## Commit messages

Write the subject in the imperative and under about 70 characters ("Hold pokes when the raw price is far from the anchor"). Use the body to say why, not what.

## Code of conduct

Everyone taking part follows the [Code of Conduct](CODE_OF_CONDUCT.md).

## Security

Do not open public issues for vulnerabilities. See [SECURITY.md](SECURITY.md).
