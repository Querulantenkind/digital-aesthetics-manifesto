# Collaborative Projects: Creating Together

## Introduction

These exercises explore collective creativity—projects that require multiple people, shared vision, distributed labor, and consensus.

Collaboration teaches us that creation is social, knowledge is collective, and the best work emerges from genuine solidarity.

---

## Project 1: The Collaborative Zine

### Concept
Multiple contributors create sections of a single publication.

### Participants
4-12 people

### Timeline
4-6 weeks

### Process

**Week 1: Planning**
- Choose theme
- Decide format (print/digital/both)
- Assign sections
- Establish deadlines

**Week 2-4: Creation**
- Each person creates their section
- Check-ins every week
- Share drafts for feedback

**Week 5: Assembly**
- Compile all sections
- Design layout
- Edit for consistency

**Week 6: Distribution**
- Print/publish
- Launch event
- Send to contributors

### Roles

- **Editor**: Oversees timeline, maintains vision
- **Contributors**: Write/create individual sections
- **Designer**: Layout and visual coherence
- **Distributor**: Handles printing, mailing, uploading

### Section Ideas

- Personal essays (theme-related)
- Poetry
- Visual art (photos, illustrations, ASCII)
- Interviews
- How-to guides
- Resource lists
- Comics

### Example Structure (24-page zine)

```
Page 1: Cover (collaborative title + image)
Page 2-3: Introduction (editor)
Page 4-5: Essay 1 (contributor A)
Page 6-7: Poetry + art (contributors B + C)
Page 8-9: Interview (contributor D)
Page 10-11: How-to guide (contributor E)
Page 12-13: Photo essay (contributor F)
Page 14-15: Short fiction (contributor G)
Page 16-17: Resources (collaborative)
Page 18-19: Comics (contributor H)
Page 20-21: Reflections (multiple contributors)
Page 22-23: Credits + call for next issue
Page 24: Back cover (contact/distribution info)
```

### Distribution

- Print 100+ copies
- Leave in coffee shops, bookstores, libraries
- Mail to other zine-makers
- Upload PDF to Archive.org
- Announce on social media

### Reflection

- How did collaboration change your process?
- What conflicts arose and how were they resolved?
- Would you work with these people again?
- What's the relationship between individual voice and collective product?

---

## Project 2: The Exquisite Corpse Website

### Concept
Collaborative website where each person builds one page without seeing others' work until the end.

### Participants
3-10 people

### Timeline
2-3 weeks

### Process

**Week 1: Setup**
- Choose site theme/purpose
- Create git repository
- Define constraints:
  - Color palette (shared)
  - Font choices (shared)
  - Navigation structure
  - File naming convention

**Week 2: Creation**
- Each person builds their page
- No peeking at others' pages
- Commit to separate branches

**Week 3: Reveal & Integration**
- Merge all pages
- Add navigation between pages
- Fix conflicts
- Deploy site

### Technical Setup

```bash
# Repository structure
website/
├── index.html (coordinator creates)
├── page-1/ (contributor A)
│   ├── index.html
│   └── style.css
├── page-2/ (contributor B)
│   ├── index.html
│   └── style.css
├── page-3/ (contributor C)
│   ├── index.html
│   └── style.css
└── shared/
    ├── colors.css (shared palette)
    └── fonts.css (shared typography)
```

### Constraints

**Shared**:
- Color palette (exactly 5 colors)
- Font choices (2 fonts max)
- Page size (single screen, no scrolling)

**Individual Freedom**:
- Layout
- Content
- Interactivity
- Imagery

### Example Theme
"Digital Solitude"—each page explores isolation/connection in digital spaces

### Reflection

- How does not seeing others' work affect your choices?
- What happens when pages are combined?
- Did the site have unintended coherence?
- What conflicts emerged during integration?

---

## Project 3: The Collective Manifesto

### Concept
Group writes a manifesto together through iterative process.

### Participants
5-15 people

### Timeline
3-4 weeks

### Process

**Week 1: Individual Writing**
- Each person writes 5 statements
- "We believe..."
- "We reject..."
- "We demand..."

