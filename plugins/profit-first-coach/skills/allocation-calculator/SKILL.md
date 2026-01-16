---
name: allocation-calculator
description: Calculate exact dollar amounts for Profit First allocations based on income and percentages. Use on allocation days (10th and 25th).
---

# Allocation Calculator

Calculate the exact dollar amounts to transfer to each Profit First account based on income received and current allocation percentages.

## When to Use

Use this skill on allocation days (10th and 25th of each month) to calculate how much to transfer from the INCOME account to each destination account.

## Input Required

1. **Income Amount**: Balance in INCOME account to be allocated
2. **Allocation Percentages**: Current percentages for each account
   - Profit %
   - Owner's Pay %
   - Tax %
   - OpEx %

Note: Use CURRENT percentages (CAPs), not target percentages (TAPs), unless you've fully transitioned.

## Calculation

For each account:
```
Allocation Amount = Income Amount × (Percentage / 100)
```

## Response Format

```
## Profit First Allocation

### Income to Allocate: $X

### Allocations

| Account | Percentage | Amount |
|---------|------------|--------|
| Profit | X% | $X.XX |
| Owner's Pay | X% | $X.XX |
| Tax | X% | $X.XX |
| Operating Expenses | X% | $X.XX |
| **Total** | **100%** | **$X.XX** |

### Transfer Instructions

1. ✅ Transfer $X.XX to **PROFIT** account
2. ✅ Transfer $X.XX to **OWNER'S PAY** account
3. ✅ Transfer $X.XX to **TAX** account
4. ✅ Transfer $X.XX to **OPEX** account

### Hold Account Transfers (Separate Bank)

After the above transfers:
- Move PROFIT balance to **PROFIT HOLD** at separate bank
- Move TAX balance to **TAX HOLD** at separate bank

### Verification
After all transfers, INCOME account should show: $0.00
```

## Example Calculation

**Input:**
- Income to allocate: $10,000
- Profit: 5%
- Owner's Pay: 50%
- Tax: 15%
- OpEx: 30%

**Output:**

| Account | Percentage | Amount |
|---------|------------|--------|
| Profit | 5% | $500.00 |
| Owner's Pay | 50% | $5,000.00 |
| Tax | 15% | $1,500.00 |
| Operating Expenses | 30% | $3,000.00 |
| **Total** | **100%** | **$10,000.00** |

## Handling Cents/Rounding

When allocations don't divide evenly:
1. Calculate each allocation and round to nearest cent
2. Any rounding difference (usually a few cents) goes to OpEx
3. Total must equal exact income amount

**Example with rounding:**
- Income: $1,547.00
- Profit 5%: $77.35
- Owner's Pay 50%: $773.50
- Tax 15%: $232.05
- OpEx 30%: $464.10
- Total: $1,547.00 ✓

## For Product Businesses with Materials Account

If the business has a Materials/Inventory account, allocate that FIRST:

```
1. Materials: X% → Materials Account
2. Remaining = Income - Materials allocation
3. Apply TAPs to Remaining (this is the Real Revenue)
```

**Example:**
- Income: $10,000
- Materials: 40% → $4,000 to Materials
- Remaining (Real Revenue): $6,000
- Apply TAPs to $6,000:
  - Profit 5%: $300
  - Owner's Pay 50%: $3,000
  - Tax 15%: $900
  - OpEx 30%: $1,800

## Validation Checks

Before presenting allocations, verify:
- [ ] All percentages sum to 100%
- [ ] All amounts sum to income total
- [ ] No negative amounts
- [ ] Amounts are rounded to cents

If percentages don't sum to 100%, alert the user and ask them to verify their current allocation percentages.

## Important Reminders

1. **Allocate PROFIT first** - This is the core principle
2. **Use current percentages** - Not targets unless fully transitioned
3. **Transfer to HOLD accounts** - Profit and Tax should move to separate bank
4. **INCOME should be empty** - After allocation, nothing left in INCOME
5. **Only pay bills from OpEx** - Never from other accounts

## Attribution

Allocation methodology from Profit First by Mike Michalowicz. For the complete methodology, see "Profit First" at profitfirstbook.com.
