# Monero tx_extra statistics
Author: Neptune Research & Isthmus (Noncesense Research Lab, noncesense.org)  
Date: September 23 2020

As of mainnet block 2180399


# Tag usage
## Tags used together in same transaction (COINBASE)

```
SELECT
	COUNT(1) AS n_tx,
	n_padding,
	n_pubkey,
	n_extra_nonce,
	n_payment_id,
	n_payment_id8,
	n_merge_mining,
	n_pubkey_additional,
	n_mysterious_minergate
FROM tx_extra_tag_count C
WHERE C.tx_hash IS NULL
GROUP BY
	n_padding,
	n_pubkey,
	n_extra_nonce,
	n_payment_id,
	n_payment_id8,
	n_merge_mining,
	n_pubkey_additional,
	n_mysterious_minergate
ORDER BY n_tx DESC
```

| "n_tx"  | "n_padding" | "n_pubkey" | "n_extra_nonce" | "n_payment_id" | "n_payment_id8" | "n_merge_mining" | "n_pubkey_additional" | "n_mysterious_minergate" | 
|---------|-------------|------------|-----------------|----------------|-----------------|------------------|-----------------------|--------------------------| 
| 1115971 | 0           | 1          | 1               | 0              | 0               | 0                | 0                     | 0                        | 
| 84480   | 0           | 1          | 1               | 0              | 0               | 1                | 0                     | 0                        | 
| 17280   | 1           | 1          | 1               | 0              | 0               | 0                | 0                     | 0                        | 
| 10277   | 0           | 1          | 0               | 0              | 0               | 0                | 0                     | 0                        | 
| 5305    | 1           | 1          | 0               | 0              | 0               | 0                | 0                     | 0                        | 
| 2896    | 1           | 1          | 1               | 0              | 0               | 1                | 0                     | 0                        | 


## Tags used together used in same transaction (USER)

```
SELECT
	COUNT(1) AS n_tx,
	n_padding,
	n_pubkey,
	n_extra_nonce,
	n_payment_id,
	n_payment_id8,
	n_merge_mining,
	n_pubkey_additional,
	n_mysterious_minergate
FROM tx_extra_tag_count C
WHERE C.tx_hash IS NOT NULL
GROUP BY
	n_padding,
	n_pubkey,
	n_extra_nonce,
	n_payment_id,
	n_payment_id8,
	n_merge_mining,
	n_pubkey_additional,
	n_mysterious_minergate
ORDER BY n_tx DESC
```

