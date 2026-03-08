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

Take these sprint retrospective notes and produce: what went well, what needs improvement, action items for next sprint.
