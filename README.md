# Streamlining IT Procurement: Automating Standard Laptop Orders with Flow Designer

## Problem Statement
The current IT procurement process lacks efficiency and automation, causing delays and manual
overhead, particularly for standard laptop orders.

## Solution
A ServiceNow Flow Designer flow that automates standard laptop requests end to end:

1. Employee submits the "Standard Laptop" catalog item.
2. Flow checks the request against standard-model rules (approved models list).
3. Standard requests are auto-approved; non-standard ones route to the manager / IT approver.
4. Flow creates the procurement/fulfilment catalog task and assigns it to the Procurement group.
5. Requester receives notifications on approval, ordering and delivery.

## Structure
| Path | Purpose |
|------|---------|
| `src/flows/` | Flow Designer flow definition (JSON spec) |
| `src/catalog/` | Catalog item and variable definitions |
| `src/business_rules/` | Server-side scripts |
| `src/notifications/` | Email notification templates |
| `config/` | Environment and instance settings |
| `docs/` | Design notes and setup guide |
| `tests/` | Test scenarios and validation script |

## Setup
1. `npm install`
2. Copy `config/instance.example.json` to `config/instance.json` and fill in your instance details.
3. Recreate the flow in Flow Designer using `src/flows/standard_laptop_order.flow.json` and
   `docs/setup-guide.md`, or import via an update set.
4. `npm test` to validate the configuration files.

> Note: generated from the document title and problem statement only. Adjust to match your full design.