| "n_tx"      | "n_padding" | "n_pubkey" | "n_extra_nonce" | "n_payment_id" | "n_payment_id8" | "n_merge_mining" | "n_pubkey_additional" | "n_mysterious_minergate" | 
|-------------|-------------|------------|-----------------|----------------|-----------------|------------------|-----------------------|--------------------------| 
|     5004288 | 0           | 1          | 0               | 0              | 1               | 0                | 0                     | 0                        | 
|     1756871 | 0           | 1          | 0               | 0              | 0               | 0                | 0                     | 0                        | 
|     1631841 | 0           | 1          | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     95445   | 0           | 1          | 0               | 0              | 0               | 0                | 0                     | 1                        | 
|     52095   | 0           | 1          | 0               | 1              | 0               | 0                | 0                     | 1                        | 
|     38081   | 0           | 1          | 0               | 0              | 0               | 0                | 16                    | 0                        | 
|     30484   | 0           | 1          | 0               | 0              | 0               | 0                | 3                     | 0                        | 
|     21178   | 0           | 1          | 0               | 0              | 0               | 0                | 11                    | 0                        | 
|     15471   | 0           | 1          | 0               | 0              | 0               | 0                | 4                     | 0                        | 
|     7222    | 0           | 1          | 0               | 0              | 0               | 0                | 6                     | 0                        | 
|     6386    | 0           | 1          | 0               | 0              | 0               | 0                | 5                     | 0                        | 
|     4725    | 0           | 1          | 0               | 0              | 0               | 0                | 7                     | 0                        | 
|     4296    | 0           | 1          | 0               | 0              | 0               | 0                | 8                     | 0                        | 
|     4049    | 0           | 1          | 0               | 0              | 0               | 0                | 9                     | 0                        | 
|     3834    | 0           | 1          | 0               | 0              | 0               | 0                | 10                    | 0                        | 
|     2084    | 0           | 1          | 0               | 0              | 0               | 0                | 12                    | 0                        | 
|     1898    | 0           | 1          | 0               | 0              | 0               | 0                | 13                    | 0                        | 
|     1773    | 0           | 1          | 0               | 0              | 0               | 0                | 14                    | 0                        | 
|     1717    | 0           | 1          | 0               | 0              | 0               | 0                | 15                    | 0                        | 
|     711     | 0           | 1          | 0               | 0              | 0               | 0                | 1                     | 0                        | 
|     705     | 0           | 1          | 0               | 0              | 1               | 0                | 1                     | 0                        | 
|     638     | 0           | 1          | 0               | 0              | 1               | 0                | 0                     | 1                        | 
|     445     | 0           | 1          | 0               | 1              | 0               | 0                | 1                     | 0                        | 
|     401     | 0           | 1          | 0               | 0              | 0               | 0                | 26                    | 0                        | 
|     325     | 0           | 2          | 0               | 0              | 1               | 0                | 0                     | 0                        | 
|     308     | 0           | 1          | 0               | 0              | 0               | 0                | 21                    | 0                        | 
|     295     | 0           | 15         | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     288     | 0           | 1          | 1               | 0              | 0               | 0                | 0                     | 0                        | 
|     187     | 0           | 1          | 0               | 0              | 0               | 0                | 2                     | 0                        | 
|     164     | 0           | 225        | 0               | 0              | 1               | 0                | 0                     | 0                        | 
|     164     | 0           | 2          | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     153     | 0           | 1          | 0               | 0              | 0               | 0                | 19                    | 0                        | 
|     131     | 0           | 1          | 0               | 0              | 0               | 0                | 20                    | 0                        | 
|     126     | 0           | 1          | 0               | 0              | 0               | 0                | 18                    | 0                        | 
|     117     | 0           | 1          | 0               | 0              | 0               | 0                | 17                    | 0                        | 
|     98      | 0           | 1          | 0               | 0              | 0               | 0                | 22                    | 0                        | 
|     92      | 0           | 1          | 0               | 0              | 0               | 0                | 24                    | 0                        | 
|     87      | 0           | 1          | 0               | 0              | 0               | 0                | 23                    | 0                        | 
|     83      | 0           | 30         | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     77      | 0           | 10         | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     72      | 0           | 1          | 0               | 0              | 0               | 0                | 25                    | 0                        | 
|     69      | 0           | 50         | 0               | 0              | 1               | 0                | 0                     | 0                        | 
|     58      | 0           | 25         | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     52      | 0           | 1          | 0               | 0              | 0               | 0                | 32                    | 0                        | 
|     35      | 0           | 1          | 0               | 0              | 0               | 0                | 27                    | 0                        | 
|     32      | 0           | 20         | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     27      | 0           | 2          | 0               | 0              | 0               | 0                | 0                     | 0                        | 
|     18      | 0           | 5000       | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     17      | 0           | 1          | 0               | 0              | 0               | 0                | 31                    | 0                        | 
|     16      | 0           | 5000       | 0               | 0              | 1               | 0                | 0                     | 0                        | 
|     15      | 0           | 50         | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     15      | 0           | 1          | 1               | 1              | 0               | 0                | 0                     | 0                        | 
|     14      | 0           | 1          | 0               | 0              | 1               | 0                | 2                     | 0                        | 
|     11      | 0           | 1          | 0               | 0              | 0               | 0                | 28                    | 0                        | 
|     9       | 0           | 1          | 0               | 0              | 0               | 0                | 30                    | 0                        | 
|     9       | 0           | 1          | 0               | 0              | 2               | 0                | 0                     | 0                        | 
|     7       | 0           | 50         | 0               | 0              | 0               | 0                | 0                     | 0                        | 
|     7       | 0           | 100        | 0               | 0              | 1               | 0                | 0                     | 0                        | 
|     6       | 0           | 1          | 0               | 1              | 0               | 0                | 3                     | 0                        | 
|     5       | 0           | 1          | 0               | 0              | 0               | 0                | 29                    | 0                        | 
|     5       | 0           | 1          | 0               | 1              | 0               | 0                | 5                     | 0                        | 
|     5       | 0           | 100        | 0               | 0              | 0               | 0                | 0                     | 0                        | 
|     5       | 0           | 225        | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     5       | 0           | 1001       | 0               | 0              | 1               | 0                | 0                     | 0                        | 
|     4       | 0           | 2          | 0               | 0              | 0               | 0                | 2                     | 0                        | 
|     4       | 0           | 10         | 0               | 0              | 1               | 0                | 0                     | 0                        | 
|     4       | 0           | 4001       | 0               | 0              | 1               | 0                | 0                     | 0                        | 
|     4       | 0           | 1001       | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     3       | 0           | 4001       | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     3       | 0           | 1          | 0               | 1              | 0               | 0                | 4                     | 0                        | 
|     3       | 0           | 15         | 0               | 0              | 0               | 0                | 0                     | 0                        | 
|     2       | 0           | 1          | 0               | 1              | 0               | 0                | 11                    | 0                        | 
|     2       | 0           | 2          | 0               | 1              | 0               | 0                | 2                     | 0                        | 
|     2       | 0           | 1          | 0               | 1              | 0               | 0                | 15                    | 0                        | 
|     2       | 0           | 3          | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     2       | 0           | 405        | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     2       | 0           | 11         | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     2       | 0           | 25         | 0               | 0              | 0               | 0                | 0                     | 0                        | 
|     2       | 0           | 2          | 0               | 0              | 1               | 0                | 2                     | 0                        | 
|     1       | 0           | 1          | 0               | 1              | 0               | 0                | 6                     | 0                        | 
|     1       | 0           | 405        | 0               | 0              | 1               | 0                | 0                     | 0                        | 
|     1       | 0           | 1000       | 0               | 0              | 1               | 0                | 0                     | 0                        | 
|     1       | 0           | 1001       | 0               | 0              | 0               | 0                | 0                     | 0                        | 
|     1       | 0           | 1          | 0               | 1000           | 0               | 0                | 0                     | 0                        | 
|     1       | 0           | 5          | 0               | 0              | 1               | 0                | 0                     | 0                        | 
|     1       | 0           | 6          | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     1       | 0           | 10         | 0               | 0              | 0               | 0                | 0                     | 0                        | 
|     1       | 0           | 1          | 0               | 100            | 0               | 0                | 0                     | 0                        | 
|     1       | 0           | 1          | 0               | 4              | 0               | 0                | 0                     | 0                        | 
|     1       | 0           | 20         | 0               | 0              | 0               | 0                | 0                     | 0                        | 
|     1       | 0           | 1          | 0               | 3              | 0               | 0                | 0                     | 0                        | 
|     1       | 0           | 1          | 0               | 2              | 0               | 0                | 0                     | 0                        | 
|     1       | 0           | 1          | 0               | 1              | 0               | 0                | 16                    | 0                        | 
|     1       | 0           | 1          | 0               | 1              | 0               | 0                | 14                    | 0                        | 
|     1       | 0           | 1          | 0               | 1              | 0               | 0                | 13                    | 0                        | 
|     1       | 0           | 5000       | 0               | 0              | 0               | 0                | 0                     | 0                        | 
|     1       | 0           | 100        | 0               | 1              | 0               | 0                | 0                     | 0                        | 
|     1       | 0           | 1          | 0               | 1              | 0               | 0                | 9                     | 0                        | 

