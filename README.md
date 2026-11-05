# Mobile Currency Exchange System

Individual project for Network Issues in Mobile Systems, developed by Murat Aydın.

## Project scope

The planned mobile app supports account registration, login, simulated PLN funding,
current and historical NBP exchange rates, currency purchases and sales, wallet
balances, and transaction history. All funding and exchanges are simulated.

## Planned architecture

- Mobile client: React Native, Expo, and TypeScript
- Web service: Node.js, Express, and TypeScript
- Database: SQLite
- External exchange-rate source: National Bank of Poland (NBP) API

The mobile client communicates with the web service over Wi-Fi or cellular
networks. The service retrieves NBP rates, validates requests, and records
authoritative wallet balances and transaction outcomes in SQLite.

## Network failure handling

The client will show cached rates with their last update time when offline.
New exchanges and funding requests will be blocked while offline. If a submitted
request loses its response, the client will check its outcome after reconnecting.
Any retry will reuse the original operation ID to prevent duplicate balance changes.

## Current milestone

M1 covers analysis and design, including requirements, network failure scenarios,
architecture and data flows, UML diagrams, an ERD, and an API outline.
