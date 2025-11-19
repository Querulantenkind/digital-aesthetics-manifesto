# Documentation as Art: Collection

## Introduction

This collection celebrates documentation that transcends mere utility—READMEs, man pages, API docs, and comments that are carefully crafted, beautifully formatted, and genuinely helpful works of art.

Great documentation is invisible when everything works, but invaluable when something breaks. These examples show that technical writing can be elegant, even poetic.

---

## Classic Man Pages

### 1. man ascii

```
ASCII(7)                Linux Programmer's Manual               ASCII(7)

NAME
       ascii - ASCII character set encoded in octal, decimal, and hexadecimal

DESCRIPTION
       ASCII  is the American Standard Code for Information Interchange.
       It is a 7-bit code. Many 8-bit codes (e.g., ISO 8859-1, the  Linux
       default  character  set)  contain  ASCII as their lower half.  The
       international counterpart of ASCII is known as ISO 646.

       The following table contains the 128 ASCII characters.

       Oct   Dec   Hex   Char   Description
       ───────────────────────────────────────────────────
       000   0     00    NUL    '\0' (null character)
       001   1     01    SOH    (start of heading)
       002   2     02    STX    (start of text)
       ...
       040   32    20    SP     (space)
       041   33    21    !      (exclamation mark)
       ...
       101   65    41    A
       102   66    42    B
       ...
```

**Why it's art:**
- Clean, organized table
- Three numbering systems side-by-side
- Concise descriptions
- Historical context included
- Perfectly formatted for 80-column terminals

**Philosophy:** Reference documentation at its finest—comprehensive, clear, timeless.

---

### 2. man hier (Filesystem Hierarchy)

```
HIER(7)                Linux Programmer's Manual               HIER(7)

NAME
       hier - description of the filesystem hierarchy

DESCRIPTION
       A typical Linux system has, among others, the following directories:

       /      This is the root directory.  This is where the whole tree starts.

       /bin   This  directory contains executable programs which are needed in
              single user mode and to bring the system up or repair it.

       /boot  Contains static files for the boot loader.  This directory holds
              only the files which are needed during the boot process.

       /dev   Special or device files, which refer to physical devices.

       /etc   Contains configuration files which are local to the machine.

       /home  On machines with home directories for users, these are usually
              beneath this directory, directly or not.  The structure of this
              directory depends on local administration decisions (optional).

       /lib   This directory should hold those shared libraries that are 
              necessary to boot the system and to run the commands in the root
              filesystem.
       ...
```

**Why it's exemplary:**
- Explains the implicit (filesystem structure)
- Organized alphabetically
- Consistent structure (name, then description)
- Canonical reference for 50+ years

**Impact:** Generations of developers learned Unix structure from this man page.

---

### 3. man ascii-art (Hypothetical—But Should Exist!)

