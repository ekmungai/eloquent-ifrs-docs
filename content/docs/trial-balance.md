---
title: 'Trial Balance'
date: 2018-11-28T15:14:39+10:00
weight: 21
---

The Trial Balance is a listing of all accounts in the chart of accounts, grouped by whether they belong to the Income Statement or Balance which compares their debit and credit balances. The debit and credit sides of this report must always be in agreement.

### Construction
An TrialBalance
+ `$year`: The year for which account balances should be included in the report. Defaults to the current year.

### Attributes
+ `entity`: The Entity object associated with the report.
+ `reportingPeriod`: The ReportingPeriod object associated with the report.
+ `balances`: The credit and debit balances for the report.
+ `accounts`: An array of the accounts included in the report grouped by their categories.

### Methods
+ `$trialBalance->toString():` Prints out a summarized version of the report as a string. !!IMPORTANT!! this method is only intended for debugging and should never be used for production. 
+ `$incomeStatement->getSections():` Retrieves the balances of the sections of the report, grouped by the categories therein. 
+ `$incomeStatement->attributes():` Presents the report's attributes as an array. Useful for debugging. 

### Constants
+ `IncomeStatement::TITLE`: The title of the report. 
+ `IncomeStatement::ASSETS`: The Assets section of the report. Includes both Current and Non-current assets. 
+ `IncomeStatement::LIABILITIES`: The Liabilities section of the report. Includes both Current and Non-current liabilities.
+ `IncomeStatement::EQUITY`: The Equity section of the report. 
+ `IncomeStatement::RECONCILIATION`: The Non Reconciliation section of the report. 
