# ORCA Terminal

Autonomous XAUUSD trading terminal for MetaTrader 5.

## Project status

The ORCA repository now contains the upstream `MooreSi/forex-gold` application source, imported from its `main` branch on 25 November 2026. The import commit is recorded in Git history. ORCA-specific trading changes and qualification are still in development; this repository is not yet an ORCA-validated release.

The first ORCA release is scoped to XAUUSD and will be developed in shadow mode before any MT5 demo execution is enabled.

## Safety rules

- Live trading remains disabled throughout development and validation.
- All autonomous entries must pass the existing shared order funnel and risk controls.
- Unknown broker execution outcomes must never be treated as confirmed absence or blindly retried.
- Automated tests must use mocks/fakes and must never place, modify, or close broker orders.
- Existing order sizing, opening, and closing behaviour must not be changed without review and attended demo validation.

## Development sequence

1. Audit the imported upstream application and establish reproducible test results.
2. Integrate the ORCA decision coordinator with the existing Breakout, Reversal, and Trend PA engines.
3. Add a persistent shadow-decision ledger and conflict/staleness tests.
4. Validate strategy behaviour with historical XAUUSD data and realistic costs.
5. Complete the ORCA dashboard and MT5 demo qualification.

## Important

The upstream application is the foundation, not the finished ORCA product. Do not treat a successful source import as proof that ORCA's autonomous decision system, broker connection, or trading behaviour has been validated.
