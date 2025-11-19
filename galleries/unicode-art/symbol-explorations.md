# Unicode Art: Symbol Explorations

## Introduction

Unicode contains over 140,000 characters across hundreds of scripts and symbol sets. This document explores specific Unicode ranges useful for text-based art, analyzing their properties, uses, and aesthetic possibilities.

---

## Box-Drawing Characters (U+2500–U+257F)

### Overview

128 characters specifically designed for drawing boxes, frames, and diagrams in text mode.

### Character Sets

**Single horizontal lines:**
```
─ ━  (light, heavy)
```

**Single vertical lines:**
```
│ ┃  (light, heavy)
```

**Corners:**
```
Light:    ┌ ┐ └ ┘
Heavy:    ┏ ┓ ┗ ┛
Double:   ╔ ╗ ╚ ╝
Rounded:  ╭ ╮ ╰ ╯
```

**T-junctions:**
```
├ ┤ ┬ ┴  (light)
┣ ┫ ┳ ┻  (heavy)
╠ ╣ ╦ ╩  (double)
```

**Crossings:**
```
┼ (light)
╋ (heavy)
╬ (double)
```

### Combinations

**Mixed weight:**
```
╓─────╖
║     ║
╙─────╜
```
(Double vertical, single horizontal)

### Complete Table Format

```
┌────┬────┬────┐
│ A  │ B  │ C  │
├────┼────┼────┤
│ 1  │ 2  │ 3  │
├────┼────┼────┤
│ X  │ Y  │ Z  │
└────┴────┴────┘
```

### Artistic Uses

**Pixel frames:**
```
┏━━━━━━━━━━┓
┃          ┃
┃  CONTENT ┃
┃          ┃
┗━━━━━━━━━━┛
```

**Nested structures:**
```
╔══════════╗
║ ┌──────┐ ║
║ │ Text │ ║
║ └──────┘ ║
╚══════════╝
```

**Abstract patterns:**
```
┌┬┐├┼┤└┴┘
├┼┤├┼┤├┼┤
└┴┘├┼┤├┼┤
   └┴┘└┴┘
```

---

## Block Elements (U+2580–U+259F)

### Overview

32 characters for creating solid areas, gradients, and pixel-art-style graphics.

### Full Blocks

```
█ Full block (U+2588)
▓ Dark shade (U+2593)
▒ Medium shade (U+2592)
░ Light shade (U+2591)
```

### Half Blocks

```
▀ Upper half block
▄ Lower half block
▌ Left half block
▐ Right half block
```

### Quarter Blocks

```
▖ Lower left quadrant
▗ Lower right quadrant
▘ Upper left quadrant
▙ Upper left + lower left + lower right
▚ Upper left + lower right
▛ Upper left + upper right + lower left
▜ Upper left + upper right + lower right
▝ Upper right quadrant
▞ Upper right + lower left
▟ Upper right + lower left + lower right
```

### Gradients

**Horizontal gradient:**
```
████▓▓▓▓▒▒▒▒░░░░
```

**Vertical shading:**
```
█████
▓▓▓▓▓
▒▒▒▒▒
░░░░░
```

### Pixel Art

**Using half blocks:**
```
▄▄▀▀▀▀▄▄
██████
████  ██
██████
```

### Progress Bars

```
[██████████░░░░░░░░░░] 50%
[████████████████░░░░] 80%
[████████████████████] 100%
```

### Artistic Patterns

```
█░█░█░█░█░
░█░█░█░█░█
█░█░█░█░█░
░█░█░█░█░█
```

---

## Geometric Shapes (U+25A0–U+25FF)

### Squares

```
■ Black square (U+25A0)
□ White square (U+25A1)
▪ Black small square (U+25AA)
▫ White small square (U+25AB)
◼ Black medium square (U+25FC)
◻ White medium square (U+25FB)
```

### Circles

```
● Black circle (U+25CF)
○ White circle (U+25CB)
◉ Fisheye (U+25C9)
◎ Bullseye (U+25CE)
⊙ Circled dot operator (U+2299)
```

