# Terminal Design Toolkit

## Introduction

**Terminals are not just functional tools—they are canvases for design.**

From color schemes to typography, from layout to interaction patterns, terminal design combines aesthetics with usability to create environments where people spend hours coding, writing, and creating.

This guide teaches you how to design beautiful, functional terminal environments: from choosing colors to configuring shells, from selecting fonts to crafting prompts.

---

## What is Terminal Design?

### Definition

**Terminal design** is the practice of customizing terminal emulators to be both aesthetically pleasing and functionally optimal for your workflow.

**Elements:**
- Color schemes
- Typography (fonts)
- Prompts (shell customization)
- Window management (tiling, splits)
- Status bars
- Keybindings

### Why Design Your Terminal?

**Practical reasons:**
- Spend hours per day in terminal—make it pleasant
- Reduce eye strain
- Improve productivity
- Personal workspace

**Aesthetic reasons:**
- Expression through environment
- Pride in tools
- Community participation (r/unixporn)
- Craft over convenience

---

## Core Elements

### 1. Terminal Emulator

**The software that displays your terminal.**

**Popular choices:**

**Linux:**
- **Alacritty** - GPU-accelerated, minimal, fast
- **kitty** - Feature-rich, GPU-accelerated, extensible
- **Wezterm** - Rust-based, highly configurable
- **urxvt (rxvt-unicode)** - Lightweight, classic
- **st (simple terminal)** - Suckless philosophy, patch-based

**macOS:**
- **Alacritty** - Cross-platform
- **iTerm2** - Feature-rich, macOS-native
- **kitty** - Works on macOS too
- **Terminal.app** - Default, simple

**Windows:**
- **Windows Terminal** - Modern, Microsoft-official
- **Alacritty** - Works on Windows
- **ConEmu** - Legacy but powerful

**Choosing criteria:**
- Performance (speed, GPU acceleration)
- Configurability (YAML, TOML, code-based?)
- Features (tabs, splits, ligatures)
- Aesthetics (rendering quality, font support)

### 2. Color Scheme

**16 ANSI colors + background + foreground.**

**Standard ANSI colors:**
```
Normal:          Bright:
0: Black         8:  Bright Black (gray)
1: Red           9:  Bright Red
2: Green         10: Bright Green
3: Yellow        11: Bright Yellow
4: Blue          12: Bright Blue
5: Magenta       13: Bright Magenta
6: Cyan          14: Bright Cyan
7: White         15: Bright White

Plus:
Background color
Foreground (text) color
```

**Popular schemes:**

**Solarized:**
- Designed by Ethan Schoonover
- 16 colors, carefully balanced
- Light and dark variants
- High contrast, low brightness
- Excellent for long sessions

**Gruvbox:**
- Warm, retro vibe
- Earthy tones
- Easy on eyes
- Popular in r/unixporn

**Nord:**
- Cool, arctic palette
- Blues and grays
- Minimalist aesthetic
- Consistent across apps

**Dracula:**
- Purple/pink/cyan
- Dark background
- High contrast
- Popular, widely ported

**Tokyo Night:**
- Inspired by Tokyo at night
- Deep blues, vibrant accents
- Modern aesthetic

**Base16:**
- Framework for building themes
- Consistent structure
- Thousands of variants

**One Dark/One Light:**
- From Atom editor
- Balanced, professional
- Widely supported

**Custom:**
- Build your own
- Use terminal-sexy.com or similar tools
- Test thoroughly

### 3. Font

**Monospace fonts only.**

**Characteristics to consider:**

**Readability:**
- Clear distinction between similar characters (0 vs O, 1 vs l vs I)
- Comfortable size (usually 12-14pt)
- Good spacing

**Style:**
- Rounded vs. sharp
- Weight (thickness)
- Character width (condensed vs. wide)

**Features:**
- **Ligatures** - Combined characters (e.g., `=>` becomes `⇒`)
- **Powerline symbols** - Special glyphs for fancy prompts
- **Icon fonts** - Nerd Fonts patch for file icons

**Recommended fonts:**

