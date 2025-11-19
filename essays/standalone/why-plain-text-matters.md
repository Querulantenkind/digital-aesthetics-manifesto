# Why Plain Text Matters: Longevity and Accessibility

## Introduction

In 1978, someone wrote a text file.

In 2025, you can still read it. No conversion needed. No special software. No emulation. Just open it and read.

Try that with a Microsoft Word document from 1995. Or a PageMaker file from 1990. Or a WordPerfect document from 1985. Good luck.

Plain text endures.

This essay argues that plain text is not a compromise or a limitation—it's the most robust, accessible, and future-proof way to store information. In a digital world of constant obsolescence, plain text is the bedrock.

---

## What Is Plain Text?

### Definition

Plain text is text encoded in a simple character encoding (ASCII, UTF-8) with no formatting, styling, or embedded objects. Just characters.

**Plain text:**
```
This is plain text.
It has no formatting.
```

**Not plain text:**
- Microsoft Word (.docx) - Binary format with embedded XML
- PDF - Complex format with fonts, layout, rendering instructions
- Rich Text Format (.rtf) - Includes formatting codes
- HTML with styling - Markup and presentation mixed

### Why the Distinction Matters

Plain text files are:
- **Human-readable** - Open in any text editor
- **Machine-readable** - Easy to parse and process
- **Cross-platform** - Works on any operating system
- **Version-controllable** - Git and other VCS work perfectly
- **Future-proof** - Will work decades from now

Formatted documents require:
- Specific software (often proprietary)
- Compatible versions
- Correct fonts and resources
- Rendering engines

They're fragile. Plain text is robust.

---

## The Problem with Formatted Documents

### Proprietary Formats

**Microsoft Word (.doc/.docx):**
- Requires Microsoft Office (or complex reverse-engineering)
- Format changes between versions
- Fonts may not be available
- Macros may not work
- Corruption is common

**Adobe PDF:**
- "Portable" in name, complex in reality
- Difficult to edit
- Accessibility issues (screen readers struggle)
- DRM can lock documents
- Large file sizes

**Pages, WordPerfect, QuarkXPress, etc.:**
- Proprietary formats
- Software may be discontinued
- Old files become unreadable

### The Obsolescence Problem

**Timeline:**
- **1980s:** WordStar - dominant word processor
  - **2025:** Files difficult to read
- **1990s:** WordPerfect - market leader
  - **2025:** Software mostly gone, format obscure
- **2000s:** Microsoft Office dominance
  - **2025:** Old .doc files often have compatibility issues
- **2010s:** Cloud documents (Google Docs, Office 365)
  - **Future:** What happens when the company shuts down?

**Plain text from any of these eras:** Still perfectly readable.

### Vendor Lock-In

Proprietary formats create dependency:
- You must keep using the software
- You must pay for upgrades
- You can't easily switch to alternatives
- Your data is hostage

Plain text has no vendor. It belongs to everyone and no one.

---

## The Advantages of Plain Text

### 1. Longevity

**Plain text from 1970s Unix systems:** Still readable today.

**Text from 1950s teletypes:** If you have it, you can read it.

**Future:** As long as computers process text, plain text will work.

No other digital format has this track record.

### 2. Universality

Plain text works on:
- Any operating system (Linux, macOS, Windows, BSD, etc.)
- Any device (computers, phones, tablets, e-readers)
- Any editor (Notepad, Vim, Emacs, VSCode, nano, etc.)
- Any context (terminals, GUIs, web browsers)

Write once, read anywhere. Actually.

### 3. Size Efficiency

**Plain text:** Tiny.
- This essay: ~15 KB as .txt
- Average book: 300-500 KB as .txt

**Compare:**
- Same text as .docx: 3-5× larger (embedded XML, metadata)
- As PDF: 5-10× larger (fonts, rendering info)
- As webpage with images/CSS: 10-50× larger

Plain text respects bandwidth, storage, and the environment.

### 4. Searchability

**Plain text:** Every word is searchable.
- `grep` searches instantly
- Full-text search is trivial
- No special tools needed

**PDFs:** Searchable only if OCRed or properly created  
**Word docs:** Need compatible software to search  
**Scanned documents:** Not searchable at all (unless OCRed)

### 5. Version Control

Plain text works perfectly with Git and other version control systems:

**Track changes:**
```
- Old text
+ New text
```

**Collaborate:**
- Multiple people edit
- Merge changes
- View history
- Revert if needed

**Binary formats:** Git can't diff them. You see "file changed" but not *what* changed.

### 6. Automation and Processing

Plain text is scriptable:

**Transform:**
```bash
sed 's/old/new/g' file.txt
```

**Filter:**
```bash
grep "keyword" *.txt
```

**Combine:**
```bash
cat *.txt > combined.txt
```

**Count:**
```bash
wc -w file.txt
```

Try doing that with Word documents.

### 7. Privacy

Plain text files:
- Contain no hidden metadata (no author, edit times, tracked changes)
- Can't phone home
- Can't execute malicious code
- Are transparent

Word documents can embed:
- Your name and computer ID
- Edit history
- Hidden tracked changes
- Macros (potential malware)

### 8. Accessibility

Plain text works with:
- Screen readers (perfect compatibility)
- Braille displays
- Text-to-speech
- Large print displays
- Any assistive technology

Rich formats often break accessibility.

---

## Plain Text in Practice

### Writing

**Use plain text for:**
- Notes and thoughts
- Drafts of articles, essays, stories
- Research and documentation
- Personal journals
- Lists and reminders

**Tools:**
- Any text editor (Vim, Emacs, Notepad++, VSCode, Sublime)
- Mobile apps (iA Writer, 1Writer, Drafts)
- Sync via Dropbox, Syncthing, or Git

### Documentation

**Plain text formats:**
- **Markdown** - Simple formatting (headings, lists, links)
- **AsciiDoc** - More features, still readable as text
- **Org-mode** - Emacs outlining and planning
- **reStructuredText** - Python documentation

All are:
- Readable without rendering
- Convertible to HTML, PDF, etc.
- Version-controllable
- Future-proof

**Examples:**
- Most open source projects use Markdown READMEs
- This manifesto is written in Markdown
- Programming language docs (Python uses reStructuredText)

### Code

Source code is plain text. This is not accidental.

**Benefits:**
- Git works perfectly
- Any editor works
- `grep`, `sed`, `awk` all work
- Cross-platform collaboration
- No compilation needed to read

Imagine if code were in Word documents. Absurd.

### Communication

**Plain text email:**
- Works on all email clients
- No HTML rendering issues
- No tracking pixels
- Faster to load
- More private

**Markdown in messages:**
- Many tools support it (Slack, Discord, GitHub, Reddit)
- Simple formatting without rich text complexity

### Data

**CSV (Comma-Separated Values):**
Plain text format for tabular data:
```
name,age,city
Alice,30,Seattle
Bob,25,Portland
```

**JSON (JavaScript Object Notation):**
Plain text for structured data:
```json
{
  "name": "Alice",
  "age": 30,
  "city": "Seattle"
}
```

**YAML:**
Plain text for configuration:
```yaml
name: Alice
age: 30
city: Seattle
```

All human-readable, all version-controllable, all future-proof.

### Configuration

System and application configs as plain text:
- `.bashrc`, `.vimrc`, `.gitconfig`
- `nginx.conf`, `sshd_config`
- `package.json`, `requirements.txt`

**Benefits:**
- Edit with any editor
- Track changes in Git
- Share "dotfiles" with others
- Understand what's configured

---

## Markdown: Plain Text with Light Structure

Markdown bridges plain text and formatted documents.

### What Is Markdown?

Lightweight markup language created by John Gruber (2004).

**Syntax:**
```markdown
# Heading 1
## Heading 2

**Bold** and *italic*

- List item
- Another item

[Link text](https://example.com)

`code` and ```code blocks```
```

**Readable as plain text**, but can be converted to:
- HTML
- PDF
- DOCX (if you must)
- Presentations (with tools like reveal.js)

### Why Markdown Matters

**Simple enough** for anyone to learn  
**Powerful enough** for documentation  
**Widespread** - GitHub, Reddit, Discord, Slack, many blogs  
**Future-proof** - It's just text

**This manifesto is written in Markdown.**

### Tools

- **Editors:** VSCode, Typora, iA Writer, Bear, Obsidian
- **Static site generators:** Jekyll, Hugo, 11ty
- **Converters:** Pandoc (Markdown → anything)
- **Viewers:** Built into GitHub, GitLab, etc.

---

## When Plain Text Isn't Enough

### Legitimate Use Cases for Rich Formats

**Print design:**
- Magazines, books, brochures
- Fine typography control needed
- Use: InDesign, LaTeX, Scribus

**Legal documents:**
- Signatures, official forms
- Use: PDF (but generate from plain text when possible)

**Presentations:**
- Visual slides
- Use: reveal.js (from Markdown), LaTeX Beamer, or PowerPoint if necessary

**Complex layouts:**
- Infographics, posters
- Use: Design software (Inkscape, Figma, etc.)