## Tags not known to Monero Core software
There are NO unknown tags on the mainnet as of 2180399

    -- No results
    SELECT *
    FROM tx_extra_tag
    WHERE tx_extra_tag_id > 8




# Tag statistics: Public key
## Histogram
```
SELECT
	COUNT(1) AS n,
	n_pubkey
FROM tx_extra_tag_count C
GROUP BY n_pubkey
ORDER BY n DESC
```

| "n"         | "n_pubkey" | 
|-------------|------------| 
|     9924701 | 1          | 
|     524     | 2          | 
|     298     | 15         | 
|     169     | 225        | 
|     91      | 50         | 
|     83      | 30         | 
|     82      | 10         | 
|     60      | 25         | 
|     35      | 5000       | 
|     33      | 20         | 
|     13      | 100        | 
|     10      | 1001       | 
|     7       | 4001       | 
|     3       | 405        | 
|     2       | 11         | 
|     2       | 3          | 
|     1       | 1000       | 
|     1       | 5          | 
|     1       | 6          | 

Note there is no n_pubkey = 0 column: EVERY coinbase and user transaction has a public key.


# Tag statistics: Public Key Additional (Subaddress key)
Note: number of keys in tag data matches number of outputs in transaction

## Histogram
```
SELECT
	COUNT(1) AS n,
	n_pubkey_additional
FROM tx_extra_tag_count C
GROUP BY n_pubkey_additional
ORDER BY n DESC
```

