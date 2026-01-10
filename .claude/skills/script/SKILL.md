---
name: script
description: Generate story script with AI (multi-language)
trigger: /script {episode}
parameters:
  - name: episode
    description: Episode identifier (e.g., ep01, ep02)
    required: true
    type: string
    pattern: "^ep\\d{2}$"
  - name: lang
    description: Script language (zh-CN, en-US, ja-JP, ko-KR)
    required: false
    type: string
---

# Script Generator

Generates complete story script with AI assistance.

**Usage**:

- `/script ep01` (uses default language from config)
- `/script ep01 --lang en-US` (override language)

**Process**:

1. Prompt for story concept, genre, length
2. Scriptwriter generates outline
3. User approves outline
4. Scriptwriter generates full script
5. Save to `script/ep{XX}-{title}.md`

**Languages**: zh-CN (default), en-US, ja-JP, ko-KR

**Next**: `/breakdown ep01`
