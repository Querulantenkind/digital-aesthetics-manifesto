# Terminal Interface Designs: Pattern Analysis

## Introduction

This document analyzes recurring design patterns in exceptional terminal interfaces, examining what makes them intuitive, efficient, and beautiful.

---

## Layout Patterns

### 1. Single-Pane Focus

```
┌────────────────────────────────┐
│                                │
│         MAIN CONTENT           │
│                                │
│                                │
│                                │
│                                │
├────────────────────────────────┤
│ Status bar                     │
└────────────────────────────────┘
```

**Examples:** vim, htop (process view), less

**Characteristics:**
- One primary content area
- Status/command bar at bottom
- Minimal distraction
- Maximum space for content

**When to use:**
- Reading/editing single file
- Viewing single data stream
- Focus is paramount

**Strengths:**
- Simple, clear
- Easy to implement
- Fast rendering

**Weaknesses:**
- No context from other files/views
- Switching views requires navigation

---

### 2. Two-Pane Split

```
┌──────────────┬────────────────┐
│              │                │
│    LEFT      │     RIGHT      │
│    PANE      │     PANE       │
│              │                │
│              │                │
│              │                │
├──────────────┴────────────────┤
│ Status                        │
└───────────────────────────────┘
```

**Examples:** ranger (directories), lazygit (files/diff), tmux splits

**Characteristics:**
- Two parallel views
- Often context + detail
- Can be vertical or horizontal split
- Adjustable split ratio

**Common uses:**
- **Left:** List of items
- **Right:** Detail/preview of selected item
- **Top:** Source code
- **Bottom:** Terminal output

**Strengths:**
- Context maintained
- Compare two things side-by-side
- Natural information flow

**Weaknesses:**
- Less space for each pane
- Can feel cramped on narrow terminals

**Implementation note:**
Use box-drawing characters for clean separator: `│` (vertical) or `─` (horizontal)

---

### 3. Three-Pane "Miller Columns"

```
┌──────┬──────┬──────────────┐
│      │      │              │
│ L1   │ L2   │  PREVIEW     │
│      │      │              │
│      │      │              │
├──────┴──────┴──────────────┤
│ Status                     │
└────────────────────────────┘
```

**Examples:** ranger, macOS Finder (in column view), some mail clients

**Characteristics:**
- **Left:** Parent directory / category
- **Center:** Current selection's contents
- **Right:** Preview of selected item
- Shows hierarchy and context

**When to use:**
- File management
- Hierarchical data (folders, org charts, categories)
- Need for context at multiple levels

**Strengths:**
- Excellent for navigation
- Shows where you are in hierarchy
- Immediate preview

**Weaknesses:**
- Requires wider terminal (80+ cols minimum)
- Complex to implement
- Lot of information to track

---

### 4. Dashboard / Multi-Widget

```
┌─ Widget 1 ─┬─ Widget 2 ───┐
│            │              │
│            │              │
├────────────┼──────────────┤
│ Widget 3   │  Widget 4    │
│            │              │
└────────────┴──────────────┘
```

**Examples:** btop, gotop, system monitors, kubernetes dashboards

**Characteristics:**
- Multiple independent information panels
- Often updated in real-time
- Grid-based layout
- Each widget self-contained

**Common widgets:**
- CPU graph
- Memory usage
- Network traffic
- Process list
- Disk I/O

**Strengths:**
- Overview at a glance
- Efficient use of screen space
- Customizable layouts

**Weaknesses:**
- Overwhelming if poorly organized
- Real-time updates can be CPU-intensive
- Hard to focus on one metric

**Design tips:**
- Use borders to separate clearly
- Consistent widget styling
- Allow hiding/showing widgets
- Consider adaptive layout (reflow on resize)

---

### 5. List + Detail (Master-Detail)

```
┌─ List ───────────────────┐
│ Item 1                   │
│ Item 2 ◄──selected       │
│ Item 3                   │
│ Item 4                   │
│ ...                      │
├──────────────────────────┤
│ ╔═ Details of Item 2 ═══╗│
│ ║ Name: Item 2          ║│
│ ║ Date: 2023-11-20      ║│
│ ║ Size: 1.2 MB          ║│
│ ║ Status: Active        ║│
│ ╚═══════════════════════╝│
└──────────────────────────┘
```

