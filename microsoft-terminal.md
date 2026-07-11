# Windows Terminal
Windows Terminal is Microsoft's open-source terminal application for Windows, unifying the modern Windows Terminal and the legacy Windows console host into a single application.<br>
It supports multiple shells (PowerShell, cmd, WSL) with tabbed and paned layouts, and renders text through a GPU-accelerated pipeline built around `ControlCore` and `TerminalCore`. The project is a large-scale C++/WinRT codebase with strict contribution standards; all merges require maintainer review approval and passing CI checks across the Azure Pipelines suite.

<a href="https://github.com/microsoft/terminal">Github Repo</a>

## My Contributions
* <a href="https://github.com/microsoft/terminal/pull/20239">PR 20239</a> | <a href="https://github.com/microsoft/terminal/issues/20219">Issue 20219</a> *(superseded — see note)*:  Fixed a stale hyperlink hover-state bug where `_updateHoveredCell`'s early-return guard skipped re-querying the buffer after mouse-wheel scrolling shifted the viewport under a stationary cursor, leaving the hover underline stuck on a hyperlink that had scrolled away. Fix cleared the cached hovered cell (`ClearHoveredCell`) immediately after `UpdateScrollbar` to force re-evaluation against the actual buffer cell.
  * **Note:** Superseded by maintainer <a href="https://github.com/carlos-zamora">@carlos-zamora</a>'s own implementation, <a href="https://github.com/microsoft/terminal/pull/20357">PR 20357</a> (merged), which was explicitly based on this PR and closes the same issue.