### Triangles

```
▲ Black up-pointing triangle
△ White up-pointing triangle
▼ Black down-pointing triangle
▽ White down-pointing triangle
◀ Black left-pointing triangle
◁ White left-pointing triangle
▶ Black right-pointing triangle
▷ White right-pointing triangle
```

### Diamonds

```
◆ Black diamond
◇ White diamond
◈ White diamond containing black small diamond
```

### Stars

```
★ Black star
☆ White star
✦ Black four-pointed star (U+2726)
✧ White four-pointed star (U+2727)
✯ Pinwheel star (U+272F)
```

### Artistic Examples

**Bullet points with hierarchy:**
```
● Main point
  ○ Sub-point
    ▪ Detail
      ▫ Further detail
```

**Pattern design:**
```
★ ☆ ★ ☆ ★
 ☆ ★ ☆ ★ ☆
★ ☆ ★ ☆ ★
```

**Shape morphing sequence:**
```
● → ◉ → ◎ → ⊙
```

---

## Arrows (U+2190–U+21FF)

### Basic Arrows

```
← Left (U+2190)
↑ Up (U+2191)
→ Right (U+2192)
↓ Down (U+2193)
↔ Left-right (U+2194)
↕ Up-down (U+2195)
```

### Diagonal Arrows

```
↖ Northwest (U+2196)
↗ Northeast (U+2197)
↘ Southeast (U+2198)
↙ Southwest (U+2199)
```

### Double Arrows

```
⇐ Leftwards double arrow
⇑ Upwards double arrow
⇒ Rightwards double arrow
⇓ Downwards double arrow
⇔ Left-right double arrow
```

### Curved Arrows

```
↰ Upwards arrow with tip leftwards
↱ Upwards arrow with tip rightwards
↲ Downwards arrow with tip leftwards
↳ Downwards arrow with tip rightwards
↴ Rightwards arrow with corner downwards
↵ Downwards arrow with corner leftwards
```

### Flowchart Example

```
[Start]
   ↓
[Process]
   ↓
[Decision] → [Yes] → [Action]
   ↓                    ↓
  [No]                 [End]
   ↓                    ↑
[Other] ───────────────┘
```

### Circular Arrows

```
↶ Anticlockwise top semicircle arrow
↷ Clockwise top semicircle arrow
↺ Anticlockwise open circle arrow
↻ Clockwise open circle arrow
⟲ Anticlockwise gapped circle arrow
⟳ Clockwise gapped circle arrow
```

**Use:** Refresh, reload, cycle operations

---

## Mathematical Symbols (U+2200–U+22FF)

### Operators

```
∀ For all
∃ There exists
∅ Empty set
∈ Element of
∉ Not an element of
∏ N-ary product
∑ N-ary summation
∫ Integral
∞ Infinity
√ Square root
∛ Cube root
∜ Fourth root
```

### Relations

```
≈ Almost equal to
≠ Not equal to
≡ Identical to
≤ Less than or equal to
≥ Greater than or equal to
± Plus-minus
∓ Minus-plus
÷ Division
× Multiplication
```

### Set Theory

```
∩ Intersection
∪ Union
⊂ Subset of
⊃ Superset of
⊆ Subset of or equal to
⊇ Superset of or equal to
```

### Logic

```
∧ Logical and
∨ Logical or
¬ Not
⊕ XOR
⊤ Down tack (true)
⊥ Up tack (false)
```

### Artistic/Decorative Use

**Divider:**
```
∿∿∿∿∿∿∿∿∿∿∿∿∿∿∿
```

**Pattern:**
```
≈≈≈≈≈≈≈≈≈≈
∞ ∫ ∑ ∏ √
≈≈≈≈≈≈≈≈≈≈
```

---

## Braille Patterns (U+2800–U+28FF)

### Overview

256 Braille characters, surprisingly useful for graphics and patterns.

### Structure

