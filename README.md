# Test-Api

## Requirements

Create an API specification and build a simple RESTFUL API for a stock trading platform with the following requirements, no database setup is required - use a singleton for any storage needs spanning multiple requests.
* Get *companies*
  * Predefined companies with the following symbols - `AMZN`, `TSLA` and `BLKFNCH`.
* Companies can issue *shares*, a quantity of shares are issued at a set price - starting shares for each company are 100,000 @ £40 for `AMZN`, 10,000 @ £200 for `TSLA` and 600 @ £60 for `BLKFNCH`.
* Create *orders*
  * An order consists of a `symbol`, `min` order price, `max` order price, `quantity`, and `type` (`buy` or `sell`).
* Get outstanding orders - an order has a `status` of `processing` or `processed`.
* Get status of a specific order
* If an order is created that can't be satisfied, it remains in a backlog queue until it is able to be addressed by an incoming order.

Set starting orders for each company as 
```
[
  { "symbol":"AMZN", "min":40, "max":40, "quantity":100, "type":"buy" },
  { "symbol":"TSLA", "min":200, "max":200, "quantity":2000, "type":"buy" },
  { "symbol":"BLKFNCH", "min":60, "max":60, "quantity":30, "type":"buy" }
]
```

## Outcomes
* API specification document
* dotnet core project
* simple unit tests
