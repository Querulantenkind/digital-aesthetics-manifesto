# Terminal Interaction Models: Deep Dive

## Introduction

This document examines how users interact with terminal interfaces at a fundamental level—exploring input methods, feedback mechanisms, and the cognitive models users build when working with TUIs.

---

## Input Models

### 1. Character-by-Character Input

**Raw terminal input:**
```
User types: h e l l o
Terminal receives: 'h' 'e' 'l' 'l' 'o'
```

**Characteristics:**
- Each keystroke is an event
- No buffering (unless explicitly added)
- Immediate response possible

**Use cases:**
- Navigation (arrow keys, hjkl)
- Single-key commands (q to quit, d to delete)
- Games and interactive animations

**Implementation note:**
Requires putting terminal in "raw mode" (vs. canonical/cooked mode)

---

### 2. Line-Buffered Input

**Standard shell behavior:**
```
User types: hello[Enter]
Terminal receives: "hello\n"
```

**Characteristics:**
- Edit before sending (backspace works)
- Submit with Enter
- Familiar to all terminal users

**Use cases:**
- Command-line interfaces
- Forms and text input
- Anything requiring multi-character input

**Benefits:**
- User can correct typos before submission
- Standard readline support (Ctrl+A, Ctrl+E, etc.)

---

### 3. Modal Input (Vim-Style)

**Mode determines key meaning:**

**Normal mode:**
```
j → move down
d → delete command
/ → search command
```

**Insert mode:**
```
j → literal 'j' character
d → literal 'd' character
/ → literal '/' character
```

**Visual mode:**
```
j → extend selection down
d → delete selection
```

**Characteristics:**
- Same keys, different meanings per mode
- Mode indicator crucial (always show current mode)
- Steep learning curve, high efficiency

**Benefits:**
- Powerful command composability (d2w, c$, yap)
- Keep hands on home row
- Extensive functionality without modifier keys

**Challenges:**
- Confusing for beginners
- "How do I exit vim?" meme
- Mode confusion (typing in wrong mode)

**Design tips:**
- **Clear mode indicators** (color-coded, always visible)
- **Easy mode switching** (Esc to normal is standard)
- **Help for confused users** (show "Press Esc to return to normal mode")

---

### 4. Modifier Keys (Ctrl, Alt, Shift)

**Common patterns:**

**Ctrl combinations:**
```
Ctrl+C - Cancel/interrupt
Ctrl+D - End of input/exit
Ctrl+Z - Suspend
Ctrl+S - Save (in editors)
Ctrl+F - Find/search
```

**Alt combinations:**
```
Alt+F - Forward word
Alt+B - Backward word
Alt+D - Delete word
```

**Shift combinations:**
```
Shift+Arrow - Select text
Shift+Tab - Reverse Tab
```

**Benefits:**
- No mode switching needed
- Familiar from GUI applications
- Modifier indicates "special" action

**Challenges:**
- Terminal may not support all combinations
- Some combinations reserved by shell (Ctrl+S traditionally stops output)
- Harder to press (multiple keys)

**Cross-platform issues:**
- Mac uses Cmd instead of Ctrl for some things
- Alt doesn't work in all terminals (sends Escape sequence)

---

### 5. Function Keys (F1-F12)

```
F1  - Help
F2  - Rename
F3  - View
F5  - Refresh
F10 - Quit/Menu
```

**Examples:** Midnight Commander, mcedit, htop

**Benefits:**
- Labeled on keyboard
- Don't conflict with text input
- Can be shown in UI (bottom bar)

**Challenges:**
- May be captured by terminal emulator or OS
- Laptop keyboards often require Fn modifier
- Not all terminals support F13-F24

**Design tip:** Show available F-keys in bottom bar:
```
├────────────────────────────────────────┤
│ F1 Help  F2 Edit  F5 Reload  F10 Quit │
└────────────────────────────────────────┘
```

---

### 6. Mouse Input

**Capabilities:**
- Click to select items
- Drag to select range
- Right-click for context menu
- Scroll wheel

**Support varies:**
- Some terminals support mouse (xterm, iTerm2, Windows Terminal)
- Others don't (older terminals)
- SSH may not forward mouse events

**Implementation:**
Enable with ANSI escape sequences:
```
\033[?1000h   - Enable mouse tracking
\033[?1000l   - Disable mouse tracking
```

**Design decision:** Mouse support should enhance, not replace keyboard navigation

