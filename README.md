# ORCA Terminal

Autonomous XAUUSD trading terminal for MetaTrader 5.

## Project status

This repository is the canonical development workspace. The first release is scoped to XAUUSD only and will be developed in shadow mode before any MT5 demo execution is enabled.

## Safety rules

- Live trading remains disabled throughout development and validation.
- All autonomous entries must pass the existing shared order funnel and risk controls.
- Unknown broker execution outcomes must never be treated as confirmed absence or blindly retried.
- Automated tests must use mocks/fakes and must never place, modify, or close broker orders.
- Existing order sizing, opening, and closing behaviour must not be changed without review and attended demo validation.

## Development sequence

1. Import and verify the audited `MooreSi/forex-gold` source snapshot.
2. Integrate the ORCA decision coordinator with the existing Breakout, Reversal, and Trend PA engines.
3. Add a persistent shadow-decision ledger and conflict/staleness tests.
4. Validate strategy behaviour with historical XAUUSD data and realistic costs.
5. Complete dashboard and MT5 demo qualification.

## Important

The repository is currently a clean workspace. The audited source archive and Phase 2 coordinator package are maintained separately until the full source tree is imported here. Do not treat this README-only repository as a runnable trading application.