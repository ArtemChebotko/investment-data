<div class="top">

# Populate tables
### [◂](command:katapod.loadPage?step2){.steps} Step 3 of 10 [▸](command:katapod.loadPage?step4){.steps}
</div>

Execute the CQL script to insert sample data:
```
SOURCE 'assets/investment_data.cql'
```

Retrieve all rows from table `accounts_by_user`:
```
SELECT * FROM accounts_by_user;        
```

Retrieve all rows from table `positions_by_account`:
```
SELECT * FROM positions_by_account;
```

Retrieve all rows from table `trades_by_a_d`:
```
SELECT * FROM trades_by_a_d;                    
```

Retrieve all rows from table `trades_by_a_td`:
```
SELECT * FROM trades_by_a_td;
```

Retrieve all rows from table `trades_by_a_std`:
```
SELECT * FROM trades_by_a_std;       
```

Retrieve all rows from table `trades_by_a_sd`:
```
SELECT * FROM trades_by_a_sd;       
```

[continue](command:katapod.loadPage?step4){.orange_bar}