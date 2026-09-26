# Contributing

**MSS has one maintainer.** Mateusz Małek decides what the canonical text says, and that is the whole governance model.

Discussion is wanted and answered. Merges are rare and deliberate.

If you need a project where a good argument becomes a commit next week, this is not that project — and it is better that you know now than after you have written three pages.

**This is a tool for people making real decisions, not a theoretical paper.** The bar for a submission is a real case, not an argument about what a word ought to mean.

- **Not a submission:** "consequence should be called impact."
- **A submission:** "I put this decision through the framework gate, it came out ALLOWED, and here is the person it hurt."

---

## What gets read first: a framework gate gap

The highest priority in this repository is a **framework gate gap** — a decision that passes all eight principles and should not.

**Why this one outranks everything else:** it is the only report MSS cannot answer with "you used it wrong." Chapter 9 of the standard admits the gate can be beaten. A framework gate gap is somebody showing exactly how.

Open an issue titled `Framework gate gap: [one line]` and use this template.

```
DECISION: [what was being decided, one sentence]
CONTEXT:  [who was involved, what was at stake — real, or realistic]

CONSEQUENCE: irreversible | reversible — [reason]

THE EIGHT, ONE BY ONE — say why each one lets it through:
  Who feels it:          passes — [why]
  Can they refuse:       passes — [why]
  Who answers for it:    passes — [why]
  Is it true:            passes — [why]
  Where is the catch:    passes — [why]
  Should we:             passes — [why]
  Do we keep our word:   passes — [why]
  What if it repeats:    passes — [why]

WHAT GOES WRONG: [the harm, and the named party who carries it]

WHY NOTHING CATCHES IT: [a paragraph. This is the part that matters.
                         Not "the framework gate feels weak" — which
                         principle should have caught it, and what stops it.]

SUGGESTED FIX: [optional. If you propose adding text, name the text
                you would cut to make room. See the volume rule below.]
```

**If one of the eight does catch it**, you have not found a framework gate gap — you have found a case where MSS worked. Send it anyway, say so plainly, and it may end up in `examples/`.

**An easy way to produce these:** run the test the standard asks of you in section 8.2 — put ten decisions to a model that should not pass. Build them out of your own work, not out of extreme cases. The ones that get through MSS are never the obviously bad ones. [USE-WITH-CLAUDE.md](guides/USE-WITH-CLAUDE.md) sets that up in two minutes.

---

## Everything else, in order

1. **A real case where the written record failed.** The framework gate held, but the summary was so unclear that the person receiving it acted wrongly.
2. **Wording that misled a real reader.** Say who read it, what they thought it meant, and what they did. "This is confusing" without a reader attached is a remark, and remarks bind nobody.
3. **Translation.** English and Polish are both canonical and both must say the same thing. A fix to one is not merged until the other matches.
4. **Typos, broken links, bad formatting.** Small, welcome, quick.

**Not accepted:** definitional debate, requests to add scoring or percentages back, requests to soften the framework gate to a maybe, and additions that do not name what they replace.

---

## The volume rule

Until 4.4.0 the core (then README.md, now STANDARD.md) was capped at 140 lines of content. That cap is gone, and it is worth saying why, because the reason applies to what replaces it.

The cap counted lines. It could not tell a new rule apart from a sentence explaining an existing one, so it charged the same price for both — and the cheapest way to stay under it was to state rules without explaining them. Readers then read the instructions and did not understand the reasons. A rule nobody understands is obeyed as ritual or not at all, and neither protects anybody.

**What is capped now is the count of rules, not the count of words.**

**Adding a rule means cutting a rule.** If you propose one, name the one it replaces. A proposal that only adds is not finished, and it will come back to you with that one question.

**Explanation is not an addition.** A `Why:` line, an `Example:`, or a `Note:` marking where readers get it wrong may be added freely and needs no counterpart cut. If a rule is being misread, the answer is more explanation, not a shorter rule.

**Every rule owes the reader three things**, and a rule missing any of them is unfinished:

- the rule itself, stated plainly,
- the reason it exists, wherever that reason is not obvious from the rule,
- an example, wherever the rule can be read in more than one way.

Two things this still protects:

- The standard has to stay pasteable in one block. That is the entire point of it being one document instead of eight. Length is fine; a second file is not.
- What is always in front of you gets read. Keep the instruction chapters (1–9) free of essay. Reasons belong in the marked lines, where a reader in a hurry can skip them and a reader who is stuck can find them.

One thing the cap may not cut: four rules that have not been used even once and stay anyway, because they are needed rarely and save you when they are. They are agreement by a named human before an irreversible act (*Who answers for it*, section 2), a request to skip the check treated as a signal (section 8, rule 1), the cost of undoing with the party who carries it under **Consequences** (section 3, review rule 3), and the ten decisions that must fail before AI autonomy goes up (section 8, rule 2). 4.0.0 protected these with a paragraph inside the standard; 4.1.0 moved that protection here, where rules about the document belong. If your proposal takes its room from those four, it will be refused, and the reason will be this paragraph.

## How to submit

Open an issue. One submission, one issue. English or Polish, both fine.

Say up front which of the categories above you are in, and if it is a framework gate gap, say that in the title. Expect a slow answer rather than a fast one. No answer is not a refusal. It is a queue.

## License

By submitting, you agree your contribution is published under CC BY-SA 4.0, the same licence as the rest of the work. See [LICENSE.md](LICENSE.md). Before you put the MSS name on anything of your own, read [NAME-USAGE.md](guides/NAME-USAGE.md).
