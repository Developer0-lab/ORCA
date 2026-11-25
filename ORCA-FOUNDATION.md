# ORCA Foundation

ORCA is built on the latest upstream snapshot of [MooreSi/forex-gold](https://github.com/MooreSi/forex-gold), branch `main`.

## Import status

The upstream source is not yet imported into this repository. Run the **Sync latest upstream foundation** workflow from the Actions tab and enter `SYNC` to import the current upstream main branch.

The workflow preserves this file, `ORCA-README.md`, and itself. Upstream-owned files are replaced by the latest upstream snapshot.

## ORCA operating decisions

- Product name: ORCA Terminal.
- Broker platform: MetaTrader 5 (MT5); Exness is the intended broker.
- Initial instrument: XAUUSD only.
- Autonomy: autonomous analysis and decision-making, subject to hard operator-defined risk limits and an emergency stop.
- Development sequence: import and audit upstream; establish reproducible tests; implement ORCA-specific changes; shadow mode; demo validation; only then consider any live-trading enablement.
- Live trading stays disabled during development and validation.

## Safety rules

- Never claim profitability without independently verified evidence.
- Never use live credentials or place real-money orders during automated tests.
- Keep all existing upstream trading safety gates unless a reviewed, tested change justifies otherwise.
- Preserve the upstream AGPL-3.0 licence and comply with its source-availability requirements for modified/networked versions.
- Treat broker timeouts and unknown order outcomes as unknown; never blindly retry an order.
