# QSO-PAYMENTS

Auditable payment-intent, allocation, settlement-adapter, receipt, dispute, and distribution contracts for the QSO ecosystem.

## GitHub Pages

The project site is published from the `docs/` directory through the Pages workflow in `.github/workflows/pages.yml`.

## Safety boundary

QSO objects produce bounded, reviewable payment intents. They do not directly custody assets, sign transactions, or execute production transfers. External adapters remain disabled until separately authorized, tested, and audited.