**Classic:**
- **Courier New** - Standard, works everywhere
- **Monaco** - macOS classic
- **Consolas** - Windows classic

**Modern coding fonts:**
- **Fira Code** - Excellent ligatures
- **JetBrains Mono** - Clear, modern, free ligatures
- **Cascadia Code** - Microsoft, includes ligatures
- **Hack** - Designed for source code
- **Source Code Pro** - Adobe, open source

**Bitmap fonts (retro aesthetic):**
- **Terminus** - Clean, sharp pixels
- **Tamsyn** - Classic bitmap feel
- **Cozette** - Tiny, pixel-perfect

**Nerd Fonts:**
- Patched versions of popular fonts
- Includes icons/glyphs
- Essential for advanced prompts
- Download from nerdfonts.com

### 4. Shell and Prompt

**Shell:** The command interpreter (bash, zsh, fish)  
**Prompt:** What you see before cursor

**Popular shells:**

**Bash:**
- Default on most Linux
- Ubiquitous
- Simple, reliable

**Zsh:**
- Bash-compatible, more features
- Popular on macOS (now default)
- Highly customizable
- Oh My Zsh framework

**Fish:**
- User-friendly, out-of-box features
- Auto-suggestions
- Syntax highlighting
- Different syntax (not POSIX)

**Prompt customization:**

**Minimalist:**
```
$
```

**Classic:**
```
user@hostname:~/path $
```

**Git-aware:**
```
~/project (main*) $
```

**Multi-line:**
```
┌─[user@hostname]─[~/project]
└─$
```

**Powerline/Starship:**
```
 ~/project  main  10.5s 
❯
```

**Prompt frameworks:**
- **Starship** - Fast, cross-shell, Rust-based
- **Oh My Zsh** - Zsh framework, themes/plugins
- **Powerlevel10k** - Fast, feature-rich Zsh theme
- **Pure** - Minimal, async Zsh prompt

---

## Step-by-Step Setup

### Step 1: Choose Terminal Emulator (15 min)

**Decision factors:**

**For speed/simplicity:**
- Alacritty - Minimal config, blazing fast

**For features:**
- kitty - GPU-accelerated + tabs/splits/ligatures
- iTerm2 (macOS) - Feature-rich

**For philosophy:**
- st - Suckless, patch yourself

**Install example (Linux):**
```bash
# Alacritty
sudo apt install alacritty   # Debian/Ubuntu
sudo pacman -S alacritty     # Arch
brew install alacritty       # macOS

# kitty
sudo apt install kitty
```

### Step 2: Select Color Scheme (30 min)

**Browse options:**
- **terminal.sexy** - Web-based editor
- **base16-project.github.io** - Framework
- **iterm2colorschemes.com** - 200+ themes

**Test before committing:**

**Create test file:**
```bash
curl -s https://gist.githubusercontent.com/lilydjwg/fdeaf79e921c2f413f44b6f613f6ad53/raw/94d8b2be62657e96488038b0e547e3009ed87d40/colors.sh | bash
```
(Shows all 256 colors)

**Apply to terminal:**

**Alacritty example:**

Config file: `~/.config/alacritty/alacritty.toml`

```toml
[colors.primary]
background = "#1e1e1e"
foreground = "#d4d4d4"

[colors.normal]
black   = "#000000"
red     = "#cd3131"
green   = "#0dbc79"
yellow  = "#e5e510"
blue    = "#2472c8"
magenta = "#bc3fbc"
cyan    = "#11a8cd"
white   = "#e5e5e5"

[colors.bright]
black   = "#666666"
red     = "#f14c4c"
green   = "#23d18b"
yellow  = "#f5f543"
blue    = "#3b8eea"
magenta = "#d670d6"
cyan    = "#29b8db"
white   = "#ffffff"
```

**Test with Vim, ls, etc.:**
```bash
vim ~/.bashrc
ls --color=auto
```

### Step 3: Choose and Install Font (20 min)

**Download Nerd Font:**

```bash
# Example: JetBrains Mono Nerd Font
cd ~/Downloads
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.0.0/JetBrainsMono.zip
unzip JetBrainsMono.zip -d ~/.local/share/fonts/
fc-cache -fv  # Refresh font cache
```