| "n"     | "n_pubkey_additional" | 
|---------|-----------------------| 
| 9779111 | 0                     | 
| 38082   | 16                    | 
| 30490   | 3                     | 
| 21180   | 11                    | 
| 15474   | 4                     | 
| 7223    | 6                     | 
| 6391    | 5                     | 
| 4725    | 7                     | 
| 4296    | 8                     | 
| 4050    | 9                     | 
| 3834    | 10                    | 
| 2084    | 12                    | 
| 1899    | 13                    | 
| 1861    | 1                     | 
| 1774    | 14                    | 
| 1719    | 15                    | 
| 401     | 26                    | 
| 308     | 21                    | 
| 209     | 2                     | 
| 153     | 19                    | 
| 131     | 20                    | 
| 126     | 18                    | 
| 117     | 17                    | 
| 98      | 22                    | 
| 92      | 24                    | 
| 87      | 23                    | 
| 72      | 25                    | 
| 52      | 32                    | 
| 35      | 27                    | 
| 17      | 31                    | 
| 11      | 28                    | 
| 9       | 30                    | 
| 5       | 29                    | 

## Usage per version
```
SELECT
	V0."height",
	V0.version" AS "version_from",
	V."height",
	V."version" AS "version_to",
	SUM(n_pubkey_additional)
FROM monero_version V
JOIN monero_version V0 ON V0."version" = V."version" - 1
JOIN tx_extra_tag_count C ON C.block_height >= V0."height" AND C.block_height < V."height"
WHERE n_pubkey_additional > 0
GROUP BY V0."height", V0."version", V."height", V."version"
```

| "height" | "version_from" | "height" | "version_to" | "sum"  | 
|----------|-----------|----------|-----------|--------| 
| 1400000  | 6         | 1546000  | 7         | 1872   | 
| 1546000  | 7         | 1685555  | 8         | 57106  | 
| 1685555  | 8         | 1686275  | 9         | 488    | 
| 1686275  | 9         | 1788000  | 10        | 116379 | 
| 1788000  | 10        | 1788720  | 11        | 3937   | 
| 1788720  | 11        | 1978433  | 12        | 597089 | 
| 1978433  | 12        | 2180399  | 13        | 577610 | 

Questions:

1. Have more than 16 additional pubkeys ever been given on a transaction, after v9 which started consensus for max 16 outputs per transaction?
    Answer: No

    ```
    -- No results
    SELECT
        COUNT(1)
    FROM tx_extra_tag_count C
    WHERE n_pubkey_additional > 16
        AND block_height >= 1686275 -- v9
    ```

2. Have more additional pubkeys than number of outputs ever been given on a transaction?
    Answer: No

    ```
    SELECT
        COUNT(1)
    FROM tx_extra_tag_count C
    JOIN tx_io I ON I.tx_hash = C.tx_hash
    WHERE C.n_pubkey_additional > I.n_output
    ```