Each Braille character consists of up to 8 dots:
```
Dot positions:
1 4
2 5
3 6
7 8
```

### Examples

```
⠀ Blank
⠁ Dot 1
⠂ Dot 2
⠃ Dots 1,2
⠄ Dot 3
...
⣿ All dots filled
```

### Artistic Uses

**Gradients:**
```
⠀⠁⠃⠇⠏⠟⠿⣿
```

**Sparklines/Charts:**
```
⡀⡄⡆⡇⣇⣧⣷⣿
```

**Loading spinners:**
```
⠋ ⠙ ⠹ ⠸ ⠼ ⠴ ⠦ ⠧ ⠇ ⠏
```

**Pixel art (very high resolution):**
```
⣿⣿⣿⣿⣿
⣿⠀⠀⠀⣿
⣿⠀⠀⠀⣿
⣿⣿⣿⣿⣿
```

---

## Miscellaneous Symbols (U+2600–U+26FF)

### Weather

```
☀ Sun
☁ Cloud
☂ Umbrella
☃ Snowman
☄ Comet
⛈ Thunder cloud and rain
❄ Snowflake
⛅ Sun behind cloud
```

### Zodiac

```
♈ Aries    ♉ Taurus   ♊ Gemini
♋ Cancer   ♌ Leo      ♍ Virgo
♎ Libra    ♏ Scorpio  ♐ Sagittarius
♑ Capricorn ♒ Aquarius ♓ Pisces
```

### Chess

```
♔ White king   ♚ Black king
♕ White queen  ♛ Black queen
♖ White rook   ♜ Black rook
♗ White bishop ♝ Black bishop
♘ White knight ♞ Black knight
♙ White pawn   ♟ Black pawn
```

### Music

```
♩ Quarter note
♪ Eighth note
♫ Beamed eighth notes
♬ Beamed sixteenth notes
♭ Flat
♮ Natural
♯ Sharp
```

### Other Symbols

```
☺ White smiling face
☹ White frowning face
☠ Skull and crossbones
☢ Radioactive
☣ Biohazard
☮ Peace symbol
☯ Yin yang
☸ Wheel of dharma
✝ Latin cross
✡ Star of David
☪ Star and crescent
```

---

## Dingbats (U+2700–U+27BF)

### Pointing Hands

```
☛ Black right pointing index
☞ White right pointing index
☜ White left pointing index
```

### Checkmarks and X's

```
✓ Check mark
✔ Heavy check mark
✕ Multiplication X
✖ Heavy multiplication X
✗ Ballot X
✘ Heavy ballot X
```

### Crosses

```
✙ Greek cross
✚ Heavy Greek cross
✛ Open centre cross
✜ Heavy open centre cross
```

### Decorative

```
✣ Four balloon-spoked asterisk
✤ Heavy four balloon-spoked asterisk
✥ Four club-spoked asterisk
✦ Black four pointed star
✧ White four pointed star
✰ Shadowed white star
✱ Heavy asterisk
✲ Open centre asterisk
✳ Eight spoked asterisk
✴ Eight pointed black star
✵ Eight pointed pinwheel star
```

### Artistic Examples

**Task list:**
```
✓ Complete documentation
✗ Fix bug #123
✓ Deploy to production
```

**Decorative border:**
```
✦ ━━━━━━━━━━━━ ✦
✧  Content Here  ✧
✦ ━━━━━━━━━━━━ ✦
```

---

## Superscripts and Subscripts

### Superscripts (scattered ranges)

```
⁰ ¹ ² ³ ⁴ ⁵ ⁶ ⁷ ⁸ ⁹
⁺ ⁻ ⁼ ⁽ ⁾
ᵃ ᵇ ᶜ ᵈ ᵉ ᶠ ᵍ ʰ ⁱ ʲ ᵏ ˡ ᵐ ⁿ ᵒ ᵖ ʳ ˢ ᵗ ᵘ ᵛ ʷ ˣ ʸ ᶻ
```

### Subscripts (U+2080–U+209F)

