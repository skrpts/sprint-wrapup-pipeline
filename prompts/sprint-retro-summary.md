---
type: prompt
id: sprint-retro-summary
title: Sprint Retro Summary
description: "Task prompt for structuring sprint retrospective notes into actionable categories"
tags: [Production, Agile, Metrics]
inputs:
  sprint_number:
    label: "Sprint Number"
    description: "The sprint number"
    example: "14"
    required: true
    type: text
context_params:
  retro_brief:
    label: "Retro Brief"
    description: "The summarised retrospective brief from the earlier summarisation stage."
    required: false
    default_from_previous: true
  action_items:
    label: "Action Items"
    description: "The action items extracted from the retrospective."
    required: false
  progress:
    label: "Tracked Progress"
    description: "The tracked sprint progress from the progress-tracking stage."
    required: false
connections:
  - target: text-summarisation
    type: derived_from
  - target: action-item-extraction
    type: derived_from
  - target: progress-tracking
    type: derived_from
---

## Purpose

Converts raw sprint retrospective notes into a structured summary with clear categories for what went well, what needs improvement, and concrete action items for the next sprint.

## Prompt

Take the following sprint retrospective analysis and produce a structured summary: what went well, what needs improvement, and action items for next sprint.

## Sprint

{{input.sprint_number}}

## Retrospective Brief

{{step.context.retro_brief}}

## Action Items

{{step.context.action_items}}

## Tracked Progress

{{step.context.progress}}
