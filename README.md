# SkippyMemory

This directory is intended to live as its own git repository, separate from the main `SkippyBot` repo.

Expected remote:
- Repository name: `SkippyMemory`
- Visibility: `private`

Notes:
- The parent repository already ignores `data/memory/`, so this nested repo stays isolated.
- `channelssetup.md` and the operational `data/` subtree belong in this repo together.
- Runtime startup pulls the latest repo state before memory-backed services start, and runtime shutdown commits and pushes the final state as its last sync step.