**Configure terminal:**

**Alacritty:**
```toml
[font]
normal = { family = "JetBrainsMono Nerd Font", style = "Regular" }
size = 12.0
```

**kitty:**
```
font_family      JetBrainsMono Nerd Font
font_size        12.0
```

**Test:**
- Restart terminal
- Check for ligatures: type `=>`, `!=`, `->>`
- Check for icons (if using Starship or similar)

### Step 4: Configure Shell (30-60 min)

**If using Zsh + Starship (recommended for beginners):**

**Install Zsh:**
```bash
sudo apt install zsh
chsh -s $(which zsh)  # Set as default shell
```

**Install Starship:**
```bash
curl -sS https://starship.rs/install.sh | sh
```

**Configure:**

Add to `~/.zshrc`:
```bash
eval "$(starship init zsh)"
```

**Customize Starship:**

Create `~/.config/starship.toml`:
```toml
format = """
[┌───────────────────>](bold green)
[│](bold green)$directory$git_branch$git_status
[└─>](bold green) """

[directory]
style = "blue"

[git_branch]
symbol = " "
style = "bright-black"

[git_status]
style = "red"
```

**Reload:**
```bash
source ~/.zshrc
```

### Step 5: Add Syntax Highlighting (15 min)

**Zsh Syntax Highlighting:**

```bash
# Install
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.zsh/zsh-syntax-highlighting

# Add to ~/.zshrc
source ~/.zsh/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```

**Fish:**
Built-in syntax highlighting (no config needed).

### Step 6: Configure Status Bar (optional, 30 min)

**If using tmux:**

**Install tmux:**
```bash
sudo apt install tmux
```

**Configure status bar:**

`~/.tmux.conf`:
```bash
# Status bar
set -g status-position bottom
set -g status-style 'bg=#1e1e1e fg=#d4d4d4'
set -g status-left ''
set -g status-right '#[fg=green]#S #[fg=blue]%H:%M '

# Active window highlight
setw -g window-status-current-style 'fg=#1e1e1e bg=#0dbc79 bold'
```

**Reload:**
```bash
tmux source-file ~/.tmux.conf
```

---

## Design Principles

### 1. Contrast

**Essential for readability.**

**Background vs. foreground:**
- High contrast reduces eye strain
- Not too high (pure white on black harsh)
- Test: Can you read for 30 min comfortably?

**Syntax highlighting:**
- Comments: lower contrast (muted)
- Keywords: higher contrast (stand out)
- Strings: distinctive color

**WCAG guidelines:**
- Contrast ratio 4.5:1 minimum for text
- Test with: contrastchecker.com

### 2. Consistency

**Colors should have meaning.**

**Common conventions:**
- Red: errors, warnings, git deletions
- Green: success, git additions
- Blue: directories, info
- Yellow: warnings (less severe than red)
- Cyan: links, special files

**Apply consistently:**
- Across prompt, syntax, ls colors
- Across all tools (vim, tmux, etc.)

### 3. Balance

**Not too busy, not too sparse.**

**Information density:**
- Include useful info (git status, exit code)
- Exclude noise (unnecessary decorations)

**Visual weight:**
- Balance colors (not all bright)
- Use neutral base (bg, fg)
- Accent colors for highlights

### 4. Ergonomics

**Design for long sessions.**

**Reduce eye strain:**
- Medium-dark backgrounds (not pure black)
- Muted colors (not neon)
- Appropriate font size

**Cognitive load:**
- Prompt should be scannable
- Important info emphasized
- Consistent layout

### 5. Personality

**Your terminal, your style.**

**Express yourself:**
- Color palette reflects your taste
- Prompt shows your priorities
- Decorations (ASCII art, quotes) if you like

**Examples:**
- Minimalist: One line, essential info only
- Cyberpunk: Neon colors, glitch aesthetics
- Retro: Green-on-black, bitmap font
- Warm: Gruvbox, soft contrast

---

## Advanced Customization

### 1. Window Manager Integration

