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

The rest are optional, the start and end dates will be automatically calculated to the nearest financial year based on your computer's date.

The output is 5 files, for example:

```
airbnb_2014-2015.csv
payouts_2014-2015.csv
time_2014-2015.csv
duration_2014-2015.txt
income_2014-2015.txt
```

On the command line it looks like:

```
Start - End: 2014 - 2015
Results will be saved to: /somewhere/someplace
Downloading transaction history...
Finished downloading. Beginning data munging.
Finished munging. Exporting data to specified directory.
Income earned: 100000
Nights stayed: 9000
```

## dependencies

* httpie - https://github.com/jkbrzt/httpie
* csvkit - https://github.com/onyxfish/csvkit

## improvements

Replace httpie with curl.
