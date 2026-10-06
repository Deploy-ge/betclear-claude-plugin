# BetClear for Claude

BetClear helps people stop gambling. This plugin connects Claude to the BetClear
remote MCP server so Claude can block gambling sites on a device, check whether a
website is a gambling site, estimate what gambling costs, and help someone get
through an urge to bet.

## What it includes

- A remote MCP server, `https://www.betclear.app/api/mcp` (Streamable HTTP, no
  authentication), with five read-only tools:
  - `block_gambling_sites`: setup steps for iPhone, Android, Mac or Windows 11.
  - `check_gambling_site`: whether a domain is on the BetClear gambling blocklist.
  - `gambling_cost_calculator`: turns a weekly gambling spend into monthly,
    yearly and multi-year totals.
  - `urge_support`: practical ways to get through an urge, plus free support
    organisations.
  - `explain_betclear`: what BetClear is, how it works and what it costs.
- One skill, `betclear`, that tells Claude when to call each tool.

## Data handling

- The plugin has no hooks, scripts or local code. It only declares the remote
  server above, run by BetClear.
- The server receives only what Claude passes to a tool: a platform name, a
  domain, a weekly amount and currency, and an optional locale. No account, login,
  name, email or other personal data is requested or stored.
- BetClear records only that a tool was called (tool name, assistant name and
  locale) to measure usage. It does not log the domain or the amount.
- Tool answers include a link to https://www.betclear.app. Nothing is sent to any
  other service.
- Privacy policy: https://www.betclear.app/en/privacy

## Limits

BetClear is a website blocker, not clinical or crisis support. No blocker can
guarantee every gambling site is covered. If you or someone else is in danger,
contact your local emergency services.

Documentation: https://www.betclear.app/en/mcp
Support: hello@betclear.app
