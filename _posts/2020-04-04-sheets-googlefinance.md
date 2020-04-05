---
layout: post
category: google-sheets
---
# How to use the Google Finance function in Google Sheets

Use the `GOOGLEFINANCE()` formula in Google sheets.

## Examples

Current stock price:
```
=GOOGLEFINANCE("GOOG")
=GOOGLEFINANCE("GOOG", "price")
```

The 52-week low price:
`=GOOGLEFINANCE("GOOG", "low52")`

How far delayed the real-time data is.
`=GOOGLEFINANCE("GOOG", "datadelay")`

## Mutual funds

Previous day's closing price.
`=GOOGLEFINANCE("FSKAX", "closeyest")`

Name of mutual fund:
`=GOOGLEFINANCE("FSKAX", "name")`

Fund's expense ratio:
`=GOOGLEFINANCE("FSKAX", "expenseratio")`

Amount of the most recent cash distribution:
`=GOOGLEFINANCE("FSKAX", "incomedividend")`

Date of the most recent cash distribution:
`=GOOGLEFINANCE("FSKAX", "incomedividenddate")`

Amount of the most recent capital gain distribution.
`=GOOGLEFINANCE("FSKAX", "capitalgain")`

Date of the most recent capital gain distribution.
`=GOOGLEFINANCE("FSKAX", "capitalgaindate")`

The year-to-date return:
`=GOOGLEFINANCE("FSKAX", "returnytd")`

`=GOOGLEFINANCE("GOOG", "price", "1/1/2014", "12/31/2014", "DAILY")`

Sources:

<https://youtu.be/zOJ1l0S-Zj0>
<https://support.google.com/docs/answer/3093281?hl=en>
