# dorafactory Summary (Monthly)

_Source_: [dorafactory.polkaholic.io](https://dorafactory.polkaholic.io)

*Relay Chain*: kusama
*Para ID*: 2115



| Month | Start Block | End Block | # Blocks | # Signed Extrinsics (total) | # Active Accounts (avg) | # Addresses with Balances (max) | Issues |
| ----- | ----------- | --------- | -------- | --------------------------- | ----------------------- | ------------------------------- | ------ |
| [2023-04-01 to 2023-04-18](/kusama/2115-dorafactory/2023-04-30.md) | 1,712,752 | 1,818,800 | 106,049 | 16 | 4 | 369 | -   |   
| [2023-03-01 to 2023-03-31](/kusama/2115-dorafactory/2023-03-31.md) | 1,529,417 | 1,712,751 | 183,335 | 21 | 3 | 369 | -   |   
| [2023-02-01 to 2023-02-28](/kusama/2115-dorafactory/2023-02-28.md) | 1,364,746 | 1,529,416 | 164,671 | 15 | 3 | 369 | -   |   
| [2023-01-01 to 2023-01-31](/kusama/2115-dorafactory/2023-01-31.md) | 1,183,033 | 1,364,745 | 181,713 | 14 | 3 | 369 | -   |   
| [2022-12-01 to 2022-12-31](/kusama/2115-dorafactory/2022-12-31.md) | 1,006,303 | 1,183,032 | 176,730 | 10 | 3 | 370 | -   |   
| [2022-11-01 to 2022-11-30](/kusama/2115-dorafactory/2022-11-30.md) | 831,862 | 1,006,302 | 174,441 | 18 | 4 | 370 | -   |   
| [2022-10-01 to 2022-10-31](/kusama/2115-dorafactory/2022-10-31.md) | 652,187 | 831,861 | 179,675 | 44 | 4 | 370 | -   |   
| [2022-09-01 to 2022-09-30](/kusama/2115-dorafactory/2022-09-30.md) | 481,123 | 652,186 | 171,064 | 15 | 3 | 368 | -   |   
| [2022-08-01 to 2022-08-31](/kusama/2115-dorafactory/2022-08-31.md) | 322,638 | 481,122 | 158,485 | 42 | 4 | 368 | -   |   
| [2022-07-01 to 2022-07-31](/kusama/2115-dorafactory/2022-07-31.md) | 166,140 | 322,637 | 156,498 | 50 | 4 | 367 | -   |   
| [2022-06-01 to 2022-06-30](/kusama/2115-dorafactory/2022-06-30.md) | 1,626 | 166,139 | 164,514 | 23 | 4 | 367 | -   |   
| [2022-05-31 to 2022-05-31](/kusama/2115-dorafactory/2022-05-31.md) | 1 | 1,625 | 1,625 |  | 3 | 1 | -   |   

## Tables:

* _Blocks_: `bigquery-public-data.crypto_kusama.blocks2115` (date-partitioned by `block_time`) - [Schema](/schema/balances.json)
* _Extrinsics_: `bigquery-public-data.crypto_kusama.extrinsics2115` (date-partitioned by `block_time`) - [Schema](/schema/extrinsics.json)
* _Events_: `bigquery-public-data.crypto_kusama.events2115` (date-partitioned by `block_time`) - [Schema](/schema/events.json)
* _Transfers_: `bigquery-public-data.crypto_kusama.transfers2115` (date-partitioned by `block_time`) - [Schema](/schema/transfers.json)
* _Balances_: `bigquery-public-data.crypto_kusama.balances2115` (date-partitioned by `ts`) - [Schema](/schema/balances.json)
* _Active Accounts_: `bigquery-public-data.crypto_kusama.accountsactive2115` (date-partitioned by `ts`) - [Schema](/schema/accountsactive.json)
* _Passive Accounts_: `bigquery-public-data.crypto_kusama.accountspassive2115` (date-partitioned by `ts`) - [Schema](/schema/accountspassive.json)
* _New Accounts_: `bigquery-public-data.crypto_kusama.accountsnew2115` (date-partitioned by `ts`) - [Schema](/schema/accountsnew.json)
* _Reaped Accounts_: `bigquery-public-data.crypto_kusama.accountsreaped2115` (date-partitioned by `ts`) - [Schema](/schema/accountsreaped.json)
* _Assets_: `bigquery-public-data.crypto_kusama.assets` (filter on `2115`) - [Schema](/schema/assets.json)
* _XCM Assets_: `bigquery-public-data.crypto_kusama.xcmassets` (filter on `para_id`) - [Schema](/schema/xcmassets.json)
* _XCM Transfers_: `bigquery-public-data.crypto_kusama.xcmtransfers` (filter on `origination_para_id` or `destination_para_id`, date-partitioned by `origination_ts`) - [Schema](/schema/xcmtransfers.json)
* _XCM Messages_: `bigquery-public-data.crypto_kusama.xcm` (filter on `origination_para_id` or `destination_para_id`, date-partitioned by `origination_ts`) - [Schema](/schema/xcm.json)

### # Blocks
```bash
SELECT LAST_DAY( date(block_time)) as monthDT,
  Min(date(block_time)) startBN, max(date(block_time)) endBN, 
 min(number) minBN, max(number) maxBN, 
 count(*) numBlocks, max(number)-min(number)+1-count(*) as numBlocks_missing 
FROM `bigquery-public-data.crypto_kusama.blocks2115` 
group by monthDT 
order by monthDT desc
```


Report source: [https://cdn.polkaholic.io/substrate-etl/kusama/2115.json](https://cdn.polkaholic.io/substrate-etl/kusama/2115.json) | See [Definitions](/DEFINITIONS.md) for details | [Submit Issue](https://github.com/colorfulnotion/substrate-etl/issues)
