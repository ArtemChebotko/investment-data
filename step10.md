<div class="top">

# Design query Q3.5
### [◂](command:katapod.loadPage?step9){.steps} Step 10 of 10 [▸](command:katapod.loadPage?finish){.steps}
</div>

Find all trades for account `joe001`, date range `2020-09-07` - `2020-09-11` and instrument symbol `AAPL`; order by trade date (desc):

<details>
  <summary>Solution</summary>

```
SELECT account, 
       TODATE(DATEOF(trade_id)) AS date, 
       trade_id, type, symbol,
       shares, price, amount 
FROM trades_by_a_sd
WHERE account = 'joe001'
  AND symbol = 'AAPL'
  AND trade_id > maxTimeuuid('2020-09-07')
  AND trade_id < minTimeuuid('2020-09-12');
```

</details>

[continue](command:katapod.loadPage?finish){.orange_bar}
