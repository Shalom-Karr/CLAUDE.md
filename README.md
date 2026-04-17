# CLAUDE.md

Custom behavioral instructions for Claude AI that define working preferences across execution, decision-making, communication, and code practices.

## Purpose

This file contains generalized behavioral guidelines that can be placed in `~/.claude/CLAUDE.md` to apply globally across all projects when working with Claude Code or Claude Desktop.

## Key Features

- **Execution preferences**: Run to completion, use idle time productively, monitor long processes with concrete metrics
- **Delegation strategy**: Create sub-agents for small tasks to preserve focus on bigger-picture outcomes
- **Decision-making rules**: Action over discussion, pragmatic over perfect, minimal over-planning
- **Communication style**: Direct, concise, cold-readable updates with progress numbers
- **Code practices**: HTTP-first extraction, SQLite persistence, minimal abstractions, surgical changes
- **UI conventions**: Dark theme for ops pages, light theme for user-facing, TailwindCSS via CDN
- **Documentation standards**: Always write docs, concise and factual, technical with code examples
- **Error recovery**: Skip logic, caching, idempotent re-runs, monitor background processes
- **Git workflow**: Clear commit messages, no force push, stage specific files, check for sensitive data
- **Testing approach**: Run things, test things, fix things

## Installation

Place this file at `~/.claude/CLAUDE.md` to apply these preferences globally across all Claude interactions.

## Usage

Once installed, Claude will automatically reference these preferences when making decisions about:
- How to approach tasks
- When to ask for confirmation vs. proceeding directly
- Communication style and verbosity
- Code architecture and implementation choices
- Documentation and testing practices

## Customization

Edit `CLAUDE.md` directly to modify preferences. Changes take effect immediately in new conversations.