**For Linux with tiling WMs (i3, bspwm, sway):**

**Scratchpad terminal:**
- Hidden terminal, toggle with keybind
- Always available
- Quick commands without switching workspace

**i3 config example:**
```
# Scratchpad terminal
for_window [instance="dropdown_term"] floating enable
for_window [instance="dropdown_term"] resize set 1200 800
for_window [instance="dropdown_term"] move position center
for_window [instance="dropdown_term"] move scratchpad

# Toggle with F12
bindsym $mod+grave [instance="dropdown_term"] scratchpad show

# Launch on startup
exec --no-startup-id alacritty --class dropdown_term
```

### 2. Multiplexing (tmux/screen)

**Split terminals, persist sessions.**

**Basic tmux workflow:**

**Start tmux:**
```bash
tmux
```

**Keybindings (prefix: Ctrl+b):**
```
Ctrl+b %   - Split vertically
Ctrl+b "   - Split horizontally
Ctrl+b o   - Switch panes
Ctrl+b c   - New window
Ctrl+b n   - Next window
Ctrl+b d   - Detach session
```

**Reattach:**
```bash
tmux attach
```

**Custom config highlights:**

```bash
# Remap prefix to Ctrl+a
set -g prefix C-a
unbind C-b

# Enable mouse
set -g mouse on

# Pane borders
set -g pane-border-style 'fg=#666666'
set -g pane-active-border-style 'fg=#0dbc79'
```

### 3. Shell Plugins

**Extend functionality.**

**Zsh plugins (via Oh My Zsh or manual):**

**Useful plugins:**
- **zsh-autosuggestions** - Fish-like suggestions
- **zsh-syntax-highlighting** - Color commands
- **fzf** - Fuzzy finder integration
- **z** - Jump to frequent directories

**Install example (zsh-autosuggestions):**
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions

# Add to ~/.zshrc
source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
```

### 4. Custom Scripts and Functions

**Enhance prompt with scripts.**

**Example: Show Git branch in prompt (DIY):**

```bash
# In ~/.bashrc or ~/.zshrc

git_branch() {
  git branch 2>/dev/null | grep '^*' | colrm 1 2
}

# Use in prompt
export PS1='\u@\h \w $(git_branch) $ '
```

**More complex: Exit code indicator:**

```bash
exit_code() {
  if [ $? -eq 0 ]; then
    echo "✓"
  else
    echo "✗"
  fi
}
```

### 5. Dynamic Themes

**Change theme based on context.**

**Time-based (light during day, dark at night):**

```bash
# In ~/.zshrc

hour=$(date +%H)
if [ $hour -ge 8 ] && [ $hour -lt 18 ]; then
  # Daytime: light theme
  export THEME="light"
else
  # Nighttime: dark theme
  export THEME="dark"
fi
```

**Load corresponding Alacritty theme:**
```bash
alacritty-themes $THEME
```

**Or change Vim colorscheme:**
```bash
echo "colorscheme $THEME" > ~/.vim_theme
```

---

## Showcasing Your Setup

### 1. Screenshots

**Tools:**

**Linux:**
```bash
# Full terminal
scrot terminal.png

# Selected area
scrot -s terminal.png

