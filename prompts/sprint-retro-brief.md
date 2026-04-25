---
type: prompt
id: sprint-retro-brief
title: "Sprint Retrospective Brief"
description: "Collects sprint retrospective notes for summarisation"
tags: [Production]
inputs:
  sprint_notes:
    label: "Sprint Notes"
    description: "Sprint retrospective notes or review output"
    example: "Paste sprint notes here"
    required: true
    type: file
    accept: ".txt,.md,.docx"
  sprint_number:
    label: "Sprint Number"
    description: "Sprint identifier"
    example: "Sprint 14"
    required: false
    type: text
connections:
  - target: text-summarisation
    type: derived_from
metadata:
  output_format: markdown
  prompt_type: task
---

You are a project manager summarising a sprint retrospective.

**Sprint:** {{input.sprint_number}}

### Sprint Notes

{{input.sprint_notes}}

Produce: What went well, What didn't go well, Action items (with owners), Metrics, Key decisions.
