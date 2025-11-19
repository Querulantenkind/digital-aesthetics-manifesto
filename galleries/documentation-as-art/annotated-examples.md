# Documentation as Art: Annotated Examples

## Introduction

This document provides deep analysis of exemplary documentation, examining line-by-line what makes it effective, beautiful, and user-centered.

---

## Example 1: The Curl Man Page

### Full Text (Abbreviated)

```
CURL(1)                    Curl Manual                    CURL(1)

NAME
       curl - transfer a URL

SYNOPSIS
       curl [options / URLs]

DESCRIPTION
       curl  is  a tool for transferring data from or to a server using one of
       the supported protocols (DICT, FILE, FTP, FTPS, GOPHER, GOPHERS,  HTTP,
       HTTPS, IMAP, IMAPS, LDAP, LDAPS, MQTT, POP3, POP3S, RTMP, RTMPS, RTSP,
       SCP, SFTP, SMB, SMBS, SMTP, SMTPS, TELNET, TFTP, WS and WSS).

       curl is powered by libcurl for all transfer-related features. See 
       libcurl(3) for details.

PROTOCOLS
       curl supports numerous protocols. This man page describes command line
       options. For protocol-specific options, see the specific man pages.

URL
       The URL syntax is protocol-dependent. Details described in RFC 3986.

       You can specify multiple URLs or parts of URLs by writing part sets
       within braces and quoting the URL as in:

         "http://site.{one,two,three}.com"

       or get sequences of alphanumeric series by using [] as in:

         "ftp://ftp.example.com/file[1-100].txt"

OPTIONS
       -d, --data <data>
              (HTTP MQTT) Sends the specified data in a POST request to the
              HTTP server, in the same way that a browser does when a user
              has filled in an HTML form and pressed the submit button.

       -H, --header <header/@file>
              (HTTP) Extra header to include in the request when sending HTTP
              to a server. You may specify any number of extra headers.

       -o, --output <file>
              Write output to <file> instead of stdout.

EXAMPLES
       curl https://example.com
              Fetch a website and display on stdout

       curl -o file.html https://example.com
              Fetch and save to file

       curl -d "name=alice" https://example.com/api
              POST data to endpoint

SEE ALSO
       wget(1), ftp(1), libcurl(3)
```

### Line-by-Line Analysis

**Header:**
```
CURL(1)                    Curl Manual                    CURL(1)
```
- **Format:** `NAME(SECTION) TITLE NAME(SECTION)`
- **Purpose:** Standard Unix man page header
- **Note:** `(1)` means user command (vs. (3) library, (7) miscellaneous)

**NAME section:**
```
NAME
       curl - transfer a URL
```
- **One line description** - Appears in `man -k` searches
- **Ultra-concise** - Essential function only
- **Note:** "transfer" not "download" (bidirectional)

**SYNOPSIS:**
```
SYNOPSIS
       curl [options / URLs]
```
- **Simplified syntax** - Details come later
- **Convention:** `[]` means optional, `|` means OR
- **Note:** Slash suggests "either/or both"

**DESCRIPTION (opening):**
```
curl  is  a tool for transferring data from or to a server using one of
the supported protocols (DICT, FILE, FTP, FTPS, ... WS and WSS).
```
**Analysis:**
- **Complete protocol list** - Shows scope immediately
- **"from or to"** - Clarifies bidirectional
- **"tool"** - Positioning (not library, not service)

**DESCRIPTION (libcurl mention):**
```
curl is powered by libcurl for all transfer-related features. See 
libcurl(3) for details.
```
**Why this matters:**
- **Attribution** - Credits underlying library
- **Depth pointer** - "For details, see X"
- **Cross-reference** - `(3)` is library docs
- **Separation of concerns** - CLI vs. library

**URL syntax:**
```
You can specify multiple URLs or parts of URLs by writing part sets
within braces and quoting the URL as in:

  "http://site.{one,two,three}.com"
```
**Teaching technique:**
- **Abstract explanation first** ("part sets within braces")
- **Concrete example second** (actual URL)
- **Indented code block** - Visually distinct
- **Result:** Pattern + instance = understanding

