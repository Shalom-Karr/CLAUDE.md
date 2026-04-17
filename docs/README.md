# Documentation

This directory contains additional context and information for Claude to reference during interactions.

## What to Add Here

Add markdown files containing:

- **Project-specific context**: Technical details, architecture decisions, or implementation notes that Claude should know
- **Domain knowledge**: Industry-specific information, terminology, or business logic
- **Reference materials**: API documentation, data schemas, integration guides
- **Troubleshooting guides**: Common issues and their solutions
- **Historical context**: Why certain decisions were made, deprecated approaches to avoid

## About the Repository Owner

This repository is maintained by Shalom Karr, who works with:

- **Execution style**: Direct, action-oriented, run to completion
- **Code preferences**: Pragmatic solutions, minimal abstractions, SQLite for persistence, HTTP-first data extraction
- **UI preferences**: Dark themes for ops pages (#0f172a bg, #1e293b cards), light themes for user-facing pages, TailwindCSS via CDN
- **Documentation expectations**: Always create docs, concise and factual, technical with code examples
- **Git workflow**: Clear commit messages explaining why, no force pushes, stage specific files
- **Communication style**: Concise, direct, no over-explanation, progress with concrete numbers

See `CLAUDE.md` in the root directory for complete behavioral preferences.

## File Naming

Use descriptive names like:
- `architecture.md` - System architecture overview
- `api-reference.md` - API endpoints and usage
- `deployment.md` - Deployment procedures
- `troubleshooting.md` - Common issues and solutions

## Format

All files should be markdown (`.md`) for consistency and readability.
