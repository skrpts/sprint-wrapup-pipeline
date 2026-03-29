---
type: prompt
id: summarise-text
title: Summarise Text
description: "Core prompt for condensing text into concise summaries"
tags: [Production, Agile, Metrics]
connections:
  - target: text-summarisation
    type: derived_from
---

## Purpose

General-purpose summarisation prompt that captures key points, decisions, and action items from any text input.

## Prompt

You are an expert summariser. Given the following text, produce a concise summary capturing the key points, decisions, and action items.

### Inputs

{{input.meeting_notes}}