**Week 2: First Synthesis**
- Share all statements
- Group them by theme
- Vote on priorities
- Draft first version

**Week 3: Refinement**
- Circulate draft
- Each person edits/comments
- Group meeting to discuss changes
- Second draft

**Week 4: Finalization**
- Final edits
- Design manifesto
- Publish
- Sign collectively

### Structure

```markdown
# [GROUP NAME] MANIFESTO

## Preamble
We, the undersigned, [context and purpose]...

## Beliefs
1. We believe that...
2. We believe that...
[5-10 core beliefs]

## Rejections
1. We reject...
2. We reject...
[5-10 things opposed]

## Demands
1. We demand...
2. We demand...
[5-10 specific demands]

## Commitments
1. We commit to...
2. We commit to...
[5-10 things we will do]

## Signatories
[Names/handles of all contributors]

[Date]
```

### Facilitation Tips

- Use collaborative editing tools (HedgeDoc, Etherpad)
- Set clear deadlines
- Vote on contentious points
- Allow dissent notes
- Consensus on final version

### Variations

- **Poetry manifesto**: Each section a poem
- **Visual manifesto**: Primarily images/symbols
- **Living document**: Update annually
- **Response manifesto**: Reply to existing manifesto

### Reflection

- How did individual voices become collective voice?
- What was lost and gained in consensus?
- Can a manifesto truly represent a group?
- How does public declaration change commitment?

---

## Project 4: The Shared Terminal Session

### Concept
Multiple people log into a shared terminal, create art/text collaboratively in real-time.

### Participants
2-6 people (small enough to not create chaos)

### Timeline
2-4 hours (single session)

### Technical Setup

Use `tmux` for shared terminal:

```bash
# Host creates session
tmux -S /tmp/shared new -s collab
chmod 777 /tmp/shared

# Others join
tmux -S /tmp/shared attach -t collab
```

Or use **tmate** for internet-based sharing:

```bash
# Host starts tmate
tmate

# Share SSH command with collaborators
tmate show-messages
```

### Activities

**Collaborative ASCII Art**:
- Each person adds to a shared canvas
- Use text editor (vim, nano, emacs)
- No verbal communication, only through additions

**Chain Story**:
- Each person writes 2-3 sentences
- Pass to next person
- Continue until complete

**Live Coding**:
- Build program together
- Each person writes functions
- Integrate as you go

**Terminal Jazz**:
- Improvise with text/symbols
- Respond to what others create
- Pure visual/textual play

### Example: Collaborative Poem

```
Person A types:
in the terminal's glow

Person B adds:
in the terminal's glow
we meet as ghosts

Person C continues:
in the terminal's glow
we meet as ghosts
leaving only traces

Person A returns:
in the terminal's glow
we meet as ghosts
leaving only traces
of thought, briefly visible

Person B concludes:
in the terminal's glow
we meet as ghosts
leaving only traces
of thought, briefly visible
before the prompt returns
```

### Rules

- **Respect**: Don't delete others' work without consensus
- **Build**: Add to what's there
- **Communicate**: Use comments or chat
- **Save**: Regularly save work

### Reflection

- How does simultaneous creation feel?
- What emerged that no individual would create?
- How did you negotiate control?
- What's the equivalent in non-digital collaboration?

---

## Project 5: The Community Wiki

### Concept
Collective knowledge base built and maintained by community.

### Participants
Open-ended (5-50+ people)

### Timeline
Ongoing (months to years)

### Setup

Use existing wiki software:
- **MediaWiki** (like Wikipedia)
- **DokuWiki** (simpler, file-based)
- **TiddlyWiki** (single HTML file)
- **BookStack** (book-style organization)

### Content Areas

- **Local knowledge**: History, resources, places
- **Technical documentation**: How-tos, guides
- **Cultural archive**: Stories, traditions, memories
- **Political education**: Theory, analysis, tactics
- **Creative resources**: Galleries, inspirations, techniques

### Example: Neighborhood Wiki

