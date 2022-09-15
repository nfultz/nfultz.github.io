<!-- njnmdoc:  title="Google Sheets"  -->

Imagine you have three columns, monthly statement date, cash deposited, final balance.

To calc Internal rate of return, do

```
=XIRR({$E$2:E142;-F142}, {$B$2:B142;B142})
```

the curly braces will construct arrays. Note the negative sign on F142 - this is as if you
did a full withdrawal. the $ anchors are such that this can be filled down over the whole
set of data.
