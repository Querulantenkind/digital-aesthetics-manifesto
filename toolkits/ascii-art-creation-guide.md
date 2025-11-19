# ASCII Art Creation Guide

## Introduction

**ASCII art** is the practice of creating images using characters from the ASCII character set.

Born from technical constraints of early computing, ASCII art has evolved into a distinct aesthetic practice—**text as image, code as canvas**.

This guide teaches you how to create ASCII art: from simple borders to complex portraits, from manual creation to tool-assisted workflows.

---

## What is ASCII Art?

### Definition

**ASCII art** uses printable characters (letters, numbers, symbols) to create visual images.

**Character set:**
- 95 printable ASCII characters
- Space to tilde (` ` to `~`)
- No extended Unicode (that's Unicode art)

### Types

**1. Line art:**
```
    /\_/\
   ( o.o )
    > ^ <
```

**2. Block/solid art:**
```
█████╗ ██████╗ ████████╗
██╔══██╗██╔══██╗╚══██╔══╝
███████║██████╔╝   ██║   
██╔══██║██╔══██╗   ██║   
██║  ██║██║  ██║   ██║   
╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝   
```

**3. Grayscale/shaded art:**
```
         .:=*#@@@@#*=:.
      -*@@@@@@@@@@@@@@@@*-
    =@@@@@#*+====+*#@@@@@#=
   #@@@@+.          .+@@@@#
  *@@@#.              .#@@@*
  @@@#                  #@@@
```

**4. Text-based typography:**
```
 _____ _          _  _   
|_   _| |__   ___(_)| |_ 
  | | | '_ \ / _ \ || __|
  | | | | | |  __/ || |_ 
  |_| |_| |_|\___|_| \__|
```

---

## Tools and Environment

### 1. Text Editors

**Monospace fonts essential.**

**Recommended editors:**

**Terminal-based:**
- **Vim/Neovim** - Modal editing, precision control
- **Emacs** - artist-mode, picture-mode for drawing
- **nano** - Simple, beginner-friendly

**GUI editors:**
- **VS Code** - Extensions available, good font rendering
- **Sublime Text** - Fast, clean
- **Notepad++** - Windows, simple

**Font recommendations:**
- **Cascadia Code** - Clean, modern
- **Fira Code** - Excellent character spacing
- **Hack** - Designed for readability
- **JetBrains Mono** - Clear distinction between similar characters
- **Courier New** - Classic, reliable

**Settings:**
- Monospace font (obviously)
- Line spacing: 1.0 or 1.1
- Tab width: varies by style (often 2 or 4 spaces)
- Wrap: OFF (critical for alignment)
- Show whitespace characters (helpful)

### 2. Online Tools

**ASCII generators (image-to-ASCII):**

- **ASCII-art-generator.org** - Web-based converter
- **asciiart.club** - Multiple algorithms
- **text-image.com** - Customizable output

**Character reference:**
- **ascii-code.com** - Complete ASCII table
- **unicode-table.com** - Extended characters

**Live editors:**
- **asciiflow.com** - Draw diagrams with mouse
- **texteditor.com/ascii-art** - Browser-based editor

### 3. Software/CLI Tools

**Converters:**
```bash
# jp2a - JPEG to ASCII
jp2a --width=80 image.jpg

# ascii-image-converter
ascii-image-converter image.png -C -W 80

# img2txt (libcaca)
img2txt -W 80 -f utf8 image.jpg
```

**Figlet/Toilet (text to ASCII):**
```bash
# figlet - classic
figlet "Hello"

# toilet - colored ASCII art
toilet -f mono12 "ASCII"
```

**cowsay/ponysay:**
```bash
# cowsay - speaking cow
echo "Hello" | cowsay

# fortune + cowsay
fortune | cowsay
```

---

## Basic Techniques

### 1. Character Selection

**Characters vary in visual density.**

**Density scale (light to dark):**
```
Lightest: . , - ` '
Light:    : ; ! i l
Medium:   o c e
Dense:    C O G Q
Densest:  @ # $ % &
```

**Example gradient:**
```
..:;+=xX$&#
```

**Common building blocks:**

**Lines:**
```
Horizontal: - _ =
Vertical:   | ¦ !
Diagonal:   / \ 
```

**Corners:**
```
.----.    +----+    ┌────┐
|    |    |    |    │    │
'----'    +----+    └────┘
```

**Curves:**
```
.---.     .===.     ╭───╮
(   )     (   )     │   │
'---'     '==='     ╰───╯
```

### 2. Line Art Basics

**Start simple.**

**Box:**
```
+---+
|   |
+---+
```

**House:**
```
   /\
  /  \
 /    \
+------+
|  __  |
| |  | |
+------+
```

**Tree:**
```
   *
  ***
 *****
*******
   |
  |||
```

**Practice:**
- Draw simple shapes
- Use consistent character choices
- Maintain spacing

### 3. Typography/Text Art

**Using figlet:**

```bash
$ figlet -f banner "CODE"

 ####   ####  #####  ##### 
#    # #    # #    # #     
#      #    # #    # ##### 
#      #    # #    # #     
#    # #    # #    # #     
 ####   ####  #####  ##### 
```

**Styles:**
- **banner** - Bold, blocky
- **slant** - Italic diagonal
- **small** - Compact
- **standard** - Default
- **big** - Large, clear

**Manual text art:**

```
  ____ ___  ____  _____ 
 / ___/ _ \|  _ \| ____|
| |  | | | | | | |  _|  
| |__| |_| | |_| | |___ 
 \____\___/|____/|_____|
```

**Tips:**
- Trace letters first in blocks
- Use `#`, `@`, `█` for solid areas
- Leave negative space

### 4. Shading and Gradients

**Grayscale using character density.**

**Simple gradient:**
```
          
....      Light
::::      
++++      Medium
####      
@@@@      Dense
          
```

**Sphere example:**
```
        .:-=+*#%@%#*+=-:.
     :+#%@@@@@@@@@@@@@@%#+:
   =#@@@@@#*+======+*#@@@@@#=
  +@@@@#+.            .+#@@@@+
 *@@@*.                  .*@@@*
=@@@-                      -@@@=
#@@+                        +@@#
@@@.                        .@@@
#@@+                        +@@#
=@@@-                      -@@@=
 *@@@*.                  .*@@@*
  +@@@@#+.            .+#@@@@+
   =#@@@@@#*+======+*#@@@@@#=
     :+#%@@@@@@@@@@@@@@%#+:
        .:-=+*#%@%#*+=-:.
```

**Key:**
- Center = lightest (highlight)
- Edges = darkest (shadow)
- Gradual transition

### 5. Proportions and Spacing

**ASCII characters are taller than wide.**

**Typical character ratio:**
- Width:Height = 1:2 (approximately)
- Horizontal spaces ≠ vertical spaces

**Adjust for aspect ratio:**

**Circle (before adjustment):**
```
  ***
 *****
  ***
```
(Looks like vertical oval)

**Circle (after adjustment - wider):**
```
  *****
 *******
  *****
```

**Tip:** Use more horizontal space than vertical.

---

## Advanced Techniques

### 1. Large-Scale Images

**Portrait/photo conversion:**

**Workflow:**
1. Choose image (high contrast works best)
2. Convert to grayscale
3. Use converter tool (jp2a, ascii-image-converter)
4. Adjust width (40-120 characters typical)
5. Manual touch-ups

**Example command:**
```bash
jp2a --width=80 portrait.jpg > portrait.txt
```

**Post-processing:**
- Enhance contrast (replace characters)
- Clean up noise
- Add details

### 2. Color ASCII Art (ANSI)

**ANSI escape codes add color.**

**Basic colors:**
```bash
echo -e "\033[31mRed text\033[0m"
echo -e "\033[32mGreen text\033[0m"
echo -e "\033[34mBlue text\033[0m"
```

**Colored ASCII:**
```
\033[31m   *   \033[0m      # Red star
\033[32m  ***  \033[0m      # Green tree
\033[34m ***** \033[0m      # Blue base
```

**Tools:**
- **toilet** - Built-in color support
- **lolcat** - Rainbow gradients
- Manual ANSI codes

### 3. Animated ASCII

**Frame-by-frame animation.**

**Simple example (spinning line):**

Frame 1:
```
|
```

Frame 2:
```
/
```

Frame 3:
```
-
```

Frame 4:
```
\
```

**Implementation:**
```bash
#!/bin/bash
while true; do
  clear
  echo "|"
  sleep 0.2
  clear
  echo "/"
  sleep 0.2
  clear
  echo "-"
  sleep 0.2
  clear
  echo "\\"
  sleep 0.2
done
```

**Frame-based animation:**
- Create each frame as separate ASCII art
- Display frames in sequence
- Use `sleep` for timing
- Clear screen between frames

**Tools:**
- **AAlib** - ASCII art animation library
- **Ncurses** - Terminal graphics
- Shell scripts

### 4. ASCII Comics/Storyboards

**Panels with text.**

**Example:**
```
.----------------.  .----------------.
|   "Hello!"     |  |   "Hi there!"  |
|                |  |                |
|    \(^_^)/     |  |     (^_^)      |
|                |  |                |
'----------------'  '----------------'
         |                  |
         v                  v
.----------------.  .----------------.
|  "How are you?"|  |  "I'm great!"  |
|                |  |                |
|     (^_^)      |  |    \(^o^)/     |
|                |  |                |
'----------------'  '----------------'
```

**Elements:**
- Panel borders
- Speech bubbles
- Characters
- Text

### 5. Logos and Branding

**ASCII logos for projects.**

**Example (fictional brand):**
```
 _____ ______ _____ _   _ 
|_   _|  ____/ ____| | | |
  | | | |__ | |    | |_| |
  | | |  __|| |    |  _  |
 _| |_| |___| |____| | | |
|_____|______\_____|_| |_|
```

**Uses:**
- Terminal splash screens
- CLI tool headers
- README.md files
- Boot messages

---

## Styles and Movements

### 1. Old-School ASCII (1960s-1990s)

**Characteristics:**
- Simple line art
- Limited characters (original ASCII only)
- Functional (diagrams, flowcharts)

**Example:**
```
START
  |
  v
[Process]
  |
  v
<Decision> --Yes--> [Action1]
  |
  No
  |
  v
[Action2]
  |
  v
 END
```

### 2. ANSI Art (1980s-1990s)

**BBS era art.**

**Characteristics:**
- Block characters (█ ▄ ▀ ▌ ▐)
- 16-color ANSI palette
- Often included animation
- Scene/demoscene style

**Influenced by:**
- BBS culture
- Cracktros
- Demo scene graphics

### 3. ASCII Emoticons (1980s-present)

**Expressive faces.**

**Western style:**
```
:)  :D  :(  ;)  :P  :O  :|
```

**Japanese kaomoji:**
```
(^_^)  (>_<)  (o_o)  (^_^;)  (T_T)
```

**Complex kaomoji:**
```
┬┴┬┴┤(･_├┬┴┬┴     # Peek
(ﾉ◕ヮ◕)ﾉ*:･ﾟ✧      # Celebration
(╯°□°）╯︵ ┻━┻      # Table flip
```

### 4. Neotraditional ASCII (2000s-present)

**Revival with modern tools.**

**Characteristics:**
- Sophisticated shading
- Large-scale images
- Photo-realistic attempts
- Unicode box-drawing characters (borderline)

### 5. Minimal ASCII (Contemporary)

**Less is more.**

**Example:**
```
  •
 /|\
 / \
```

**Principles:**
- Maximum expression, minimum characters
- Negative space
- Suggestion over detail

---

## Step-by-Step Projects

### Project 1: Simple Cat (15 min)

**Goal:** Create recognizable cat face.

**Step 1: Basic structure**
```
 /\_/\
(     )
(     )
```

**Step 2: Add features**
```
 /\_/\
( o o )
(  ^  )
```

**Step 3: Refine**
```
 /\_/\
( o.o )
 > ^ <
```

**Done!**

### Project 2: Isometric Cube (30 min)

**Goal:** Draw 3D-looking cube.

**Step 1: Front face**
```
    +
   /|
  / |
 /  |
+---+
```

**Step 2: Add depth**
```
    +-----+
   /     /|
  /     / |
 /     /  |
+-----+   |
|     |   +
|     |  /
|     | /
|     |/
+-----+
```

**Step 3: Clean up**
```
     +-----+
    /     /|
   /     / |
  /     /  |
 +-----+   |
 |     |   +
 |     |  /
 |     | /
 |     |/
 +-----+
```

**Experiment:** Try different orientations.

### Project 3: ASCII Portrait (60-90 min)

**Goal:** Convert photo to ASCII art.

**Step 1: Choose image**
- High contrast
- Clear features
- Not too complex
- Square-ish ratio

**Step 2: Convert with tool**
```bash
jp2a --width=60 portrait.jpg > portrait_raw.txt
```

**Step 3: Manual refinement**
- Enhance eyes
- Clarify edges
- Fix character choices
- Adjust shading

**Step 4: Add details**
- Hair texture
- Shadow emphasis
- Highlights

**Example (simplified):**
```
            ..:--=+**+==-:..            
        .-+*%@@@@@@@@@@@@@@%*+-.        
      =*@@@@@#*+======+*#@@@@@*=      
    :%@@@@#-              -#@@@@%:    
   =@@@%=                    =%@@@=   
  +@@@+        ..  ..          +@@@+  
 =@@@:       .#@@..@@#.         :@@@= 
.@@@-        .#@@..@@#.          -@@@.
*@@*           ....               *@@*
@@@.                              .@@@
@@@                                @@@
#@@+          ----------          +@@#
=@@@:          -@@@@@@-          :@@@=
 +@@@+          .++++.          +@@@+ 
  :%@@@#:                    :#@@@%:  
   .+@@@@%+-.            .-+%@@@@+.   
     .=*@@@@@#*+====+*#@@@@@*=.     
        .-+*%@@@@@@@@@@@@%*+-.        
            ..:--=+++=--:..            
```

---

## Common Mistakes and Solutions

### Mistake 1: Inconsistent Spacing

**Problem:**
```
+----+
|  |
+----+
```
(Left edge misaligned)

**Solution:**
Use a grid. Count characters. Use editor with column markers.

### Mistake 2: Wrong Font

**Problem:**
Art looks perfect in one editor, broken in another.

**Solution:**
- Always use monospace fonts
- Test in multiple environments
- Avoid proprietary fonts

### Mistake 3: Forgetting Aspect Ratio

**Problem:**
Circles look like ovals.

**Solution:**
Remember characters are ~2x taller than wide. Compensate horizontally.

### Mistake 4: Too Dense

**Problem:**
Over-shading, hard to see forms.

**Solution:**
Use full range of character densities. Leave whitespace.

### Mistake 5: No Contrast

**Problem:**
Everything is mid-gray.

**Solution:**
Push lights lighter, darks darker. Exaggerate.

---

## ASCII Art Culture

### Historical Context

**1960s-1970s:** 
- Teletype machines
- Mainframe printouts
- Functional diagrams

**1980s-1990s:**
- BBS culture explosion
- ANSI art dominance
- Competition and groups

**2000s:**
- IRC, forums
- Signature art
- Emoticon evolution

**2010s-present:**
- Terminal customization
- Retro aesthetic revival
- Digital art recognition

### Community and Sharing

**Where to share:**
- **reddit.com/r/ASCII_Archive** - Gallery
- **asciiart.eu** - Large collection
- **textart.io** - Community and tools
- **GitHub** - Code art, README decoration

**Formats:**
- Plain text (.txt)
- Markdown code blocks
- HTML `<pre>` tags
- Image screenshots (for color ANSI)

**Etiquette:**
- Credit original artists
- Preserve formatting
- Use code blocks (Markdown, HTML)
- Test before sharing

---

## Resources and References

### Character Sets

**ASCII table:**
```
Dec Hex Char    Dec Hex Char    Dec Hex Char    Dec Hex Char
 32  20 Space   48  30 0        64  40 @        80  50 P
 33  21 !       49  31 1        65  41 A        81  51 Q
 34  22 "       50  32 2        66  42 B        82  52 R
 35  23 #       51  33 3        67  43 C        83  53 S
 36  24 $       52  34 4        68  44 D        84  54 T
 37  25 %       53  35 5        69  45 E        85  55 U
 38  26 &       54  36 6        70  46 F        86  56 V
 39  27 '       55  37 7        71  47 G        87  57 W
 40  28 (       56  38 8        72  48 H        88  58 X
 41  29 )       57  39 9        73  49 I        89  59 Y
 42  2A *       58  3A :        74  4A J        90  5A Z
 43  2B +       59  3B ;        75  4B K        91  5B [
 44  2C ,       60  3C <        76  4C L        92  5C \
 45  2D -       61  3D =        77  4D M        93  5D ]
 46  2E .       62  3E >        78  4E N        94  5E ^
 47  2F /       63  3F ?        79  4F O        95  5F _
```

### Software

**Editors:**
- **Vim** + artist-mode
- **Emacs** + picture-mode
- **VS Code** + ASCII Draw extension

**Generators:**
- **jp2a** - JPEG to ASCII
- **figlet** - Text to ASCII
- **toilet** - Colored ASCII text
- **ascii-image-converter** - Modern converter

**Libraries:**
- **AAlib** - ASCII art library (C)
- **ascii_magic** - Python library
- **image-to-ascii** - Node.js

### Learning Resources

**Tutorials:**
- **asciiart.website** - Techniques
- **chris.com/ascii** - Joan Stark's tutorials
- **textfiles.com** - Historical archives

**Collections:**
- **asciiart.eu** - Massive gallery
- **ascii.co.uk** - UK collection
- **16colo.rs** - ANSI art archive

---

## Exercises

### Exercise 1: Character Exploration (15 min)

**Task:** Create a gradient using 10 different characters.

**Goal:** Understand character density.

### Exercise 2: Logo Recreation (30 min)

**Task:** Take a simple logo (Nike swoosh, Apple logo, etc.). Recreate in ASCII.

**Goal:** Practice line work.

### Exercise 3: Self-Portrait (60 min)

**Task:** Create ASCII art self-portrait.

**Goal:** Learn shading and detail.

### Exercise 4: Animated Sequence (45 min)

**Task:** Create 4-frame animation (e.g., bouncing ball).

**Goal:** Understand frame-based animation.

### Exercise 5: ASCII Story (30 min)

**Task:** Create 3-panel comic strip in ASCII.

**Goal:** Combine art and narrative.

---

## Advanced Topics

### 1. Unicode Box Drawing

**Beyond ASCII (but related):**

**Box drawing characters:**
```
┌─┬─┐  ╔═╦═╗  ╭─┬─╮
├─┼─┤  ╠═╬═╣  ├─┼─┤
└─┴─┘  ╚═╩═╝  ╰─┴─╯
```

**When to use:**
- Modern terminals (UTF-8 support)
- Cleaner diagram lines
- More visual options

**When NOT to use:**
- Strict ASCII requirement
- Legacy system compatibility
- Broadest accessibility

### 2. ASCII in Code

**Embedded ASCII art:**

```python
def print_header():
    print(r"""
 _____ _____ ____  _____
|_   _|  _  |    \|   __|
  | | |     |  |  |   __|
  |_| |__|__|____/|_____|
    """)
```

**Docstring art:**
```python
"""
    +---+
    | T |  Task Manager v2.0
    +---+
"""
```

### 3. Generative ASCII Art

**Algorithmic creation:**

```python
import random

def generate_noise(width, height):
    chars = " .:-=+*#%@"
    for _ in range(height):
        line = ""
        for _ in range(width):
            line += random.choice(chars)
        print(line)

generate_noise(40, 20)
```

**Possibilities:**
- Procedural landscapes
- Random patterns
- Data visualization

### 4. ASCII Data Visualization

**Charts in plain text:**

**Bar chart:**
```
Sales Report
============
Jan: ████████████ 120
Feb: ████████████████ 160
Mar: ██████████ 100
Apr: ████████████████████ 200
```

**Line graph:**
```
200|              *
150|         *   / 
100|    *   /   /  
 50| *     /   /   
  0|___________________
    Jan Feb Mar Apr
```

**Tools:**
- **gnuplot** (dumb terminal mode)
- **asciichart** (Node.js)
- **termgraph** (Python)

---

## Final Tips

**1. Start Simple**
Don't try portraits on day one. Start with shapes.

**2. Study Examples**
Look at existing ASCII art. How did they solve problems?

**3. Use Tools**
Converters are not cheating. They're assistants.

**4. Practice Spacing**
Spacing is 80% of ASCII art success.

**5. Test Everywhere**
View your art in multiple terminals, editors, fonts.

**6. Embrace Constraints**
Limitations = creativity.

**7. Share Your Work**
ASCII art is community art. Share it.

---

## Conclusion

ASCII art is:
- An art form (not just nostalgia)
- A skill (practice improves)
- A community (join it)
- A philosophy (embrace constraints)

**Start creating. One character at a time.**

```
   _____  _____  _____ _____ _____ 
  |     ||     ||   __| __  |_   _|
  |   --||   --||   __|    -| | |  
  |_____||_____||__|  |__|__| |_|  
                                   
```

---

**License:** CC0 1.0 Universal (Public Domain)  
**Author:** Digital Aesthetics Manifesto Contributors  
**Date:** November 19, 2025