# Or use maim
maim -s terminal.png
```

**macOS:**
```bash
# Cmd+Shift+4, then select window
```

**Tips:**
- Clean prompt (clear or reset)
- Show interesting command (neofetch, ls, vim)
- Good lighting (contrast visible)

### 2. Dotfiles Repository

**Share your configs on GitHub.**

**Structure:**
```
dotfiles/
├── alacritty/
│   └── alacritty.toml
├── zsh/
│   └── .zshrc
├── tmux/
│   └── .tmux.conf
├── starship/
│   └── starship.toml
└── README.md
```

**README should include:**
- Screenshot
- List of tools/versions
- Installation instructions
- Font requirements
- Credit/inspiration

**Symlink dotfiles:**
```bash
ln -s ~/dotfiles/alacritty/alacritty.toml ~/.config/alacritty/alacritty.toml
ln -s ~/dotfiles/zsh/.zshrc ~/.zshrc
```

### 3. Community Sharing

**Where to share:**

**Reddit:**
- **r/unixporn** - Show off your setup
- Read rules (required info in comments)
- Format: `[WM/DE] Desktop description`

**GitHub:**
- Tag: `dotfiles`, `terminal`, `theme`
- Add screenshot to README

**Blogs/Social:**
- Write setup guide
- Share process
- Inspire others

---

## Common Pitfalls

### Pitfall 1: Unreadable Colors

**Problem:**
Low contrast, can't see text.

**Solution:**
Test contrast. Use tools like contrastchecker.com.

### Pitfall 2: Too Much Information

**Problem:**
Prompt cluttered with unnecessary data.

**Solution:**
Minimize. Only show what you actually use.

### Pitfall 3: Slow Prompt

**Problem:**
Prompt takes 1+ seconds to render.

**Solution:**
- Use fast prompt (Starship, Powerlevel10k instant prompt)
- Avoid slow commands in prompt (network calls)

### Pitfall 4: Inconsistent Font Rendering

**Problem:**
Looks different on different monitors/OSes.

**Solution:**
Test on target environments. Stick to well-supported fonts.

### Pitfall 5: Not Portable

**Problem:**
Setup only works on your machine.

**Solution:**
- Use standard tools
- Document dependencies
- Test on fresh install

---

## Inspiration and Resources

### Color Scheme Resources

**Galleries:**
- **terminal.sexy** - Design and preview
- **iterm2colorschemes.com** - 200+ ready-made
- **base16-project.github.io** - Theme framework

**Tools:**
- **Alacritty themes** - GitHub repo with hundreds
- **Gogh** - Terminal color scheme installer (Linux)

### Dotfiles to Study

**GitHub searches:**
- `dotfiles alacritty`
- `dotfiles zsh starship`

**Notable examples:**
- Search "awesome dotfiles" on GitHub
- Look at r/unixporn top posts, check comments for repos

### Terminal Emulator Docs

- **Alacritty:** github.com/alacritty/alacritty
- **kitty:** sw.kovidgoyal.net/kitty
- **Wezterm:** wezfurlong.org/wezterm

### Prompt Frameworks

- **Starship:** starship.rs
- **Powerlevel10k:** github.com/romkatv/powerlevel10k
- **Oh My Zsh:** ohmyz.sh

---

## Example Configurations

### Example 1: Minimal Setup

**Goal:** Fast, clean, distraction-free.

**Terminal:** Alacritty  
**Shell:** Bash  
**Prompt:** Single line, `user@host path $`  
**Colors:** Solarized Dark  
**Font:** JetBrains Mono, 12pt

**Config:**

`~/.config/alacritty/alacritty.toml`:
```toml
[font]
size = 12
normal = { family = "JetBrains Mono" }

[colors.primary]
background = "#002b36"
foreground = "#839496"

