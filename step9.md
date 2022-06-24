<div class="top">

# Design query Q3.4
### [◂](command:katapod.loadPage?step8){.steps} Step 9 of 10 [▸](command:katapod.loadPage?step10){.steps}
</div>

Find all trades for account `joe001`, date range `2020-09-07` - `2020-09-11`, transaction type `buy` and instrument symbol `AAPL`; order by trade date (desc):

<details>
  <summary>Solution</summary>

```
SELECT account, 
       TODATE(DATEOF(trade_id)) AS date, 
       trade_id, type, symbol,
       shares, price, amount 
FROM trades_by_a_std
WHERE account = 'joe001'
  AND symbol = 'AAPL'
  AND type = 'buy'
  AND trade_id > maxTimeuuid('2020-09-07')
  AND trade_id < minTimeuuid('2020-09-12');
```

</details>

[continue](command:katapod.loadPage?step10){.orange_bar}
