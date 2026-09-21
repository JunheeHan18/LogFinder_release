# LogFinder 2.7.0.0

## Highlights

- Completed the Analyze window migration to WPF (viewer, highlight groups, compressed view, find, extract, merge, scrap); printing keeps the original GDI+ implementation
- New Log Management panel: rule-based archiving and deletion with a guard, a preview plan, verification before delete, and a saved report
- New Timeline tab: merges several logs in timestamp order, marks silent gaps, and detects timestamp formats automatically
- New Duplicate Finder: detects repeated lines with configurable normalization of the parts that vary
- New document tabs: open a whole log from the result list, reorder tabs by dragging, auto-refresh while monitoring
- New analysis panel in the main window, sharing the same control as the separate Analyze window
- Rewritten user manual (Korean and English), shipped with the package and opened by Help

## Improvements

- Navigator (folder tree) opens in about 3.5 seconds instead of about 60 on large trees, without caching, so disk changes are still reflected
- Search results can be sent straight to the Timeline tab, and the navigator can add a whole folder
- Log files can now be filtered by their content keywords when archiving or deleting

## Fixes

- A subfolder without read permission no longer aborts the whole search
- Matched lines are now capped per file (50,000 by default) and the tab header states when the cap was hit
- Multi Keyword and Match Case are now remembered between runs
- CP949 (Korean ANSI) logs are no longer garbled; search, viewer, timeline and duplicate finder share one encoding decision
- Recycle Bin deletion refuses paths that have no Recycle Bin instead of letting the shell delete permanently
- Archive name collisions between groups are refused before anything is deleted
- Help now finds the manual next to the executable, so it works on installed copies

## Package

- `LogFinder_v2.7.0.0.zip`
- Requires the .NET 8 Desktop Runtime (x64)
- Unpack and run `LogFinder.exe`; keep the `docs` folder next to it so Help can show the manual
