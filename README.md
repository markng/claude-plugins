# Claude Plugins Marketplace

Personal Claude Code plugin marketplace by Mark Sherwin Gonzales.

## Installation

Add this marketplace to Claude Code:

```
/plugin marketplace add markng/claude-plugins
```

## Available Plugins

| Plugin | Description |
|--------|-------------|
| `claude-speech` | Text-to-speech for Claude responses using macOS `say` command |
| `profit-first-coach` | Profit First CFO advisor using Mike Michalowicz's methodology for behavioral cash management |

## Installing Plugins

After adding the marketplace:

```
/plugin install claude-speech@markng-plugins
```

## Plugin Details

### claude-speech

Speaks Claude's responses aloud using macOS text-to-speech.

**Features:**
- Toggle via natural language ("turn on speech", "stop talking")
- Non-blocking background speech
- Requires macOS and `jq`

**Usage:**
- Enable: `touch ~/.claude-speak` or say "turn on speech"
- Disable: `rm ~/.claude-speak` or say "turn off speech"

**Note:** The Stop hook must be manually added to your settings.json for full functionality. See plugin README for details.

### profit-first-coach

A comprehensive Profit First CFO advisor implementing Mike Michalowicz's methodology for behavioral cash management.

**Features:**
- Target Allocation Percentages (TAP) lookup by revenue tier
- Real Revenue calculator (excluding pass-through expenses)
- Allocation calculator for income distribution
- CAP to TAP transition planning
- Quarterly profit distribution calculator
- Integration with Xero and banking MCPs

**Skills Included:**
- `/tap-lookup` - Find recommended TAPs for your revenue tier
- `/real-revenue-calculator` - Calculate true operating revenue
- `/allocation-calculator` - Distribute income across accounts
- `/cap-to-tap-planner` - Plan transition from current to target allocations
- `/quarterly-distribution` - Calculate profit distributions

**Documentation:**
- TAPs reference tables by business stage
- Account structure guide (5 foundational + advanced accounts)
- Implementation guide for Profit First setup
- Banking/accounting integration setup

## License

MIT