# ... (Solarized colors)
```

`~/.bashrc`:
```bash
PS1='\u@\h \W $ '
```

### Example 2: Feature-Rich Developer Setup

**Goal:** Git integration, icons, status info.

**Terminal:** kitty  
**Shell:** Zsh + Oh My Zsh  
**Prompt:** Starship with git/time/exit code  
**Colors:** Dracula  
**Font:** FiraCode Nerd Font, 13pt  
**Extras:** tmux, zsh-autosuggestions

**Key features:**
- Ligatures for code
- Git status in prompt
- File icons in ls (via Nerd Font)
- Persistent tmux sessions

### Example 3: Retro/Hacker Aesthetic

**Goal:** Green-on-black, minimal, old-school.

**Terminal:** urxvt or st  
**Shell:** Bash  
**Prompt:** Simple `$` or `>`  
**Colors:** Green (#00ff00) on black (#000000)  
**Font:** Terminus (bitmap)

**Config:**

`~/.Xresources` (urxvt):
```
URxvt.background: #000000
URxvt.foreground: #00ff00
URxvt.font: xft:Terminus:size=12
URxvt.scrollBar: false
```

```bash
xrdb -merge ~/.Xresources
```

**Prompt:**
```bash
PS1='> '
```

---

## Exercises

### Exercise 1: Color Scheme From Scratch

**Task:** Design custom 16-color palette.

**Process:**
1. Choose background and foreground
2. Pick 8 colors (black through white)
3. Create brighter variants (8 more)
4. Test in terminal

**Tools:** terminal.sexy or hex color picker

### Exercise 2: Prompt Design

**Task:** Create custom prompt without frameworks.

**Requirements:**
- Show current directory
- Show Git branch (if in repo)
- Use colors

**Hint:** Bash/Zsh prompt escapes (check man pages).

### Exercise 3: Font Comparison

**Task:** Try 5 different fonts. Use each for 1 hour.

**Goal:** Find your favorite based on readability and aesthetics.

### Exercise 4: Dotfiles Repository

**Task:** Create GitHub repo with your configs.

**Include:**
- Terminal emulator config
- Shell config
- README with screenshot
- Installation script

### Exercise 5: Theme All Your Tools

**Task:** Match color scheme across terminal, Vim, tmux.

**Goal:** Consistent aesthetic across environment.

---

## Advanced Topics

### 1. True Color (24-bit) Support

**Enable millions of colors (not just 256).**

**Check support:**
```bash
echo $COLORTERM  # Should output "truecolor" or "24bit"
```

**Enable in tmux:**
```bash
# ~/.tmux.conf
set -g default-terminal "tmux-256color"
set -ga terminal-overrides ",*256col*:Tc"
```

**Benefits:**
- Smooth gradients
- Accurate color reproduction
- Better theme fidelity

### 2. Transparency and Blur

**Eye candy (or distraction, depending on taste).**

**Alacritty:**
```toml
[window]
opacity = 0.9
blur = true
```

**kitty:**
```
background_opacity 0.9
background_blur 10
```

**Considerations:**
- Readability over transparency
- Battery drain (GPU usage)
- Compositor required (Linux)

### 3. Keybinding Customization

**Remap keys for efficiency.**

**Alacritty example:**
```toml
[[keyboard.bindings]]
key = "V"
mods = "Control|Shift"
action = "Paste"

[[keyboard.bindings]]
key = "C"
mods = "Control|Shift"
action = "Copy"
```

### 4. Dynamic Titles

**Show current process in window title.**

**Bash:**
```bash
PROMPT_COMMAND='echo -ne "\033]0;${PWD##*/}\007"'
```

**Shows current directory name in title bar.**

---

## Conclusion

**Terminal design is:**
- Functional (usability matters)
- Aesthetic (beauty matters)
- Personal (your space)
- Iterative (evolve over time)

**Start simple:**
- Pick a color scheme you like
- Choose a readable font
- Configure basic prompt

**Evolve:**
- Tweak colors
- Add information to prompt
- Optimize keybindings
- Share with community

**Your terminal is your workspace. Make it yours.**

---

## Further Reading

**This Repository:**
- `/case-studies/contemporary/riced-linux-desktops.md` - Community and culture
- `/case-studies/contemporary/terminal-aesthetics-revival.md` - Modern tools
- `/essays/standalone/poetry-of-constraints.md` - Philosophy

**External:**
- **r/unixporn** - Community showcase
- **Starship docs** - starship.rs
- **Alacritty wiki** - GitHub wiki with themes

**Books:**
- *The Linux Command Line* by William Shotts (functionality)
- *Bash Guide for Beginners* (scripting prompts)

---

```
 _____ ____ __  __ ____    _    __  __  __   
|_   _| ___|  \/  |  _ \  / \  |  \/  |/ /_  
  | | | |_  | |\/| | | | |/ _ \ | |\/| | '_ \ 
  | | |  _| | |  | | |_| / ___ \| |  | | (_) |
  |_| |_|   |_|  |_|____/_/   \_\_|  |_|\___/ 
```

**Now design your terminal.**

---

**License:** CC0 1.0 Universal (Public Domain)  
**Author:** Digital Aesthetics Manifesto Contributors  
**Date:** November 19, 2025
