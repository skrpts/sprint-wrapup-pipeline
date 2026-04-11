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

{{steps.previous.output}}

## Action Items from Stage 2

{{steps.Action Item Extraction.output}}
