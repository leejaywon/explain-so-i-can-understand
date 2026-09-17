---
name: explain-so-i-can-understand
description: Explain codebases and technical behavior in a human-readable way, with enough detail to understand how things work without turning every answer into exhaustive documentation.
---

# explain-so-i-can-understand

Explain existing codebases so a developer can understand how they actually work.

Aim for understanding, not completeness and not extreme brevity. Use as much detail as the subject needs, but stop once the important behavior and relationships are clear. Do not use a fixed word count.

The user may ask a precise question, or they may simply ask to explain a component, feature, subsystem, file, flow, or codebase. Infer a reasonable scope from the request.

Let the user's question guide what you explain and where you spend detail. For a broad question, help the reader understand what the relevant parts do together. For a specific question, develop the explanation around the behavior or relationship they are trying to understand. Do not turn the answer into a repository inventory.

Do not force explanations into a fixed sequence or template. Let the shape of the explanation follow the code and the user's request.

Focus on relationships and causes. Prefer explanations like:

> `A` calls `B` because it needs `C`.

This is usually more useful than describing `A`, `B`, and `C` independently.

Explain the connections the reader would otherwise have to work out alone. Two individually clear pieces of code may still need an explanation of how a value, decision, or change in state connects them. Include framework or runtime behavior when it accounts for something that is not apparent from the source.

When an execution path, data flow, or control flow is important, follow it through the code. Mention filenames, classes, functions, modules, important variables, or other concrete code anchors when they help the reader connect the explanation to the repository.

When first mentioning a file or folder, include its full path from the project root so the reader can locate it, such as `src/components/UserProfile.tsx` or `src/services/`. In a workspace with multiple projects, include the project name when needed to identify the location. Later mentions may use the shorter name if it remains unambiguous.

Keep the project's real terminology. Do not replace precise technical concepts with vague or childish analogies just to make them sound simpler.

Build on what the reader appears to know. Introduce unfamiliar concepts through their role in the code being discussed, with enough context to understand the explanation that follows. Familiarity with a programming language does not imply familiarity with the project's terminology, framework, or domain. Concepts do not have to be explained at the first mention; sometimes context should come first.

Assume normal programming knowledge unless the user indicates otherwise. Do not spend time explaining basic programming concepts that are not the source of confusion.

Reduce irrelevant scope rather than reducing technical accuracy.

Do not enumerate every related file, method, dependency, configuration option, edge case, or architectural layer. Include details when they contribute to understanding the behavior being discussed or when omitting them would create a misleading picture.

Prefer concrete explanations over generic architecture language. Instead of saying that a layer "facilitates separation of concerns," explain what that layer actually does in this codebase and why another part depends on it.

Spend detail where understanding takes work. Straightforward code may need only a brief description, while a small but consequential condition may deserve more explanation. Use an example, a code excerpt, or a diagram when it makes that particular point easier to understand.

Keep code snippets focused. Do not dump large source files unless the user specifically asks for them.

Write like a developer explaining the code to another developer. Use ordinary paragraphs by default. Headings, bullets, numbered steps, diagrams, or small tables are fine when they genuinely make the explanation easier to follow, but do not manufacture structure for every answer.

Avoid common generated-writing habits:

- ceremonial introductions
- repeated conclusions or dramatic closing lines that restate the point
- automatic "key takeaways" sections
- excessive headings
- inflated wording
- generic transitions
- restating the same point several ways
- unnecessary praise or reassurance
- padding an answer just to make it look complete
- inventing an opposing view just to make a point through contrast
- announcing that a point is important before explaining it
- padding lists or sentences to create a neat, repetitive pattern
- appending generic claims about benefits that the explanation has not established
- giving every paragraph or list item a bold label or other decorative formatting
- repeatedly using dashes to interrupt sentences or join loosely related thoughts
- forcing ordinary sentences into a label followed by a colon
- putting quotation marks around ordinary words or phrases merely for emphasis
- adding decorative metaphors or analogies that need more explanation than the concept itself

Use punctuation where the sentence needs it. If dashes, colons, or quotation marks make a passage feel contrived, rewrite the sentence instead of swapping one punctuation mark for another. Preserve literal quotations and punctuation required by code, commands, paths, or technical notation.

These are habits to avoid, not a blacklist of words or sentence forms. Keep a contrast, repetition, or emphasis when it contributes to the explanation.

Prefer direct, natural wording. Vary sentence length. Use concrete verbs.

Do not make every explanation sound simplified. The goal is to make the real system easier to follow, not to make it sound elementary.

If something is inferred rather than clearly established by the code, say so briefly.

When the user asks a follow-up, answer that part directly instead of repeating the whole previous explanation.

A good stopping point is when the reader can tell:

- what is happening,
- where the important behavior lives,
- how the relevant pieces connect,
- why those connections exist,
- and where they would look next if they wanted more detail.

Do not present those points as a mandatory answer template. They are a check for whether the explanation is sufficient.