**Best practice:**
```
✓ Support both mouse and keyboard
✓ Mouse is optional enhancement
✗ Don't require mouse (must work without)
```

---

## Feedback Models

### 7. Immediate Visual Feedback

**Principle:** Every action has visible consequence

**Examples:**

**A. Selection highlight**
```
  Item 1
→ Item 2    ← selected (arrow/color/bold)
  Item 3
```

**B. Command echo**
```
You pressed: d
Deleting...
```

**C. State change**
```
[ ] Task 1   →  [x] Task 1
(unchecked)     (checked)
```

**Why critical:**
- User knows action was recognized
- Reduces uncertainty
- Builds confidence

**Timing:** Should be instantaneous (<100ms)

---

### 8. Progressive Disclosure

**Show information as needed, not all at once**

**Example A: File manager**
```
Initial view:
  documents/
  
After selection:
  documents/
  ├─ Size: 24 MB
  ├─ Items: 142 files
  └─ Modified: 2 hours ago
```

**Example B: Error messages**
```
Simple: ✗ Connection failed

Detailed (on request):
✗ Connection failed
  Server: example.com:443
  Error: ETIMEDOUT
  Stack trace: ...
```

**Benefits:**
- Reduces clutter
- Allows deep diving when needed
- Respects user's attention

---

### 9. Undo Indication

**Pattern:** Show what was undone and offer redo

```
Deleted 3 files  [Undo with 'u']
```

**After undo:**
```
Restored 3 files  [Redo with 'Ctrl+R']
```

**Critical for:**
- Destructive actions (delete, overwrite)
- Building user confidence
- Encouraging exploration (safe to experiment)

---

### 10. Error Recovery

**Principle:** Don't just show error—suggest fix

**Bad:**
```
Error: Invalid input
```

**Better:**
```
Error: Invalid date format
Expected: YYYY-MM-DD
Example: 2023-11-20
```

**Best:**
```
Error: Invalid date format "11/20/2023"
Expected: YYYY-MM-DD
Did you mean: 2023-11-20? [Y/n]
```

**Components of good error messages:**
1. **What went wrong** (context)
2. **Why it's wrong** (explanation)
3. **How to fix it** (action)
4. **Example** (if format-related)

---

## Cognitive Models

### 11. Mental Model: Layers and Focus

**User understanding:**
```
┌─ Current focus ────────────────┐
│ I am HERE                      │
│ (this pane, this item)         │
└────────────────────────────────┘
       ↓
┌─ Context layer ────────────────┐
│ Surrounding information        │
│ (other panes, metadata)        │
└────────────────────────────────┘
       ↓
┌─ Background layer ─────────────┐
│ Hidden but accessible          │
│ (other tabs, background tasks) │
└────────────────────────────────┘
```

**Design implication:**
- **Focus** should be obvious (cursor, highlight)
- **Context** should be visible but secondary
- **Background** indicated but not distracting

---

### 12. Mental Model: State Machines

**Users think in states:**

```
Initial → Loading → Success
              ↓
            Error → Retry → Success
```

**Each state needs:**
- Clear indicator (what state am I in?)
- Available actions (what can I do now?)
- Transitions (how do I get to next state?)

**Example: Git workflow in lazygit**

```
State 1: Working directory
Actions: Stage files, view diff, commit
→ Stage files

State 2: Staged changes
Actions: Unstage, commit, view staged diff
→ Commit

State 3: Clean working directory
Actions: Push, pull, view log
```

---

### 13. Mental Model: Hierarchies and Trees

**Users navigate conceptually:**

```
Where am I?
  /home/user/projects/myapp

How did I get here?
  Home → Projects → MyApp

Where can I go?
  Up: Projects
  Down: src/, tests/, README.md
  Sibling: ../otherapp
```

**Design pattern: Breadcrumbs**
```
┌─ /home/user/projects/myapp ───────────┐
│                                        │
│ src/                                   │
│ tests/                                 │
│ README.md                              │
└────────────────────────────────────────┘
```

**Navigation shortcuts:**
- `..` or `-` for parent
- `/` for root
- `~` for home
- `g` for "go to" menu

---

### 14. Mental Model: Spatial Memory

**Users remember locations spatially**

"The CPU graph is top-left"  
"File list is in the middle pane"  
"Status bar is at bottom"

