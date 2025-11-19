# Tools and Software

## Introduction

Practical tools for privacy, security, creation, and resistance. This guide prioritizes free/open source software, privacy-respecting alternatives, and tools that empower users.

**Philosophy**: Tools should serve users, not extract data. Prefer self-hosted, decentralized, and open source when possible.

---

## I. Privacy and Security Fundamentals

### Encrypted Messaging

**Signal**  
https://signal.org/  
**Platform**: iOS, Android, Desktop  
**License**: Free and open source (GPLv3)

Gold standard for encrypted messaging. End-to-end encryption by default. Metadata minimization. Disappearing messages. Non-profit Signal Foundation.

**Use for**: Private conversations, group organizing, file sharing

---

**Element (Matrix)**  
https://element.io/  
**Platform**: iOS, Android, Desktop, Web  
**License**: Open source (Apache)

Decentralized, federated encrypted messaging. Based on Matrix protocol. Self-hostable. Bridges to other platforms.

**Use for**: Communities, teams, bridging other platforms

---

**Briar**  
https://briarproject.org/  
**Platform**: Android  
**License**: Open source (GPLv3)

Peer-to-peer encrypted messaging. Works without internet via Bluetooth/WiFi. Designed for activists in hostile environments.

**Use for**: Protest coordination, internet shutdowns, high-threat environments

---

### Email

**ProtonMail**  
https://proton.me/mail  
**Platform**: Web, iOS, Android, Desktop  
**Model**: Freemium

End-to-end encrypted email. Zero-access architecture. Based in Switzerland. Free tier available.

**Use for**: Secure email with non-technical contacts

---

**Tutanota**  
https://tutanota.com/  
**Platform**: Web, iOS, Android, Desktop  
**License**: Freemium, open source client

Encrypted email with calendar. Automatic encryption. European privacy laws. Lower cost than ProtonMail.

**Use for**: Personal secure email, calendar

---

**Thunderbird**  
https://www.thunderbird.net/  
**Platform**: Desktop  
**License**: Free and open source (MPL)

Email client with PGP support via plugins. Supports multiple accounts. Highly customizable.

**Use for**: Managing multiple email accounts with encryption

---

### Web Browsing

**Tor Browser**  
https://www.torproject.org/  
**Platform**: Desktop, Android  
**License**: Free and open source

Anonymous web browsing via Tor network. Routes traffic through multiple relays. Essential for anonymity.

**Use for**: Anonymous browsing, accessing censored content, whistleblowing

---

**Firefox**  
https://www.mozilla.org/firefox/  
**Platform**: Desktop, iOS, Android  
**License**: Free and open source (MPL)

Privacy-focused browser from non-profit. Customizable. Strong tracking protection. Open source.

**Recommended Extensions**:
- uBlock Origin (ad/tracker blocking)
- Privacy Badger (tracker blocking)
- HTTPS Everywhere (force HTTPS)
- Containers (isolate browsing contexts)

---

**Brave**  
https://brave.com/  
**Platform**: Desktop, iOS, Android  
**License**: Free and open source (MPL)

Privacy-first browser with built-in ad/tracker blocking. Chromium-based. Built-in Tor mode.

**Note**: Cryptocurrency integration controversial but optional

---

### Browser Extensions

**uBlock Origin**  
https://ublockorigin.com/  
**Platform**: Firefox, Chrome, Edge

Best ad/tracker blocker. Open source. Efficient. Highly configurable.

**Install on**: Every browser you use

---

**Privacy Badger**  
https://privacybadger.org/  
**Platform**: Firefox, Chrome, Edge

EFF-developed tracker blocker. Learns to block trackers automatically. Complementary to uBlock Origin.

---

**Decentraleyes**  
https://decentraleyes.org/  
**Platform**: Firefox, Chrome

Blocks CDN tracking by serving libraries locally. Improves privacy and speed.

---

### VPN Services