**OPTIONS format:**
```
-d, --data <data>
       (HTTP MQTT) Sends the specified data in a POST request...
```
**Structure:**
- **Short + long form** (`-d` and `--data`)
- **Parameter placeholder** (`<data>`)
- **Protocol scope** (`(HTTP MQTT)`) - When applicable
- **Description** - What it does, how it works

**Why this works:**
- **Scannable** - Short flag prominent
- **Descriptive** - Long flag self-documenting
- **Scoped** - Don't use `-d` with FTP (makes no sense)

**EXAMPLES section:**
```
EXAMPLES
       curl https://example.com
              Fetch a website and display on stdout

       curl -o file.html https://example.com
              Fetch and save to file
```
**Critical section:**
- **Immediately usable** - Copy-paste ready
- **Progressive complexity** - Simple → advanced
- **Commented** - Each example explained
- **Real domains** - example.com (RFC 2606 reserved)

**SEE ALSO:**
```
SEE ALSO
       wget(1), ftp(1), libcurl(3)
```
**Cross-references:**
- **Related tools** (wget, ftp)
- **Related docs** (libcurl)
- **Discovery aid** - "If you need X, try Y"

---

### What Makes This Exemplary?

**1. Follows conventions**
- Standard Unix man page format
- Predictable structure (NAME, SYNOPSIS, DESCRIPTION, OPTIONS, EXAMPLES, SEE ALSO)
- Users know where to look for what

**2. Layered information**
- Quick overview (NAME, SYNOPSIS)
- Full details (DESCRIPTION, OPTIONS)
- Practical application (EXAMPLES)

**3. Cross-references**
- Points to related tools
- Points to deeper docs (libcurl)
- Acknowledges ecosystem

**4. Examples-driven**
- Not just theory
- Immediately actionable
- Progressive complexity

**5. Respectful of reader's time**
- Can read top-to-bottom OR jump to section
- Scannable structure
- No fluff

---

## Example 2: Python's `requests` Library Docs

### Full Text (Simplified)

```python
"""
requests
~~~~~~~~

:copyright: (c) 2023 by Kenneth Reitz.
:license: Apache 2.0, see LICENSE for more details.

Requests is an elegant and simple HTTP library for Python.

Usage:

   >>> import requests
   >>> r = requests.get('https://httpbin.org/get')
   >>> r.status_code
   200
   >>> r.json()
   {'origin': '1.2.3.4', ...}

Available methods:
- requests.get(url, params=None, **kwargs)
- requests.post(url, data=None, json=None, **kwargs)
- requests.put(url, data=None, **kwargs)
- requests.delete(url, **kwargs)
- requests.head(url, **kwargs)
- requests.options(url, **kwargs)

All methods return a Response object.

Response object attributes:
- r.status_code    : HTTP status code (int)
- r.text           : Response body as string
- r.content        : Response body as bytes
- r.json()         : Parse JSON response
- r.headers        : Response headers (dict)
- r.cookies        : Cookies (dict)
- r.elapsed        : Time taken (timedelta)
- r.url            : Final URL (after redirects)

Examples:

# GET with parameters
>>> r = requests.get('https://httpbin.org/get', params={'key': 'value'})

# POST with JSON
>>> r = requests.post('https://httpbin.org/post', json={'key': 'value'})

# Custom headers
>>> headers = {'User-Agent': 'my-app/1.0'}
>>> r = requests.get('https://example.com', headers=headers)

# Handling errors
>>> try:
...     r = requests.get('https://example.com/bad-url')
...     r.raise_for_status()  # Raises HTTPError for 4xx/5xx
... except requests.HTTPError as e:
...     print(f"Error: {e}")

For full documentation, see: https://docs.python-requests.org
"""
```

### Analysis

**Docstring header:**
```python
"""
requests
~~~~~~~~

:copyright: (c) 2023 by Kenneth Reitz.
:license: Apache 2.0, see LICENSE for more details.
```

