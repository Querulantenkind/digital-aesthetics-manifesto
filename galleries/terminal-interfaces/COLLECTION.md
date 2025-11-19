# Terminal Interfaces: Collection

## Introduction

This collection showcases exceptional terminal user interfaces (TUIs)—applications that demonstrate beauty, clarity, and thoughtful design within the constraints of text-based interaction.

---

## System Monitoring

### 1. htop (Interactive Process Viewer)

```
  1  [||||||||||||||||||||                 52.3%]
  2  [|||||||||||||                         38.7%]
  3  [|||||||||||||||||||||||               65.1%]
  4  [||||||||||||||                        40.2%]
  Mem[||||||||||||||||||||||||         7.2G/16.0G]
  Swp[||                               512M/4.00G]

  PID USER      PRI  NI  VIRT   RES S CPU% MEM%   TIME+  Command
 1234 user       20   0 2847M  892M S  3.0  5.5  0:45.23 firefox
 5678 user       20   0 1024M  256M S  1.3  1.6  0:12.45 code
```

**Design elements:**
- Color-coded CPU bars (green → yellow → red)
- Hierarchical process tree view
- Real-time updates
- Keyboard-driven navigation
- Clear typography with alignment

**Why it's excellent:**
- Dense information, high clarity
- Color enhances understanding without overwhelming
- Intuitive keybindings (F-keys at bottom)

---

### 2. btop (Modern Resource Monitor)

```
╭─ CPU ────────────────────────────────────────╮
│ Core 1 ▁▂▃▅▆▇█████▇▆▅▃▂▁     87%  3.6 GHz  │
│ Core 2 ▁▁▂▃▄▅▆▇████▇▆▅▄▃▂▁   65%  3.4 GHz  │
│ Core 3 ▁▂▃▄▅▇███████▇▅▄▃▂▁   72%  3.5 GHz  │
│ Core 4 ▁▁▁▂▃▄▅▆▇███▇▆▅▄▃▂   58%  3.3 GHz  │
├─ Memory ─────────────────────────────────────┤
│ ████████████████░░░░░░░░  12.4/32.0 GB     │
├─ Network ─────────────────────────────────────┤
│ ↓ 2.4 MB/s  ▁▂▃▅▇█████▇▅▃▂▁                │
│ ↑ 0.8 MB/s  ▁▁▂▃▄▅▆▆▆▅▄▃▂▁                 │
╰───────────────────────────────────────────────╯
```

**Design elements:**
- Box-drawing characters for clean borders
- Sparkline graphs showing history
- Gradient color schemes
- Responsive layout
- Mouse support (optional)

**Innovations:**
- Modern aesthetic (vs. traditional terminal look)
- Smooth animations
- GPU monitoring support

---

### 3. gotop (Minimalist Alternative)

```
CPU  ███████████████░░░░░░░  75%
MEM  ████████░░░░░░░░░░░░░░  32%
DISK ████░░░░░░░░░░░░░░░░░░  18%
NET  ↓1.2M ↑450K

PROCS: 245  RUNNING: 3  THREADS: 1023
```

**Design philosophy:**
- Extreme minimalism
- Single-screen overview
- No scrolling needed
- Clear hierarchy

---

## File Managers

### 4. ranger (Vim-Inspired File Manager)

```
┌──────────────┬──────────────┬──────────────────────┐
│ Documents    │ projects/    │ main.py             │
│ Downloads    │ notes/       │   def hello():      │
│ Pictures     │ scripts/     │       print("Hi")   │
│ Videos       │ data.csv     │                      │
│ Music        │ README.md    │ Python script        │
│ projects/ ► │ todo.txt     │ Modified: 2h ago     │
└──────────────┴──────────────┴──────────────────────┘
        ← → navigate    d: delete    r: rename
```

**Design elements:**
- Three-column "Miller columns" view
- Left: parent directory
- Center: current directory
- Right: preview of selected file
- Vim keybindings
- Syntax-highlighted previews

