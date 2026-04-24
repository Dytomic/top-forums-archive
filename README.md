# Tales of Pirates Forums Archive

Archived snapshots of three community forums covering the Tales of Pirates (TOP), Pirate King Online (PKO), and Kings of Pirates (KOP) game engine family. Preserved as a research archive by [Dytomic](https://github.com/Dytomic), an independent MMORPG studio, to keep years of private-server development knowledge accessible, since community forums periodically go offline.

Each forum is stored in both **original unmodified HTML** (for fidelity) and **Markdown** (for search and reference).

## Contents

| Forum | Source | Language | Threads | Sections |
|-------|--------|----------|---------|----------|
| [PKO DEV](pkodev) | [pkodev.com](https://pkodev.com) | English | 166 | 12 |
| [RageZone: Tales of Pirates](ragezone) | [forum.ragezone.com](https://forum.ragezone.com/community/tales-of-pirates.440/) | English | 1,350 | 5 |
| [Go-Piratia](gopiratia) | [go-piratia.ru](https://go-piratia.ru) | Russian | 167 | 24 |
| **Total** | | | **1,683** | **41** |

## Why this archive exists

Tales of Pirates (TOP), known regionally as Pirate King Online (PKO) or Kings of Pirates (KOP), is a 2005-era MMORPG whose engine, client, and server stack have been the subject of long-running community reverse-engineering work. Much of the technical knowledge about the engine (source builds, server setup guides, mod releases, Lua scripting, client patching, packet analysis) lives only in community forum threads, many of which predate modern archiving.

Several of these forums have gone through server migrations, database resets, moderation purges, or outright shutdowns over the years. This archive preserves the public technical content of three of the most active forums in the TOP/PKO/KOP scene, at a known point in time, for ongoing research reference.

## Forum details

### PKO DEV (pkodev.com)

A developer-centric forum focused on Tales of Pirates private-server development: source code releases, server setup guides, Lua scripting, client modding, and community collaboration.

Key content preserved:

- **Guides**: Full source code setup, server setup guides (binaries and source), quest creation, map coordinates and locations
- **Releases**: 97-thread archive covering Tales of Pirate 2022 DX9, Tales of Pirate 2026 DX9, Corsair Online, PKO Admin Tool, and the 2016 Source Code release
- **Development**: Fitting room, shadow font, sit button, banish soul, resurrection system, level-next-to-nickname, auto-stat button, weekprize addon
- **Programming**: DX9 rendering discussions
- **Questions & Help**: 21 threads (most active Q&A thread: 53 replies on "Help with 2022 DX9 Files")

### RageZone: Tales of Pirates (forum.ragezone.com)

The Tales of Pirates subforum on [RageZone](https://forum.ragezone.com), one of the longest-running MMO private-server community sites. This is the largest of the three archives with 1,350 threads across five sections.

| Section | Threads |
|---------|---------|
| Main | 1,105 |
| Help | 200 |
| Releases | 25 |
| Tutorials | 17 |
| Developments | 3 |

### Go-Piratia (go-piratia.ru)

Russian-language Tales of Pirates / Piratia community forum. Covers development, guides, private-server discussion, releases, and general community topics for the Russian-speaking ToP scene. 24 sections spanning applications, archive, buying, C++, development, documentation, general, guides, and more.

## Repository structure

```
top-forums-archive/
├── pkodev/
│   ├── html/     Original HTML snapshots
│   └── *.md      Markdown index and per-section content
├── ragezone/
│   └── html/     Original HTML snapshots, organized by section
└── gopiratia/
    ├── html/     Original HTML snapshots
    └── md/       Markdown conversions
```

## Status

Preserved. The archive is static and is not being actively updated. Content is a point-in-time snapshot of each forum at the time of capture.

## Related

- [Dytomic](https://github.com/Dytomic) — parent organization
- [dytomic-github-io](https://github.com/Dytomic/Dytomic.github.io) — Dytomic studio archive and main site, which describes this archive in its Research section
- [pkodev-V3ct0r1024](https://github.com/Dytomic/pkodev-V3ct0r1024) — mirrored TOP/PKO community mods, tools, and server projects (V3ct0r1024)
- [pkodev-Perseus](https://github.com/Dytomic/pkodev-Perseus) — mirrored TOP/PKO community server, proxy, and CMS projects (Perseus)

## License and attribution

Forum content is © the original authors. This repository mirrors publicly accessible posts for preservation and research reference only; no ownership of the underlying content is claimed. If you are an author and would like a post removed, open an issue.
