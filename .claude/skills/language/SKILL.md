---
name: language
description: Set output language preference for script generation
trigger: /language
---

# Language Configuration

Set the default language for script generation and storyboard outputs.

## Usage

```
/language zh-CN
```

Or:

```
/language
```

(Will prompt for language selection)

## Supported Languages

- **zh-CN**: Chinese (Simplified) - 简体中文 [DEFAULT]
- **en-US**: English (United States)
- **ja-JP**: Japanese - 日本語
- **ko-KR**: Korean - 한국어

## What This Does

1. **Updates** `.agent-state.json` with language preference
2. **Applies to**:

   - Script generation language
   - Character dialogue
   - Scene descriptions
   - All generated narrative content

3. **Does NOT affect**:
   - Image prompts (always optimized for AI models)
   - Technical configurations
   - System commands

## Scope

### Global Language Setting

Sets default for all new episodes:

```
/language zh-CN
```

Saves to `.agent-state.json`:

```json
{
  "language": "zh-CN",
  ...
}
```

### Per-Episode Language

Override for a specific episode:

```
/script ep02 --lang en-US
```

Episode-specific setting in `.agent-state.json`:

```json
{
  "episodes": {
    "ep02": {
      "language": "en-US",
      ...
    }
  }
}
```

## Language Characteristics

### Chinese (zh-CN) - 简体中文

- Literary, descriptive scene descriptions
- Natural Chinese dialogue with context-appropriate formality
- Chinese punctuation (「」for quotes)
- Cultural context included when relevant
- **Default language for this system**

### English (en-US)

- Clear, active voice for action lines
- Contemporary dialogue style
- Standard screenplay formatting
- Concise and direct descriptions

### Japanese (ja-JP) - 日本語

- Descriptive visual language
- Appropriate honorifics (さん、様、ちゃん, etc.)
- Japanese cultural context
- Japanese punctuation

### Korean (ko-KR) - 한국어

- Natural Korean sentence structure
- Appropriate speech levels (존댓말/반말)
- Korean cultural appropriateness
- Korean punctuation

## Example

```
User: /language en-US

System: ✓ Language set to English (en-US)

        All new scripts will be generated in English.
        Existing episodes retain their current language.

        To generate a specific episode in a different language:
        /script ep02 --lang ja-JP

User: /script ep03

System: Language: English (en-US)
        Generating script for ep03...
```

## Viewing Current Language

```
/status
```

Output will show:

```
Global Language: Chinese (zh-CN)

Episode ep01:
  Language: Chinese (zh-CN)
  ...

Episode ep02:
  Language: English (en-US)  ← Episode-specific override
  ...
```

## Notes

- **Image prompts** are always generated in English for optimal AI model compatibility
- **Motion prompts** are always in English (video models are English-trained)
- **Scripts and narrative content** use your selected language
- **Character names** can be in any language regardless of script language

## Recommended Workflow

1. **Set global language** before starting project:

   ```
   /language zh-CN
   ```

2. **Generate multilingual series** if needed:

   ```
   /script ep01 --lang zh-CN  (Chinese episode)
   /script ep02 --lang en-US  (English episode)
   /script ep03 --lang ja-JP  (Japanese episode)
   ```

3. **All episodes share storyboard stages**, but narrative content adapts to language
