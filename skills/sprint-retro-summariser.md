---
type: skill
id: sprint-retro-summariser
title: Sprint Retro Summary Builder
description: "Assembling the sprint retrospective brief, action items, and tracked progress into a structured, team-ready retro summary"
tags: [Production, Agile, Metrics]
connections:
  - target: llm-service
    type: runs_on
metadata:
  estimated_duration: "3 minutes"
  avg_tokens: 2500
  trigger: manual
---

## Sprint Retro Summary Builder

This skill assembles the outputs of the earlier pipeline stages into a single, structured sprint retrospective summary ready for the team.

### Core Capability

Given the summarised retrospective brief, the extracted action items, and the tracked sprint progress, this skill organises everything into clear categories — what went well, what needs improvement, and prioritised action items with owners for the next sprint.

### Method

1. **Gather inputs:** Take the retrospective brief, the action-item list, and the progress summary from the upstream stages.
2. **Categorise:** Sort the discussion into what went well, what needs improvement, and concrete next-sprint actions.
3. **Prioritise:** Order action items by impact and assign owners where the notes make them clear.

### Output Structure

A structured markdown summary with headed sections for strengths to maintain, improvement areas, and owned action items. This is the deliverable the language-polish stage refines for publication.
