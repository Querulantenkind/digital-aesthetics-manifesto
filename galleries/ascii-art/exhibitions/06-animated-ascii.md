# Animated ASCII

**Curated by**: Digital Aesthetics Manifesto Community  
**Opening**: November 19, 2025  
**Theme**: Time-based ASCII art and animation

## Curatorial Statement

ASCII art doesn't have to be static. From the earliest days of computing, artists have explored animation—scrolling text, rotating shapes, morphing patterns. These works add the dimension of time to ASCII's spatial constraints.

Animated ASCII appears in terminal screensavers, demo scene productions, BBS animations, loading screens, and standalone art pieces. Some animations are loops—repeating patterns that mesmerize through rhythm. Others are narratives—telling stories frame by frame.

This exhibition presents animated ASCII works as static "film strips"—showing key frames and describing the motion. While this loses the temporal experience, it preserves the artistic ambition and technical achievement of animation in text.

*(Note: This is a curated documentation of animated works. To experience the animations themselves, see the supplementary files or visit the online gallery.)*

---

## Featured Works

### 1. Spinning Globe

**Frames** (8-frame loop, showing 4 representative frames):

```
Frame 1:          Frame 3:          Frame 5:          Frame 7:
    ___              ___               ___              ___
   /   \            /   \             /   \            /   \
  | :-: |          | .:. |           | -:- |          | .:. |
   \___/            \___/             \___/            \___/
```

**Artist**: Anonymous  
**Date**: 1996  
**Technique**: Character rotation  
**Frame count**: 8 frames  
**Loop duration**: ~2 seconds at 4 FPS

**Notes**: Simple but effective—three characters (: . -) rotate positions to create the illusion of a spinning sphere. The parentheses outline remains constant. This technique was popular in BBS loading screens.

---

### 2. Falling Rain

**Frames** (showing progression):

```
Frame 1:                Frame 2:                Frame 3:
                        |                       | |
  |   |                 |   |   |               |   |   |
|   |     |           |   |     |   |         |   |     |   |
    |   |   |             |   |   |   |           |   |   |   |
  |       |             |       |   |           |       |   |   |
                        |                       |       |
```

**Artist**: Unknown  
**Date**: 1998  
**Technique**: Vertical scroll with stagger  
**Frame count**: Infinite loop (procedural)  
**Speed**: 10 FPS

**Notes**: Each raindrop (vertical bar) descends one line per frame. New drops appear at top randomly. The staggered timing prevents synchronization, creating realistic rain effect. Demo scene classic.

---

### 3. Walking Stick Figure

**Frames** (8-frame walk cycle):

```
Frame 1:    Frame 2:    Frame 3:    Frame 4:    Frame 5:    Frame 6:    Frame 7:    Frame 8:
  \o/         \o          \o_         \o/          o/          o           o_          \o/
   |           |\          |           |           |           |\          |            |
  / \          | \         |\         / \         / \         / |          |\          / \
                 \           \                              \              \
```

**Artist**: "Animator_ASCII"  
**Date**: 2001  
**Technique**: Frame-by-frame animation  
**Frame count**: 8 frames  
**Loop duration**: 1 second at 8 FPS

**Notes**: Classic walk cycle—arms and legs alternate. The figure advances slightly each frame (though not shown here due to static presentation). Simple but requires careful attention to anatomy and timing.

---

### 4. Beating Heart

**Frames** (4-frame loop, showing all frames):

```
Frame 1:           Frame 2:           Frame 3:           Frame 4:
   _  _              _ _                _  _              _ __
  / \/ \            / V \              / \/ \            / VV \
  |    |            |    |             |    |            |    |
   \  /              \  /               \  /              \  /
    \/                \/                 \/                \/
```

**Artist**: Anonymous  
**Date**: 1997  
**Technique**: Expand/contract cycle  
**Frame count**: 4 frames  
**Loop duration**: 1 second at 4 FPS

**Notes**: The heart expands (frames 2-3) and contracts (frames 4-1), creating pulse effect. The V character at top center is key—it becomes VV when expanded. Simple symbol, powerful effect—especially popular for Valentine's Day email signatures.

---

### 5. Loading Bar

**Frames** (showing progression over 10 seconds):

```
Frame 1:     [          ] 0%
Frame 3:     [==        ] 20%
Frame 5:     [====      ] 40%
Frame 7:     [======    ] 60%
Frame 9:     [========  ] 80%
Frame 10:    [==========] 100% Complete!
```

**Artist**: System tool (generic)  
**Date**: 1990s-present  
**Technique**: Progressive fill  
**Frame count**: Variable (depends on process)  
**Speed**: Variable (reflects actual progress)

**Notes**: Not artistic per se, but ubiquitous functional animation. The progress bar is one of the most common animated ASCII elements—every command-line tool uses variants. The equals signs fill left-to-right as process completes.

---

### 6. Rotating Cube

**Frames** (12-frame rotation, showing 6 key frames):

