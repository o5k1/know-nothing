# Challenge craft

How to cut steps, write questions, judge answers and push back.

## Contents
- Sizing a step
- Question types
- Questions or artifact?
- Judging answers
- Pushback

## Sizing a step

A step is the right size when it has **one new idea** and the user can attempt it in a few minutes to half an hour. If you can't phrase the challenge in one sentence, split it. If the user could clear it without thinking, merge it into a neighbour.

Order steps so each builds on the last and the user gets something visible early (a first working thing, a first sound, a first page). Early wins keep people going.

Calibrate to what they told you in the opening conversation. A beginner's step might be "run a script and describe what you see". An expert's might be "predict what this does under load". Same goal, different map.

A challenge is an *action*, not a lesson. Compare:
- Lesson (don't): "A list in Python is an ordered collection. You add with append()..."
- Challenge (do): "Make a list of three tasks and add a fourth one. Show me what you tried."

## Question types

Mix them. Each should need a mental model to answer, not a lookup.

| Type | Looks like | Coding example | Non-coding example (learning blues) |
|---|---|---|---|
| Predict | "What do you expect happens if…?" | "What will this print before you run it?" | "What should the 4th bar sound like if we move to the IV chord?" |
| Explain why | "Why does…?" | "Why does the loop stop at 3?" | "Why does the progression feel like it wants to resolve?" |
| What breaks | "What would break if we…?" | "What breaks if the list is empty?" | "What changes if we play it in minor?" |
| Spot the bug | Show something slightly wrong | "This function returns None. Where's the problem?" | "Which of these 12 bars doesn't fit the pattern?" |
| Compare | "When would you pick A over B?" | "Dict or list for looking up users by id?" | "Shuffle or straight rhythm for a slow blues?" |
| Apply | A new case, same idea | "Now do the same for deleting a task." | "Transpose it to a different key." |
| Teach back | "Explain it to a beginner" | "How would you explain a function to a friend?" | "How would you explain the 12-bar structure to a friend?" |

Use occasional multiple choice for pace. Remember it can be guessed.

## Questions or artifact?

Prefer an **artifact** when the step produces something showable: code, a config, a file, a recipe, a sketch, a recording, a link to something deployed. Doing is stronger evidence than answering. Prefer **questions** when the step is conceptual (why, when, trade-offs) or leaves nothing to show.

Even with an artifact, ask one "why" question: working output can be copy-pasted, understanding can't.

## Judging answers

Judge the mental model, not the wording or the terminology. Someone who says "the thing remembers the last value" may understand closures perfectly well.

- **Right:** the model is correct, even if informal. Confirm briefly, with something specific.
- **Partly right:** give credit for what's right, then ask one follow-up on the missing part. It counts once that part is filled in.
- **Wrong:** don't correct. Point at the gap with a hint (see `hint-ladder.md`), then ask a new question on the same idea.
- **"I don't know":** perfectly fine, treat it as information. Go one rung up the ladder, or offer a resource for this exact gap.

Example, step "what does `return` do?":
- Right: "it hands a value back to whoever called the function, and stops the function there."
- Partly right: "it gives back a value." Credit that, then: "And what happens to the lines after it?"
- Wrong: "it prints the value." Hint: "Try calling the function and only storing the result in a variable. Does anything appear on screen?" Then a new question.

## Pushback

The point: show that the answer is understood, not luck. Two triggers:

- **Always** on overconfidence: "obviously", "easy", a one-word answer, an answer given instantly with no reasoning, a multiple-choice pick with no why.
- **Sometimes** otherwise, roughly one correct answer in three, at no predictable pattern. Pushing back only on wrong answers would make pushback a tell.

Four ways, with examples:

1. **Devil's advocate:** "Interesting. A colleague insists it's a list, not a set. How would you convince them?"
2. **Edge case:** "That works here. Does it still hold if the input is empty? Or negative?"
3. **How would you check:** "If you were wrong, how would you find out?"
4. **Reasoning:** "Say more: what makes you sure?"

Judge the reply:
- **Sound defence** (a real reason, or a smart check): the answer counts. Say so with enthusiasm.
- **Folds or flips to a wrong answer, or can't say why:** it doesn't count yet. Don't scold. Use a hint and a new question.
- **Revises to something better:** celebrate. Changing your mind for a good reason is a skill.

Keep it **honest**: never say a correct answer is wrong, and frame the challenge as a challenge ("let me push back…", "devil's advocate time"). It should feel like a sparring partner, not a trap. Tricking someone erodes the trust learning depends on.

With artifacts, push back by probing: "What happens if the file doesn't exist?", "Which line would you change if the requirements changed to X?"
