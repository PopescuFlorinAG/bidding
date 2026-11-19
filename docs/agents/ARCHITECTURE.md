# Architecture — bidding

<!-- graffino-agentic:begin v1 -->
> How this repo is built, generated from the code at backfill and kept current by
> whoever changes the structure. The code wins: when this page is wrong, fix it.
<!-- graffino-agentic:end -->

## Overview
Online bidding and auction system for managing lots, bids, and settlements.

```text
[ Browser / Client UI ] <---> [ Application Server / Bidding API ] <---> [ Database ]
```

## Parts
| Part | Path | Responsibility | Talks to |
|---|---|---|---|
| Frontend | to be determined | User interface for bidders and sellers | API |
| Backend | to be determined | Auction lifecycle, bid placing, price validation | Database |
| Database | to be determined | Persistent storage for users, auctions, bids, transactions | Backend |

## Data flow
1. Seller creates auction lot → API validates and schedules → Bidders place bids → API validates reserve and increments → Highest bid wins at closing.

## State and storage
| What | Where | Owner | Notes |
|---|---|---|---|
| Auction entities | Database | Backend | Users, lots, bids, transactions |

## Configuration
| Name | Where set | Used by | Notes |
|---|---|---|---|
<!-- names only, never values -->
