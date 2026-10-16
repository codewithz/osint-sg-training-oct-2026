# Lab 2.1 Operator behaviour comparison

| Duration | Type | Running case | Assessed |
| --- | --- | --- | --- |
| 10 minutes (instructor demo; delegates follow along and take the reference sheet) | Demo, with a short try-it | No | No |

## Aim

See, side by side, how the same query behaves on different search engines, and leave with a personal reference sheet of what works where.

## Outcome

A one-page **operator reference sheet** with engine-specific notes, and one query you built that works on one engine and fails on the others.

## The analogy: the same order at three different kopitiams

Ask for "teh-c" at three stalls. One gives you tea with evaporated milk, one with condensed milk, one asks whether you want it hot. Same words, three results. This demo shows you which stall reads your words which way, before you rely on the result in a live case.

## What you need to do

- [ ] Watch the instructor run the same four queries on four engines
- [ ] Write down where results differ and the reason you think so
- [ ] Try one query of your own that behaves differently across engines
- [ ] Fill in your reference sheet

**Deliverable:** `operator-reference.md`.

## What the instructor sets up beforehand

- Four engines open in separate tabs on the demo laptop (Google, Bing, Yandex, and one regional engine such as Baidu or Naver)
- Four prepared queries using a harmless public topic (a well-known Singapore landmark, a public company, a historical event)
- The reference sheet template below, shared with delegates

## Before you start

- Read [S1 Advanced search](../sessions/s1-advanced-search.md).
- **Tools:** the `scratch` Firefox profile in your VM.

## Rules for this lab

- Use only the public, non-sensitive topics the instructor gives you.
- Do not search for individuals.

## Steps

### Step 1: Watch the demo (5 min)

The instructor runs these four queries on every engine, and you record the first result and the number of results for each:

| Query pattern | Example topic | Look for |
| --- | --- | --- |
| Exact phrase | `"Marina Bay Sands"` | Does the engine honour the quotes? |
| Exclusion | `Merlion -statue` | Does the exclusion work? |
| Site restriction | `site:gov.sg budget` | Does it return only that domain? |
| File type | `filetype:pdf Singapore annual report` | Does it return only PDFs? |

### Step 2: Note the differences (3 min)

For each query, write one line on what differed between engines and a guess at why (different index, different handling of operators, personalisation).

### Step 3: Build your own divergent query (2 min)

Combine two operators on a harmless topic so that it succeeds on one engine and fails on the others. Share it with the room.

## Reference sheet template

```markdown
# Operator reference sheet

| Operator | Google | Bing | Yandex | Regional engine | Notes |
| --- | --- | --- | --- | --- | --- |
| "exact phrase" | | | | | |
| -exclude | | | | | |
| site: | | | | | |
| filetype: | | | | | |
| intitle: | | | | | |
| date filter | | | | | |

## Quirks I observed
-

## My divergent query
-
```

## Common mistakes

- Forgetting that results change with location. Note your egress country.
- Assuming an operator works because it did last month.

## Summary

Search engines are different stalls with the same menu words. The sheet you built is your own cheat card, and you should re-check it every few months because operators change without notice.

## Carries forward

- Lab 2.2 and Lab 2.3 use these operators.
- Keep the sheet in `00-admin/` of the running case.
