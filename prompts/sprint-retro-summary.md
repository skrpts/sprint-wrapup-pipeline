---
type: prompt
id: sprint-retro-summary
title: Sprint Retro Summary
description: "Task prompt for structuring sprint retrospective notes into actionable categories"
tags: [Production]
connections:
  - target: text-summarisation
    type: derived_from
  - target: action-item-extraction
    type: derived_from
---

## Purpose

Converts raw sprint retrospective notes into a structured summary with clear categories for what went well, what needs improvement, and concrete action items for the next sprint.

## Prompt

Take the following sprint retrospective analysis and produce a structured summary: what went well, what needs improvement, and action items for next sprint.

## Sprint

{{input.sprint_number}}

## Summary from Stage 1

[The summary of retro notes from Stage 1]

## Action Items from Stage 2

[The extracted action items from Stage 2]
