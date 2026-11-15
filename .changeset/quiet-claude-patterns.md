---
'@mastra/schema-compat': patch
---

Fixed Anthropic tool and structured output schemas losing `pattern`, `minLength`, `maxLength` and `format` on Claude models other than `claude-3.5-haiku`. These keywords were being removed and rewritten into the property description, so the model no longer saw them as schema constraints. Only `claude-3.5-haiku` still gets this rewrite.
