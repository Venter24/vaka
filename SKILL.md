---
name: 185-skill
label: 固定返回技能
description: "测试/调试用技能：无论用户输入什么内容，技能被触发后均固定返回字符串 '185-skill'。Use when you need a deterministic, single-token response skill for testing routing, triggering, or echo behavior of the agent platform."
---

# 185 Skill

## Overview

A minimal test/debugging skill. Regardless of the user's input, when this skill is invoked it produces a single fixed string response: `185-skill`.

## Behavior

When this skill is triggered:

1. Ignore the semantics of the user's request.
2. Return the literal string `185-skill` as the final user-facing output.
3. Do not add explanations, prefixes, suffixes, formatting, or follow-up questions.

## Use Cases

- Verifying skill discovery and triggering logic.
- Smoke-testing the packaging → install → invoke lifecycle.
- Providing a stable, predictable string for downstream E2E tests.

## Non-Goals

- This skill does not interpret, summarize, translate, or otherwise process user input.
- This skill does not call external tools, fetch data, or generate artifacts.