**Examples:** Email clients, RSS readers, issue trackers

**Characteristics:**
- Top: List of items (emails, articles, tasks)
- Bottom: Full details of selected item
- Vertical split common (list on top)

**Variation: Horizontal split**
```
┌─ List ─┬─ Detail ──────────┐
│ Item 1 │                   │
│ Item 2 │  Details of       │
│ Item 3 │  selected item    │
└────────┴───────────────────┘
```

**Strengths:**
- Natural reading flow
- Good for text-heavy content
- Familiar pattern (most email clients use this)

**Weaknesses:**
- Detail pane can dominate
- Switching items requires re-rendering large pane

---

### 6. Tabbed Interface

```
┌─[ Tab 1 ]─[ Tab 2 ]─[ Tab 3 ]────┐
│                                   │
│         Content of Tab 1          │
│                                   │
│                                   │
├───────────────────────────────────┤
│ Status                            │
└───────────────────────────────────┘
```

**Examples:** tmux (windows), screen, vim (buffers with tabline), browsers

**Characteristics:**
- Multiple views in same space
- Switch between tabs
- Only one visible at a time

**Visual styles:**

**Style A: Top tabs**
```
 Tab1 │ Tab2 │ Tab3 
──────┴──────┴──────────
```

**Style B: Numbered**
```
[1:main] [2:logs] [3:debug]
─────────────────────────────
```

**Strengths:**
- Many views in limited space
- Familiar UI pattern
- Easy switching (often Ctrl+number)

**Weaknesses:**
- Can't see multiple tabs simultaneously
- Tab bar takes vertical space

---

### 7. Floating Windows / Overlays

```
┌────────────────────────────┐
│                            │
│  Main content...           │
│       ┌────────────┐       │
│       │  Dialog    │       │
│       │  box       │       │
│       └────────────┘       │
│                            │
└────────────────────────────┘
```

**Examples:** Dialog boxes, modal prompts, pop-up help

**Characteristics:**
- Temporary overlay
- Blocks main interface (modal)
- Often centered
- Draws focus

**Common uses:**
- Confirmation dialogs ("Are you sure?")
- Input prompts ("Enter filename:")
- Error messages
- Help screens

**Implementation:**
- Save screen content beneath
- Draw dialog on top
- Restore on close

**Best practices:**
- Make dismissal obvious (show "OK" / "Cancel")
- Use border for clear boundary
- Shadow effect (if terminal supports) for depth

---

## Navigation Patterns

### 8. Vim-Style Keybindings

```
h - left    j - down    k - up    l - right
gg - top    G - bottom  / - search
dd - delete yy - yank   p - paste
```

**Used by:** vim, ranger, tig, less, man pages, many TUIs

**Rationale:**
- Home row efficiency
- No arrow key reaching
- Modal editing (normal/insert modes)
- Powerful composability (d2w = delete 2 words)

**Adaptation in TUIs:**
- Often without modes (always in "normal" mode)
- `hjkl` for navigation
- `/` for search
- `?` for help
- `q` to quit

**Benefit:** Consistency across tools for users familiar with vim

---

### 9. Arrow Keys + Mnemonics

```
↑↓←→  - navigate
Enter - select/open
Space - toggle/mark
d - delete
r - rename
q - quit
? - help
```

**Used by:** nnn, midnight commander, many file managers

**Rationale:**
- Arrow keys intuitive for new users
- Letter keys as mnemonics (d=delete, r=rename)
- No mode confusion

**Best practices:**
- Single-letter commands (fast)
- Consistent across views
- Show available commands at bottom

---

### 10. Tab Completion

```
$ cd /usr/lo[TAB]
$ cd /usr/local/

$ git che[TAB]
checkout  cherry    cherry-pick

$ SELECT * FROM us[TAB]
users  user_sessions  user_preferences
```

**Essential for:**
- Shell commands
- File paths
- SQL clients (pgcli, mycli)
- Any command-line interface

