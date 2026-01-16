---
name: tap-lookup
description: Look up Target Allocation Percentages (TAPs) based on revenue level. Returns recommended Profit First percentages for Profit, Owner's Pay, Tax, and OpEx.
---

# TAP Lookup

Look up the recommended Target Allocation Percentages (TAPs) for a business based on their Real Revenue level.

## Usage

Provide the annual Real Revenue amount and receive the recommended TAPs.

## Input Required

- **Real Revenue**: Annual revenue minus materials and subcontractors (if applicable)

If the user provides Total Revenue and has significant materials/subcontractors (>25%), remind them to calculate Real Revenue first using the `real-revenue-calculator` skill.

## TAP Table

| Real Revenue | Profit | Owner's Pay | Tax | OpEx |
|--------------|--------|-------------|-----|------|
| $0 - $250,000 | 5% | 50% | 15% | 30% |
| $250,001 - $500,000 | 10% | 35% | 15% | 40% |
| $500,001 - $1,000,000 | 15% | 20% | 15% | 50% |
| $1,000,001 - $5,000,000 | 10% | 10% | 15% | 65% |
| $5,000,001 - $10,000,000 | 15% | 5% | 15% | 65% |
| $10,000,001 - $50,000,000 | 20% | 0% | 15% | 65% |

## Response Format

When providing TAPs, format as:

```
## Recommended TAPs for [Revenue Tier]

Based on Real Revenue of $X, your Target Allocation Percentages are:

| Account | TAP |
|---------|-----|
| Profit | X% |
| Owner's Pay | X% |
| Tax | X% |
| Operating Expenses | X% |
| **Total** | **100%** |

### Key Notes for This Tier
[Include relevant notes based on tier]
```

## Tier-Specific Notes

**$0-$250K**:
- Owner's Pay is highest (50%) because you ARE the business
- Profit starts at 5% - small but builds the habit
- OpEx is constrained (30%) to force discipline early

**$250K-$500K**:
- Profit doubles to 10% as business stabilizes
- Owner's Pay decreases as business can afford more help
- OpEx increases to 40% for growth infrastructure

**$500K-$1M**:
- Profit at 15% - business is truly profitable
- Owner's Pay at 20% - may be taking salary + distributions
- OpEx at 50% - significant team and infrastructure

**$1M-$5M**:
- Profit drops to 10% temporarily for scale investment
- Owner's Pay at 10% - mostly distributions now
- OpEx at 65% - significant operational complexity

**$5M-$10M**:
- Profit back to 15%
- Owner's Pay at 5% - minimal salary, mostly profit distributions
- OpEx steady at 65%

**$10M-$50M**:
- Profit at 20% - highly profitable at scale
- Owner's Pay at 0% - all compensation through distributions
- OpEx at 65%

## Important Reminders

1. **These are TARGETS, not starting points** - Use the 3% rule to gradually move toward TAPs
2. **Industry variations exist** - Some industries have different recommended TAPs
3. **Tax may vary** - 15% is standard but consult a CPA for your situation
4. **Real Revenue matters** - Product businesses must use Real Revenue, not Total Revenue

## Attribution

TAPs are from the Profit First methodology by Mike Michalowicz. For the complete methodology, see "Profit First" at profitfirstbook.com.
