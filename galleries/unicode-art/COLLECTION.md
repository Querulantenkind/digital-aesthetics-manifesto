# Unicode Art Collection

## Introduction

**Unicode art** expands beyond the original 95 ASCII characters to use the full Unicode character set—thousands of symbols, shapes, and scripts from writing systems around the world.

Where ASCII art is constrained to letters, numbers, and basic punctuation, Unicode art has access to:
- Box-drawing characters (┌─┐)
- Block elements (█▓▒░)
- Mathematical symbols (∑∫√∞)
- Geometric shapes (●■◆★)
- Arrows (←↑→↓↔)
- Emoji and pictographs
- Scripts from every language

**Note:** Unlike ASCII art, Unicode art requires UTF-8 encoding and may not render consistently across all systems, fonts, and terminals.

---

## Navigation

- **This file (COLLECTION.md)** - Curated gallery of Unicode art
- **symbol-explorations.md** - Deep dives into specific Unicode ranges
- **experimental-works.md** - Pushing boundaries of text-based art

---

## Box-Drawing Art

### 1. Simple Frame

```
┌────────────────┐
│                │
│  Hello, World  │
│                │
└────────────────┘
```

**Characters used:** `┌ ─ ┐ │ └ ┘`  
**Style:** Clean, professional, UI-like  
**Common use:** Frames, menus, terminal interfaces

---

### 2. Double-Line Box

```
╔════════════════╗
║                ║
║   IMPORTANT    ║
║                ║
╚════════════════╝
```

**Characters used:** `╔ ═ ╗ ║ ╚ ╝`  
**Effect:** Heavier, more emphasis  
**Common use:** Highlighting, headers, warnings

---

### 3. Complex Nested Boxes

```
╔═══════════════════════════╗
║ ┌───────────────────────┐ ║
║ │ ╭─────────────────╮   │ ║
║ │ │  Nested Boxes   │   │ ║
║ │ │  Different      │   │ ║
║ │ │  Styles         │   │ ║
║ │ ╰─────────────────╯   │ ║
║ └───────────────────────┘ ║
╚═══════════════════════════╝
```

**Technique:** Mixing light, heavy, rounded styles  
**Effect:** Depth, hierarchy  
**Use:** Complex UI, layered information

---

### 4. Table Layout

```
┌────────┬────────┬────────┐
│  Name  │  Age   │  City  │
├────────┼────────┼────────┤
│  Alice │   30   │  NYC   │
│  Bob   │   25   │  LA    │
│  Carol │   35   │  SF    │
└────────┴────────┴────────┘
```

**Technique:** T-junctions for intersections  
**Use:** Data presentation, documentation, CLI tools

---

### 5. Tree Structure with Box-Drawing

```
project/
├── src/
│   ├── main.rs
│   ├── lib.rs
│   └── utils/
│       ├── parser.rs
│       └── lexer.rs
├── tests/
│   └── integration_test.rs
└── Cargo.toml
```

**Tool:** `tree` command output  
**Characters:** `├ └ │ ─`  
**Use:** File system visualization, hierarchies

---

## Block Elements

### 6. Gradient Bar

```
██████████░░░░░░░░░░
▓▓▓▓▓▓▓▓▓▓▒▒▒▒▒▒▒▒▒▒
```

**Characters:** `█ ▓ ▒ ░` (full, dark, medium, light)  
**Effect:** Shading, progress bars  
**Use:** Visualizations, loading indicators

---

### 7. Pixel Art (Block-based)

```
░░░░██████░░░░
░░██████████░░
░░██░░██░░██░░
░░██████████░░
░░░░██░░██░░░░
░░██░░░░░░██░░
░░████████████
```

**Technique:** Using blocks as pixels  
**Style:** Retro gaming aesthetic  
**Effect:** Chunky, lo-fi

---

### 8. Shading Demo

