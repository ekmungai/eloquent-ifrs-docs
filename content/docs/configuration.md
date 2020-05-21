---
title: 'Configuration'
date: 2019-02-11T19:30:08+10:00
draft: false
weight: 3
---

### Default Configuration

The package installs with the default settings as regards the names of Accounts/Transactions Types, Report Titles and Section names as well as Accounts Codes. To adjust these settings use the Laravel artisan publish command to install the ifrs configuration to your applications config folder where you can edit it.

```
php artisan vendor:publish
```

### Financial Terms
Standard accounting terms such as `Balance::DEBIT` and `Balance::CREDIT` as well as Reporting period status `[ReportingPeriod::OPEN, ReportingPeriod::CLOSED, ReportingPeriod::ADJUSTING]` are also defined in the configuration files.

### Object Names

Names refer to the human readable lables attached to Account and Transaction types, Report Titles and their Sections. By default, the account and transaction type and report title  names are equivalent to their object types. 

For example, the name for the `Account::INVENTORY` account type is *Inventory* while that for `Account::BANK` is *Bank*. Similarly for Transactions, the name of the `Transaction::CS` transaction type is *Cash Sale* while the name that referes to the `IncomeStatement::TITLE` is *Income Statement*.

Names do not always follow the object type however, for instance the name for a `Transaction::IN` is *Client Invoice* and that for `Transaction::JN` is *Journal Entry* so you should always check the configuration file to be sure.

### Account Codes

Account codes are the numerical representation of the Account object type. Some countries have a reccommended scheme for allocating account codes that is aimed at improving the comparability between financial reports of different entities. For example, revenue accounts codes are numbers between 4000 and 5000 according to the German SKR04 scheme. A default scheme is included in the configuration file.

### Aging Schedule Brackets

These are the time chunks into which the outstanding balances for client receivables and supplier paybles are split. A default segmentation is included in the configuration file.

### Ledger Hashing Algorithm

Eloquent IFRS hashes the contents of the Ledger to maintain transactional integrity. The algorithm used for this process can be set by changing the value of `hashing_algorithm`. This value defaults to PHP's internal `PASSWORD_DEFAULT` 

***