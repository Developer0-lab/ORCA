# ORCA Foundation

ORCA is built on the upstream [MooreSi/forex-gold](https://github.com/MooreSi/forex-gold) application, branch `main`.

## Import status

The upstream source has been imported into this repository. GitHub Actions run [45579047319](https://github.com/Developer0-lab/ORCA/actions/runs/45579047319) completed successfully on 25 November 2026. The resulting import commit is [24eedd343b29e5f8528be28d8ba8438381aaf2f3](https://github.com/Developer0-lab/ORCA/commit/24eedd343b29e5f8528be28d8ba8438381aaf2f3).

The sync workflow preserves ORCA's README, this foundation document, and ORCA's workflow files while replacing upstream-owned files from the latest upstream `main` snapshot.

## ORCA operating decisions

- Product name: ORCA Terminal.
- Broker platform: MetaTrader 5 (MT5); Exness is the intended broker.
- Initial instrument: XAUUSD only.
- Autonomy: autonomous analysis and decision-making, subject to hard operator-defined risk limits and an emergency stop.
- Development sequence: audit imported source; establish reproducible tests; implement ORCA-specific changes; shadow mode; attended demo validation; only then consider any live-trading enablement.
- Live trading stays disabled during development and validation.

## Safety rules

- Never claim profitability without independently verified evidence.
- Never use live credentials or place real-money orders during automated tests.
- Keep all existing upstream trading safety gates unless a reviewed, tested change justifies otherwise.
- Preserve the upstream AGPL-3.0 licence and comply with its source-availability requirements for modified/networked versions.
- Treat broker timeouts and unknown order outcomes as unknown; never blindly retry an order.
- Do not modify order placement, closing, or sizing paths without the required owner review and attended demo validation.