```
Home Page
├── History
│   ├── Founding
│   ├── Notable Events
│   └── Oral Histories
├── Resources
│   ├── Community Organizations
│   ├── Mutual Aid Networks
│   └── Emergency Contacts
├── Places
│   ├── Parks & Gathering Spaces
│   ├── Businesses
│   └── Historical Sites
├── Culture
│   ├── Local Artists
│   ├── Events & Traditions
│   └── Stories
└── How-To
    ├── Gardening
    ├── Organizing
    └── Skill Shares
```

### Governance

- **Open editing**: Anyone can contribute
- **Moderation team**: Handles disputes, vandalism
- **Version control**: All changes tracked
- **Talk pages**: Discuss changes before making them
- **Style guide**: Maintain consistency

### Maintenance

- Weekly: Check recent changes, fix vandalism
- Monthly: Review most-visited pages, update stale info
- Quarterly: Backup entire wiki
- Annually: Assess structure, major reorganization if needed

### Reflection

- How does collective ownership affect quality?
- What conflicts arise in knowledge representation?
- Who contributes and who doesn't—why?
- How does wiki become community memory?

---

## Project 6: The Chain Letter / Zine

### Concept
Each person receives package, adds to it, sends to next person. Final recipient publishes entire work.

### Participants
6-12 people

### Timeline
3-6 months (depends on chain length)

### Process

**Initiator**:
- Creates first section (4-8 pages)
- Establishes theme and format
- Mails to Person 2

**Chain Members**:
- Receive package
- Read everything so far
- Add their section (4-8 pages)
- Mail to next person

**Final Recipient**:
- Compiles entire work
- Designs layout
- Publishes/distributes
- Sends copies back to all contributors

### Package Contents

- All previous sections
- Instruction sheet
- Address of next person
- Return postage (if possible)
- Small gift/artifact (optional)

### Themes

- "Journey": Each person adds a leg
- "City": Each person documents their neighborhood
- "Year": Each person adds a season
- "Transformation": Each person modifies previous work

### Variations

- **Digital**: Email PDF, each adds pages
- **Visual**: Start with image, each transforms it
- **Code**: Each person adds to program
- **Object**: Physical object that accumulates modifications

### Reflection

- How does seeing previous work influence yours?
- What's special about physical mail vs digital?
- Did a narrative emerge across contributions?
- What's the relationship between sequence and meaning?

---

## Project 7: The Collective Archive

### Concept
Group documents and archives shared history, culture, or movement.

### Participants
5-20 people

### Timeline
Ongoing (minimum 6 months)

### Process

**Phase 1: Collection (Month 1-2)**
- Decide what to archive (movement documents, personal stories, ephemera)
- Gather materials from contributors
- Scan/photograph physical items
- Record oral histories

**Phase 2: Organization (Month 3-4)**
- Develop organization system
- Tag and categorize
- Write descriptions
- Create metadata

**Phase 3: Platform (Month 5-6)**
- Build archive website or use existing platform
- Upload materials
- Create navigation
- Write about archive

**Phase 4: Maintenance (Ongoing)**
- Accept new submissions
- Update descriptions
- Backup regularly
- Promote archive

### Archive Topics

- **Movement archive**: Documents from organizing campaigns
- **Cultural archive**: Art, music, writing from community
- **Oral history**: Recorded interviews with elders, activists
- **Ephemera**: Flyers, zines, posters, stickers
- **Digital artifacts**: Websites, social media, code

### Technical Setup

Simple option:
```
archive/
├── index.html (browse interface)
├── 1990s/
│   ├── 1995-protest-flyer.pdf
│   ├── 1997-zine-issue-01.pdf
│   └── metadata.json
├── 2000s/
│   └── ...
├── oral-histories/
│   ├── interview-001.mp3
│   ├── interview-001-transcript.txt
│   └── ...
└── about.html
```

Or use platforms:
- **Internet Archive** (archive.org)
- **Omeka** (archive platform)
- **Mukurtu** (indigenous knowledge archive)
- **Archive-It** (web archiving)

### Metadata Standard

