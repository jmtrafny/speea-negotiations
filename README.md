# Contract Policy Modeler

A private, in-browser tool that helps SPEEA-represented Boeing employees decide **how they will vote before the contract arrives**. You define what a satisfactory contract would give you, weigh the tradeoffs, and write down your evidence and decision rules ahead of time, so reading the tentative agreement becomes a checklist instead of a scramble.

**This is an independent, one-person project.** It is not made, reviewed, endorsed, or sponsored by SPEEA or The Boeing Company. It contains no contract terms, no bargaining updates, and no vote recommendation. SPEEA and Boeing are named only to describe the vote the tool is meant to help you prepare for.

## Try it

Open [`defret.html`](defret.html) directly in a browser. There is nothing to build or install — it's a single self-contained HTML file with inline CSS and JavaScript, and no external requests, fonts, libraries, or analytics.

## What it does

The modeler walks you through six steps:

1. **Set the frame** — describe what a contract worth voting for should give you, your comparison horizon, and the baseline you'll measure offers against.
2. **Define outcomes** — decide which topics count as tradeable dials (pay, remote work, hours and leave, health benefits, retirement, employment security, coworker outcomes, voice and process, or your own). For each dial, write the low end and high end of a realistic range in your own words, plus the outcome halfway in value to you. Each topic has a made-up example range you can open for reference; nothing is prefilled.
3. **Set priorities** — express relative importance either as swing weights or as a simple ranking. Percentages are calculated from your inputs. Nothing is pre-weighted.
4. **Check tradeoffs** — answer pairwise comparisons and calibrate hypothetical package bundles against your own judgment, with basic consistency checks between your weights and your stated preferences.
5. **Write the rules** — record your own rules for evidence, contingent pay, ambiguous facts, combined concessions, coworker interests, and the risk of further bargaining. These stay as your own words and are never converted into a score.
6. **Save your policy** — export a readable Markdown or text policy document, or the full JSON profile, and optionally freeze a dated, versioned snapshot.

## What it doesn't do

- It does not contain any SPEEA or Boeing contract language, past agreements, or bargaining updates.
- It does not parse a real contract, map clauses to your outcomes, or score an actual offer.
- It does not forecast bargaining outcomes, strike risk, or a future offer.
- It does not tell you how to vote. The numerical index is a personal, provisional check against your own stated judgments, not an assessment instrument.

## Privacy

- After the page loads, it makes no network requests. Nothing you type is sent anywhere.
- Your profile stays in this browser tab unless you explicitly turn on **Remember this profile in this browser** (unencrypted `localStorage`) or export it yourself.
- **Export JSON** is the portable backup. Browser storage does not follow you to another device, and it can be cleared by clearing site data.
- Policy-text exports omit a few private structured fields (salary, commute, current arrangement, financial goal, budget, and disruption horizon) by default. Free text is never automatically redacted. Review any export before sharing it.
- Share the blank link with coworkers, never a filled-in profile.

## Versioning and revisions

Each profile carries a revision number and an optional frozen snapshot marker. Freezing locks the interface against accidental edits. Starting a new revision requires recording a reason, and the prior policy text is archived inside your JSON profile. Snapshot IDs are non-cryptographic change markers, not signatures. They don't prove authorship or detect tampering.

## Method references

The pairwise-comparison and swing-weight approach follows standard multi-criteria decision analysis practice:

- [UK government — Multi-criteria analysis: a manual (2009)](https://assets.publishing.service.gov.uk/media/5a790545e5274a2acd18b975/1132618.pdf), §§5.4 and 6.2
- [NASA Systems Engineering Handbook — Decision Analysis](https://www.nasa.gov/reference/6-8-decision-analysis/)

## Status

Version 1.0. Not a validated assessment instrument, just a structured way to write your own values down before you need them.