```
₀ ₁ ₂ ₃ ₄ ₅ ₆ ₇ ₈ ₉
₊ ₋ ₌ ₍ ₎
ₐ ₑ ₕ ᵢ ⱼ ₖ ₗ ₘ ₙ ₒ ₚ ᵣ ₛ ₜ ᵤ ᵥ ₓ
```

### Uses

**Mathematics:**
```
xⁿ + yⁿ = zⁿ
H₂O  CO₂  C₆H₁₂O₆
```

**Footnotes:**
```
Text with footnote¹ and another².

¹ First footnote
² Second footnote
```

---

## Playing Cards (U+1F0A0–U+1F0FF)

```
🂠 Joker
🂡-🂮 Spades (Ace through King)
🂱-🂾 Hearts
🃁-🃎 Diamonds
🃑-🃞 Clubs
🃟 Joker
```

**Note:** May render as emoji (color) in some systems.

---

## Combining Characters

### Diacritical Marks (U+0300–U+036F)

Can be combined with base characters to create new forms.

```
a + ̄ = ā (macron)
e + ̀ = è (grave)
i + ́ = í (acute)
o + ̂ = ô (circumflex)
u + ̈ = ü (dieresis)
```

### Artistic/Glitch Effects

**Overlaying marks:**
```
Z̴̡̢̧̛͔̻͓̬̳̰̜̲̦̩̫̻̲̦̯͂ͅa̷̧̱̦̜̙̘̻̰̺̹̯̥̦̱̲̹̻̘̒̈́̃̂l̸̡̧̢̛̬̱͍̫̳̙͇̗̬̱̹̰̙͑̾̐̃̊͛̐͜͠g̶̢̛̙̫̱̺̱͔̺̪̬͙̳̟͇̍̎̉̈́̇̌̓͊̽̊͂̚o̵̢̨̨̨̺͙̩̦̬̱̝̖̠̫̥̎̇̎̈́̒̓͋͗̐̚ͅ
```

**Warning:** Can break rendering, use sparingly.

---

## Technical Notes

### Character Width Issues

Some Unicode characters are:
- **Half-width** (1 cell): Latin, ASCII-compatible
- **Full-width** (2 cells): CJK characters, some emoji
- **Zero-width** (0 cells): Combining marks
- **Ambiguous width**: Depends on locale/font

**Test your art** in target terminal to ensure proper alignment.

### Font Coverage

Not all fonts include all Unicode characters.

**Well-supported ranges:**
- Box-drawing
- Block elements
- Basic geometric shapes
- Common arrows

**Less supported:**
- Rare mathematical symbols
- Ancient scripts
- Recently-added emoji

**Solution:** Document font requirements, test widely.

---

## Finding Characters

### Tools

1. **unicode-table.com** - Browse by range
2. **character map (OS)** - System tool
3. **shapecatcher.com** - Draw shape, find character
4. **copychar.cc** - Quick copy

### Search Strategies

- Browse by Unicode block/range
- Search by name (e.g., "triangle")
- Look at similar characters
- Check combining possibilities

---

## Artistic Philosophy

### When to Use Unicode

**Use Unicode when:**
- Cleaner representation needed
- Working in modern terminal
- Enhanced visuals worth compatibility trade-off
- Target audience has UTF-8 support

### When to Stick to ASCII

**Use ASCII when:**
- Maximum compatibility required
- Philosophical commitment to constraints
- Email/plain text environments
- Retro aesthetic desired

---

## Further Exploration

**Experiment with:**
- Mixing ranges (boxes + shapes + arrows)
- Creating alphabets from symbols
- Building patterns from repeating characters
- Using rare/obscure Unicode for unique effects

**In this repository:**
- `/galleries/unicode-art/COLLECTION.md` - Examples
- `/galleries/unicode-art/experimental-works.md` - Pushing boundaries

---

**License:** CC0 1.0 Universal (Public Domain)  
**Author:** Digital Aesthetics Manifesto Contributors  
**Date:** November 19, 2025