3. Interesting pattern: there is a transaction source which writes an additional public key tag with no data.

    Sub-field tag = ```0400```
    - Tag = `04` = Pubkey additional
    - Size = `0`

    ```
    -- 1860 transactions
    SELECT
        COUNT(1)
    FROM tx_extra_data
    WHERE
        tx_extra_tag_id = 7 -- pubkey_additional
        AND "data" IS NULL
    ```

# Tag statistics: Padding
## Histogram
```
SELECT
	COUNT(1) AS n,
	n_padding
FROM tx_extra_tag_count C
GROUP BY n_padding
ORDER BY n DESC
```

| "n"     | "n_padding" | 
|---------|-------------| 
| 9900635 | 0           | 
| 25481   | 1           | 

## Usage per version
```
SELECT
	V0."height",
	V0.version" AS "version_from",
	V."height",
	V."version" AS "version_to",
	SUM(n_padding)
FROM monero_version V
JOIN monero_version V0 ON V0."version" = V."version" - 1
JOIN tx_extra_tag_count C ON C.block_height >= V0."height" AND C.block_height < V."height"
GROUP BY V0."height", V0."version", V."height", V."version"
```

| "height" | "version_from" | "height" | "version_to" | "sum" | 
|----------|-----------|----------|-----------|-------| 
| 0        | 1         | 1009827  | 2         | 23988 | 
| 1009827  | 2         | 1141317  | 3         | 763   | 
| 1141317  | 3         | 1220516  | 4         | 727   | 
| 1220516  | 4         | 1288616  | 5         | 0     | 
| 1288616  | 5         | 1400000  | 6         | 0     | 
| 1400000  | 6         | 1546000  | 7         | 0     | 
| 1546000  | 7         | 1685555  | 8         | 1     | 
| 1685555  | 8         | 1686275  | 9         | 0     | 
| 1686275  | 9         | 1788000  | 10        | 0     | 
| 1788000  | 10        | 1788720  | 11        | 0     | 
| 1788720  | 11        | 1978433  | 12        | 0     | 
| 1978433  | 12        | 2180399  | 13        | 2     | 


# Tag statistics: Extra nonce
## Histogram
```
SELECT
	COUNT(1) AS n,
	n_extra_nonce
FROM tx_extra_tag_count C
GROUP BY n_extra_nonce
ORDER BY n DESC
```

| "n"     | "n_extra_nonce" | 
|---------|-----------------| 
| 8705186 | 0               | 
| 1220930 | 1               | 

## Usage per version
```
SELECT
	V0."height",
	V0.version" AS "version_from",
	V."height",
	V."version" AS "version_to",
	SUM(n_extra_nonce)
FROM monero_version V
JOIN monero_version V0 ON V0."version" = V."version" - 1
JOIN tx_extra_tag_count C ON C.block_height >= V0."height" AND C.block_height < V."height"
GROUP BY V0."height", V0."version", V."height", V."version"
```

| "height" | "version_from" | "height" | "version_to" | "sum"  | 
|----------|-----------|----------|-----------|--------| 
| 0        | 1         | 1009827  | 2         | 278205 | 
| 1009827  | 2         | 1141317  | 3         | 54178  | 
| 1141317  | 3         | 1220516  | 4         | 54085  | 
| 1220516  | 4         | 1288616  | 5         | 62509  | 
| 1288616  | 5         | 1400000  | 6         | 92649  | 
| 1400000  | 6         | 1546000  | 7         | 125803 | 
| 1546000  | 7         | 1685555  | 8         | 118414 | 
| 1685555  | 8         | 1686275  | 9         | 562    | 
| 1686275  | 9         | 1788000  | 10        | 80773  | 
| 1788000  | 10        | 1788720  | 11        | 566    | 
| 1788720  | 11        | 1978433  | 12        | 164128 | 
| 1978433  | 12        | 2180399  | 13        | 189057 | 


## Usage per transaction type
```
SELECT
	CASE WHEN tx_hash IS NULL THEN 1 ELSE 0 END AS is_coinbase,
	COUNT(1) AS n
FROM tx_extra_tag_count C
WHERE n_extra_nonce > 0
GROUP BY is_coinbase 
```

|is_coinbase|n|
|-----------|-|
|0|303|
|1|1220627|