**Variations:**
- **Single match:** Auto-complete immediately
- **Multiple matches:** Show list, complete common prefix
- **Cycle through:** Press Tab repeatedly to cycle

**Advanced:** Context-aware completion (knows Git branches, database tables, etc.)

---

## Information Display Patterns

### 11. Progress Indicators

**A. Linear Progress Bar**
```
[████████████░░░░░░░░░░░] 60%
```

**B. Spinner (Indeterminate)**
```
⠋ Loading...
⠙ Loading...
⠹ Loading...
⠸ Loading...
```

**C. Percentage Only**
```
Progress: 60%
```

**D. With Details**
```
[████████████░░░░░░░░░░░] 60%  (6/10 files)
Estimated time: 2m 15s remaining
```

**When to use:**
- **Bar:** Known total (downloading file, processing list)
- **Spinner:** Unknown duration (waiting for server)
- **Percentage:** Space-constrained

**Implementation tips:**
- Update smoothly (not every millisecond)
- Show ETA when possible
- Allow cancellation (show Ctrl+C message)

---

### 12. Real-Time Graphs

**A. Sparklines (Compact)**
```
CPU: ▁▂▃▅▆▇█▇▆▅▃▂▁ 45%
```

**B. Multi-Line ASCII Graph**
```
100% ┤     ╭─╮
 75% ┤   ╭─╯ ╰╮
 50% ┤ ╭─╯    ╰─╮
 25% ┤─╯        ╰──
  0% ┴──────────────
```

**C. Bar Chart**
```
Mon ████████████ 78%
Tue ████████████████ 95%
Wed █████████ 62%
Thu ██████████████ 85%
```

**Use cases:**
- System monitoring (CPU, memory, network)
- Time series data
- Comparing values

**Implementation:**
- Unicode box-drawing for smooth lines: `─│┌┐└┘├┤┬┴┼`
- Block elements for bars: `█▓▒░`
- Braille characters for high-resolution: `⠁⠂⠃⠄⠅⠆⠇⠈`

---

### 13. Color-Coding for State

**Common mappings:**
```
🟢 Green   - Success, normal, good
🟡 Yellow  - Warning, moderate, attention
🔴 Red     - Error, critical, danger
🔵 Blue    - Information, neutral
⚪ Gray    - Disabled, inactive, secondary
```

**Examples:**

**A. Process states**
```
✓ nginx     Running   [green]
⚠ database  Warning   [yellow]
✗ redis     Stopped   [red]
```

**B. Git diff**
```
+ added line      [green]
- removed line    [red]
  unchanged line  [white]
```

**C. Test results**
```
✓ test_login      PASS [green]
✓ test_signup     PASS [green]
✗ test_payment    FAIL [red]
```

**Accessibility:**
- Don't rely on color alone (use symbols: ✓✗⚠)
- Provide monochrome mode
- Test in different color schemes

---

### 14. Tables and Lists

**A. Simple List**
```
- Item 1
- Item 2
- Item 3
```

**B. Aligned Table**
```
ID    Name         Size    Date
---   ----------   -----   ----------
1     document.txt 12 KB   2023-11-20
2     photo.jpg    2.1 MB  2023-11-19
3     script.sh    1.8 KB  2023-11-18
```

**C. Box-Drawing Table**
```
┌────┬─────────────┬───────┬────────────┐
│ ID │ Name        │ Size  │ Date       │
├────┼─────────────┼───────┼────────────┤
│ 1  │ document.txt│ 12 KB │ 2023-11-20 │
│ 2  │ photo.jpg   │ 2.1 MB│ 2023-11-19 │
│ 3  │ script.sh   │ 1.8 KB│ 2023-11-18 │
└────┴─────────────┴───────┴────────────┘
```

**D. Compact Tree**
```
project/
├── src/
│   ├── main.py
│   └── utils.py
├── tests/
│   └── test_main.py
└── README.md
```

**When to use:**
- **Simple list:** Minimal info, fast rendering
- **Aligned table:** Multiple columns, need clarity
- **Box-drawing:** Formal, dense data, clear separation
- **Tree:** Hierarchical relationships

