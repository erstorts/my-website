---
title: "Colorado Catholic Business Directory"
slug: co-catholic-directory
status: "Live"
role: "Solo builder"
featured: false
order: 4
last_updated: "July 2026"
summary: "A searchable directory app used at monthly community meetings, built from messy source data."
angle: "Most of the work was upstream: ingesting and cleaning inconsistent records into something people can actually search."
stack:
  - Streamlit
  - Python
  - Data cleaning
links:
  live: # add the live URL
  repo: # https://github.com/erstorts/...
---

<!--
  DRAFT COPY — Emmett to rewrite. Replace every [PLACEHOLDER]. No em dashes. Result first.
-->

## Problem

A local community had a growing list of member businesses in [PLACEHOLDER: the messy source, e.g. a spreadsheet] that was hard to search and easy to let go stale. They needed something usable in the room during a monthly meeting.

## Approach

I put the effort where it mattered, in ingestion and cleaning, then wrapped a light Streamlit interface around the clean data. The app is deliberately simple. The reliability comes from the pipeline behind it.

## What I built

- A repeatable ingestion and cleaning step that turns inconsistent records into a consistent dataset.
- A Streamlit directory people can search and filter live.

## Outcome

Used at monthly meetings by [PLACEHOLDER: who and how many]. [PLACEHOLDER: any other concrete result.]

## Why it is here

It is a small, honest example of the unglamorous half of data work: the cleanup that makes everything downstream trustworthy.
