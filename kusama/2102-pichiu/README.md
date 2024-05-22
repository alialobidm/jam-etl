# pichiu Summary (Monthly)

_Source_: [pichiu.polkaholic.io](https://pichiu.polkaholic.io)

*Relay Chain*: kusama
*Para ID*: 2102



| Month | Start Block | End Block | # Blocks | # Signed Extrinsics (total) | # Active Accounts (avg) | # Addresses with Balances (max) | Issues |
| ----- | ----------- | --------- | -------- | --------------------------- | ----------------------- | ------------------------------- | ------ |
| [2023-04-01 to 2023-04-18](/kusama/2102-pichiu/2023-04-30.md) | 1,507,014 | 1,570,649 | 63,636 | 49 | 2 | 1,147 | -   |   
| [2023-03-01 to 2023-03-31](/kusama/2102-pichiu/2023-03-31.md) | 1,395,989 | 1,507,013 | 111,025 | 70 | 2 | 1,146 | -   |   
| [2023-02-01 to 2023-02-28](/kusama/2102-pichiu/2023-02-28.md) | 1,295,607 | 1,395,988 | 100,382 | 34 | 2 | 1,145 | -   |   
| [2023-01-01 to 2023-01-31](/kusama/2102-pichiu/2023-01-31.md) | 1,165,361 | 1,295,606 | 130,246 | 90 | 3 | 1,143 | -   |   
| [2022-12-01 to 2022-12-31](/kusama/2102-pichiu/2022-12-31.md) | 956,906 | 1,165,360 | 208,455 | 58 | 4 | 1,119 | -   |   
| [2022-11-01 to 2022-11-30](/kusama/2102-pichiu/2022-11-30.md) | 747,379 | 956,905 | 209,527 | 75 | 4 | 1,118 | -   |   
| [2022-10-01 to 2022-10-31](/kusama/2102-pichiu/2022-10-31.md) | 531,527 | 747,378 | 215,852 | 146 | 5 | 1,104 | -   |   
| [2022-09-01 to 2022-09-30](/kusama/2102-pichiu/2022-09-30.md) | 334,461 | 531,526 | 197,066 | 57 | 3 | 655 | -   |   
| [2022-08-01 to 2022-08-31](/kusama/2102-pichiu/2022-08-31.md) | 154,154 | 334,460 | 180,307 | 113 | 3 | 651 | -   |   
| [2022-07-01 to 2022-07-31](/kusama/2102-pichiu/2022-07-31.md) | 34,486 | 154,153 | 119,668 | 16 | 1 | 5 | -   |   
| [2022-06-21 to 2022-06-30](/kusama/2102-pichiu/2022-06-30.md) | 1 | 34,485 | 34,485 | 7 | 1 | 3 | -   |   

## Tables:

* _Blocks_: `bigquery-public-data.crypto_kusama.blocks2102` (date-partitioned by `block_time`) - [Schema](/schema/balances.json)
* _Extrinsics_: `bigquery-public-data.crypto_kusama.extrinsics2102` (date-partitioned by `block_time`) - [Schema](/schema/extrinsics.json)
* _Events_: `bigquery-public-data.crypto_kusama.events2102` (date-partitioned by `block_time`) - [Schema](/schema/events.json)
* _Transfers_: `bigquery-public-data.crypto_kusama.transfers2102` (date-partitioned by `block_time`) - [Schema](/schema/transfers.json)
* _Balances_: `bigquery-public-data.crypto_kusama.balances2102` (date-partitioned by `ts`) - [Schema](/schema/balances.json)
* _Active Accounts_: `bigquery-public-data.crypto_kusama.accountsactive2102` (date-partitioned by `ts`) - [Schema](/schema/accountsactive.json)
* _Passive Accounts_: `bigquery-public-data.crypto_kusama.accountspassive2102` (date-partitioned by `ts`) - [Schema](/schema/accountspassive.json)
* _New Accounts_: `bigquery-public-data.crypto_kusama.accountsnew2102` (date-partitioned by `ts`) - [Schema](/schema/accountsnew.json)
* _Reaped Accounts_: `bigquery-public-data.crypto_kusama.accountsreaped2102` (date-partitioned by `ts`) - [Schema](/schema/accountsreaped.json)
* _Assets_: `bigquery-public-data.crypto_kusama.assets` (filter on `2102`) - [Schema](/schema/assets.json)
* _XCM Assets_: `bigquery-public-data.crypto_kusama.xcmassets` (filter on `para_id`) - [Schema](/schema/xcmassets.json)
* _XCM Transfers_: `bigquery-public-data.crypto_kusama.xcmtransfers` (filter on `origination_para_id` or `destination_para_id`, date-partitioned by `origination_ts`) - [Schema](/schema/xcmtransfers.json)
* _XCM Messages_: `bigquery-public-data.crypto_kusama.xcm` (filter on `origination_para_id` or `destination_para_id`, date-partitioned by `origination_ts`) - [Schema](/schema/xcm.json)

### # Blocks
```bash
SELECT LAST_DAY( date(block_time)) as monthDT,
  Min(date(block_time)) startBN, max(date(block_time)) endBN, 
 min(number) minBN, max(number) maxBN, 
 count(*) numBlocks, max(number)-min(number)+1-count(*) as numBlocks_missing 
FROM `bigquery-public-data.crypto_kusama.blocks2102` 
group by monthDT 
order by monthDT desc
```


Report source: [https://cdn.polkaholic.io/substrate-etl/kusama/2102.json](https://cdn.polkaholic.io/substrate-etl/kusama/2102.json) | See [Definitions](/DEFINITIONS.md) for details | [Submit Issue](https://github.com/colorfulnotion/substrate-etl/issues)
