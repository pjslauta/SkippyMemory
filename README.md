# SkippyMem

This directory is intended to live as its own git repository, separate from the main `SkippyBot` repo.

Expected remote:
- Repository name: `SkippyMem`
- Visibility: `private`

Notes:
- The parent repository already ignores `data/memory/`, so this nested repo stays isolated.
- Runtime auth/session/cache material is excluded by this repo's local `.gitignore`.
- Durable memory content such as `channelssetup.md` can be versioned here independently of the main app codebase.