**Design implication:**
- **Consistent layout** (don't move things around)
- **Stable positions** (panes stay in place)
- **Predictable behavior** (same action, same result)

**Bad:** Panels that swap positions based on focus  
**Good:** Panels stay in place, change appearance to show focus

---

## Interaction Patterns in Practice

### 15. Command Composition (Vim-Style)

**Grammar of commands:**

```
[count] [operator] [motion]

Examples:
d2w      = delete 2 words
c$       = change to end of line
y3j      = yank 3 lines down
5dd      = delete 5 lines
```

**Mental model:**
- **Verb + noun** structure
- **Composable** (learn 5 operators × 10 motions = 50 combinations)
- **Repeatable** with `.` command

**Power:** Once learned, incredibly efficient

---

### 16. Context Menus and Quick Actions

**Interaction flow:**

```
1. User on file "document.txt"
2. Press 'm' (menu) or right-click
3. See context-specific options:
   ┌─────────────┐
   │ Open        │
   │ Edit        │
   │ Delete      │
   │ Properties  │
   └─────────────┘
4. Select action
5. Action executed with context
```

**Benefits:**
- Discoverability (see all options)
- Context-aware (only relevant actions)
- Keyboard or mouse

---

### 17. Fuzzy Finding

**Interaction:**

```
User types: "mapy"
↓
Matches: "main.py" (ma-p-y)
         "mapper.py" (ma-p-y)
         "my_app.py" (m-a-py)
```

**Algorithm:** Substring matching with:
- Bonus for word starts
- Bonus for consecutive characters
- Penalty for gaps

**Use cases:**
- File finding
- Command palette
- Switching buffers/tabs
- Any large list

**Why powerful:**
- Fast typing (no need to be precise)
- Fault-tolerant (typos OK)
- Scales to thousands of items

---

### 18. Incremental Search

**Interaction:**

```
Initial: 1000 items visible

User types: "t"
Filter: 200 items starting with 't'

User types: "te"
Filter: 50 items starting with 'te'

User types: "tes"
Filter: 8 items starting with 'tes'

User selects from 8
```

**Benefits:**
- Live feedback (see results as typing)
- Easy correction (backspace to widen)
- Faster than scrolling

---

## Advanced Patterns

### 19. Multi-Selection

**Techniques:**

**A. Range selection**
```
1. Move to first item
2. Press V (visual mode)
3. Move to last item
4. All between selected
```

**B. Toggle selection**
```
1. Move to item, press Space
2. Move to another, press Space
3. Non-contiguous selection
```

**C. Select all / none**
```
Ctrl+A - Select all
Ctrl+D - Deselect all
```

**Actions on multi-selection:**
```
Selected: 5 items
Actions: Delete all, Move all, Copy all
```

---

### 20. Batch Operations with Preview

**Pattern:**

```
Step 1: Select files
┌───────────────────┐
│ ☑ file1.txt       │
│ ☑ file2.txt       │
│ ☐ file3.txt       │
└───────────────────┘

Step 2: Choose action (e.g., delete)

Step 3: Preview consequences
┌─────────────────────────────┐
│ This will delete:           │
│  - file1.txt (1.2 KB)       │
│  - file2.txt (3.4 KB)       │
│                             │
│ Continue? [y/N]             │
└─────────────────────────────┘

Step 4: Confirm or cancel
```

**Why important:**
- Prevents accidents
- User sees exactly what will happen
- Builds trust

---

### 21. Streaming / Infinite Scroll

**For large datasets (logs, search results):**

```
[Item 1]
[Item 2]
[Item 3]
...
[Item 100]
── Loading more... ──
[Item 101] ← loaded as user scrolls
[Item 102]
```

**Implementation:**
- Load initial batch (e.g., 100 items)
- Monitor scroll position
- Load more when near bottom
- Background loading (spinner/indicator)

**Benefits:**
- Fast initial load
- Handles millions of items
- Smooth UX

---

### 22. Macros and Repetition

**Pattern (Vim-inspired):**

```
1. Start recording: qa (record to register 'a')
2. Perform actions: dd (delete line), j (move down)
3. Stop recording: q
4. Replay: @a (execute macro)
5. Repeat: 10@a (execute 10 times)
```

**Use cases:**
- Repetitive editing tasks
- Batch transformations
- User-defined automation

---

## Accessibility in Interaction

### 23. Screen Reader Support

**Describe what's happening:**

```
Bad:
[Item selected]

Good:
"File 'document.txt' selected. 
Size: 12 kilobytes. 
Modified 2 hours ago.
Options: open, edit, delete, rename."
```

**Principles:**
- **Announce state changes**
- **Describe UI structure** (e.g., "Entering file list. 3 items.")
- **Confirm actions** (e.g., "File deleted")

---

### 24. Keyboard Navigation for All

**Every UI element accessible:**

```
Tab       - Next field
Shift+Tab - Previous field
Arrow     - Within lists/menus
Enter     - Activate
Esc       - Cancel/back
Space     - Toggle (checkboxes)
```

**Test:** Can you accomplish every task without a mouse?

---

### 25. Customizable Keybindings

**Allow users to remap:**

```
# config.conf
key.quit = q
key.delete = d
key.rename = r
key.help = ?

# Alternative for Dvorak users:
key.quit = x
key.delete = d
key.rename = l
```

**Benefits:**
- Accessibility (physical limitations)
- Preference (Dvorak, Colemak layouts)
- Conflict resolution (terminal quirks)

---

## Performance and Responsiveness

### 26. Perceived Performance

**User perception:**
- **<100ms:** Instant (feels immediate)
- **100-300ms:** Noticeable but acceptable
- **300-1000ms:** Slight delay (show spinner)
- **>1000ms:** Slow (show progress bar)

**Techniques:**

**A. Optimistic UI**
```
User clicks "Delete"
→ Immediately update UI (remove item)
→ Send delete request in background
→ If fails, restore item + show error
```

**B. Background work**
```
User opens file manager
→ Show cached list immediately
→ Refresh in background
→ Update when new data arrives
```

**C. Lazy loading**
```
User scrolls to folder
→ Load only visible items
→ Load adjacent items (predictive)
→ Unload items far away
```

---

### 27. Debouncing and Throttling

**Debouncing** (wait for pause):
```
User types: h e l l [pause] o
          ↓ Only search after pause
Search: "hello"
```

**Use for:** Search as you type, resize handling

**Throttling** (limit rate):
```
Mouse moves 100 times/sec
          ↓ Only process every 10th event
Update: 10 times/sec
```

**Use for:** Mouse tracking, scroll events

---

## Interaction Anti-Patterns

### ❌ What NOT to Do

**1. Inconsistent keybindings**
```
In view A: 'q' quits
In view B: 'q' does something else
❌ User is confused
```

**2. Hidden functionality**
```
Secret keybinding with no hint
❌ User never discovers feature
```

**3. No feedback**
```
User presses button... nothing visible happens
❌ Did it work? Should I press again?
```

**4. Destructive actions without confirmation**
```
Press 'd', all files deleted permanently
❌ Accidental data loss
```

**5. Modal dialogs within modal dialogs**
```
Dialog opens... another dialog inside... another...
❌ "Dialog hell" - can't remember how to get back
```

**6. Blocking the entire UI**
```
Loading... [entire interface frozen]
❌ User can't do anything else, can't even cancel
```

**7. Assuming terminal capabilities**
```
Requires 256 colors / mouse / unicode
Doesn't work in basic terminal
❌ Breaks for some users
```

---

## Design Principles for Interaction

### The 10 Commandments:

1. **Immediate feedback** - Every action has visible result
2. **Reversible actions** - Undo when possible
3. **Confirm destructive actions** - Ask before deleting
4. **Show available options** - Help is accessible
5. **Consistent keybindings** - Same key, same action
6. **Progressive disclosure** - Details on demand
7. **Good error messages** - Explain + suggest fix
8. **Keyboard-first, mouse-optional** - All features via keyboard
9. **Respect muscle memory** - Stable, predictable layout
10. **Performance** - Feels fast (<100ms response)

---

## Further Reading

**In this repository:**
- `/galleries/terminal-interfaces/COLLECTION.md` - Examples
- `/galleries/terminal-interfaces/interface-designs.md` - Layout patterns
- `/toolkits/terminal-design-toolkit.md` - How to build

**External:**
- Don Norman - "The Design of Everyday Things"
- Jakob Nielsen - Usability heuristics
- Vim documentation - Modal editing philosophy
- ncurses HOWTO - Terminal programming basics

---

**Study how users think. Design for humans, not machines.**

---

**License:** CC-BY-SA 4.0 International  
**Author:** Digital Aesthetics Manifesto Contributors  
**Date:** November 19, 2025
