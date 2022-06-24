<div class="top">

# Design query Q3.2
### [◂](command:katapod.loadPage?step6){.steps} Step 7 of 10 [▸](command:katapod.loadPage?step8){.steps}
</div>

Find all trades for account `joe001` and date range `2020-09-07` - `2020-09-11`; order by trade date (desc):

<details>
  <summary>Solution</summary>

```
SELECT account, 
       TODATE(DATEOF(trade_id)) AS date, 
       trade_id, type, symbol,
       shares, price, amount 
FROM trades_by_a_d
WHERE account = 'joe001'
  AND trade_id > maxTimeuuid('2020-09-07')
  AND trade_id < minTimeuuid('2020-09-12');
```

</details>

[continue](command:katapod.loadPage?step8){.orange_bar}