```json
{
  "title": "Rent Strike Flyer",
  "date": "1995-03-15",
  "creator": "Tenants United",
  "description": "Call to action for city-wide rent strike",
  "format": "PDF scan of original flyer",
  "subjects": ["housing", "organizing", "1990s"],
  "rights": "CC-BY-SA 4.0",
  "collection": "Housing Justice Movement"
}
```

### Reflection

- What's the political importance of archives?
- Who decides what's preserved and what's forgotten?
- How to make archives accessible?
- What's the relationship between memory and justice?

---

## Project 8: The Round-Robin Story

### Concept
Each person writes a chapter of a shared story, taking turns.

### Participants
3-8 people

### Timeline
2-4 months

### Process

**Setup**:
- Decide on genre, setting, initial situation
- Establish world rules (for sci-fi/fantasy)
- Set chapter length (1,000-2,000 words)
- Determine order

**Rotation**:
- Person A writes Chapter 1
- Person B writes Chapter 2 (reading Chapter 1)
- Person C writes Chapter 3 (reading Chapters 1-2)
- Continue until complete or predetermined end

**Completion**:
- Final person writes conclusion
- Group edits for consistency
- Publish collectively

### Rules

- Can't kill other people's characters without permission
- Must resolve previous cliffhanger
- Can introduce new characters/plot threads
- Must maintain continuity

### Example Setup

**Genre**: Cyberpunk  
**Setting**: 2045, megacity, climate chaos  
**Initial**: A package arrives with no sender, just coordinates  
**Rules**: Near-future tech only, maintain gritty tone

### Variations

- **Branching**: Each chapter offers two endings, next writer chooses
- **Constraint rotation**: Each chapter has different constraint
- **Character focus**: Each writer follows different character
- **Competitive**: Each writer tries to make resolution impossible for next

### Reflection

- How did others' choices affect your creativity?
- What surprised you about collective storytelling?
- Is the whole greater than the sum?
- How does this compare to solo writing?

---

## Project 9: The Collaborative Code Project

### Concept
Group builds a functional program/tool together.

### Participants
3-10 programmers

### Timeline
4-12 weeks

### Process

**Week 1: Planning**
- Define project scope
- Choose tech stack
- Design architecture
- Assign modules

**Week 2-10: Development**
- Each person develops their module
- Regular integration (CI/CD)
- Code reviews
- Documentation

**Week 11-12: Polish & Launch**
- Bug fixes
- User testing
- Documentation
- Release

### Project Ideas

- **Collaborative text editor** (like HedgeDoc)
- **Privacy tool** (encrypted messaging, file sharing)
- **Art generator** (generative ASCII/ANSI art)
- **Game** (text adventure, roguelike, MUD)
- **Archive platform** (for communities)
- **Learning tool** (tutorials, quizzes)

### Example: ASCII Art Collaboration Tool

```
Features:
- Real-time shared canvas
- Multiple users can draw simultaneously
- Chat sidebar
- Export to text file
- Gallery of past works

Modules:
- Person A: Server & real-time sync
- Person B: Canvas rendering & drawing tools
- Person C: User authentication
- Person D: Chat system
- Person E: Export & gallery
```

### Git Workflow

```bash
# Main branch: stable releases
main

# Development branch: integration
dev

# Feature branches: individual work
feature/canvas-drawing
feature/user-auth
feature/chat-system
```

### Best Practices

- **Communicate**: Daily standups (async is fine)
- **Document**: Code comments, README, API docs
- **Test**: Write tests for your modules
- **Review**: All code gets reviewed before merging
- **License**: Choose open source license

### Reflection

- What makes collaborative coding different from solo?
- How did technical decisions become social negotiations?
- What conflicts arose and how were they resolved?
- Would you build more software collaboratively?

---

## Project 10: The Public Performance

### Concept
Create and perform a piece for public audience—theater, poetry, music, etc.

### Participants
4-20 people

### Timeline
6-12 weeks

### Process

**Week 1-2: Concept**
- Brainstorm themes
- Decide format
- Assign roles
- Scout venue

**Week 3-8: Creation**
- Write script/score
- Rehearse regularly
- Build props/costumes
- Design marketing

