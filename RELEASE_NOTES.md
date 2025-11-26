## Release Notes

### Features
- **Plugin API & Virtual Lines**: Introduced a background process API, demo recording script, and a robust virtual lines system for plugin-driven persistent annotations, including background colors and interleaved transform mode. This enabled a new magit-style git blame plugin with history navigation.
- **Editor Enhancements**: Added a resizable file explorer, search options bar (case-sensitive, whole word, regex), and confirmation prompts for closing modified buffers and quitting.
- **Tooling**: The `bump-version` script was rewritten in Python, now including release note generation.

### Bug Fixes
- **Display & Scrolling**: Resolved issues with mouse scroll, horizontal scrolling, viewport reset on cursor movement, view transform header visibility, and cursor invisibility with ANSI escape codes. Fixed line number display for empty buffers and source lines.
- **Editing & Search**: Corrected auto-dedent behavior, fixed large file save corruption, ensured search highlights update with option toggles, and stabilized suggestions/command palette column widths.
- **Stability**: Addressed tab flicker, improved auto-revert with debounce and scroll preservation, and temporarily ignored several flaky/failing tests to stabilize CI.

### Improvements & Refactoring
- **Architecture**: Major reorganization of source code into a layered architecture (`model`, `app`, `view`, `input`, `services`, `primitives`). Comprehensive documentation was added for Buffer vs View state separation and the Layout Layer architecture. Visual tests were consolidated, and `ARCHITECTURE.md` was simplified.
- **CI/CD**: Switched to `cargo-nextest` for improved test performance, added Linux platform support, and updated GitHub Actions dependencies.