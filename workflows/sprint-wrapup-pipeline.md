---
type: workflow
id: sprint-wrapup-pipeline
title: Sprint Wrapup Pipeline
description: "Summarises sprint retrospective and extracts action items for the next sprint"
tags: [Production]
connections:
  - target: text-summarisation
    type: uses
  - target: action-item-extraction
    type: uses
  - target: sprint-retro-summary
    type: uses
---

## Overview

This workflow processes sprint retrospective notes through summarisation and action item extraction, then produces a structured retro summary ready for the team.

## Pipeline Stages

### Stage 1: Summarise Retro Notes

Invoke the **text-summarisation** skill against the raw retrospective notes to distil key themes and discussion points.

### Stage 2: Extract Action Items

Invoke the **action-item-extraction** skill to capture all improvement actions agreed during the retro.

### Stage 3: Format Retro Summary

Invoke the **sprint-retro-summary** prompt to combine outputs into a structured summary with clear sections for what went well, what needs improvement, and prioritised action items.

## Output

A structured retrospective summary containing:

- What went well (team strengths to maintain)
- What needs improvement (areas for the next sprint)
- Action items with owners for the next sprint