**Mullvad**  
https://mullvad.net/  
**Price**: €5/month  
**Platform**: Desktop, iOS, Android

Privacy-focused VPN. No account required—just account number. Anonymous payment options. No logs. Based in Sweden.

**Best for**: Privacy, anonymity

---

**ProtonVPN**  
https://protonvpn.com/  
**Price**: Free tier, paid plans  
**Platform**: Desktop, iOS, Android

From ProtonMail team. Free tier available. Secure Core (multi-hop). No logs.

**Best for**: Budget-conscious, ProtonMail users

---

**Riseup VPN**  
https://riseup.net/vpn  
**Price**: Donation-based  
**Platform**: Desktop, Android

Activist collective-run VPN. No logs, no tracking. Based on donations.

**Best for**: Activists, those who support activist infrastructure

---

### Password Management

**Bitwarden**  
https://bitwarden.com/  
**Platform**: Desktop, iOS, Android, Web, CLI  
**License**: Open source, freemium

Best open source password manager. Self-hostable. Free tier generous. Clean interface.

**Use for**: Storing passwords, 2FA codes, secure notes

---

**KeePassXC**  
https://keepassxc.org/  
**Platform**: Desktop  
**License**: Free and open source (GPLv3)

Offline password database. No cloud sync (use Syncthing or similar). Maximum control and security.

**Use for**: Offline password storage, maximum security

---

**pass**  
https://www.passwordstore.org/  
**Platform**: Linux, macOS (CLI)  
**License**: Free and open source (GPLv2)

Command-line password manager using GPG and git. Extremely simple. Perfect for terminal enthusiasts.

**Use for**: Command-line workflows, minimalist security

---

### Two-Factor Authentication

**Aegis Authenticator**  
https://getaegis.app/  
**Platform**: Android  
**License**: Free and open source (GPLv3)

2FA app with encrypted backup. Clean interface. Export options.

**Use for**: 2FA codes on Android

---

**Authenticator (by 2Stable)**  
**Platform**: iOS  
**License**: Free

Clean, simple 2FA app for iOS. No iCloud sync (privacy feature).

**Use for**: 2FA codes on iOS

---

### File Encryption

**VeraCrypt**  
https://www.veracrypt.fr/  
**Platform**: Desktop  
**License**: Free and open source

Full-disk encryption and encrypted containers. TrueCrypt successor. Industry standard.

**Use for**: Encrypting drives, creating encrypted volumes

---

**age**  
https://age-encryption.org/  
**Platform**: CLI (all platforms)  
**License**: Free and open source (BSD)

Simple, modern file encryption tool. "Everyone needs a tool like PGP. But simpler."

```bash
# Encrypt a file
age -r recipient-pubkey file.txt > file.txt.age

# Decrypt
age -d -i private-key file.txt.age > file.txt
```

**Use for**: Encrypting files, command-line workflows

---

## II. Operating Systems

### Privacy-Focused OS

**Tails**  
https://tails.boum.org/  
**Platform**: Live USB/DVD  
**License**: Free and open source (Debian-based)

Live operating system leaving no trace. Routes all traffic through Tor. Includes encryption tools. Boots from USB.

**Use for**: Whistleblowing, journalism, activism, anonymous communication

---

**Qubes OS**  
https://www.qubes-os.org/  
**Platform**: Desktop  
**License**: Free and open source

Security through compartmentalization. Uses VMs to isolate activities. Steep learning curve but maximum security.

**Use for**: High-security computing, separating personal/work/sensitive

---

**GrapheneOS**  
https://grapheneos.org/  
**Platform**: Pixel phones  
**License**: Free and open source

Hardened Android with enhanced privacy and security. Removes Google services. Active development.

**Use for**: Secure Android alternative (requires Pixel hardware)

---

### Linux Distributions

**Debian**  
https://www.debian.org/  
**License**: Free and open source

Stable, principled, community-driven. Foundation for Ubuntu and many others. Excellent for servers and desktops.