**Why it's excellent:**
- Context at a glance
- Keyboard-driven efficiency
- Image previews (in supporting terminals)

---

### 5. nnn (Minimal File Manager)

```
~/projects ────────────────────────────── 23 items ─
 drwxr-xr-x  luca    4.0K  website/
 drwxr-xr-x  luca    4.0K  scripts/
 -rw-r--r--  luca   15.2K  notes.md
 -rw-r--r--  luca    2.1M  data.csv
 -rwxr-xr-x  luca    1.4K  backup.sh

─────────────────────────────────────────────────────
 6.2M/512G used  ·  23 items  ·  5 selected
```

**Design philosophy:**
- Brutalist minimalism
- Single-pane focus
- Blazing fast (written in C)
- Minimal dependencies
- Customizable via plugins

---

### 6. lf (List Files - Go Implementation)

```
┌─ /home/user/documents ───────────────────────────┐
│                                                   │
│  📁 archive/          2023-01-15                  │
│  📁 work/             2023-11-20                  │
│  📄 resume.pdf        124 KB                      │
│  📄 notes.txt         8.2 KB                      │
│  📷 photo.jpg         2.1 MB                      │
│                                                   │
├───────────────────────────────────────────────────┤
│ 5 items · 2.3 MB · pdf,txt,jpg                   │
└───────────────────────────────────────────────────┘
```

**Features:**
- Configurable layout
- Preview scripts
- Custom commands
- Server/client architecture

---

## Text Editors

### 7. vim/neovim (With Statusline)

```
┌─ main.py ────────────────────────────────────────┐
│ 1  def calculate_total(items):                   │
│ 2      total = 0                                  │
│ 3      for item in items:                         │
│ 4 ●        total += item.price                    │
│ 5      return total                               │
│ 6                                                  │
│~                                                   │
│~                                                   │
└───────────────────────────────────────────────────┘
 NORMAL  main.py [+]  4:12  utf-8  python  65%
```

**Design elements:**
- Mode indicator (color-coded)
- File status
- Cursor position
- Encoding and filetype
- Scroll percentage
- Optional: Git branch, linter status, LSP info

**Customization:** Statusline plugins (vim-airline, lualine)

---

### 8. helix (Modern Modal Editor)

```
┌─ config.toml ──────────────────── main ─────────┐
│   1 [general]                                     │
│   2 theme = "gruvbox"                             │
│ >  3 line-number = "relative"                     │
│   4                                               │
│   5 [editor]                                      │
│   6 mouse = true                                  │
│~                                                   │
└───────────────────────────────────────────────────┘
 NOR  config.toml  3 sel  3:1  utf8  toml  main
```