```
Frame 1:        Frame 3:        Frame 5:        Frame 7:        Frame 9:        Frame 11:
    +---+           +---+           +---+          +---+           +---+           +---+
   /|  /|          /|  /|          /|  /|         /|  /|          /|  /|          /|  /|
  + +--+ |        + +--+ |        + +--+ |       + +--+ |        + +--+ |        + +--+ |
  |/   |/         |/   |/         |/   |/        |/   |/         |/   |/         |/   |/
  +----+          +----+          +----+         +----+          +----+          +----+
```

**Artist**: Demo scene collective  
**Date**: 1995  
**Technique**: Isometric projection with rotation  
**Frame count**: 12 frames  
**Loop duration**: 3 seconds at 4 FPS

**Notes**: The cube appears to rotate through subtle character shifts. The wireframe (plus signs at vertices, lines for edges) creates 3D illusion. Classic demo scene achievement—3D rotation in text mode.

---

### 7. Text Scroll

**Frames** (horizontal scroll showing message):

```
Frame 1:  [================================]
Frame 2:  [===============Welcome==========]
Frame 3:  [=======Welcome to===============]
Frame 4:  [Welcome to the==================]
Frame 5:  [to the BBS======================]
Frame 6:  [BBS! Enjoy your stay!===========]
Frame 7:  [Enjoy your stay! Enjoy==========]
Frame 8:  [stay! Enjoy your stay!==========]
(continues scrolling...)
```

**Artist**: BBS sysops (generic technique)  
**Date**: 1990s  
**Technique**: Horizontal text scroll  
**Frame count**: Variable (depends on message length)  
**Speed**: 2-5 FPS (readable pace)

**Notes**: Scrolling messages were common on BBS login screens and terminal apps. Text moves right-to-left (or left-to-right), wrapping continuously. The brackets frame the "window" through which the infinite scroll passes.

---

### 8. Bouncing Ball

**Frames** (showing trajectory):

```
Frame 1:      Frame 2:      Frame 3:      Frame 4:      Frame 5:      Frame 6:      Frame 7:
   o


                  o                            o                            o              o



___________   ___________   ___________   ___________   ___________   ___________   __o________
```

**Artist**: Unknown  
**Date**: 2000  
**Technique**: Parabolic motion  
**Frame count**: 14 frames (full bounce)  
**Loop duration**: ~2 seconds at 7 FPS

**Notes**: The ball (o) follows parabolic arc—rising, reaching apex, falling, bouncing off ground. Physics simulation in ASCII. Simple but satisfying—demonstrates how motion implies weight and gravity even with minimal graphics.

---

### 9. Typing Effect

**Frames** (showing text appearing letter by letter):

```
Frame 1:   >
Frame 3:   > Lo
Frame 5:   > Loading
Frame 7:   > Loading sy
Frame 9:   > Loading system
Frame 11:  > Loading system...
Frame 13:  > Loading system...
Frame 14:  > Loading system... _
Frame 16:  > Loading system... Done!
```

**Artist**: System tool (generic)  
**Date**: 1980s-present  
**Technique**: Sequential character reveal  
**Frame count**: Variable (depends on text length)  
**Speed**: 5-10 characters per second

**Notes**: Text appears character by character, often with blinking cursor (_). Common in terminal applications, installation scripts, and game interfaces. Creates anticipation and suggests live processing rather than pre-recorded output.

---

### 10. Morphing Face

**Frames** (5-frame morph from happy to sad):

```
Frame 1:        Frame 2:        Frame 3:        Frame 4:        Frame 5:
   O   O           O   O           O   O           O   O           O   O
     ‿               –               —               ‿               ︵
```

**Artist**: "EmoticonArtist"  
**Date**: 2004  
**Technique**: Emotional transition  
**Frame count**: 5 frames  
**Loop duration**: 2.5 seconds at 2 FPS (then reverses)

**Notes**: Simple emoticon morphs from happy (‿) to sad (︵) through neutral states. The eyes (O) remain constant—all expression is in the mouth. Minimal but effective emotional communication. Popular in instant messaging clients.

---

## Animation Techniques

### Frame-by-Frame

**Description**: Artist creates each frame manually, like traditional animation.

**Advantages**: Total control, can create complex narratives and expressions.

**Challenges**: Time-consuming, requires planning to maintain consistency.

**Uses**: Character animation, complex scenes, artistic expression.

### Procedural/Algorithmic

**Description**: Code generates frames based on rules—physics simulations, mathematical patterns, randomized elements.

**Advantages**: Can create infinite variations, smooth motion, responsive to input.

**Challenges**: Requires programming knowledge, less artistic control.

**Uses**: Screen savers, loading animations, abstract patterns, particle effects.

### Scrolling

**Description**: Static content moves across screen—horizontal (text scroll) or vertical (credits).

**Advantages**: Simple to implement, creates motion without redrawing entire frame.

**Challenges**: Limited to linear motion, can be monotonous.