**Elements:**
- **Title with underline** - Visual emphasis
- **Copyright/license** - Legal clarity
- **Attribution** - Creator visible

**Opening line:**
```
Requests is an elegant and simple HTTP library for Python.
```

**Analysis:**
- **Positioning** - "elegant and simple" (design goals)
- **Scope** - "HTTP library" (what it does)
- **Audience** - "for Python" (language-specific)

**"Usage" section with doctest:**
```python
Usage:

   >>> import requests
   >>> r = requests.get('https://httpbin.org/get')
   >>> r.status_code
   200
```

**Why doctests?**
- **Executable documentation** - Can run as tests
- **Shows input AND output** - Complete picture
- **Interactive style** - Mimics REPL experience
- **Copy-pasteable** - Remove `>>>` and run

**Method list:**
```python
Available methods:
- requests.get(url, params=None, **kwargs)
- requests.post(url, data=None, json=None, **kwargs)
```

**Structure:**
- **Signature included** - Shows parameters
- **Grouped logically** - HTTP methods together
- **Scannable** - Bullet list format

**Response object attributes:**
```python
Response object attributes:
- r.status_code    : HTTP status code (int)
- r.text           : Response body as string
- r.content        : Response body as bytes
```

**Format:**
- **Attribute name** - Actual code
- **Type hint** - `(int)`, `(dict)`, etc.
- **Description** - What it contains

**Why effective:**
- **Quick reference** - Scan for what you need
- **Type information** - Avoids mistakes
- **Concise** - No unnecessary words

**Examples with comments:**
```python
# GET with parameters
>>> r = requests.get('https://httpbin.org/get', params={'key': 'value'})
```

**Pattern:**
- **Comment describes scenario** (`# GET with parameters`)
- **Code shows how** (`requests.get(...)`)
- **Progressive disclosure** - More complex examples later

**Error handling example:**
```python
# Handling errors
>>> try:
...     r = requests.get('https://example.com/bad-url')
...     r.raise_for_status()  # Raises HTTPError for 4xx/5xx
... except requests.HTTPError as e:
...     print(f"Error: {e}")
```

**Why include this:**
- **Common task** - Everyone hits errors
- **Best practice** - Shows proper pattern
- **Inline comments** - Explains magic (`raise_for_status()`)

**Footer:**
```
For full documentation, see: https://docs.python-requests.org
```

**Purpose:**
- **Depth pointer** - This is overview, full docs elsewhere
- **Web presence** - Link to comprehensive resource
- **Separation** - Quick ref vs. tutorial vs. API docs

---

### What Makes This Exemplary?

**1. Executable examples**
- Doctests verify documentation stays accurate
- Users can try immediately

**2. Progressive disclosure**
- Simple example first
- Advanced examples later
- Depth available via link

**3. Type information**
- Parameters shown with types
- Return types documented
- Reduces guesswork

**4. Real-world scenarios**
- Not just "hello world"
- Includes error handling
- Shows parameters, headers, JSON

**5. Self-contained but not comprehensive**
- Enough to get started
- Points to full docs for depth

---

## Example 3: Git's Status Output

### Output Sample

```
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   src/main.py
        new file:   src/utils.py

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes)
        modified:   README.md
        deleted:    old_file.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        temp.log
        .env.local
```

### Analysis

**State declaration:**
```
On branch main
Your branch is up to date with 'origin/main'.
```

**What it tells you:**
- **Current branch** - Where am I?
- **Remote sync status** - Am I ahead/behind/synced?

**Why this matters:**
- **Context first** - Before listing changes, establish WHERE you are
- **Remote awareness** - Prevent push conflicts

**Grouped changes:**
```
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   src/main.py
```

**Structure:**
- **Group header** ("Changes to be committed")
- **Help text** (how to undo this state)
- **File list** with status

**Why this grouping:**
- **Git has 3 states** - Untracked, unstaged, staged
- **Each state has actions** - add, commit, restore
- **Clear boundaries** - User knows what will be committed