**Box-drawing characters:**
- `─ │` - lines
- `┌ ┐ └ ┘` - corners
- `├ ┤ ┬ ┴ ┼` - intersections

---

## Interaction Patterns

### 15. Command Palette / Fuzzy Finder

```
> Type to search...
┌─────────────────────────────┐
│ ● File: Open Recent         │
│   File: Save All            │
│   Edit: Find and Replace    │
│   Git: Commit               │
│   Help: Show Keybindings    │
└─────────────────────────────┘
```

**Examples:** fzf, telescope (neovim), VS Code command palette

**Characteristics:**
- Type to filter
- Fuzzy matching (typos OK)
- Shows all available commands
- Keyboard-driven selection

**Benefits:**
- Discoverability (see all options)
- Fast for power users
- No need to memorize all keybindings

---

### 16. Context Menus / Quick Actions

```
┌─ Actions ───────────┐
│ ● Open              │
│   Edit              │
│   Delete            │
│   Rename            │
│   Properties        │
└─────────────────────┘
```

**Triggered by:** Right-click (if mouse support), or key (e.g., `m` for menu)

**Design tips:**
- Show current selection context
- Most common actions first
- Keyboard shortcuts shown beside options
- Quick dismiss (Esc or click outside)

---

### 17. Inline Editing

```
Before:
  Name: Alice

After (editing):
  Name: [Alice_] ← cursor here
```

**Examples:** Spreadsheets (visidata), form fills, config editors

**Pattern:**
- Press Enter/e to edit
- Inline text input (replaces cell)
- Enter to confirm, Esc to cancel
- Show cursor clearly

**Benefits:**
- No separate edit dialog
- Context visible
- Fast iteration

---

## Status and Feedback Patterns

### 18. Multi-Level Status Bar

```
┌─────────────────────────────────────────┐
│ Main content area                       │
│                                         │
├─────────────────────────────────────────┤
│ MODE    file.txt [+] 23:45  utf-8  45% │ ← Primary status
├─────────────────────────────────────────┤
│ ℹ Saved successfully                    │ ← Notification area
└─────────────────────────────────────────┘
```

**Layers:**
1. **Persistent status:** Always visible (mode, file, position)
2. **Notifications:** Temporary messages (confirmations, errors)
3. **Command line:** User input area

**Example from vim:**
```
NORMAL  main.py [+]  45,12  65%      ← status line
-- INSERT --                          ← mode line
:wq                                   ← command line
```

---

### 19. Toast Notifications (Transient Messages)

```
┌─────────────────────────────────────┐
│ Main interface                      │
│                                     │
│         ┌─ Success! ─────┐          │
│         │ File saved     │          │
│         └────────────────┘          │
│             ↑ auto-dismiss after 3s │
└─────────────────────────────────────┘
```

**Characteristics:**
- Appears temporarily
- Auto-dismisses
- Non-blocking
- Often positioned bottom-right or top-center

**Use for:**
- Success confirmations ("Saved")
- Non-critical errors ("Connection slow")
- Background task completion ("Build finished")

---

### 20. Help Overlay

```
┌─ Keybindings ──────────────────────┐
│ j/k     - navigate up/down         │
│ Enter   - open                     │
│ d       - delete                   │
│ r       - rename                   │
│ /       - search                   │
│ ?       - show this help           │
│ q       - quit                     │
│                                    │
│ Press any key to dismiss           │
└────────────────────────────────────┘
```

**Triggered by:** `?` or F1

**Best practices:**
- Show context-sensitive help (changes per view)
- Alphabetical or grouped by function
- Include examples if space permits
- Easy to dismiss

---

## Responsive Design

### 21. Adaptive Layout (Terminal Width)

**Wide terminal (120+ cols):**
```
┌──────────┬─────────────────┬──────────┐
│  Tree    │   Editor        │ Preview  │
└──────────┴─────────────────┴──────────┘
```

**Narrow terminal (80 cols):**
```
┌───────────────────────────────────────┐
│   Editor                              │
├───────────────────────────────────────┤
│ Status: file.txt                      │
└───────────────────────────────────────┘
```

**Very narrow (< 80 cols):**
```
┌─────────────────┐
│ E d i t o r     │
│ (compacted)     │
└─────────────────┘
```

