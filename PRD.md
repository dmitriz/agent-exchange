# PRD: agent-exchange

## Purpose

This agent tracks up-to-date metadata about crypto platforms, with a focus on exchanges.  
Its role is to surface relevant operational characteristics that affect investment strategy, automation, or access.

## Responsibilities

- Track whether platforms are accessible by region or citizenship
- Record KYC requirements and usage limits
- Identify supported features such as staking, margin, or order types
- Track available APIs and exposed functionality
- Detect and log changes in platform policies, fees, or listings
- Provide a clean, consistent structure of information for other agents

## Inputs

- Platform websites and official documentation
- Public changelogs, RSS feeds, and announcement blogs
- Community channels such as Reddit, Discord, or other public signals
- Direct manual updates or configured tracking lists

## Outputs

- Clear summaries of each platform’s current status and features
- Logs of meaningful changes with timestamps
- Notifications or signals that can be integrated into other agents

## Update Triggers

- Regular scheduled refreshes
- Manual triggers for immediate re-check
- Event-driven updates from feeds or external signals

## Design Principles

- Only collect data that serves a practical, defined purpose
- Ensure all outputs are usable by other agents
- Avoid complexity in data collection
- Maintain transparent and traceable logs of all changes

## Change Logging

Changes to the following must be logged and timestamped:

- Fees (e.g. maker, taker, withdrawal)
- Platform access or availability
- API capabilities
- Listings or delistings of assets
- KYC policies or tier requirements

## Integration

- Integrated by agent-trade for validating order capabilities
- Used by agent-portfolio for platform access insights
- Accepts signals from agent-news if relevant updates are detected
- Referenced by investor-index as a primary metadata source

## Status

This specification defines the initial scope for agent-exchange.  
Repository and implementation planning will follow this document.