**Inline help:**
```
(use "git restore --staged <file>..." to unstage)
```

**Why brilliant:**
- **Context-sensitive help** - Tells you HOW TO UNDO
- **Exact command** - Copy-pasteable
- **Reduces docs lookup** - No need to Google "how to unstage"

**This is the gold standard for CLI feedback:**
- Tell user current state
- Show available actions
- Provide exact commands to take those actions

**File status indicators:**
```
        modified:   src/main.py
        new file:   src/utils.py
        deleted:    old_file.txt
```

**Format:**
- **Status label** - modified/new file/deleted
- **Indentation** - Visually grouped
- **Clear** - Exactly what changed

**Untracked files:**
```
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        temp.log
        .env.local
```

**Why separate:**
- **Different state** - Not yet in Git's awareness
- **Different action** - Use `git add` to track
- **Intentional separation** - Untracked files often noise

---

### What Makes This Exemplary?

**1. State-driven**
- Clearly shows what state you're in
- Groups changes by state

**2. Actionable**
- Every message includes "how to change this"
- Exact commands provided

**3. Hierarchical**
- Context (branch, remote status)
- Changes (grouped by type)
- Actions (inline help)

**4. Educational**
- Teaches Git model (3 states)
- Shows commands (learning by doing)

**5. Compassionate**
- Assumes user might not know next step
- Provides help without condescension

---

## Example 4: Django's Development Server Output

### Sample Output

```
$ python manage.py runserver
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).
November 20, 2023 - 15:45:23
Django version 4.2.7, using settings 'myproject.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.

[20/Nov/2023 15:45:35] "GET / HTTP/1.1" 200 1234
[20/Nov/2023 15:45:36] "GET /static/style.css HTTP/1.1" 200 5678
[20/Nov/2023 15:45:38] "POST /api/login HTTP/1.1" 302 0
[20/Nov/2023 15:45:40] "GET /dashboard HTTP/1.1" 500 2345

Error details:
  File "/path/to/views.py", line 42, in dashboard_view
    result = some_function()
  NameError: name 'some_function' is not defined
```

### Analysis

**Startup sequence:**
```
Watching for file changes with StatReloader
Performing system checks...
System check identified no issues (0 silenced).
```

**What's happening:**
- **File watcher active** - Auto-reload on code changes
- **System checks running** - Pre-flight validation
- **Results** - "no issues" (or list of issues)

**Why this matters:**
- **Transparency** - User sees what's happening
- **Confidence** - "System checks" verify integrity
- **Feedback** - Issues shown before server starts

**Server info:**
```
Django version 4.2.7, using settings 'myproject.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
```

**Information provided:**
- **Version** - For debugging ("which version am I using?")
- **Settings module** - Which config is active
- **URL** - Where to access (clickable in most terminals)
- **How to stop** - CONTROL-C

**Why complete:**
- **All context needed** - Version, config, access
- **Actionable** - Click URL to open
- **Safe** - Shows how to exit

**Request logs:**
```
[20/Nov/2023 15:45:35] "GET / HTTP/1.1" 200 1234
```

**Format:** `[timestamp] "METHOD /path HTTP/version" status_code response_size`

**Why useful:**
- **Chronological** - Order of requests
- **HTTP details** - Method, path, protocol
- **Result** - Status code (200 OK, 500 Error, 302 Redirect)
- **Size** - Response bytes

**Color-coding** (in actual terminal):
- **200s (green)** - Success
- **300s (cyan)** - Redirects
- **400s (yellow)** - Client errors
- **500s (red)** - Server errors

**Error details (inline):**
```
Error details:
  File "/path/to/views.py", line 42, in dashboard_view
    result = some_function()
  NameError: name 'some_function' is not defined
```

**Why inline:**
- **Immediate feedback** - Don't need to check separate logs
- **Stack trace** - Exact location of error
- **Exception type** - NameError (not defined)

**This is exceptional UX:**
- Error appears right after request log
- File path and line number provided
- Code snippet shown

---

### What Makes This Exemplary?

