# Integrations Setup Guide

This guide covers how to connect the Profit First coach to banking and accounting systems for automated data access.

## Integration Discovery Process

### Step 1: Ask What They Use

Use `AskUserQuestion` to gather information:

```
Questions:
1. "What accounting software do you use?"
   Options: Xero, QuickBooks, FreshBooks, Wave, Spreadsheets only, Other

2. "Which bank do you use for your primary Profit First accounts?"
   Options: Relay, Mercury, NorthOne, Other

3. "Which bank do you use for HOLD accounts (should be separate institution)?"
   Options: Same as primary, Relay, Mercury, NorthOne, Other

4. "Do you have MCP integrations configured for any of these services?"
   Options: Yes, No, Not sure what MCP is
```

### Step 2: Search for Available MCPs

For each service the user mentions, use `WebSearch` to find available MCP servers:

```
WebSearch: "[service name] MCP server Claude"
```

Then report back to the user:
- Whether an MCP exists for their service
- Where to find it (GitHub repo, npm package, etc.)
- Basic setup instructions
- What capabilities it provides

### Step 3: Document Configuration

Record in the integrations state file:
- Which MCPs the user has configured
- Which MCPs are available but not yet configured (with links)
- Which services have no MCP available (manual data entry needed)

### Profit First Recommended Banks

These banks support multiple free checking accounts (essential for Profit First):
- **Relay** - Built specifically for Profit First users
- **NorthOne** - Small business focused
- **Mercury** - Startup focused

## Setup Questions

When onboarding a new business, ask these questions and then search for available MCPs:

### 1. Accounting Software

> What accounting software do you use?

After they answer, run `MCPSearch: "[their accounting software]"` to check for available integrations.

### 2. Banking Structure

> Do you have separate accounts set up for Profit First?
> - Yes, all 5 core accounts
> - Some accounts, not all
> - No, using one account
> - Planning to set up

> Which bank(s) do you use?
> - For primary accounts (INCOME, OWNER'S PAY, OPEX): ___
> - For HOLD accounts (PROFIT HOLD, TAX HOLD): ___

After they answer, run `MCPSearch: "[their bank name]"` for each bank to check for available integrations.

### 3. Data Access Preference

> How would you like to share financial data?
> - Via connected software (if MCP available)
> - Manual entry each session
> - Periodic updates to state file
> - Combination

### 4. Automation Interest

> Are you interested in automated reminders?
> - Allocation day reminders (10th & 25th)
> - Quarterly distribution reminders
> - Expense alerts
> - None needed

If yes, search for automation/CRM MCPs that might support scheduled triggers.

## State File: `profit-first-integrations.md`

After setup, create a state file to track integration configuration:

```markdown
# Profit First Integrations State

## Last Updated
[Date]

## Accounting Software
- **Platform**: [Name of accounting software]
- **MCP Available**: [Yes/No - result of MCPSearch]
- **MCP Tools**: [List discovered tools, e.g., mcp__[platform]__list-accounts]
- **Account Mapping**:
  - INCOME: [Account name in software]
  - PROFIT: [Account name in software]
  - OWNER'S PAY: [Account name in software]
  - TAX: [Account name in software]
  - OPEX: [Account name in software]

## Banking
- **Primary Bank**: [Bank name]
  - MCP Available: [Yes/No - result of MCPSearch]
  - Accounts: INCOME, OWNER'S PAY, OPEX
- **Hold Bank** (separate institution): [Bank name]
  - MCP Available: [Yes/No - result of MCPSearch]
  - Accounts: PROFIT HOLD, TAX HOLD

## Automation
- **Allocation Day Reminders**: [Enabled/Disabled]
- **Quarterly Reminders**: [Enabled/Disabled]
- **Automation MCP**: [Name and tools if available]

## Data Access Method
[How data will be accessed - via MCP, manual entry, or combination]
```

## Integration Workflows

### With Accounting MCP Connected

**Allocation Day Workflow:**
1. Coach reads account balances via MCP for INCOME balance
2. Calculates allocations using current CAPs
3. Presents transfer instructions
4. Owner executes transfers in banking app
5. Owner confirms, or coach can verify via MCP if bank feed is synced

**Monthly Review:**
1. Pull P&L via MCP for period analysis
2. Compare to TAP targets
3. Identify expense categories exceeding budget
4. Recommend adjustments

### Without Integrations

**Allocation Day Workflow:**
1. Ask owner for INCOME account balance
2. Calculate allocations using current CAPs
3. Present transfer instructions
4. Owner executes and confirms manually

**Monthly Review:**
1. Request key metrics from owner
2. Update state file with provided numbers
3. Provide analysis based on available data

## When User Adds New MCPs

If the user mentions they've configured a new MCP for their accounting software or bank:
1. Ask them to confirm it's working
2. Update the integrations state file
3. Adjust workflows to use the new integration

## Attribution

This integration guide supports the Profit First methodology by Mike Michalowicz. For the complete methodology, see [profitfirstbook.com](https://profitfirstbook.com).
