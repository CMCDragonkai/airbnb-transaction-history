# airbnb-transaction-history

This script automatically downloads your transaction history from Airbnb for Tax Purposes based on 01-07-Y to 30-06-Y+1.

Use it like:

```
airbnb-transaction-history \
--username <email> \
--password <password> \
--start <2014> \
--end <2015> \
--id <userid> \
--directory <.> \
--origin <https://www.airbnb.com.au>
```

These options are required:

```
--username
--password
```

The rest are optional.

## dependencies

* httpie - https://github.com/jkbrzt/httpie
* csvkit - https://github.com/onyxfish/csvkit

## improvements

Replace httpie with curl.