**But even then:**
- Start with plain text (outline, content, data)
- Apply formatting last
- Keep a plain text master copy

### The Principle

**Content should be plain text.**  
**Formatting should be a presentation layer.**

Separate content from presentation.

---

## How to Adopt Plain Text

### 1. Start Small

Don't convert everything at once.

**Begin with:**
- New notes and drafts
- Personal writing
- Lists and reminders

### 2. Learn Basic Markdown

30 minutes to learn, lifetime of use.

**Essential syntax:**
- `# Headings`
- `**bold**`, `*italic*`
- `- list items`
- `[links](url)`
- `` `code` ``

That's 90% of what you need.

### 3. Choose a Text Editor

Find one you like:
- **Simple:** Notepad (Windows), TextEdit (macOS), gedit (Linux)
- **Powerful:** Vim, Emacs, Sublime Text, VSCode
- **Focused writing:** iA Writer, Typora, Bear

Use what feels comfortable.

### 4. Set Up Sync

**Options:**
- Dropbox, Google Drive (for simple sync)
- Git + GitHub/GitLab (for version control)
- Syncthing (peer-to-peer, privacy-respecting)
- iCloud Drive (Apple ecosystem)

Plain text is tiny—sync is trivial.

### 5. Convert Gradually

**Don't rush.**

When you need to reference an old document:
- Open it
- Copy content to plain text
- Save as .txt or .md
- Delete or archive the original

Over time, your important documents become plain text.

### 6. Use Pandoc for Conversion

When you must produce formatted output:

```bash
pandoc input.md -o output.pdf
pandoc input.md -o output.docx
pandoc input.md -o output.html
```

**Source:** Plain text (Markdown)  
**Output:** Whatever format needed  
**Master copy:** Always plain text

---

## The Philosophy of Plain Text

### Minimalism

Plain text embodies digital minimalism:
- No excess
- No bloat
- Only what's necessary
- Form follows function

### Transparency

You can always see what's there:
- No hidden formatting
- No embedded scripts
- No mysterious metadata
- What you see is what you get (truly)

### Ownership

Plain text is **yours**:
- No vendor controls it
- No subscription required
- No software license needed
- No one can take it away

### Respect

Plain text respects:
- **Your time** - Fast to open, fast to search
- **Your bandwidth** - Small file sizes
- **Your privacy** - No tracking, no metadata
- **Your future** - Will work forever

---

## Plain Text as Resistance

In a world of:
- Planned obsolescence
- Vendor lock-in
- Surveillance capitalism
- Bloated software

Plain text is resistance.

**It says:**
- I value longevity over features
- I choose independence over convenience
- I prioritize substance over style
- I respect the future

---

## Conclusion

Plain text is not a limitation. It's a **superpower**.

It's:
- **Immortal** - Works forever
- **Universal** - Works everywhere
- **Efficient** - Tiny and fast
- **Searchable** - Every word findable
- **Versionable** - Perfect for Git
- **Automatable** - Scripts work perfectly
- **Private** - No hidden data
- **Accessible** - Works with all assistive tech
- **Independent** - No vendor lock-in

Your words matter. Your ideas matter. Your data matters.

Don't lock them in formats that will become unreadable.  
Don't trust corporations to preserve your work.  
Don't let software obsolescence erase your history.

Write in plain text.  
Store in plain text.  
Archive in plain text.

**It will outlast everything else.**

---

## Resources

### Editors

**Simple:**
- Notepad (Windows)
- TextEdit (macOS - set to plain text mode)
- gedit, nano (Linux)

**Advanced:**
- Vim: https://www.vim.org/
- Emacs: https://www.gnu.org/software/emacs/
- VSCode: https://code.visualstudio.com/
- Sublime Text: https://www.sublimetext.com/

**Writing-focused:**
- iA Writer: https://ia.net/writer
- Typora: https://typora.io/
- Bear: https://bear.app/
- Obsidian: https://obsidian.md/

### Markdown

- Markdown Guide: https://www.markdownguide.org/
- CommonMark spec: https://commonmark.org/
- Pandoc (converter): https://pandoc.org/

### Sync and Backup

- Syncthing: https://syncthing.net/ (P2P sync)
- Git: https://git-scm.com/
- rsync: Built into Unix/Linux systems

### Philosophy

- Derek Sivers, "Write plain text files": https://sive.rs/plaintext
- Steph Ango, "File over app": https://stephango.com/file-over-app

---

**Essay**: Standalone  
**Author**: Digital Aesthetics Manifesto Contributors  
**Date**: November 19, 2025  
**License**: CC-BY-SA 4.0