**1. Progressive output**
- Startup info first
- Request logs as they happen
- Errors inline

**2. Complete context**
- Version, settings, URL
- Request method, path, status
- Error location, type, message

**3. Color-coded (in practice)**
- Visual hierarchy
- Status at a glance

**4. Developer-friendly**
- Clickable URLs
- File paths (IDE can open directly)
- Stack traces with code

**5. Educational**
- Shows HTTP request/response cycle
- Status codes visible
- Errors explained

---

## Common Patterns in Excellent Documentation

### 1. Layered Information Architecture

**Pattern:**
```
Quick Start (minimal example)
    ↓
Common Use Cases (most users)
    ↓
API Reference (complete details)
    ↓
Advanced Topics (edge cases)
```

**Users enter at appropriate level:**
- Beginners: Quick Start
- Practitioners: Use Cases
- Experts: API Reference

---

### 2. Show, Don't Just Tell

**Bad:**
```
The function takes a parameter and returns a result.
```

**Good:**
```
>>> add(2, 3)
5
>>> add(10, -5)
5
```

**Pattern:** Example > Abstract description

---

### 3. Context Before Details

**Pattern:**
```
1. What this is
2. Why you'd use it
3. How to use it
4. Reference details
```

**Example (README structure):**
```
# Project Name (WHAT)

Brief description of what it does.

## Why? (WHY)

Explains problem it solves.

## Quick Start (HOW)

Minimal example.

## API Reference (DETAILS)

Full documentation.
```

---

### 4. Error Messages with Solutions

**Pattern:**
```
Problem: [what went wrong]
Reason: [why it happened]
Solution: [how to fix]
Example: [corrected code]
```

**Real example (TypeScript):**
```
Property 'length' does not exist on type 'number'
  Did you mean to use 'toString().length'?
```

---

### 5. Progressive Disclosure

**Pattern:**
```
# Basic usage
Simple example (90% of users)

# Advanced usage
<details>
  <summary>Click to expand</summary>
  Complex examples (10% of users)
</details>
```

**Benefit:** Don't overwhelm, but provide depth

---

## Documentation Anti-Patterns

### ❌ Things to Avoid

**1. Assuming knowledge**
```
❌ "Simply configure the flux capacitor"
✓ "Edit config.yaml and set flux_capacitor: true"
```

**2. Outdated examples**
```
❌ Example uses deprecated API
✓ Update docs with code
```

**3. Missing error scenarios**
```
❌ Only happy path shown
✓ Include error handling
```

**4. No examples**
```
❌ Wall of text about parameters
✓ One example worth thousand words
```

**5. Jargon without explanation**
```
❌ "Leverages paradigmatic synergies"
✓ "Combines X and Y to achieve Z"
```

**6. Broken links**
```
❌ "See documentation at [broken link]"
✓ Verify links regularly
```

**7. No version information**
```
❌ "This feature works"
✓ "Added in version 2.5"
```

---

## Principles Summary

### The Ten Commandments of Documentation

1. **Show examples** - Code speaks louder than words
2. **Provide context** - What, why, when, how
3. **Layer information** - Quick start → depth
4. **Include errors** - Show failure cases
5. **Give commands** - Exact, copy-pasteable
6. **Cross-reference** - Link related topics
7. **Version info** - When added/changed/removed
8. **Keep updated** - Docs rot quickly
9. **Test examples** - Verify they work
10. **Be kind** - Write for confused beginner

---

## Further Reading

**In this repository:**
- `/galleries/documentation-as-art/COLLECTION.md` - Example gallery
- `/galleries/documentation-as-art/artist-statements.md` - Philosophy
- `/toolkits/essay-writing-prompts.md` - Writing exercises

**External:**
- **Write the Docs** - Community and conference
- **Divio Documentation System** - 4 types framework
- **Every Layout** - Web typography and readability

---

**Great documentation is an act of empathy.**

---

**License:** CC-BY-SA 4.0 International  
**Author:** Digital Aesthetics Manifesto Contributors  
**Date:** November 19, 2025