**Best for**: Stability, principles, long-term use

---

**Arch Linux**  
https://archlinux.org/  
**License**: Free and open source

Rolling release, minimal, customizable. Steep learning curve. Excellent documentation (ArchWiki).

**Best for**: Learning Linux deeply, customization

---

**Fedora**  
https://getfedora.org/  
**License**: Free and open source

Cutting-edge, stable, open source only. Backed by Red Hat. Good balance of new and reliable.

**Best for**: Desktop use, latest software, open source commitment

---

## III. Creative and Production Tools

### Text Editors

**Vim**  
https://www.vim.org/  
**Platform**: All  
**License**: Free and open source (Vim license)

Modal text editor. Steep learning curve, extremely powerful. Runs everywhere including over SSH.

**Use for**: Code, writing, anything text-based (if you invest in learning)

---

**Emacs**  
https://www.gnu.org/software/emacs/  
**Platform**: All  
**License**: Free and open source (GPLv3)

Extensible text editor and computing environment. "A great operating system, lacking only a decent editor." (Vim users joke)

**Use for**: Writing, coding, email, org-mode, life management

---

**VSCodium**  
https://vscodium.com/  
**Platform**: Desktop  
**License**: Free and open source (MIT)

VS Code without Microsoft telemetry. Same extensions, better privacy.

**Use for**: Modern code editing without tracking

---

**Notepad++ (Windows)**  
https://notepad-plus-plus.org/  
**Platform**: Windows  
**License**: Free and open source (GPLv3)

Simple, fast, reliable text editor. Better than Windows Notepad in every way.

**Use for**: Quick text editing on Windows

---

### Writing Tools

**Markdown**  
Not software, but essential format

Plain text with minimal markup. Future-proof. Universal. Use with any editor.

**Learn**: https://commonmark.org/

---

**Pandoc**  
https://pandoc.org/  
**Platform**: CLI (all platforms)  
**License**: Free and open source (GPLv2)

Universal document converter. Markdown to PDF, HTML, LaTeX, DOCX, and dozens more formats.

```bash
pandoc input.md -o output.pdf
pandoc input.md -o output.html
pandoc input.md -o output.docx
```

**Use for**: Converting between document formats, building workflows

---

**LaTeX**  
https://www.latex-project.org/  
**Platform**: All  
**License**: Free and open source

Typesetting system for beautiful documents. Steep learning curve. Beautiful output. Standard for academic publishing.

**Use for**: Academic papers, books, anything requiring professional typography

---

**Obsidian**  
https://obsidian.md/  
**Platform**: Desktop, iOS, Android  
**License**: Free (not open source)

Markdown-based knowledge management. Local files. Backlinks and graph view. Extensive plugins.

**Use for**: Note-taking, personal knowledge base, writing

---

### ASCII Art and Terminal Design

**figlet**  
http://www.figlet.org/  
**Platform**: CLI (all platforms)  
**License**: Free and open source

ASCII banner text generator.