```
████████████████  100%
███████████▓▓▓▓▓   75%
███████▓▓▓▓▓▒▒▒▒   50%
████▓▓▓▒▒▒▒░░░░░   25%
```

**Characters:** Full → Dark → Medium → Light → Space  
**Use:** Progress indicators, data viz

---

## Geometric Shapes

### 9. Shape Palette

```
Circle:    ●○◉◎⊙
Square:    ■□▪▫◼◻
Diamond:   ◆◇
Triangle:  ▲△▼▽
Star:      ★☆✦✧✯
```

**Use:** Bullets, icons, decorative elements  
**Advantage:** Single-character symbols, clear meaning

---

### 10. Pattern Art

```
●○●○●○●○●○
○●○●○●○●○●
●○●○●○●○●○
○●○●○●○●○●
```

**Style:** Geometric, repetitive  
**Effect:** Texture, background  
**Use:** Decorative borders, fills

---

### 11. Star Field

```
       ✦         ★        ✧
   ★        ✧         ✦       
         ✧      ✦         ★
  ✦          ★        ✧
        ★         ✧        ✦
```

**Characters:** Various star symbols  
**Effect:** Depth through variety  
**Use:** Headers, decorative space themes

---

## Arrows and Connectors

### 12. Flowchart with Unicode Arrows

```
[Start] → [Process 1] → [Decision]
                            ↓
                          [Yes?]
                            ↓
                          [End]
                            ↑
                          [No] ←───┘
```

**Characters:** `→ ↓ ↑ ← ↔ ↕`  
**Advantage:** Clearer direction than ASCII `-->>`  
**Use:** Flowcharts, diagrams, documentation

---

### 13. Network Diagram

```
     ┌────────┐
     │ Server │
     └───┬────┘
         │
    ┌────┼────┐
    │    │    │
    ↓    ↓    ↓
┌───────┐┌───────┐┌───────┐
│Client1││Client2││Client3│
└───────┘└───────┘└───────┘
```

**Mix:** Box-drawing + arrows  
**Effect:** Professional, clear relationships

---

## Mathematical and Scientific

### 14. Mathematical Expression

```
     n
    ═══
    ╲
    ╱   xi² = x₁² + x₂² + ... + xₙ²
    ═══
    i=1
```

**Characters:** Summation symbols, subscripts, superscripts  
**Use:** Mathematical notation, formulas (limited)  
**Note:** True math typesetting better in LaTeX/MathML

---

### 15. Chemical Formula

```
H₂O    Water
CO₂    Carbon Dioxide
C₆H₁₂O₆  Glucose
```

**Characters:** Subscripts (₀₁₂₃₄₅₆₇₈₉)  
**Use:** Chemical formulas, scientific notation

---

## Decorative and Ornamental

### 16. Decorative Border

```
╔══════════════════════════════╗
║ ✦ ═══ Elegant Title ═══ ✦   ║
╚══════════════════════════════╝
```

**Mix:** Box-drawing + ornamental symbols  
**Style:** Formal, decorative  
**Use:** Titles, certificates, formal documents

---

### 17. Bullet Points

```
● Primary point
  ○ Secondary point
    ▪ Tertiary point
      ▫ Further detail

★ Important item
✦ Special note
✓ Completed task
✗ Failed/blocked
```

**Advantage:** Visual hierarchy without words  
**Use:** Lists, task management, documentation

---

### 18. Dividers

```
━━━━━━━━━━━━━━━━━━━━
─────────────────────
═════════════════════
• • • • • • • • • • •
✦ ✧ ✦ ✧ ✦ ✧ ✦ ✧ ✦ ✧
```

**Use:** Section breaks, visual separation  
**Variety:** Different weights and styles

---

## Text Decoration

### 19. Underlines and Overlines

```
Plain text
U̲n̲d̲e̲r̲l̲i̲n̲e̲d̲
O͞v͞e͞r͞l͞i͞n͞e͞d͞
S̶t̶r̶i̶k̶e̶t̶h̶r̶o̶u̶g̶h̶
```