**Uses**: Marquee text, credits, news tickers, BBS welcome screens.

### Cycling

**Description**: Small set of frames (2-8) loops continuously—rotating, blinking, pulsing.

**Advantages**: Minimal frames needed, effective for suggesting continuous motion.

**Challenges**: Can feel repetitive if loop is too short or obvious.

**Uses**: Loading indicators, idle animations, background elements.

### Sprite Movement

**Description**: Characters or objects move against static background.

**Advantages**: Efficiency—only moving elements redraw, background persists.

**Challenges**: Requires careful coordinate tracking, potential for artifacts.

**Uses**: Games, cursors, flying objects, walking characters.

---

## Technical Considerations

### Frame Rate

**Low (1-2 FPS)**: Suitable for slow transitions, text typing, status changes.

**Medium (3-5 FPS)**: Good for walking, simple motion, emotional expressions.

**High (6-10 FPS)**: Smooth motion, physics simulations, game animation.

**Very High (10+ FPS)**: Rarely needed for ASCII—can cause flicker, may not improve perception.

### Buffer Management

**Double buffering**: Draw next frame in memory, then swap to display. Prevents flicker and tearing.

**Dirty rectangles**: Only redraw regions that changed. Improves performance.

**Clear and redraw**: Simplest approach—clear screen, redraw everything. Can cause flicker.

### Timing

**Fixed time step**: Same delay between all frames. Predictable but may lag on slow systems.

**Variable time step**: Adjust for system performance. Smoother but requires calculation.

**V-sync**: Synchronize with display refresh. Smoothest but not always available in terminals.

### Tools and Formats

**ANSI animation**: Uses ANSI escape codes to position cursor and change colors. Common in BBS scene.

**ASCIIMation**: Web-based format for ASCII animations with frame timing.

**Terminal control codes**: Direct cursor manipulation—fast but not portable across systems.

**Video conversion**: Convert video to ASCII frames—automated but often low quality.

---

## Historical Context

**1970s-80s**: Mainframe and minicomputer animations—bouncing balls, text scrolls, screen savers.

**1980s-90s**: BBS animations—welcome screens, transitions, loading indicators. Demo scene ASCII animations.

**1990s**: ANSI art competitions included animated categories. Tools like TheDraw enabled animation creation.

**2000s**: Web-based ASCII animation tools (ASCIIMation). Animated GIFs of ASCII art.

**2010s**: Terminal-based games (roguelikes, NetHack) continued animation tradition. ASCII art in VJing and live coding performances.

**Present**: Generative ASCII animations in art installations, ASCII video filters in streaming, animated ASCII in terminal UIs.

---

## Why Animation Matters

**Adds dimension**: Time becomes part of the artwork—reveals, conceals, transforms.

**Creates narrative**: Sequential frames tell stories impossible in static images.

**Demonstrates mastery**: Animation requires technical skill beyond single-frame work.

**Engages viewer**: Motion draws attention, holds interest, creates emotional response.

**Explores medium**: Tests ASCII's limits—how much motion can text convey?

---

## Experiencing Animated ASCII

Since this exhibition presents static frames, we recommend:

1. **View supplementary files**: Many of these animations are recreated as playable files in `/galleries/ascii-art/animations/`

2. **Visit online archives**: Sites like ASCII Art Archive and The ANSI Archive host playable animations

3. **Create your own**: Use tools like:
   - `watch` command (Linux/Mac) to repeatedly run scripts
   - `asciimatics` (Python library) for animation creation
   - Terminal multiplexers with scripting support

4. **Study frame-by-frame**: Even without motion, analyzing frames teaches timing, spacing, and transformation principles

---

## Related Exhibitions

- **[Abstract Geometries](03-abstract-geometries.md)** - Many abstract patterns suggest motion even when static
- **[The Golden Age: 1990s ASCII](04-golden-age-1990s.md)** - BBS animations from the era
- **Main ASCII Gallery**: `/galleries/ascii-art/COLLECTION.md` - Includes links to animated works

---

## Further Exploration

**Tools**:
- ASCIIMation (web-based animator)
- asciimatics (Python library)
- blessed (Python terminal library with animation support)
- AAlib (ASCII art library with video conversion)

**Archives**:
- The ANSI Archive (16colors.net)
- ASCII Art Archive
- Demo scene archives (pouet.net)

**Communities**:
- Terminal animation subreddits
- Demo scene forums
- ASCII art Discord servers

---

**Exhibition organized by**: Digital Aesthetics Manifesto Community  
**Last updated**: November 19, 2025  
**License**: Individual works retain original artists' rights where known; exhibition curation CC-BY-SA 4.0

---

## Curator's Note

This exhibition is necessarily limited by the static medium of documentation. Animated ASCII truly lives in motion—in terminals, on screens, in time. We encourage viewers to seek out living examples of these works and to create their own animations. The techniques are accessible, the tools are available, and the creative possibilities are endless.

Text doesn't have to sit still.