**Week 9-11: Refinement**
- Full run-throughs
- Tech rehearsal
- Dress rehearsal
- Final adjustments

**Week 12: Performance**
- Setup
- Perform
- Document (video/photo)
- Debrief

### Performance Types

**Theater**:
- Devised piece on theme
- Adapted text
- Site-specific performance

**Poetry**:
- Collaborative reading
- Call-and-response
- Poetry slam

**Music**:
- Composed piece
- Improvisation
- Sound art

**Hybrid**:
- Performance lecture
- Live coding + music
- Interactive installation

### Example: "Terminal Chorus"

**Concept**: Five performers at terminals, "typing" a script that's projected large. Audience sees code/commands/text appearing. Performers speak some lines, type others.

**Structure**:
```
Act 1: Individual isolation (each at own terminal)
Act 2: Attempts to connect (messaging each other)
Act 3: Collective creation (building program together)
Finale: Program runs, creates visual/sonic output
```

**Roles**:
- 5 performers
- 1 technical director (projection)
- 1 sound designer
- 2 documentarians (video/photo)

### Venue Options

- Theater
- Gallery
- Public space (street, park)
- Online (livestream)
- Unconventional (parking garage, rooftop)

### Reflection

- How does live performance differ from recorded media?
- What's the role of audience?
- How did collaboration shape the work?
- Would you perform again?

---

## Long-Term Collaborative Projects

### Project A: The Collective Year

**Duration**: 12 months

**Practice**:
- Group commits to year-long creative project
- Monthly meetings
- Each person contributes regularly
- End with publication/exhibition

**Examples**:
- 365 days of collective poetry
- Monthly zine series
- Yearlong photo project
- Collaborative novel

---

### Project B: The Artist Collective

**Duration**: Ongoing

**Practice**:
- Form lasting creative collective
- Shared studio/workspace
- Regular shows/publications
- Support each other's individual work

**Structure**:
- Monthly meetings
- Rotating facilitator
- Shared expenses
- Public programming

---

### Project C: The Community School

**Duration**: Ongoing

**Practice**:
- Teach-learn collectively
- Rotating instructors
- Free or sliding-scale
- Non-hierarchical

**Courses**:
- Technical skills
- Creative practices
- Political education
- Mutual aid organizing

---

## Tips for Successful Collaboration

### Communication
- **Regular check-ins**: Schedule consistent meetings
- **Async options**: Accommodate different schedules
- **Clear expectations**: Document responsibilities
- **Conflict resolution**: Establish process before conflicts arise

### Organization
- **Shared calendar**: Track deadlines
- **Project management**: Use tools (Trello, GitHub Projects, etc.)
- **Documentation**: Write everything down
- **Version control**: Track changes (Git for code, Google Docs for text)

### Equity
- **Shared credit**: Everyone's name on final work
- **Distributed labor**: Ensure fair workload
- **Rotating leadership**: Different people lead different phases
- **Access**: Consider time, money, skills, location

### Sustainability
- **Set boundaries**: Realistic commitments
- **Build breaks**: Rest is part of process
- **Celebrate milestones**: Acknowledge progress
- **Document process**: For reflection and future collaborators

---

## Further Reading

**In this repository**:
- All `/creative-exercises/` files - Individual practices that feed collective work
- `/essays/volume-2/` - Essays on collaboration and community
- `/toolkits/` - Tools for collaborative creation

**External resources**:
- **Loomio** - Collaborative decision-making
- **Git** - Version control for collaborative coding
- **HedgeDoc** - Collaborative markdown editing
- **Sandstorm** - Self-hosted collaborative apps

---

## Closing Thoughts

Collaboration is hard. It requires patience, communication, compromise, and trust. It's slower than working alone. It's messier.

But collaboration is also:
- More fun
- More surprising
- More generous
- More sustainable
- More just

The best work—the work that changes things—is rarely made alone.

**Create together.**

---

**License**: CC0 1.0 Universal (Public Domain)  
**Contributors**: Digital Aesthetics Manifesto Community  
**Date**: November 19, 2025