```bash
figlet "Hello World"
  _   _      _ _        __        __         _     _ 
 | | | | ___| | | ___   \ \      / /__  _ __| | __| |
 | |_| |/ _ \ | |/ _ \   \ \ /\ / / _ \| '__| |/ _` |
 |  _  |  __/ | | (_) |   \ V  V / (_) | |  | | (_| |
 |_| |_|\___|_|_|\___/     \_/\_/ \___/|_|  |_|\__,_|
```

---

**jp2a**  
https://csl.name/jp2a/  
**Platform**: CLI (all platforms)  
**License**: Free and open source (GPLv2)

Converts JPEG images to ASCII art.

```bash
jp2a --width=80 image.jpg
```

---

**ASCII Art Studio** (Web)  
https://asciiart.club/  
Browser-based ASCII art editor

---

**boxes**  
https://boxes.thomasjensen.com/  
**Platform**: CLI  
**License**: Free and open source

Draws boxes around text in various styles.

```bash
echo "Hello World" | boxes
```

---

### Image Editing

**GIMP**  
https://www.gimp.org/  
**Platform**: Desktop  
**License**: Free and open source (GPLv3)

Professional image editing. Photoshop alternative. Plugins and scripting.

**Use for**: Photo editing, graphic design

---

**Inkscape**  
https://inkscape.org/  
**Platform**: Desktop  
**License**: Free and open source (GPLv3)

Vector graphics editor. Illustrator alternative. SVG-native.

**Use for**: Vector graphics, logos, illustrations

---

**ImageMagick**  
https://imagemagick.org/  
**Platform**: CLI (all platforms)  
**License**: Free and open source (Apache)

Command-line image manipulation. Batch processing, conversions, effects.

```bash
convert input.png -resize 800x600 output.png
mogrify -format jpg *.png  # Convert all PNGs to JPG
```

---

### Version Control

**Git**  
https://git-scm.com/  
**Platform**: All  
**License**: Free and open source (GPLv2)

Distributed version control. Essential for code and great for text-based work (writing, documentation).

**Learn**: https://git-scm.com/book/

---

**tig**  
https://jonas.github.io/tig/  
**Platform**: CLI  
**License**: Free and open source (GPLv2)

Text-mode interface for git. Browse commits, stage hunks, beautiful visualization.

---

## IV. Collaboration and Communication

### Self-Hosted Platforms

**Nextcloud**  
https://nextcloud.com/  
**Platform**: Self-hosted web  
**License**: Free and open source (AGPLv3)

Self-hosted file sync, calendar, contacts, notes, and more. Dropbox/Google Drive alternative.

**Use for**: Personal cloud, team collaboration

---

**HedgeDoc** (formerly CodiMD)  
https://hedgedoc.org/  
**Platform**: Self-hosted web  
**License**: Free and open source (AGPLv3)

Real-time collaborative Markdown editor. Self-hostable. Multiple users editing simultaneously.

**Use for**: Collaborative writing, meeting notes, documentation

---

**Etherpad**  
https://etherpad.org/  
**Platform**: Self-hosted web  
**License**: Free and open source (Apache)

Real-time collaborative text editing. Simple, focused. Color-coded users.

**Use for**: Quick collaborative text editing

---

### Video Conferencing

**Jitsi Meet**  
https://meet.jit.si/  
**Platform**: Web, iOS, Android  
**License**: Free and open source (Apache)

Video conferencing without accounts. Self-hostable. End-to-end encryption (with caveats).

**Use for**: Video calls without Big Tech platforms

---

**BigBlueButton**  
https://bigbluebutton.org/  
**Platform**: Self-hosted web  
**License**: Free and open source (LGPLv3)

Web conferencing system for education. Whiteboard, breakout rooms, polling.

**Use for**: Online teaching, webinars

---

### Forums and Communities

**Discourse**  
https://www.discourse.org/  
**Platform**: Self-hosted web  
**License**: Open source (GPLv2), hosting available

Modern forum software. Clean design, good moderation tools, active development.

**Use for**: Community forums, discussion spaces

---

**Lemmy**  
https://join-lemmy.org/  
**Platform**: Self-hosted, federated  
**License**: Free and open source (AGPLv3)

Federated Reddit alternative. ActivityPub protocol. Self-hostable or join existing instance.

**Use for**: Reddit-style communities, federated social

---

## V. Decentralized and Federated Social

### Fediverse

**Mastodon**  
https://joinmastodon.org/  
**Platform**: Web, iOS, Android  
**License**: Free and open source (AGPLv3)

Decentralized Twitter alternative. ActivityPub protocol. Choose instance or self-host.

**Getting started**: Choose instance from joinmastodon.org/servers

---

**Pixelfed**  
https://pixelfed.org/  
**Platform**: Web, iOS, Android  
**License**: Free and open source (AGPLv3)

Federated Instagram alternative. Photo sharing without algorithmic timeline or ads.

---

**PeerTube**  
https://joinpeertube.org/  
**Platform**: Web  
**License**: Free and open source (AGPLv3)

Decentralized video platform. YouTube alternative. Federated and peer-to-peer.

---

**WriteFreely**  
https://writefreely.org/  
**Platform**: Web  
**License**: Free and open source (AGPLv3)

Minimalist federated blogging platform. Clean, distraction-free writing. ActivityPub support.

---

### Peer-to-Peer

**Scuttlebutt**  
https://scuttlebutt.nz/  
**Platform**: Desktop, some mobile  
**License**: Free and open source (MIT)

Decentralized social network working offline. Gossip protocol. No central servers.

**Use for**: Truly decentralized social, offline-first communities

---

**IPFS** (InterPlanetary File System)  
https://ipfs.tech/  
**Platform**: All  
**License**: Free and open source (MIT/Apache)

Distributed file storage and sharing. Content-addressed. Decentralized web infrastructure.

**Use for**: Distributed file hosting, censorship resistance

---

## VI. Mobile Privacy

### Android Alternatives

**F-Droid**  
https://f-droid.org/  
**Platform**: Android  
**License**: Free and open source repository

App store for free and open source Android apps. No tracking, no proprietary code.

**Install**: First app on any Android device

---

**Aurora Store**  
https://auroraoss.com/  
**Platform**: Android (via F-Droid)  
**License**: Free and open source

Alternative front-end for Google Play. Anonymous access to Play Store apps.

**Use for**: Accessing Play Store without Google account

---

### Mobile Apps

**NewPipe**  
https://newpipe.net/  
**Platform**: Android  
**License**: Free and open source (GPLv3)

YouTube without Google. No ads, background playback, download videos. Via F-Droid.

---

**Organic Maps**  
https://organicmaps.app/  
**Platform**: iOS, Android  
**License**: Free and open source (Apache)

Offline maps based on OpenStreetMap. Fast, private, no tracking.

**Use for**: Navigation without Google/Apple

---

**Syncthing**  
https://syncthing.net/  
**Platform**: Desktop, Android  
**License**: Free and open source (MPLv2)

Continuous file synchronization. Peer-to-peer. No cloud. Your devices only.

**Use for**: Syncing files between devices privately

---

## VII. Anonymity and Activism

### Secure File Sharing

**OnionShare**  
https://onionshare.org/  
**Platform**: Desktop  
**License**: Free and open source (GPLv3)

Share files securely and anonymously via Tor. Sender and recipient both anonymous. No cloud.

**Use for**: Secure file transfer, anonymous whistleblowing

---

**Send** (send.vis.ee, fork of Firefox Send)  
**Platform**: Web  
**License**: Open source forks available

Encrypted file sharing with expiration. Various instances available.

**Use for**: Quick secure file sharing

---

### Anonymous Publishing

**SecureDrop**  
https://securedrop.org/  
**Platform**: Self-hosted Tor hidden service  
**License**: Free and open source (AGPLv3)

Anonymous whistleblower submission system. Used by journalists and news organizations.

**Use for**: Organizations accepting sensitive leaks

---

**Tor Hidden Services**  
Part of Tor Project  
https://community.torproject.org/onion-services/

Host anonymous websites accessible only via Tor. Censorship resistance.

**Use for**: Anonymous publishing, censorship circumvention

---

## VIII. Development and Hosting

### Code Hosting

**GitLab**  
https://gitlab.com/  
**Platform**: Web, self-hostable  
**License**: Open source (MIT), hosting available

Complete DevOps platform. Self-hostable. CI/CD built-in. GitHub alternative.

---

**Gitea**  
https://gitea.io/  
**Platform**: Self-hosted  
**License**: Free and open source (MIT)

Lightweight self-hosted git service. Easy to install and run. GitHub-like interface.

---

**sourcehut**  
https://sr.ht/  
**Platform**: Web  
**License**: Open source (AGPLv3)

Minimalist, efficient git hosting and project management. Email-driven workflow.

---

### Static Site Generators

**Jekyll**  
https://jekyllrb.com/  
**License**: Free and open source (MIT)

Ruby-based static site generator. GitHub Pages default. Simple, reliable.

---

**Hugo**  
https://gohugo.io/  
**License**: Free and open source (Apache)

Fast static site generator in Go. Extremely quick builds. Good documentation.

---

**mkdocs**  
https://www.mkdocs.org/  
**License**: Free and open source (BSD)

Python static site generator focused on documentation. Markdown-based. Clean themes.

---

## IX. Miscellaneous Essential Tools

### Terminal Multiplexers

**tmux**  
https://github.com/tmux/tmux  
**License**: Free and open source (BSD)

Terminal multiplexer. Split terminal, detach/reattach sessions, share terminals.

**Use for**: Managing multiple terminal sessions, pair programming

---

**screen**  
https://www.gnu.org/software/screen/  
**License**: Free and open source (GPLv3)

Original terminal multiplexer. Simpler than tmux. Runs everywhere.

---

### Shell

**zsh**  
https://www.zsh.org/  
**License**: Free and open source (MIT-like)

Powerful shell. Better than bash for interactive use. Oh-My-Zsh framework popular.

---

**fish**  
https://fishshell.com/  
**License**: Free and open source (GPLv2)

User-friendly shell. Autosuggestions, web-based configuration. "Finally, a command line shell for the 90s."

---

### Utilities

**ripgrep**  
https://github.com/BurntSushi/ripgrep  
**License**: Free and open source (MIT)

Fast grep replacement. Respects .gitignore. Essential command-line tool.

---

**fzf**  
https://github.com/junegunn/fzf  
**License**: Free and open source (MIT)

Fuzzy finder for command line. Interactive filtering. Indispensable once you use it.

---

**jq**  
https://stedolan.github.io/jq/  
**License**: Free and open source (MIT)

Command-line JSON processor. Filter, transform, extract data from JSON.

---

## X. Learning and Documentation

**man pages**  
Built into UNIX/Linux

Read the manual. Always available. High-quality documentation.

```bash
man grep
man ls
man man  # yes really
```

---

**tldr**  
https://tldr.sh/  
**Platform**: CLI, web  
**License**: Free and open source (MIT)

Simplified, practical man pages. Community-driven examples.

```bash
tldr tar
```

---

**ArchWiki**  
https://wiki.archlinux.org/

Best Linux documentation on the internet. Applicable beyond Arch.

---

**StackOverflow**  
https://stackoverflow.com/

For better or worse, essential programming resource. Search before asking.

---

## Principles for Choosing Tools

1. **Open Source**: Prefer tools you can inspect, modify, and share
2. **Privacy**: Minimize data collection and tracking
3. **Self-Hosting**: Control your own infrastructure when possible
4. **Decentralization**: Avoid single points of failure and control
5. **Simplicity**: Simple tools are easier to understand and trust
6. **Interoperability**: Prefer standards and open formats
7. **Sustainability**: Choose tools with active development and community

---

## Contributing

Tools evolve constantly. What's missing? What's outdated?

Submit updates via pull request. See [CONTRIBUTING.md](../CONTRIBUTING.md).

---

## Further Resources

- **[recommended-reading.md](recommended-reading.md)** - Learn underlying concepts
- **[communities-and-links.md](communities-and-links.md)** - Where to get help
- **Privacy Guides**: https://www.privacyguides.org/
- **AlternativeTo**: https://alternativeto.net/ (find alternatives to proprietary software)

---

**License**: CC-BY-SA 4.0  
**Contributors**: Digital Aesthetics Manifesto Community  
**Last Updated**: November 19, 2025
