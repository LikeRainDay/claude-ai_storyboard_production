---
name: Animator Skill
description: Motion prompt methodology for AI video generation models
version: 1.0.0
---

# Animator Skill

This skill package equips the Animator with specialized knowledge for creating dynamic motion prompts optimized for AI video generation workflows.

## Skill Components

### 1. **motion-prompt-methodology.md**

Comprehensive guide to motion prompt principles:

- Simplicity and focus (one primary motion)
- Directionality and speed specification
- Subject vs camera motion distinction
- Physical plausibility for video duration
- Video model optimization techniques

### 2. **Templates**

- `motion-prompt-template.md` — Structured format for motion prompt output

## Purpose

The Animator uses this skill to:

- Transform 4-panel static sequences into temporal motion descriptions
- Optimize prompts for video generation models (Runway, Pika, SVD, etc.)
- Maintain subject consistency from source sequences
- Ensure physically realistic motion descriptions

## When to Use This Skill

The Animator should reference this skill when:

- Creating motion prompts from approved sequence boards
- Resolving Director feedback about motion clarity
- Determining appropriate motion complexity for duration
- Specifying camera movement vs subject movement

## Key Principle: Simplicity Over Complexity

**Video models perform better with focused, clear instructions**:

- One primary motion (not three simultaneous actions)
- Clear directionality (left to right, toward camera, etc.)
- Realistic pacing (motion can complete in 3-5 seconds)
- Subject-focused (less exhaustive scene description than static prompts)

## Skill Activation

This skill is **always active** for the Animator agent. All motion prompts must conform to the methodology and template defined here.

---

**Usage**: The Animator agent automatically references this skill. No manual invocation required.
