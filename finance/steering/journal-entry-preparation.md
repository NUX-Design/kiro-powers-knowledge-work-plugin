# Journal Entry Preparation

Prepare journal entries with proper debits, credits, supporting detail, and review documentation.

This workflow assists with accounting operations but does not replace qualified financial review before posting.

## Typical Inputs

- Entry type such as AP accrual, fixed assets, prepaid, payroll, or revenue
- Accounting period such as `2024-12` or `2024-Q4`
- Trial balance or GL balances for affected accounts
- Subledger detail or supporting schedules
- Prior period entries for comparison when available

## Workflow

### 1. Gather Source Data

If ERP or data warehouse tools are connected:

- Pull the trial balance for the specified period.
- Pull subledger detail for relevant accounts.
- Pull prior period entries of the same type.
- Identify current GL balances for affected accounts.

If no data source is connected, ask for pasted balances, schedules, or spreadsheets.

### 2. Calculate The Entry

**AP accrual**
- Identify goods or services received but not yet invoiced.
- Debit expense or asset accounts.
- Credit accrued liabilities.

**Fixed assets**
- Pull the fixed asset register or depreciation schedule.
- Calculate period depreciation or amortization.
- Debit depreciation expense.
- Credit accumulated depreciation or amortization.

**Prepaids**
- Pull the prepaid amortization schedule.
- Calculate the period amortization.
- Debit expense accounts.
- Credit prepaid expense accounts.

**Payroll**
- Calculate unpaid salary, benefits, payroll tax, and bonus accruals.
- Debit salary, benefits, and payroll tax expense.
- Credit accrued payroll, accrued benefits, and accrued taxes.

**Revenue**
- Review contracts and performance obligations.
- Calculate recognized revenue and deferred revenue changes.
- Debit deferred revenue or accounts receivable.
- Credit revenue accounts.

### 3. Generate The Journal Entry

```markdown
Journal Entry: [Type] — [Period]
Prepared by: [User]
Date: [Period end date]

| Line | Account Code | Account Name | Debit | Credit | Department | Memo |
|------|-------------|--------------|-------|--------|------------|------|
| 1    | XXXX        | [Name]       | X,XXX |        | [Dept]     | [Detail] |
| 2    | XXXX        | [Name]       |       | X,XXX  | [Dept]     | [Detail] |
|      |             | **Total**    | X,XXX | X,XXX  |            |      |

Supporting Detail:
- [Calculation basis and assumptions]
- [Reference to supporting schedule or documentation]

Reversal: [Yes/No — if yes, specify reversal date]
```

### 4. Review Checklist

- [ ] Debits equal credits
- [ ] Correct accounting period
- [ ] Account codes are valid
- [ ] Amounts are supported and mathematically correct
- [ ] Memo is clear enough for audit review
- [ ] Department or cost center coding is correct
- [ ] Treatment is consistent with prior periods
- [ ] Reversal flag is set correctly
- [ ] Supporting documentation is referenced
- [ ] Entry is within approval authority

## Output

Provide:

- the formatted journal entry
- supporting calculations
- comparison to prior period entry when available
- items flagged for review
- posting instructions or upload guidance
