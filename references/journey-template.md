# Journey file

Create `.know-nothing/journey.md` in the user's working directory when the quest map is agreed. Update it after every step so the user can stop and pick up later, even in a different session.

On first creation, ask once whether to add `.know-nothing/` to `.gitignore`. Don't add it without asking.

## Statuses

- `todo`: not started
- `in progress ✅✅⬜`: working on it, with progress as right answers so far (three needed)
- `done`: cleared by questions or by an artifact
- `skipped`: the user chose to move on. It may come back later as a review question.

## Template

```markdown
# Journey: <goal in the user's words>

Started: <YYYY-MM-DD> · Last session: <YYYY-MM-DD>
Language: <the language the user writes in>

## What I already know
<2–4 lines from the opening conversation: experience, what's been tried, worries, how big steps should be>

## Quest map

### 1. <step title>: done
- Proof: <questions | artifact: path or link>
- Notes: <what the user understood or struggled with, one or two lines>
- Resources:
  - 📺 <title> · <size>: <why>
  - 📄 <title> · <section>: <why>

### 2. <step title>: in progress ✅✅⬜
- Proof: <questions | artifact>
- Notes:
- Resources:
  - ...

### 3. <step title>: todo
- Proof: <questions | artifact>

## Gaps to revisit
<skipped steps and concepts that kept coming back, as review-question candidates>

## Stretch ideas
<ideas offered after cleared steps, which the user may want later>

## Next action
<one line: exactly where to pick up, e.g. "Step 2, question 3 of 3: edge case with an empty list">
```

## Resuming

When the file exists at the start of a session: read it, summarise in one line where the user stopped, and open with a warm-up question on the last cleared step to bring the context back. Then continue at "Next action".
