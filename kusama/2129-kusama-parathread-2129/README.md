# kusama-parathread-2129 Summary (Monthly)

_Source_: [kusama-parathread-2129.polkaholic.io](https://kusama-parathread-2129.polkaholic.io)

*Relay Chain*: kusama
*Para ID*: 2129



| Month | Start Block | End Block | # Blocks | # Signed Extrinsics (total) | # Active Accounts (avg) | # Addresses with Balances (max) | Issues |
| ----- | ----------- | --------- | -------- | --------------------------- | ----------------------- | ------------------------------- | ------ |
| [2023-05-01 to 2023-05-02](/kusama/2129-kusama-parathread-2129/2023-05-31.md) | 1,503,355 | 1,514,494 | 11,140 | 7 |  | 5,975 | -   |   
| [2023-04-01 to 2023-04-30](/kusama/2129-kusama-parathread-2129/2023-04-30.md) | 1,295,241 | 1,503,354 | 208,114 | 134 |  | 5,975 | -   |   
| [2023-03-01 to 2023-03-31](/kusama/2129-kusama-parathread-2129/2023-03-31.md) | 1,078,183 | 1,295,240 | 215,354 | 729 |  | 5,824 | - 1,704 (0.79%) |   
| [2023-02-08 to 2023-02-28](/kusama/2129-kusama-parathread-2129/2023-02-28.md) | 937,108 | 1,078,182 | 141,075 | 392 | 13 | 5,781 | -   |   
| [2023-01-01 to 2023-01-30](/kusama/2129-kusama-parathread-2129/2023-01-31.md) | 666,173 | 872,871 | 191,618 | 339 | 9 | 5,580 | -  **BROKEN** (7.30%) |   
| [2022-12-01 to 2022-12-13](/kusama/2129-kusama-parathread-2129/2022-12-31.md) | 456,754 | 539,967 | 83,214 | 274 | 15 | 5,831 | -  **BROKEN**  |   
| [2022-11-01 to 2022-11-30](/kusama/2129-kusama-parathread-2129/2022-11-30.md) | 254,577 | 456,753 | 125,549 | 2,039 | 53 | 5,831 | - 76,628 (37.90%) |   
| [2022-10-26 to 2022-10-31](/kusama/2129-kusama-parathread-2129/2022-10-31.md) | 218,593 | 254,576 | 35,767 | 5,804 | 709 | 5,831 | - 217 (0.60%) |   

## Tables:

* _Blocks_: `bigquery-public-data.crypto_kusama.blocks2129` (date-partitioned by `block_time`) - [Schema](/schema/balances.json)
* _Extrinsics_: `bigquery-public-data.crypto_kusama.extrinsics2129` (date-partitioned by `block_time`) - [Schema](/schema/extrinsics.json)
* _Events_: `bigquery-public-data.crypto_kusama.events2129` (date-partitioned by `block_time`) - [Schema](/schema/events.json)
* _Transfers_: `bigquery-public-data.crypto_kusama.transfers2129` (date-partitioned by `block_time`) - [Schema](/schema/transfers.json)
* _Balances_: `bigquery-public-data.crypto_kusama.balances2129` (date-partitioned by `ts`) - [Schema](/schema/balances.json)
* _Active Accounts_: `bigquery-public-data.crypto_kusama.accountsactive2129` (date-partitioned by `ts`) - [Schema](/schema/accountsactive.json)
* _Passive Accounts_: `bigquery-public-data.crypto_kusama.accountspassive2129` (date-partitioned by `ts`) - [Schema](/schema/accountspassive.json)
* _New Accounts_: `bigquery-public-data.crypto_kusama.accountsnew2129` (date-partitioned by `ts`) - [Schema](/schema/accountsnew.json)
* _Reaped Accounts_: `bigquery-public-data.crypto_kusama.accountsreaped2129` (date-partitioned by `ts`) - [Schema](/schema/accountsreaped.json)
* _Assets_: `bigquery-public-data.crypto_kusama.assets` (filter on `2129`) - [Schema](/schema/assets.json)
* _XCM Assets_: `bigquery-public-data.crypto_kusama.xcmassets` (filter on `para_id`) - [Schema](/schema/xcmassets.json)
* _XCM Transfers_: `bigquery-public-data.crypto_kusama.xcmtransfers` (filter on `origination_para_id` or `destination_para_id`, date-partitioned by `origination_ts`) - [Schema](/schema/xcmtransfers.json)
* _XCM Messages_: `bigquery-public-data.crypto_kusama.xcm` (filter on `origination_para_id` or `destination_para_id`, date-partitioned by `origination_ts`) - [Schema](/schema/xcm.json)

### # Blocks
```bash
SELECT LAST_DAY( date(block_time)) as monthDT,
  Min(date(block_time)) startBN, max(date(block_time)) endBN, 
 min(number) minBN, max(number) maxBN, 
 count(*) numBlocks, max(number)-min(number)+1-count(*) as numBlocks_missing 
FROM `bigquery-public-data.crypto_kusama.blocks2129` 
group by monthDT 
order by monthDT desc
```


Report source: [https://cdn.polkaholic.io/substrate-etl/kusama/2129.json](https://cdn.polkaholic.io/substrate-etl/kusama/2129.json) | See [Definitions](/DEFINITIONS.md) for details | [Submit Issue](https://github.com/colorfulnotion/substrate-etl/issues)
