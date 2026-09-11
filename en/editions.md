# Editions and citation

[Português](../pt/edicoes.md) · **English**

The collection is alive: it changes when a better source appears, when someone corrects a figure, when a new case comes in. That is good for the work and bad for anyone who needs to cite it, because a text that keeps changing cannot be a reference for anything.

An **edition** solves this. It is a cut of the collection on a given date — frozen, packaged, and permanently identified. The collection keeps changing; the edition does not.

## What an edition is

An edition is published under the repository's **Releases** tab and gathers three things:

1. **Release notes** — what changed since the previous edition, which sources came in, what was corrected, and who contributed during the period.
2. **The single document** — that cut of the collection assembled into one file per language, for anyone who wants to read it end to end or print it.
3. **A DOI** — the permanent identifier assigned by [Zenodo](https://zenodo.org), the same kind of identifier a scientific paper carries.

The DOI is the difference between "a GitHub link that may still exist in 2030" and a reference citable in a bibliography, in public policy, in a legal filing. It keeps working even if the repository changes name, owner, or address.

## When to publish an edition

There is no calendar. An edition ships when the accumulated work justifies the effort of freezing it:

- a study has reached a state that stands on its own, with method, sources, and limits declared;
- a significant correction has changed a conclusion from an earlier edition;
- the collection went through a large reorganisation and the older version needs to stay reachable.

Publishing too many editions cheapens the idea. Publishing too few leaves the work without a fixed address.

## Naming

The edition tag follows **year dot number**, with a prefix when the cut covers a single topic:

| Tag | What it is |
|---|---|
| `2026.1` | first general edition of the collection in 2026 |
| `2026.2` | second general edition the same year |
| `datacenters-2026.1` | first edition of the data center study |

The edition title is bilingual, following the same pattern as everything in the project:

```
2026.1 — Crise ambiental e infraestrutura de IA / Environmental harm and AI infrastructure
```

## What goes into the notes

Release notes are bilingual and carry, in this order:

1. **What this edition contains** — in a few lines, what the reader will find.
2. **Changes since the previous edition** — corrections, new sources, revised conclusions. In the first edition, what existed at the start.
3. **Credits** — who contributed during the period and with what, in the form described in [contributors](contributors.md). This is where each person points at where they entered the work.
4. **Editorial record** — model and reviewer, as in any project publication.
5. **Limits** — what the edition does not claim, what remains unverified, what has not been measured.

## The steps

1. Check that both language trees are complete and in parity.
2. Generate the single document for each language and attach it to the edition.
3. Update `CITATION.cff`: fill in `version` and `date-released`.
4. Publish the release on GitHub with the tag and the notes.
5. Zenodo archives the edition on its own and returns the DOI.
6. Add the DOI to `CITATION.cff` under `identifiers`, and record the edition in this document.

## Connecting Zenodo

Done once, and it has to be done by Androquimera, because it involves authorising Zenodo to see the repository:

1. Sign in to [zenodo.org](https://zenodo.org) using the GitHub account.
2. Open the GitHub panel inside Zenodo and flip the switch for the `por-um-futuro-em-comum` repository.
3. From then on, **every release published on GitHub is archived automatically** and receives a DOI.

Zenodo reads the repository's `CITATION.cff` to fill in authorship, license, and description, and returns two identifiers: a DOI for each edition and a general DOI that always points to the most recent one. In project references, use the specific edition's DOI when citing a figure or a conclusion, and the general one when citing the project as a whole.

The repository must be public at the moment of the release, and stays reachable afterwards: Zenodo keeps its copy even if GitHub goes away.

## Published editions

None so far. The first will be recorded here when it ships.

<!-- editorial-record -->
---

**Model:** Claude Opus 5 (`claude-opus-5`).

**Reviewer:** [andromedus. (@Androquimera)](https://github.com/Androquimera).
