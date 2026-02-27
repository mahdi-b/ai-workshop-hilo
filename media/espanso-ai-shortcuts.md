# Espanso AI Prompt Shortcuts

[Espanso](https://espanso.org/) is a cross-platform text expander that helps you type faster by replacing keywords with frequently used phrases. These shortcuts are particularly useful when working with AI assistants like Claude, ChatGPT, or other LLMs.

## Installation
1. Download Espanso from [espanso.org](https://espanso.org/)
2. Add these shortcuts to your Espanso configuration file
3. Type the trigger text anywhere to expand it

## AI Prompt Shortcuts

### 1. Before You Start (`;bys`)
**Trigger:** `;bys`
**Expands to:**
> Before you start, can you walk me back through what you understood from the above, either implicit or explicit. Then explain how you'd go about solving this without implementing the solution.

**Use Case:** Great for ensuring the AI understands your request before diving into implementation. Helps catch misunderstandings early and see the AI's planned approach.

---

### 2. No Assumptions (`;noa`)
**Trigger:** `;noa`
**Expands to:**
> Don't assume anything. If there's ambiguity, missing context, or anything you're unsure about, ask me questions first rather than guessing at what I mean.

**Use Case:** Prevents the AI from making incorrect assumptions. Encourages clarifying questions when your initial prompt might be ambiguous.

---

### 3. Help Me Prompt (`;hmp`)
**Trigger:** `;hmp`
**Expands to:**
> Based on the idea above, interview me to help me turn it into a well-scoped prompt. Ask up to 5 clarifying questions, one at a time. After my answers, write a final, ready-to-use prompt that includes the goal, relevant context, constraints, and desired output format — something I can paste into a new chat and get a good result on the first try.

**Use Case:** Transforms vague ideas into well-structured prompts. The AI will guide you through creating a comprehensive prompt that gets better results.

## How to Add to Espanso

Add these to your Espanso `match` file (usually `~/.config/espanso/match/base.yml` on Mac/Linux or `%APPDATA%\espanso\match\base.yml` on Windows):

```yaml
matches:
  - trigger: ";bys"
    replace: "Before you start, can you walk me back through what you understood from the above, either implicit or explicit. Then explain how you'd go about solving this without implementing the solution."

  - trigger: ";noa"
    replace: "Don't assume anything. If there's ambiguity, missing context, or anything you're unsure about, ask me questions first rather than guessing at what I mean."

  - trigger: ";hmp"
    replace: "Based on the idea above, interview me to help me turn it into a well-scoped prompt. Ask up to 5 clarifying questions, one at a time. After my answers, write a final, ready-to-use prompt that includes the goal, relevant context, constraints, and desired output format — something I can paste into a new chat and get a good result on the first try."
```

## Tips for Using These Shortcuts

1. **Start conversations with `;noa`** when your request might have multiple interpretations
2. **Use `;bys`** for complex technical tasks to verify understanding before implementation
3. **Apply `;hmp`** when you have a rough idea but need help structuring it properly
4. **Combine shortcuts** - you can use multiple in the same conversation as needed
5. **Customize the triggers** - change `;bys` to something else if you prefer different keywords

## Why These Work

These prompts leverage key principles of effective AI interaction:
- **Clarity First**: Ensuring mutual understanding before action
- **Explicit Communication**: Removing ambiguity from instructions
- **Structured Thinking**: Breaking down complex ideas into well-defined components
- **Iterative Refinement**: Using the AI to help improve your own prompting

## Additional Resources

- [Espanso Documentation](https://espanso.org/docs/)
- [Prompt Engineering Guide](../demos/prompt_errors_playground.html)
- [AI Workshop Materials](../index.html)

---

*These shortcuts were shared during the "AI, Demystified" workshop by Mahdi Belcaid at UH Mānoa.*