*(This doesn't exist in most systems, but imagine if it did...)*

```
ASCII-ART(7)            Linux User's Manual            ASCII-ART(7)

NAME
       ascii-art - creating visual art with ASCII characters

DESCRIPTION
       ASCII art is the practice of creating images using only the 95
       printable characters defined by the ASCII standard (plus space).

       Common techniques include:

       Line Art    Using characters like | - / \ + to draw outlines
       Density     Using .:-=+*#%@ for shading (light to dark)
       Typography  Arranging letters/words to form shapes

       Example:
              |\__/,|   (`\
            _.|o o  |_   ) )
          -(((---(((--------

SEE ALSO
       unicode(7), figlet(6), cowsay(1), toilet(1)
```

**Why this would be great:**
- Explains cultural practice through official documentation
- Legitimizes art form
- Provides entry point for curious users

---

## Beautiful READMEs

### 4. The Poetic README (lodash)

```markdown
# lodash

The Lodash library exported as a UMD module.

Generated using lodash-cli:
$ npm run build
$ lodash -o ./dist/lodash.js
$ lodash core -o ./dist/lodash.core.js

## Installation

In a browser:
```html
<script src="lodash.js"></script>
```

Using npm:
```shell
$ npm i lodash
```

In Node.js:
```js
const _ = require('lodash');
```
\`\`\`

**Why it works:**
- Shows multiple installation methods
- Code examples for each environment
- Clean, scannable structure
- Gets out of your way quickly

---

### 5. The Narrative README (curl)

```markdown
# curl

curl is a command line tool for transferring data specified with URL syntax.

## History

curl was first released in 1998. That makes it older than most of the
internet as we know it. It has been used for decades, shipped by virtually
every OS, installed on billions of devices.

## What Does curl Do?

curl transfers data from or to a server. It supports HTTP, HTTPS, FTP,
FTPS, SCP, SFTP, TFTP, LDAP, LDAPS, FILE, POP3, IMAP, SMB, SMTP, and more.

curl is powered by libcurl for all transfer-related features.

## Features

- **Protocols**: All the protocols
- **Performance**: Lightning fast
- **Portable**: Runs everywhere
- **Standards**: Follows RFCs meticulously
- **Well-tested**: Massive test suite
```

**Why it's effective:**
- Tells a story (historical context)
- Explains "why" not just "what"
- Lists features with personality
- Pride in craft is evident

**Lesson:** Good documentation has a voice.

---

### 6. The Visual README (Rich, Python library)

```markdown
# Rich

Rich is a Python library for rich text and beautiful formatting in the terminal.

╭───────────────────── Features ─────────────────────╮
│ • Rich syntax highlighting                        │
│ • Beautiful tracebacks                            │
│ • Progress bars that actually look good           │
│ • Tables, trees, columns, panels                  │
│ • Markdown rendering in the terminal              │
│ • And much more!                                  │
╰────────────────────────────────────────────────────╯

## Quick Start

```python
from rich import print

print("[bold magenta]Hello[/bold magenta] World!")
```

Output:
**Hello** World! (in magenta)
\`\`\`

**Why it's art:**
- Uses its own features in the README (dogfooding)
- Box-drawing for visual interest
- Color/formatting in examples
- Shows, doesn't just tell

---

## API Documentation

### 7. Stripe API Docs

```markdown
## Create a Charge

POST https://api.stripe.com/v1/charges

Creates a charge on a customer's card.

### Parameters

| Parameter   | Type    | Description                              |
|-------------|---------|------------------------------------------|
| amount      | integer | Amount in cents (required)               |
| currency    | string  | Three-letter ISO code (required)         |
| source      | string  | Payment source token (required)          |
| description | string  | Arbitrary description (optional)         |

### Returns

Returns a charge object if the charge succeeded. Throws an error otherwise.

### Example Request

```shell
curl https://api.stripe.com/v1/charges \
  -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
  -d amount=2000 \
  -d currency=usd \
  -d source=tok_visa \
  -d description="Charge for jenny.rosen@example.com"
```

### Example Response

```json
{
  "id": "ch_1EqL2G2eZvKYlo2C8ZqXSCrP",
  "object": "charge",
  "amount": 2000,
  "currency": "usd",
  "status": "succeeded"
}
```
\`\`\`

**Why it's exemplary:**
- Clear structure (params → returns → example)
- Includes curl example (immediately usable)
- Shows both request and response
- Error cases documented

**Standard:** Many API docs follow this pattern now (because it works).

---

### 8. Unix Philosophy in Docs (cat man page)

```
CAT(1)                   User Commands                  CAT(1)

NAME
       cat - concatenate files and print on the standard output

SYNOPSIS
       cat [OPTION]... [FILE]...

DESCRIPTION
       Concatenate FILE(s) to standard output.

       With no FILE, or when FILE is -, read standard input.

       -n, --number
              number all output lines

       -b, --number-nonblank
              number nonempty output lines, overrides -n

EXAMPLES
       cat f - g
              Output f's contents, then standard input, then g's contents.

       cat    Copy standard input to standard output.

SEE ALSO
       tac(1), rev(1)
```

**Why it's philosophy:**
- Simple tool, simple docs
- Examples show Unix composition (`-` for stdin)
- Cross-references related tools
- Embodies "do one thing well"

---

## Inline Comments as Literature

### 9. Linux Kernel Comments (Linus Torvalds)

```c
/*
 * This is the main, per-schedule-entity walking of the tree.
 *
 * The "interesting" case is when we find a queued entity in the tree
 * that is currently running on the CPU - in which case we need to
 * select the "next" thing to run.
 *
 * Don't even ask me what this does, I'm just typing what I see.
 */
```

**Why it's honest:**
- Last line is self-deprecating humor
- Explains "why" (intent) not "what" (obvious from code)
- Human voice in technical documentation

---

### 10. Source Code Poems (DOOM engine)

```c
//
// P_CheckPosition
// This is purely informative, nothing is modified
// (except things picked up).
// 
// in:
//  a mobj_t (can be valid or invalid)
//  a position to be checked
//   (doesn't need to be related to the mobj_t->x,y)
//
// during:
//  special things are touched if MF_PICKUP
//  early out on solid lines?
//
// out:
//  newsubsec
//  floorz
//  ceilingz
//  tmdropoffz
//   the lowest point contacted
//   (monsters won't move to a dropoff)
//  speciallines[]
//  numspeciallines
//
```

**Why it's beautiful:**
- Structured like a play (in: during: out:)
- Clear contract of function
- Parenthetical asides (human thinking visible)

---

### 11. NASA Code Comments

```c
/*
 * This code is executed when the spacecraft is in launch ascent.
 * Lives depend on this working correctly.
 * 
 * DO NOT MODIFY without full review by guidance team.
 * Last modified: 1969-07-16
 * Reviewer: Margaret Hamilton
 * Test status: Passed 1000 simulations
 */
```

**Why it's powerful:**
- Context (literal life-or-death stakes)
- Attribution (who to ask)
- Test status (confidence level)
- Humility (respect for consequences)

**Lesson:** Comments can carry weight, history, responsibility.

---

## Error Messages as UX

### 12. Rust Compiler Errors

```
error[E0382]: use of moved value: `s`
 --> main.rs:5:20
  |
3 |     let s = String::from("hello");
  |         - move occurs because `s` has type `String`
4 |     takes_ownership(s);
  |                     - value moved here
5 |     println!("{}", s);
  |                    ^ value used here after move
  |
  = note: move occurs because `String` does not implement the `Copy` trait

help: consider cloning the value if the performance cost is acceptable
  |
4 |     takes_ownership(s.clone());
  |                      ++++++++
```

**Why it's art:**
- Shows exact location with carets (^)
- Explains what happened and why
- Suggests fix with example
- Educational (teaches language concepts)

**Impact:** Rust's errors helped make the language accessible.

---

### 13. Git Error Messages (with humor)

```
$ git push origin master
To github.com:user/repo.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'github.com:user/repo.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

**Why it's helpful:**
- Explains problem (remote has changes)
- Suggests solution (pull first)
- Points to documentation (man page)
- Polite tone ("you may want to")

---

## Changelogs as Narrative

### 14. Semantic Versioning Changelog

```markdown
# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/),
and this project adheres to [Semantic Versioning](https://semver.org/).

## [2.0.0] - 2023-11-20

### Added
- New `exportToCSV()` function for data export
- Dark mode support
- Keyboard shortcuts (see docs/shortcuts.md)

### Changed
- **BREAKING**: Renamed `getData()` to `fetchData()` for clarity
- Improved error handling in API module
- Updated dependencies (see package.json)

### Fixed
- Fixed crash when loading empty datasets
- Corrected timezone handling in date parser

### Removed
- **BREAKING**: Removed deprecated `oldFunction()` (use `newFunction()`)

## [1.5.1] - 2023-10-15

### Fixed
- Hotfix for login redirect bug
```

**Why it's exemplary:**
- Structured (Added/Changed/Fixed/Removed)
- Version numbers + dates
- Breaking changes clearly marked
- Links to relevant documentation

---

### 15. Human Changelog (curl example)

```markdown
## Version 8.5.0 - Nov 20, 2023

This release includes the following changes:

- We fixed the bug where cookies weren't handled correctly in redirects. 
  Sorry about that—turns out edge cases really do happen at the edge!

- Added support for... [technical details]

- Daniel spent 3 weeks tracking down a race condition. It's fixed now.
  We celebrated with cake.

As always, thanks to the 47 contributors who made this release possible.
```

**Why it's human:**
- Acknowledges mistakes (transparency)
- Shows personality (cake!)
- Gratitude for contributors
- Technical + social information

---

## Tutorials and Guides

### 16. The Gentle Introduction (Django Tutorial)

```markdown
## Your First Django App

Let's learn by example.

Throughout this tutorial, we'll walk you through the creation of a basic
poll application. It'll consist of two parts:

- A public site that lets people view polls and vote
- An admin site that lets you add, change, and delete polls

We'll assume you have Django installed already. You can tell Django is
installed and which version by running:

$ python -m django --version

If Django is installed, you should see the version. If it isn't, you'll
get "No module named django".

This tutorial is written for Django 5.0 and Python 3.10 or later.
```

**Why it's welcoming:**
- "Let's learn by example" (inviting tone)
- Concrete project (not abstract)
- Prerequisites stated clearly
- Verification step (check install)

---

### 17. The Reference Card (Git)

```
Git Quick Reference

Setup
  git init                Create repository
  git clone <url>         Clone repository

Changes
  git status              Check status
  git add <file>          Stage file
  git commit -m "msg"     Commit staged

Branches
  git branch              List branches
  git branch <name>       Create branch
  git checkout <branch>   Switch branch
  git merge <branch>      Merge branch

Remote
  git pull                Fetch + merge
  git push                Push commits
  git remote -v           List remotes

Undo
  git reset <file>        Unstage file
  git checkout -- <file>  Discard changes
  git revert <commit>     Revert commit
```

**Why it's useful:**
- One page, everything you need
- Command + description
- Grouped by function
- Perfect for printing

---

## ASCII Art in Documentation

### 18. Architecture Diagrams (in README)

```
                    ┌─────────────┐
                    │   Browser   │
                    └──────┬──────┘
                           │ HTTPS
                           ▼
                    ┌─────────────┐
                    │  Nginx      │ (Load Balancer)
                    └──────┬──────┘
                           │
              ┌────────────┼────────────┐
              ▼            ▼            ▼
         ┌────────┐   ┌────────┐   ┌────────┐
         │ App 1  │   │ App 2  │   │ App 3  │
         └────┬───┘   └────┬───┘   └────┬───┘
              │            │            │
              └────────────┼────────────┘
                           ▼
                    ┌─────────────┐
                    │  Database   │
                    │  (Postgres) │
                    └─────────────┘
```

**Why it's effective:**
- Shows architecture at a glance
- No external tool required (plain text)
- Version controlled with code
- Visible in terminal

---

### 19. Data Flow Diagrams

```
   Input File
       │
       ▼
  ┌─────────┐
  │ Parser  │
  └────┬────┘
       │ (AST)
       ▼
  ┌─────────┐
  │Validator│
  └────┬────┘
       │ (Validated AST)
       ▼
  ┌─────────┐
  │Compiler │
  └────┬────┘
       │ (Bytecode)
       ▼
  ┌─────────┐
  │   VM    │
  └────┬────┘
       │
       ▼
   Output
```

**What it shows:**
- Data transformations (AST → Validated AST → Bytecode)
- Pipeline stages
- Flow of execution

---

## Documentation Philosophy

### What makes documentation art?

**1. Clarity**
- Says what it means
- Means what it says
- No ambiguity

**2. Empathy**
- Written for the reader, not the author
- Anticipates questions
- Meets users where they are

**3. Completeness**
- All the information needed
- Nothing extraneous
- Appropriate depth

**4. Beauty**
- Pleasant to read
- Well-formatted
- Visually organized

**5. Maintainability**
- Easy to update
- Version-controlled
- Living document (not abandoned)

---

## Further Exploration

**In this repository:**
- `/galleries/documentation-as-art/annotated-examples.md` - Deep analysis
- `/galleries/documentation-as-art/artist-statements.md` - Philosophy

**External:**
- **Write the Docs** - Conference and community
- **The Documentation System** (Divio) - 4 types of docs
- **Style guides:** Google, Microsoft, Apple

---

**Good documentation is an act of care—for your users, your collaborators, and your future self.**

---

**License:** CC-BY-SA 4.0 International  
**Curator:** Digital Aesthetics Manifesto Contributors  
**Date:** November 19, 2025
