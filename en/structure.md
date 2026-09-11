# Collection structure

[Português](../pt/estrutura.md) · **English**

This document fixes how the project names and organises its files. The rule exists for a simple reason: a bilingual collection that grows without convention becomes unreadable within months, and newcomers find nothing. Anyone proposing a structural change should amend this document in the same delivery.

## The layout

```
por-um-futuro-em-comum/
├── README.md              short bilingual door for arrivals
├── CONTRIBUTING.md        bilingual door for contributors
├── LICENSE.md             license, bilingual
├── CITATION.cff           citation metadata, machine-read
├── AGENTS.md              instructions for agents
├── CLAUDE.md              instructions for Claude
│
├── pt/                    the full collection in Brazilian Portuguese
│   ├── README.md          index of this tree
│   ├── manifesto.md
│   ├── pesquisa/
│   │   ├── README.md      research index
│   │   └── datacenters/
│   │       └── README.md  index of this study
│   └── ...
│
├── en/                    the full collection in English, names in English
│   ├── README.md
│   ├── manifesto.md
│   └── research/
│       └── datacenters/
│
└── dados/                 raw data, language-neutral, cited by both trees
    └── datacenters/
```

**One tree per language, complete and independent.** Readers enter at their own language root and never need to leave it, except to reach a raw data file. Adding Spanish tomorrow means creating `es/` mirroring the structure, touching nothing else.

## Filename rules

**1. Lowercase, no accents, no spaces, hyphens between words.**

```
right:  affected-communities.md
wrong:  Affected Communities.md, COMMUNITIES.md, affected_communities.md
```

**2. No cedillas, tildes, or accents in filenames.** This is not fussiness:

- In a URL, `ações.md` becomes `a%C3%A7%C3%B5es.md`, which nobody can read aloud or type.
- Unicode has two ways to write "ç". Windows, macOS, and Linux disagree on which to use, so the same file can appear twice in history, or vanish on a contributor's machine.
- Some publishing tools simply fail on them.

**The accent belongs in the title inside the file.** The filename is an address; the title is what the reader reads:

```
file:        pt/pesquisa/acoes.md
first line:  # Caminhos de ação
```

**3. The name is translated along with the text.** A file in the English tree has an English name, folders included. `pt/pesquisa/acoes.md` corresponds to `en/research/actions.md`. An English reader should never meet a Portuguese word in an address, nor the reverse: the project is bilingual in every instance, and the address is the first thing a person reads.

**4. Exception: names the machine recognises are not translated.**

| Name | Who reads it | What breaks if translated |
|---|---|---|
| `README.md` | GitHub, site generators | The folder loses its visible index |
| `LICENSE.md` | GitHub, license tooling | The project stops declaring a license |
| `CONTRIBUTING.md` | GitHub | The notice shown when opening an issue or PR disappears |
| `CITATION.cff` | GitHub, Zenodo, reference managers | The citation button disappears |
| `AGENTS.md`, `CLAUDE.md` | AI agents | The agent cannot find its instructions |

These are technical names, like a file extension. Translating them does not make the project more bilingual; it only switches the feature off. Their *contents*, on the other hand, are bilingual.

**5. `README.md` is the index of every folder.** Every content folder has one, in both languages, presenting what lives there and why. It is the file GitHub displays automatically when the folder is opened.

**6. No loose content files at the root.** The root holds only the doors and the technical names in the table above.

## Document rules

**Header.** Directly under the title, the language line, with the current language in bold and its counterpart as a link:

```markdown
# Paths for action

[Português](../../pt/pesquisa/acoes.md) · **English**
```

**Internal links are always relative** (`../../pt/pesquisa/acoes.md`), never starting with `/`. Relative links work when browsing GitHub and are converted automatically on the project site. Absolute links break in both.

**Footer.** Every document ends with the editorial record, in the form defined in [editorial credits](editorial-credits.md):

```markdown
<!-- editorial-record -->
---

**Model:** model name (`identifier`).

**Reviewer:** reviewer's public name.
```

**Dates in numeric form, year to day:** `2026-09-10`. Never `10/09/2026`, which an English reader takes to mean 9 October.

## Growing without getting lost

**A new research topic** is a new folder inside `pesquisa/` and `research/`, with a `README.md` in each, and the complete pair of documents. Never publish one side alone: the incomplete pair is where every bilingual mess begins.

**A new document** goes into its topic folder, is cited in that folder's `README.md`, and is born in both languages.

**A new language** is a new root (`es/`, `fr/`) mirroring the structure, with every name translated. Add its door to the root `README.md`.

**A raw data file** goes to `dados/`, in the subfolder of the topic that cites it, with a descriptive name. Use the `.original` suffix when the file is a faithful copy of what the source published, with no processing: `the-dalles-opb.original.json`. Data has no language and is never duplicated; both trees cite the same file, which is why it lives outside them.

**When a folder passes about fifteen documents**, it has become two. Split it by topic before the list becomes unreadable, and update the `README.md`.

<!-- editorial-record -->
---

**Model:** Claude Opus 5 (`claude-opus-5`).

**Reviewer:** [andromedus. (@Androquimera)](https://github.com/Androquimera).
