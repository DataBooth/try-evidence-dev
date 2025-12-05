---
title: Welcome to Titanic
queries:
  - all_data: all_data_titanic.sql
---

<Details title='Titanic dataset'>
The data source is here: `https://hbiostat.org/data/repo/titanic3.csv`
</Details>

```sql select_star
  select
      *
  from titanic.raw_titanic
  group by pclass
```

<!-- ```sql orders_by_category
  select 
      date_trunc('month', order_datetime) as month,
      sum(sales) as sales_usd,
      category
  from needful_things.orders
  where category like '${inputs.category.value}'
  and date_part('year', order_datetime) like '${inputs.year.value}'
  group by all
  order by sales_usd desc
``` -->



## What's Next?

- Deploy your project with [Evidence Cloud](https://evidence.dev/cloud)