**Technique:** Combining diacritical marks  
**Warning:** Can break in many contexts  
**Use:** Emphasis in Unicode-aware systems

---

### 20. Enclosed Characters

```
Circled:     ⓐⓑⓒ ①②③
Parenthesized: ⑴⑵⑶
Squared:     🄰🄱🄲
```

**Use:** Lists, callouts, special markers  
**Note:** Rendering varies by font

---

## Emoji and Pictographs

### 21. Weather Icons

```
☀️ Sunny
☁️ Cloudy  
🌧️ Rainy
❄️ Snowy
⛈️ Stormy
```

**Note:** Emoji may render as color images, not text  
**Use:** Weather apps, quick status indicators

---

### 22. Status Indicators

```
✅ Completed
❌ Failed
⚠️ Warning
ℹ️ Info
🔄 In progress
⏸️ Paused
```

**Advantage:** Universal recognition  
**Use:** Logs, dashboards, task lists

---

## Mixed Scripts

### 23. Multilingual Art

```
╔═════════════════════════════╗
║  Hello      English         ║
║  こんにちは  Japanese        ║
║  안녕하세요  Korean          ║
║  مرحبا      Arabic          ║
║  Привет     Russian         ║
╚═════════════════════════════╝
```

**Effect:** Global, inclusive  
**Challenge:** Different scripts have different widths  
**Use:** Internationalization, cultural representation

---

## Progress and Data Visualization

### 24. Progress Bars

```
[████████████████░░░░] 80%
[▰▰▰▰▰▰▰▰▰▰▰▰▰▱▱▱▱▱] 72%
▓▓▓▓▓▓▓▓▓▓▒▒▒▒▒▒▒▒▒▒ 50%
```

**Use:** CLI tools, installers, loading screens  
**Advantage:** Clear visual feedback

---

### 25. Bar Chart

```
Sales by Quarter:
Q1 ████████████████ 160
Q2 ████████████ 120
Q3 ████████████████████ 200
Q4 ██████████ 100
```

**Technique:** Repeated block character  
**Use:** Simple data visualization in terminals

---

### 26. Sparklines

```
CPU Usage (last 60s):
▁▂▃▄▅▆▇█▇▆▅▄▃▂▁▁▂▃▄▅
```

**Characters:** Vertical bars of different heights  
**Use:** Inline charts, system monitoring  
**Advantage:** Compact, informative

---

## Combining Techniques

### 27. Dashboard Example

```
╔════════════════════════════╗
║  System Status             ║
╠════════════════════════════╣
║  CPU  ████████░░ 80%       ║
║  RAM  ██████░░░░ 60%       ║
║  DISK ██░░░░░░░░ 20%       ║
║                            ║
║  Status: ✅ All systems go ║
╚════════════════════════════╝
```

**Mix:** Boxes + blocks + emoji  
**Use:** Terminal dashboards, monitoring tools

---

### 28. File Tree with Icons

```
📁 project/
├── 📄 README.md
├── 📁 src/
│   ├── 📄 main.rs
│   └── 📄 lib.rs
└── 📁 tests/
    └── 📄 test.rs
```

**Mix:** Box-drawing + emoji  
**Effect:** More visual, easier to scan  
**Use:** Enhanced file listings

---

## Abstract and Experimental

### 29. Pattern Exploration

```
┼╋┼╋┼╋┼╋┼╋
╋┼╋┼╋┼╋┼╋┼
┼╋┼╋┼╋┼╋┼╋
╋┼╋┼╋┼╋┼╋┼
```

**Style:** Abstract, geometric  
**Effect:** Texture, rhythm  
**Use:** Decorative, backgrounds

---

### 30. Density Gradients

```
█▓▒░  Full to empty
▀▄   Half blocks
◼◻   Filled/hollow
```

