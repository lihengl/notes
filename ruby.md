# Ruby Tips

Handy scripts can be used in IRB or script files.

## Time Conversion

From Unix timestamp in millisecond to time-zoned date time.

```ruby
# This truncates the millisecond part, though.
Time.at(('1656321942269'.to_i/1000).to_i, in: '+08:00')
```
