<div class="top">

# Design query Q3.1
### [◂](command:katapod.loadPage?step5){.steps} Step 6 of 10 [▸](command:katapod.loadPage?step7){.steps}
</div>

Find all trades for account `joe001`; order by trade date (desc):

<details>
  <summary>Solution</summary>

```
SELECT account, 
       TODATE(DATEOF(trade_id)) AS date, 
       trade_id, type, symbol,
       shares, price, amount 
FROM trades_by_a_d
WHERE account = 'joe001';
```

</details>

[continue](command:katapod.loadPage?step7){.orange_bar}