**Exploration:** Different ways to show gradients  
**Use:** Shading, transitions

---

## Practical Applications

### 31. Menu Interface

```
┌─────────────────────┐
│   MAIN MENU         │
├─────────────────────┤
│ → Start New Game    │
│   Continue          │
│   Settings          │
│   Exit              │
└─────────────────────┘
```

**Elements:** Box + arrow for selection  
**Use:** Text-based UIs, terminal apps

---

### 32. Loading Animation (frames)

```
Frame 1: ⠋
Frame 2: ⠙
Frame 3: ⠹
Frame 4: ⠸
Frame 5: ⠼
Frame 6: ⠴
Frame 7: ⠦
Frame 8: ⠧
```

**Characters:** Braille patterns  
**Use:** Spinner animations  
**Tool:** Many CLI spinners use these

---

## Technical Considerations

### Character Width

**Problem:** Not all Unicode characters are monospace width.

**Full-width characters (CJK):**
```
Ａ Ｂ Ｃ  (2 cells wide each)
```

**Half-width:**
```
A B C  (1 cell wide each)
```

**Solution:** Test in target terminal, use consistent-width character sets.

---

### Font Support

**Problem:** Not all fonts include all Unicode characters.

**Solution:**
- Use common Unicode ranges (box-drawing, blocks)
- Test in multiple fonts
- Provide fallbacks
- Document font requirements

---

### Terminal Compatibility

**Problem:** Different terminals render Unicode differently.

**Recommendations:**
- Test in: Alacritty, kitty, iTerm2, Windows Terminal
- Avoid obscure Unicode ranges
- Stick to well-supported symbols
- Document rendering requirements

---

## Compared to ASCII Art

### Unicode Advantages:

✅ More characters (thousands vs. 95)  
✅ Cleaner lines (box-drawing)  
✅ Better shapes (geometric symbols)  
✅ Built-in icons (emoji)  
✅ International scripts  

### Unicode Disadvantages:

❌ Requires UTF-8 encoding  
❌ Font-dependent rendering  
❌ Less universal compatibility  
❌ May not work in all contexts (email, old systems)  
❌ Breaks "pure" ASCII aesthetic  

### When to use ASCII:

- Maximum compatibility needed
- Retro aesthetic desired
- Email/plaintext contexts
- Philosophical commitment to constraints

### When to use Unicode:

- Modern terminal environments
- Enhanced visual clarity needed
- International content
- Richer symbol set required

---

## Creating Unicode Art

### Finding Characters

**Resources:**
- **unicode-table.com** - Browse all Unicode
- **shapecatcher.com** - Draw shape, find character
- **copychar.cc** - Quick symbol copy
- **Character Map (Windows), Character Viewer (macOS)**

**Useful ranges:**
- Box-drawing: U+2500–U+257F
- Block elements: U+2580–U+259F
- Geometric shapes: U+25A0–U+25FF
- Arrows: U+2190–U+21FF
- Mathematical: U+2200–U+22FF
- Emoji: Various ranges

### Workflow:

1. Plan your art
2. Find needed characters
3. Copy to text editor
4. Arrange and refine
5. Test in target environment
6. Document character requirements

---

## Further Reading

**In this repository:**
- `/galleries/unicode-art/symbol-explorations.md` - Deep dives into Unicode ranges
- `/galleries/unicode-art/experimental-works.md` - Pushing boundaries

**External:**
- **unicode.org** - Official Unicode Consortium
- **unicode-table.com** - Browse and search characters
- **Shapecatcher** - Find characters by drawing

---

## Contributing

Submit your Unicode art via pull request. Include:
- The art itself
- Characters used (Unicode codepoints if obscure)
- Font requirements (if any)
- Rendering notes

---

**License:** CC0 1.0 Universal (Public Domain)  
**Curator:** Digital Aesthetics Manifesto Contributors  
**Date:** November 19, 2025