**Innovations:**
- Selection-first editing (vs. Vim's motion-first)
- Built-in LSP
- Tree-sitter syntax highlighting
- Modern defaults

---

### 9. micro (User-Friendly Terminal Editor)

```
┌─ notes.md ────────────────────────────────────┐
│ # Meeting Notes                                │
│                                                 │
│ - [x] Review proposal                           │
│ - [ ] Schedule follow-up                        │
│ - [ ] Send summary email                        │
│                                                 │
│                                                 │
├─────────────────────────────────────────────────┤
│ ^S Save  ^Q Quit  ^F Find  ^Z Undo  ^Y Redo   │
└─────────────────────────────────────────────────┘
```

**Philosophy:**
- Familiar keybindings (Ctrl+S, Ctrl+C, Ctrl+V)
- Mouse support by default
- No modal editing
- "What you expect" interface

---

## Git Interfaces

### 10. lazygit (Git TUI)

```
┌─ Files ──────────┬─ Branches ──────────────────────┐
│ ●● main.py      │  * main                          │
│  ● README.md    │    feature/new-ui                │
│    test.py      │    bugfix/login                  │
├──────────────────┴──────────────────────────────────┤
│ ┌─ Unstaged Changes ──────────────────────────┐    │
│ │ + def new_feature():                         │    │
│ │ +     return "Hello"                         │    │
│ │ - # TODO: implement this                     │    │
│ └──────────────────────────────────────────────┘    │
├─────────────────────────────────────────────────────┤
│ <enter> stage  <space> stage line  <c> commit      │
└─────────────────────────────────────────────────────┘
```

**Design elements:**
- Multi-pane layout
- Diff view with syntax highlighting
- Visual branch tree
- Intuitive keybindings
- Real-time updates

**Why it's excellent:**
- Makes Git approachable
- Visual feedback for every action
- Combines simplicity with power

---

### 11. tig (Text-Mode Interface for Git)

```
2023-11-20 15:30 ●─┐ feat: Add new dashboard    (HEAD -> main)
2023-11-19 12:15   │ fix: Resolve login bug
2023-11-18 09:45   ├─┐ Merge branch 'feature'
2023-11-17 16:20   │ │ feat: Implement search
2023-11-17 14:10 ●─┘ │ docs: Update README

────────────────────────────────────────────────────────
commit a1b2c3d4e5f6...
Author: Jane Doe <jane@example.com>
Date: Mon Nov 20 15:30:12 2023

    feat: Add new dashboard
    
    - Created dashboard component
    - Added data fetching
```

**Features:**
- Browse commit history
- View diffs
- Blame view
- Vim-like navigation
- Minimal, focused interface

---

## Communication

### 12. irssi (IRC Client)

```
┌─ #dev-team ──────────────────────────────────────────┐
│ 15:30 <alice> Has anyone seen the new API docs?      │
│ 15:31 <bob> Yeah, they're at /docs/api-v2            │
│ 15:32 <you> Thanks! Looking now                       │
│ 15:33 * charlie has joined #dev-team                  │
│ 15:33 <charlie> Hey everyone                          │
├───────────────────────────────────────────────────────┤
│ [15:34] [3:alice,bob,charlie,you,+5 more]             │
├───────────────────────────────────────────────────────┤
│ [#dev-team] │                                          │
└───────────────────────────────────────────────────────┘
```

**Design elements:**
- Multi-window chat
- Color-coded usernames
- Status indicators
- Highly customizable via themes

---

### 13. weechat (Modern IRC/Chat Client)

```
 ● #general      ┃ 15:45 --> alice joined
 ● #random       ┃ 15:45 <bob> Check out this link
   #dev-team     ┃ 15:46 <alice> Thanks!
   @charlie      ┃ 15:46 <you> Interesting
                 ┃ 15:47 <bob> BTW the meeting is at 4pm
                 ┃
─────────────────╂─────────────────────────────────
                 ┃ 24 users: 5 ops, 19 normal
                 ┃
─────────────────╂─────────────────────────────────
[@bob] │
```

**Features:**
- Multiple protocols (IRC, Matrix, Slack, Discord)
- Plugin system
- Script support (Python, Ruby, Lua)
- Vertical split layout option

---

## Data Viewers

### 14. visidata (Spreadsheet for Terminal)

```
┌─ sales_data.csv ─────────────────────── 3,492 rows ─┐
│ date       │ product    │ quantity │ revenue │ region │
├────────────┼────────────┼──────────┼─────────┼────────┤
│ 2023-01-01 │ Widget A   │ 152      │ $3,040  │ North  │
│ 2023-01-01 │ Gadget B   │ 87       │ $4,350  │ South  │
│ 2023-01-02 │ Widget A   │ 203      │ $4,060  │ East   │
│ 2023-01-02 │ Doohickey  │ 45       │ $1,350  │ West   │
│            │            │          │         │        │
├────────────┴────────────┴──────────┴─────────┴────────┤
│ Sum: 487  │  Total: $12,800  │  Avg: $2,630.43        │
└───────────────────────────────────────────────────────┘
    z: sort  [: filter  F: freq  +: aggregate  g: plot
```

**Design elements:**
- Spreadsheet-like interface
- Sorting, filtering, aggregating
- Plotting capabilities
- Works with CSV, JSON, SQLite, more
- Vim-inspired keybindings

**Why it's revolutionary:**
- Turns terminal into data analysis environment
- No GUI needed for exploratory analysis

---

### 15. fx (JSON Viewer)

```
{
  "users": [
    {
      "id": 1,
      "name": "Alice",
      "email": "alice@example.com",
      "active": true ◄
    },
    {
      "id": 2,
      "name": "Bob",
      "email": "bob@example.com",
      "active": false
    }
  ],
  "total": 2
}

────────────────────────────────────────
.users[0].active → true
```

**Features:**
- Syntax-highlighted JSON
- Interactive navigation
- JS expression evaluation
- Streaming support for large files

---

## Build/Task Runners

### 16. make (With Rich Output)

```
┌─ Building project... ────────────────────────────────┐
│                                                       │
│ [1/5] ✓ Compiling src/main.c                         │
│ [2/5] ✓ Compiling src/utils.c                        │
│ [3/5] ⟳ Compiling src/parser.c...                    │
│ [4/5] ⋯ Linking objects                               │
│ [5/5] ⋯ Creating binary                               │
│                                                       │
│ ████████████░░░░░░░░  60%                            │
│                                                       │
└───────────────────────────────────────────────────────┘
```

**Modern make output with:**
- Progress indicators
- Color-coding (green=success, red=error, yellow=warning)
- Emoji/Unicode symbols
- Progress bar

---

### 17. npm (Enhanced Output)

```
⠹ Installing dependencies...

┌─ Dependencies ────────────────────────────────────┐
│ ✓ react@18.2.0                                    │
│ ✓ react-dom@18.2.0                                │
│ ⟳ @types/react@18.2.45                            │
│   └─⟳ csstype@3.1.3                               │
└───────────────────────────────────────────────────┘

added 1,234 packages in 23s
```

**Design elements:**
- Animated spinner
- Tree structure for dependencies
- Success/error icons
- Summary statistics

---

## Database Clients

### 18. pgcli (PostgreSQL Client)

```
postgres@localhost:mydb> SELECT id, name, email FROM users LIMIT 3;
┌────┬───────────┬──────────────────────┐
│ id │ name      │ email                │
├────┼───────────┼──────────────────────┤
│ 1  │ Alice     │ alice@example.com    │
│ 2  │ Bob       │ bob@example.com      │
│ 3  │ Charlie   │ charlie@example.com  │
└────┴───────────┴──────────────────────┘
3 rows in set (0.05 sec)

postgres@localhost:mydb> _
```

**Features:**
- Syntax highlighting
- Auto-completion
- Multi-line editing
- Pretty tables
- Pagination for large results

---

### 19. mycli (MySQL/MariaDB Client)

```
mysql user@localhost:(none)> SHOW DATABASES;
╒════════════════════════╕
│ Database               │
╞════════════════════════╡
│ information_schema     │
│ mysql                  │
│ performance_schema     │
│ myapp                  │
│ test                   │
╘════════════════════════╛
5 rows in set (0.01 sec)
```

**Similar to pgcli:**
- Modern UX for MySQL
- Smart completion
- Syntax highlighting

---

## Package Managers

### 20. yay (AUR Helper)

```
:: Synchronizing package databases...
 core is up to date
 extra is up to date
 community is up to date

:: Searching AUR...
aur/visual-studio-code-bin 1.85.1-1 [+2314 -15]
    Visual Studio Code (binary from Microsoft)
aur/vscodium-bin 1.85.1-1 [+892 -3]
    Binary releases of VS Code without MS branding/telemetry

Install (1): visual-studio-code-bin

Continue? [Y/n] _
```

**Design philosophy:**
- Clear information hierarchy
- Vote/popularity indicators
- Interactive prompts
- Color-coded status

---

## Network Tools

### 21. gping (Visual Ping)

```
┌─ ping google.com ────────────────────────────────────┐
│                                                       │
│  120ms ┤                                              │
│   90ms ┤       ╭╮  ╭╮                                 │
│   60ms ┤   ╭╮  ││╭╮││  ╭╮                             │
│   30ms ┤ ╭╮││╭╮││││││╭╮││╭╮                           │
│    0ms ┴─┴┴┴┴┴┴┴┴┴┴┴┴┴┴┴┴┴┴──────────────────────────│
│        0s      10s      20s      30s                  │
│                                                       │
│ Min: 15ms  Avg: 42ms  Max: 103ms  Lost: 0/156 (0%)  │
└───────────────────────────────────────────────────────┘
```

**Innovation:** Turning ping into a graph
**Use:** Network monitoring, debugging latency

---

### 22. bandwhich (Bandwidth Monitor)

```
┌─ Current Bandwidth Usage ────────────────────────────┐
│ Process          │ ↓ Download   │ ↑ Upload   │ Total │
├──────────────────┼──────────────┼────────────┼───────┤
│ firefox          │ 2.4 MB/s     │ 450 KB/s   │ 2.8 MB│
│ spotify          │ 320 KB/s     │ 12 KB/s    │ 332 KB│
│ code             │ 180 KB/s     │ 80 KB/s    │ 260 KB│
│ ssh              │ 15 KB/s      │ 8 KB/s     │ 23 KB │
├──────────────────┼──────────────┼────────────┼───────┤
│ Total            │ 2.9 MB/s     │ 550 KB/s   │ 3.4 MB│
└──────────────────────────────────────────────────────┘

Connection: en0 (WiFi)  │  IP: 192.168.1.42
```

**Features:**
- Real-time bandwidth per process
- Network interface breakdown
- DNS resolver info

---

## Entertainment

### 23. cmatrix (Matrix Animation)

```
 ｦ   ｱ ﾂ  ｴ   ｳ  ｷ ｴ  ｱ ﾂ   ｦ
  ｱ ﾂ  ｴ  ｹ ﾂ  ｱ ｹ  ｴ  ｱ ﾂ  ｴ
ﾂ  ｴ  ｹ ﾂ  ｱ ｹ  ｴ   ｱ ﾂ  ｴ  ｹ
 ｴ  ｹ ﾂ  ｱ ｹ  ｴ   ｱ ﾂ  ｴ  ｹ ﾂ
  ｹ ﾂ  ｱ ｹ  ｴ   ｱ ﾂ  ｴ  ｹ ﾂ  ｱ
```

**Classic terminal screensaver** - Pure aesthetic, no function.

---

### 24. asciiquarium (Aquarium Animation)

```
                    o
      o       o  o      ><>
         ><>        o
  o                     o      o
    ><((((°>    o   o       o     
 o        o        ><>   o      o
     o        o      o     ><>
 ___________________________________
```

**ASCII animation with:**
- Swimming fish
- Rising bubbles
- Seaweed swaying
- Pure whimsy

---

## What Makes These Excellent?

### Shared Principles:

1. **Clarity over cleverness** - Information hierarchy is clear
2. **Feedback** - User always knows what's happening
3. **Consistency** - Similar actions work similarly
4. **Discoverability** - Help is accessible, keybindings shown
5. **Respect for the medium** - Works with terminal constraints, not against them

### Design Patterns:

- **Status bars** showing mode/file/position
- **Box-drawing** for clear visual separation
- **Color-coding** for semantic meaning (error=red, success=green)
- **Vim-style keybindings** for power users
- **Real-time updates** without flicker
- **Responsive layouts** adapting to terminal size

---

## Further Exploration

**In this repository:**
- `/galleries/terminal-interfaces/interface-designs.md` - Design pattern analysis
- `/galleries/terminal-interfaces/interaction-models.md` - How users interact

**Try these tools yourself:**
Most are available in package managers (`apt`, `brew`, `pacman`, etc.)

---

**Curation note:** Selected for excellence in UX design, not just functionality. Every interface here teaches something about designing for terminals.

---

**License:** CC-BY-SA 4.0 International  
**Curator:** Digital Aesthetics Manifesto Contributors  
**Date:** November 19, 2025
