---
name: cap-to-tap-planner
description: Plan the quarterly transition from Current Allocation Percentages (CAPs) to Target Allocation Percentages (TAPs) using the 3% rule.
---

# CAP to TAP Planner

Plan the gradual transition from your Current Allocation Percentages (CAPs) to your Target Allocation Percentages (TAPs) using the Profit First 3% rule.

## The 3% Rule

**Never adjust allocations by more than 3 percentage points per quarter.**

Jumping straight to TAPs will starve your business of operating cash. Gradual change prevents crisis.

## Input Required

1. **Current Allocation Percentages (CAPs)** - What you're actually doing today:
   - Profit: ___%
   - Owner's Pay: ___%
   - Tax: ___%
   - OpEx: ___%

2. **Target Allocation Percentages (TAPs)** - Where you want to be:
   - Profit: ___%
   - Owner's Pay: ___%
   - Tax: ___%
   - OpEx: ___%

## Planning Process

1. **Calculate gaps** for each account (TAP - CAP)
2. **Identify largest gaps** - prioritize accounts furthest from target
3. **Plan quarterly adjustments** - max 3% total movement per quarter
4. **Balance changes** - increases must be offset by decreases (total always 100%)

## Response Format

```
## CAP to TAP Transition Plan

### Current State

| Account | CAP (Current) | TAP (Target) | Gap |
|---------|---------------|--------------|-----|
| Profit | X% | X% | +/-X% |
| Owner's Pay | X% | X% | +/-X% |
| Tax | X% | X% | +/-X% |
| OpEx | X% | X% | +/-X% |

### Quarterly Adjustment Plan

#### Quarter 1 (Current → Q1)
| Account | Before | Change | After |
|---------|--------|--------|-------|
| Profit | X% | +X% | X% |
| Owner's Pay | X% | +X% | X% |
| Tax | X% | — | X% |
| OpEx | X% | -X% | X% |

**Rationale**: [Why these changes first]

#### Quarter 2 (Q1 → Q2)
[Same format]

#### Quarter 3 (Q2 → Q3)
[Same format]

[Continue until TAPs reached]

### Timeline Summary
- **Start**: [Current CAPs]
- **Quarters to reach TAPs**: X
- **Target completion**: [Date/Quarter]

### Priority Order
1. [First priority and why]
2. [Second priority and why]
3. [Third priority and why]
```

## Prioritization Guidelines

### Typical Priority Order:

1. **Profit** (if at 0%) - Establishing ANY profit allocation is priority #1
2. **Tax** (if under-allocated) - Avoid tax-time surprises
3. **Owner's Pay** (if under-allocated) - You need to pay yourself
4. **OpEx reduction** - The constraint that makes everything else work

### Special Cases:

- **If Tax is way under**: Prioritize to avoid IRS problems
- **If Profit is at 0%**: Even 1% is a win - start there
- **If OpEx is already tight**: Slower transition, smaller adjustments

## Example Plan

**Starting CAPs:**
- Profit: 0%
- Owner's Pay: 35%
- Tax: 10%
- OpEx: 55%

**Target TAPs ($200K business):**
- Profit: 5%
- Owner's Pay: 50%
- Tax: 15%
- OpEx: 30%

**Quarter 1:**
- Profit: 0% → 2% (+2%)
- OpEx: 55% → 53% (-2%)
- *Focus: Establish profit habit*

**Quarter 2:**
- Owner's Pay: 35% → 38% (+3%)
- OpEx: 53% → 50% (-3%)
- *Focus: Increase owner compensation*

**Quarter 3:**
- Profit: 2% → 4% (+2%)
- Tax: 10% → 11% (+1%)
- OpEx: 50% → 47% (-3%)
- *Focus: Continue profit growth, start tax catch-up*

**Quarter 4:**
- Profit: 4% → 5% (+1%)
- Tax: 11% → 13% (+2%)
- OpEx: 47% → 44% (-3%)
- *Focus: Reach profit target, continue tax*

**Quarters 5-8:** Continue until all accounts reach TAPs

**Timeline: 8 quarters (2 years) to full TAPs**

## Validation Rules

1. **Total must always equal 100%** - Every increase needs an equal decrease
2. **Max 3% total change per quarter** - Sum of all changes ≤ 3%
3. **No negative percentages** - Can't go below 0% on any account
4. **Realistic OpEx floor** - Don't cut OpEx below what's needed to operate

## Warning Signs

Alert the user if:
- OpEx would drop below 20% (may be unsustainable)
- Changes exceed 3% per quarter
- Plan would take more than 3 years (may need revenue growth first)
- Starting CAPs don't sum to 100% (data error)

## Important Notes

1. **This is a plan, not a commitment** - Adjust as circumstances change
2. **Review quarterly** - Business changes, plans should too
3. **Celebrate progress** - Each quarter closer to TAPs is a win
4. **Expense cuts required** - Moving to TAPs means reducing OpEx spending

## Attribution

The 3% rule and CAP-to-TAP methodology is from Profit First by Mike Michalowicz. For the complete methodology, see "Profit First" at profitfirstbook.com.