## Interesting cases of extra nonce in user transactions
1. How many extra nonces in user transactions?
    Answer: 303 transactions

    ```
    SELECT
        COUNT(1)
    FROM tx_extra_data
    WHERE tx_extra_tag_id = 3 -- extra nonce
        AND tx_hash IS NOT NULL
    ```

2. Of these, 260 cases with the following attributes:
    extra nonce
    + user transaction
    + size 9
    + first byte 0

    These appear to be misimplemented encrypted PIDs

    See difference:
        encrypted PID tag:  020901
        this tag:           020900

    ```
    -- 260 results
    SELECT
        *
    FROM tx_extra_data
    WHERE tx_extra_tag_id = 3 -- extra nonce
        AND "size" = 9  -- size 9
        AND SUBSTRING("data" FROM 1 FOR 1) = '\x00' -- first byte 0
        AND tx_hash IS NOT NULL     -- user transaction
    ```


# Tag statistics: Payment Ids (Unencrypted and Encrypted)
## Payment id usage x transaction I/O, since v12
Question from UkoeHB_: the core wallet only creates encrypted payment IDs for all 2-output tx, would you mind looking into the distinction (proportion encrypted IDs with 2-output and >2 output)?

```
SELECT
	COUNT(1) FILTER (WHERE I.n_output = 2) AS n_2_out,
    COUNT(1) FILTER (WHERE I.n_output <> 2) AS n_not_2_out,
    C.n_payment_id,
    C.n_payment_id8
FROM tx_extra_tag_count C
JOIN tx_io I ON I.tx_hash = C.tx_hash
WHERE C.block_height >= 1978433
GROUP BY C.n_payment_id, C.n_payment_id8
```

| PID Type | n_2_out | n_not_2_out | Comment |
| - | - | - | - |
| None | 8500 | 138590 | `n_2_out = 8500 2out tx` => these tx were therefore not generated by Core Wallet v15+. |
| Encrypted | 2747129 | 111 | - |
| Unencrypted | 701 | 0 | (1) `n_2_out = 701 2out tx` => these tx were therefore not generated by Core Wallet v15+. (2) `n_not_2_out = 0 not2out tx` => uPID was never used on a non-2-out tx since v12! |

## More than one payment ID used in same transaction
```
-- Only 1118 transactions ever
SELECT
	COUNT(1)
FROM tx_extra_tag_count C
WHERE C.n_payment_id > 1 OR C.n_payment_id8 > 1
```

# Tag statistics: Payment ID, Unencrypted
## Histogram
```
SELECT
	COUNT(1) AS n,
	n_payment_id
FROM tx_extra_tag_count C
GROUP BY n_payment_id
ORDER BY n DESC
```

| "n"     | "n_payment_id" | 
|---------|----------------| 
| 8240928 | 0              | 
| 1685183 | 1              | 
| 1       | 2              | 
| 1       | 3              | 
| 1       | 4              | 
| 1       | 100            | 
| 1       | 1000           | 

## Usage per version
```
SELECT
	V0."height",
	V0.version" AS "version_from",
	V."height",
	V."version" AS "version_to",
	SUM(n_payment_id)
FROM monero_version V
JOIN monero_version V0 ON V0."version" = V."version" - 1
JOIN tx_extra_tag_count C ON C.block_height >= V0."height" AND C.block_height < V."height"
GROUP BY V0."height", V0."version", V."height", V."version"
```

| "height" | "version_from" | "height" | "version_to" | "sum"  | 
|----------|-----------|----------|-----------|--------| 
| 0        | 1         | 1009827  | 2         | 263812 | 
| 1009827  | 2         | 1141317  | 3         | 68297  | 
| 1141317  | 3         | 1220516  | 4         | 110027 | 
| 1220516  | 4         | 1288616  | 5         | 131385 | 
| 1288616  | 5         | 1400000  | 6         | 183355 | 
| 1400000  | 6         | 1546000  | 7         | 290172 | 
| 1546000  | 7         | 1685555  | 8         | 269175 | 
| 1685555  | 8         | 1686275  | 9         | 1075   | 
| 1686275  | 9         | 1788000  | 10        | 135686 | 
| 1788000  | 10        | 1788720  | 11        | 835    | 
| 1788720  | 11        | 1978433  | 12        | 231772 | 
| 1978433  | 12        | 2180399  | 13        | 701    | 


