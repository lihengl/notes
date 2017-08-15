# MySQL Notes

Keeping tips for advanced query techniques.

## Group by Substring of Column Value

```sql
+------------------+-------+-----+
|email             |item   |count|
+------------------+-------+-----+

select email, count from holdings
where item='sword'
group by (substring(email, 1, 3)) order by email desc;
```
