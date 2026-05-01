# SkippyMemory

This directory is intended to live as its own git repository, separate from the main `SkippyBot` repo.

Expected remote:
- Repository name: `SkippyMemory`
- Visibility: `private`

Notes:
- The parent repository already ignores `data/memory/`, so this nested repo stays isolated.
- `channelssetup.md` and the tracked `data/` subtree belong in this repo together.
- The live application data root is `../data`; startup restores this repo `data/` mirror into the live root, and shutdown mirrors the live root back here before commit/push.
- Runtime startup pulls the latest repo state before memory-backed services start, and runtime shutdown commits and pushes the final state as its last sync step.