## ASCII data
See previous report: https://github.com/noncesense-research-lab/monero_tx_extra/blob/master/ascii_data.md


# Tag statistics: Payment Id, Encrypted
## Histogram
```
SELECT
	COUNT(1) AS n,
	n_payment_id8
FROM tx_extra_tag_count C
GROUP BY n_payment_id8
ORDER BY n DESC
```

| "n"     | "n_payment_id8" | 
|---------|-----------------| 
| 5006244 | 1               | 
| 4919863 | 0               | 
| 9       | 2               | 


## Usage per version
```
SELECT
	V0."height",
	V0.version" AS "version_from",
	V."height",
	V."version" AS "version_to",
	SUM(n_payment_id8)
FROM monero_version V
JOIN monero_version V0 ON V0."version" = V."version" - 1
JOIN tx_extra_tag_count C ON C.block_height >= V0."height" AND C.block_height < V."height"
GROUP BY V0."height", V0."version", V."height", V."version"
```

| "height" | "version_from" | "height" | "version_to" | "sum" | 
|----------|-----------|----------|-----------|---------| 
| 0        | 1         | 1009827  | 2         | 176     | 
| 1009827  | 2         | 1141317  | 3         | 9138    | 
| 1141317  | 3         | 1220516  | 4         | 12000   | 
| 1220516  | 4         | 1288616  | 5         | 12273   | 
| 1288616  | 5         | 1400000  | 6         | 111712  | 
| 1400000  | 6         | 1546000  | 7         | 289375  | 
| 1546000  | 7         | 1685555  | 8         | 260263  | 
| 1685555  | 8         | 1686275  | 9         | 1189    | 
| 1686275  | 9         | 1788000  | 10        | 168026  | 
| 1788000  | 10        | 1788720  | 11        | 3724    | 
| 1788720  | 11        | 1978433  | 12        | 1391146 | 
| 1978433  | 12        | 2180399  | 13        | 2747226 | 


# Tag statistics: Merge mining
## Histogram
```
SELECT
	COUNT(1) AS n,
	n_merge_mining
FROM tx_extra_tag_count C
GROUP BY n_merge_mining
ORDER BY n DESC
```

| "n"     | "n_merge_mining" | 
|---------|------------------| 
| 9838740 | 0                | 
| 87376   | 1                | 


## Usage per version
```
SELECT
	V0."height",
	V0.version" AS "version_from",
	V."height",
	V."version" AS "version_to",
	SUM(n_merge_mining)
FROM monero_version V
JOIN monero_version V0 ON V0."version" = V."version" - 1
JOIN tx_extra_tag_count C ON C.block_height >= V0."height" AND C.block_height < V."height"
WHERE n_merge_mining > 0
GROUP BY V0."height", V0."version", V."height", V."version"
```

| "height" | "version_from" | "height" | "version_to" | "sum" | 
|----------|-----------|----------|-----------|-------| 
| 0        | 1         | 1009827  | 2         | 30726 | 
| 1009827  | 2         | 1141317  | 3         | 4410  | 
| 1141317  | 3         | 1220516  | 4         | 8555  | 
| 1220516  | 4         | 1288616  | 5         | 15161 | 
| 1288616  | 5         | 1400000  | 6         | 19762 | 
| 1400000  | 6         | 1546000  | 7         | 7388  | 
| 1546000  | 7         | 1685555  | 8         | 1357  | 
| 1686275  | 9         | 1788000  | 10        | 17    | 


# Tag statistics: Mysterious Minergate
## Histogram
```
SELECT
	COUNT(1) AS n,
	n_mysterious_minergate
FROM tx_extra_tag_count C
GROUP BY n_mysterious_minergate
ORDER BY n_mysterious_minergate ASC
```

| "n"     | "n_mysterious_minergate" | 
|---------|--------------------------| 
| 9777938 | 0                        | 
| 148178  | 1                        | 


