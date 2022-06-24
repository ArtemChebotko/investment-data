<div class="top">

# Design query Q2
### [◂](command:katapod.loadPage?step4){.steps} Step 5 of 10 [▸](command:katapod.loadPage?step6){.steps}
</div>

Find all positions in account `joe001`; order by instrument symbol (asc):

<details>
  <summary>Solution</summary>

```
SELECT * 
FROM positions_by_account
WHERE account = 'joe001'; 
```

</details>

[continue](command:katapod.loadPage?step6){.orange_bar}