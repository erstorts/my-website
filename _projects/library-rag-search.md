---
title: "Library RAG Search"
slug: destiny-rag
status: "Live"
role: "Solo builder"
featured: true
order: 2
last_updated: "July 2026"
summary: "A retrieval-augmented search tool over a real library collection, built for an actual stakeholder."
angle: "Hybrid retrieval is the lever: combining dense and sparse search so a vague question still lands on the right passage."
stack:
  - Pinecone
  - OpenAI embeddings
  - GPT-4o-mini
  - Python
links:
  live: # add the live URL
  repo: # https://github.com/erstorts/destiny-rag
  writeup: # /blog/...
---

<!--
  DRAFT COPY — Emmett to rewrite in his own voice.
  Replace every [PLACEHOLDER] with a real detail. No em dashes. Result first.
-->

## Problem

[PLACEHOLDER: the stakeholder] needed to find the right material in a collection that keyword search handled badly. A reader knows what they mean but not the exact words in the text, and plain search punishes that.

## Approach

I built a retrieval-augmented pipeline around hybrid search, pairing dense embeddings with sparse matching so both meaning and exact terms count. The generation layer stays small and cheap on purpose. The value is in retrieval quality, not in a large model papering over weak retrieval.

## What I built

- A Pinecone hybrid index over the collection, with OpenAI embeddings for the dense side.
- Answer generation through GPT-4o-mini, grounded in retrieved passages.
- A working MVP a real stakeholder uses, not a demo.

## Outcome

[PLACEHOLDER: how well it works and how it is used. A retrieval-quality figure or a usage note if you have one.]

## Why it is here

It shows I can take a modern retrieval stack from a real person's problem to a live tool, and that I make deliberate cost and quality tradeoffs rather than reaching for the biggest model by default.