## Usage per version
```
SELECT
	V0."height",
	V0.version" AS "version_from",
	V."height",
	V."version" AS "version_to",
	SUM(n_mysterious_minergate)
FROM monero_version V
JOIN monero_version V0 ON V0."version" = V."version" - 1
JOIN tx_extra_tag_count C ON C.block_height >= V0."height" AND C.block_height < V."height"
WHERE n_mysterious_minergate > 0
GROUP BY V0."height", V0."version", V."height", V."version"
```

| "height" | "version_from" | "height" | "version_to" | "sum" | 
|----------|-----------|----------|-----------|-------| 
| 1009827  | 2         | 1141317  | 3         | 22345 | 
| 1141317  | 3         | 1220516  | 4         | 68483 | 
| 1220516  | 4         | 1288616  | 5         | 8926  | 
| 1288616  | 5         | 1400000  | 6         | 16085 | 
| 1400000  | 6         | 1546000  | 7         | 25279 | 
| 1546000  | 7         | 1685555  | 8         | 7060  | 



# Appendix: Monero Version table
Reference: Scheduled software upgrades, https://github.com/monero-project/monero/blob/master/README.md#scheduled-software-upgrades

```
CREATE TABLE monero_version (
    height INTEGER,
    date VARCHAR,
    version INTEGER,
    software_version VARCHAR,
    software_version_recommended VARCHAR,
    details VARCHAR
);

INSERT INTO monero_version VALUES 
    (0, '', 1, 'v0.0', 'v0.0', 'Initial'),
    (1009827, 	'2016-03-22', 2, 	'v0.9.4', 	'v0.9.4', 	'Allow only >= ringsize 3, blocktime = 120 seconds, fee-free blocksize 60 kb'),
    (1141317, 	'2016-09-21', 3, 	'v0.9.4', 	'v0.10.0', 	'Splits coinbase into denominations'),
    (1220516,   '2017-01-05', 4, 	'v0.10.1', 	'v0.10.2.1', 	'Allow normal and RingCT transactions'),
    (1288616, 	'2017-04-15', 5, 	'v0.10.3.0', 	'v0.10.3.1', 	'Adjusted minimum blocksize and fee algorithm'),
    (1400000, 	'2017-09-16', 6, 	'v0.11.0.0', 	'v0.11.0.0', 	'Allow only RingCT transactions, allow only >= ringsize 5'),
    (1546000, 	'2018-04-06', 7, 	'v0.12.0.0', 	'v0.12.3.0', 	'Cryptonight variant 1, ringsize >= 7, sorted inputs'),
    (1685555, 	'2018-10-18', 8, 	'v0.13.0.0', 	'v0.13.0.4', 	'max transaction size at half the penalty free block size, bulletproofs enabled, cryptonight variant 2, fixed ringsize 11'),
    (1686275, 	'2018-10-19', 9, 	'v0.13.0.0', 	'v0.13.0.4', 	'bulletproofs required'),
    (1788000, 	'2019-03-09', 10, 	'v0.14.0.0', 	'v0.14.1.2', 	'New PoW based on Cryptonight-R, new block weight algorithm, slightly more efficient RingCT format'),
    (1788720, 	'2019-03-10', 11, 	'v0.14.0.0', 	'v0.14.1.2', 	'forbid old RingCT transaction format'),
    (1978433, 	'2019-11-30*', 12, 	'v0.15.0.0', 	'v0.16.0.0', 'New PoW based on RandomX, only allow >= 2 outputs, change to the block median used to calculate penalty, v1 coinbases are forbidden, rct sigs in coinbase forbidden, 10 block lock time for incoming outputs')
;

-- Make a new version for the current max height of tx_extra_tag_count, so we can reflect the current version
--    SELECT block_height FROM tx_extra_tag_count ORDER BY block_height DESC LIMIT 1 = 2180399
--    We will just know that v13 is a virtual reference to the current state of v12
INSERT INTO monero_version VALUES (2180399, '2020-09-09', '13', 'CURRENT', 'CURRENT', 'CURRENT');
```