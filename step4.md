<div class="top">

# Design query Q1
### [◂](command:katapod.loadPage?step3){.steps} Step 4 of 10 [▸](command:katapod.loadPage?step5){.steps}
</div>

Find information about all investment accounts of a user with username `joe`:

<details>
  <summary>Solution</summary>

```
SELECT *
FROM accounts_by_user
WHERE username = 'joe';
```

</details>

[continue](command:katapod.loadPage?step5){.orange_bar}