**Techniques:**
- Hide optional panes
- Stack layouts vertically instead of horizontally
- Abbreviate text
- Graceful degradation

---

### 22. Overflow Handling

**A. Truncation**
```
This is a very long line that gets cu...
```

**B. Wrap**
```
This is a very long line
that wraps to next line
```

**C. Scroll indicator**
```
│ Visible content here                   ↓│
```

**D. Horizontal scrolling**
```
←This is a very long line that you can s→
```

**Choose based on:**
- **Truncate:** Single-line items (file names)
- **Wrap:** Prose, paragraphs, logs
- **Scroll:** User needs to see all (code, data tables)

---

## Animation and Transitions

### 23. Smooth Updates (Not Flickering)

**Bad:**
```
Clearing screen...
Redrawing everything...
(flicker, flicker)
```

**Good:**
```
Update only changed cells
Use double-buffering
```

**Techniques:**
- ANSI cursor positioning (`\033[row;colH`)
- Update specific cells, not full screen
- Use libraries: ncurses, termion, tui-rs

---

### 24. Loading States

**Skeleton screens:**
```
┌────────────────────────────┐
│ ░░░░░░░░░░░░░░░░░░░░░░░░░ │ ← placeholder
│ ░░░░░░░░░░░░░░░░           │
│                            │
│ ░░░░░░░░░░░░░░░░░░░░░░░░░ │
└────────────────────────────┘
```

**Advantages:**
- Shows structure before content loads
- Reduces perceived wait time
- Calmer than spinners

---

## Accessibility Patterns

### 25. Screen Reader Support

**Semantic structure:**
- Use ARIA-like labels (conceptually)
- Logical reading order
- Describe UI elements clearly

**Example:**
```
Status: 3 files selected
Available actions: Open (o), Delete (d), Rename (r)
```

---

### 26. Keyboard-Only Navigation

**Requirements:**
- Every action accessible via keyboard
- Tab/Shift+Tab for focus movement
- Arrow keys for list navigation
- Shortcut keys for common actions
- Consistent across application

**Visual focus indicators:**
```
[ Item 1 ]   ← not focused
【Item 2】   ← focused (bold brackets)
[ Item 3 ]
```

---

## Design Principles Summary

### The "terminal interface design commandments":

1. **Clarity first** - User should never wonder what state they're in
2. **Feedback always** - Confirm every action
3. **Consistency** - Similar things work similarly
4. **Discoverability** - Help accessible, shortcuts visible
5. **Efficiency** - Minimize keystrokes for common tasks
6. **Respect the medium** - Work with terminal constraints
7. **Accessibility** - Keyboard-only, screen-reader friendly
8. **Responsiveness** - Adapt to terminal size
9. **Performance** - Fast updates, no lag
10. **Beauty** - Clean, organized, pleasant to use

---

## Anti-Patterns (What NOT to Do)

### ❌ Poor Patterns:

1. **Mystery meat navigation** - No indication what keys do what
2. **Full-screen redraws** - Causes flicker
3. **Color dependency** - Meaning only conveyed by color
4. **Fixed layouts** - Breaks in small terminals
5. **Modal hell** - Too many nested dialogs
6. **Inconsistent keybindings** - `q` quits sometimes, not always
7. **No confirmation for destructive actions** - Delete without "are you sure?"
8. **Ignoring terminal capabilities** - Assuming 256 colors available

---

## Further Reading

**In this repository:**
- `/galleries/terminal-interfaces/COLLECTION.md` - Examples of excellent TUIs
- `/galleries/terminal-interfaces/interaction-models.md` - User interaction deep-dive
- `/toolkits/terminal-design-toolkit.md` - Practical guide to building TUIs

**External resources:**
- The TTY demystified (blog series on terminal internals)
- ncurses documentation
- tui-rs (Rust), blessed (Python), termion (Rust) libraries

---

**Study the best interfaces. Steal shamelessly. Improve iteratively.**

---

**License:** CC-BY-SA 4.0 International  
**Author:** Digital Aesthetics Manifesto Contributors  
**Date:** November 19, 2025
