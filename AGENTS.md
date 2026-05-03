# AGENTS.md

## Primary Rule

`AGENTS.md` is managed through the `restacked` MCP workflow and must not be directly authored by an AI in the local repository.

- Do not manually edit `AGENTS.md` as the source of truth.
- When `AGENTS.md` needs to change, propose the update through the `restacked` MCP server.
- After proposing a change, read the latest `AGENTS.md` content from the `restacked` MCP server.
- After reading `AGENTS.md` content from the `restacked` MCP server, check whether a local `AGENTS.md` file exists in the project root. If it does not exist, write a new root-level `AGENTS.md` file using the returned content exactly as provided.
- A local `AGENTS.md` file may be written only with content returned by the `restacked` MCP server.
- If `restacked` content is unavailable, stop rather than inventing or locally patching `AGENTS.md`.

## Purpose

This file defines the default working agreement for agents operating in this repository.
The repository is currently in an early bootstrap state, so agents should optimize for clarity,
small changes, and decisions that keep future structure easy to evolve.

## Operating Principles

- Inspect the current repository state before changing files.
- Prefer small, focused edits over broad speculative refactors.
- Preserve established conventions once they exist.
- Explain assumptions clearly when repository context is missing.
- Leave the tree in a state that another engineer can understand quickly.

## Repository Bootstrap Guidance

- Treat the current repository as intentionally minimal.
- Do not invent complex architecture before there is evidence it is needed.
- When creating new structure, choose names that will still make sense as the project grows.
- Add only the files required to support the immediate task.
- Keep setup and dependency choices explicit in code or documentation.

## Code Changes

- Match the style already present in the file or module you are editing.
- Avoid renaming or moving files unless the task requires it.
- Prefer straightforward implementations over clever abstractions.
- Add comments only where the code would otherwise be non-obvious.
- Do not introduce unrelated cleanup in the same change.

## Validation

- Run the narrowest useful validation for the change you made.
- If tests or build commands do not exist yet, say so explicitly.
- When validation is skipped, document why it was skipped.
- Prefer fast, local verification steps before heavier checks.

## Documentation

- Update documentation when behavior, setup, or developer workflows change.
- Keep instructions concrete and command-oriented.
- If the repository is still being scaffolded, document only what is true today.

## Collaboration

- Surface blockers early when required information is missing.
- Call out tradeoffs when there is more than one reasonable implementation path.
- Do not overwrite or revert user changes unless explicitly asked.
- Keep commit-sized changes cohesive so they are easy to review.