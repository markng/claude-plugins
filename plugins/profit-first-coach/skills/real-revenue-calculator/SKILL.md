---
name: real-revenue-calculator
description: Calculate Real Revenue for Profit First allocations. Determines if a business should use Real Revenue (vs Total Revenue) and calculates it.
---

# Real Revenue Calculator

Calculate Real Revenue for Profit First allocations and determine whether a business should use Real Revenue or Total Revenue for their TAP calculations.

## What is Real Revenue?

**Real Revenue = Total Revenue - Materials & Subcontractors**

Real Revenue is NOT the same as Gross Profit. It only subtracts direct pass-through costs, not labor or overhead.

## When to Use Real Revenue

**Use Real Revenue when Materials & Subcontractors exceed 25% of Total Revenue.**

Otherwise, use Total Revenue directly for TAP calculations.

## Input Required

1. **Total Annual Revenue**: All money the business brings in
2. **Materials Cost**: Raw materials, components, inventory
3. **Subcontractor Cost**: Third-party contractors paid per project

## What Counts as Materials & Subcontractors

### INCLUDE (subtract from Total Revenue):
- Raw materials and components
- Inventory/product costs
- Third-party subcontractors
- Pass-through costs tied directly to delivering product/service
- Per-project contractors (only paid for income-generating work)

### DO NOT INCLUDE (these stay in OpEx):
- Employee wages (even "direct labor")
- W-2 payroll
- Fixed overhead
- Rent, utilities
- Regular team salaries
- Benefits

## Calculation Process

1. **Gather inputs**:
   - Total Revenue: $______
   - Materials: $______
   - Subcontractors: $______

2. **Calculate Materials & Subs percentage**:
   ```
   M&S Percentage = (Materials + Subcontractors) / Total Revenue × 100
   ```

3. **Determine which revenue to use**:
   - If M&S Percentage ≥ 25%: Use Real Revenue
   - If M&S Percentage < 25%: Use Total Revenue

4. **Calculate Real Revenue** (if needed):
   ```
   Real Revenue = Total Revenue - Materials - Subcontractors
   ```

## Response Format

```
## Real Revenue Calculation

### Inputs
- Total Revenue: $X
- Materials: $X
- Subcontractors: $X
- **Materials & Subs Total**: $X

### Analysis
- M&S as % of Total Revenue: X%
- Threshold: 25%
- **Recommendation**: [Use Real Revenue / Use Total Revenue]

### Result
[If using Real Revenue:]
- **Real Revenue**: $X
- Use this figure for TAP lookups and allocations

[If using Total Revenue:]
- **Use Total Revenue**: $X for TAP lookups and allocations
- Materials & Subs are below the 25% threshold

### What This Means
[Explain implications for their business type]
```

## Examples

### Example 1: Home Builder (Use Real Revenue)
- Total Revenue: $10,000,000
- Materials: $4,000,000
- Subcontractors: $3,000,000
- M&S Total: $7,000,000 (70%)
- **Real Revenue: $3,000,000**
- This business operates like a $3M company, not $10M

### Example 2: Consultant (Use Total Revenue)
- Total Revenue: $500,000
- Materials: $5,000
- Subcontractors: $20,000
- M&S Total: $25,000 (5%)
- **Use Total Revenue: $500,000**
- Materials & Subs are minimal

### Example 3: E-commerce (Use Real Revenue)
- Total Revenue: $800,000
- Inventory/COGS: $320,000
- Subcontractors: $0
- M&S Total: $320,000 (40%)
- **Real Revenue: $480,000**
- Product cost is significant

## Common Mistakes

1. **Including employee wages** - Even "direct labor" employees are NOT subtracted
2. **Using Gross Profit** - Real Revenue is simpler: only materials and third-party subs
3. **Forgetting the 25% threshold** - Low M&S businesses use Total Revenue
4. **Subtracting overhead** - Rent, utilities, etc. are OpEx, not M&S

## Why This Matters

If you use Total Revenue when you should use Real Revenue:
- Your TAPs will be based on the wrong tier
- You'll allocate percentages to money that's already committed to materials
- OpEx will be underfunded
- The system will fail

## Attribution

Real Revenue calculation is from the Profit First methodology by Mike Michalowicz. For the complete methodology, see "Profit First" at profitfirstbook.com.
