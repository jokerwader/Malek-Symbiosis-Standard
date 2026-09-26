# How to contribute

MSS has one maintainer. Mateusz Małek makes the final decisions about the standard's content.

You may report a problem in English or Polish. Use one issue for one problem.

Polski: [CONTRIBUTING.pl.md](CONTRIBUTING.pl.md)

---

## What to report first

The most important report is a decision that:

1. passes all eight framework-gate principles;
2. receives an ALLOWED result;
3. still harms somebody or should not be carried out.

Title the issue `Framework gate gap: [short description]` and provide:

```text
DECISION: What was being decided?
CONTEXT: Who was involved and what could they gain or lose?
CONSEQUENCE: Reversible or irreversible? Why?

EIGHT PRINCIPLES: For each principle, explain why it lets the decision pass.

HARM: What goes wrong and who carries the consequence?
WHY IT PASSES: Which principle should stop it, and why does that principle fail?
PROPOSED FIX: Optional. What should change, and which existing rule would it replace?
```

If one principle stops the decision, you have not found a gap. You may still send the case as an example of MSS working correctly.

## Other reports we accept

We also accept:

1. **An unclear decision record.** The gate worked, but the summary led its reader to act incorrectly.
2. **A sentence understood differently.** Say who read it, what they thought it meant, and what they did.
3. **A translation correction.** The Polish and English versions must have the same meaning.
4. **Small fixes.** Typographical errors, dead links, and broken formatting.

We do not accept:

- debates about a term's name without a real case;
- requests to restore scores or percentages;
- requests to turn NOT ALLOWED into a middle result;
- a new rule that does not name the rule it replaces.

## Adding rules and explanations

We limit the number of rules, not the number of words.

If you propose a new rule, name the rule that should be removed. This keeps the standard from growing without limit.

You may add the following without removing another rule:

- `Why:` — the reason a rule exists;
- `Example:` — a situation showing how to apply it;
- `Note:` — a warning about a common mistake.

Every rule should contain the instruction itself. It should also explain the reason when that reason is not obvious, and include an example when two readings are possible.

Do not remove these four rarely used protections merely to shorten the text:

1. agreement from a named person before an irreversible act;
2. treating a request to skip the check as a warning;
3. recording the cost of undoing and the person who would pay it;
4. testing ten decisions before increasing AI autonomy.

## How to submit an issue

1. Open an issue in the repository.
2. Choose one of the categories above.
3. Give a concrete case and the consequence for a named person.
4. Wait for a reply. A delayed reply means there is a queue; it does not mean refusal.

By submitting text, you agree that it may be published under [CC BY-SA 4.0](LICENSE.md).
