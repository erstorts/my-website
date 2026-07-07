---
title: "ClickFrame"
slug: clickframe
status: "In progress"
role: "Solo builder"
featured: true
order: 1
last_updated: "July 2026"
summary: "An attribution and measurement pipeline for creators, built as a full data product end to end."
angle: "The interesting part is the measurement: tying spend to outcomes cleanly enough that a creator can trust the number and act on it."
stack:
  - Cloudflare
  - Supabase
  - Stripe
  - GA4
  - BigQuery
  - CI/CD
# Fill these in when ready. Delete any line you do not want to show.
links:
  live: # https://clickframe.example
  repo: # https://github.com/erstorts/clickframe
  writeup: # /blog/clickframe-architecture/
---

<!--
  DRAFT COPY — Emmett to rewrite in his own voice.
  Voice rules: result first, then mechanism. Concrete numbers where you have them.
  No em dashes. First person. Show the reasoning, not just the artifact.
  Replace every [PLACEHOLDER] with a real detail.
-->

## Problem

Creators spend on content and ads without a clean read on what the spend actually returns. The data lives in a handful of tools that never agree, so the honest answer to "did that work" is usually a guess. ClickFrame exists to make that answer defensible.

## Approach

I treated this as a measurement problem first and a software problem second. Before writing much code I decided what "an outcome" means, how it ties back to a specific piece of spend, and where the double-counting risks are. Then I built the smallest pipeline that produces that number end to end, with every step traceable back to source.

## What I built

A full data product, owned solo from ingestion to dashboard:

- Ingestion and event capture on Cloudflare, with data landing in Supabase.
- Payments and revenue through Stripe, reconciled against [PLACEHOLDER: what you reconcile against].
- Analytics and warehousing through GA4 and BigQuery.
- CI/CD so changes ship safely, plus disaster-recovery work after [PLACEHOLDER: the incident or risk that prompted it] so a bad day does not mean lost data.

## Outcome

[PLACEHOLDER: the strongest concrete result so far. A number if you have one. If it is early, say what is live and what it already lets a user do.]

## Why it is here

ClickFrame is on this site as evidence, not as a startup I am pitching. It shows I can stand up a whole data function alone: pipelines, payments, warehousing, deployment, and the measurement thinking that makes the output trustworthy.
