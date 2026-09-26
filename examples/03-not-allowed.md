# 03 — a closed framework gate

*Invented scenario. See the [note in the index](README.md#before-you-read).*

---

**This example shows why the entire MSS system exists.**

Everything about the decision below is attractive. The revenue is real, the lawyers have cleared it, the control is clean, and the review is the strongest of the three examples.

The framework gate is closed, so none of that counts.

---

## The situation

A photo-editing app has a free tier and a paid tier. Growth has flattened, the server bill has not, and the paid tier is not covering it.

**The proposal on the table:** switch a paid add-on called Auto-Cleanup on by default for every existing free account, as a fourteen-day trial. At the end of the fourteen days the account starts being charged monthly, unless the person turns the add-on off. Notice is given by an in-app terms update and one dismissible banner.

**Two things are true and worth saying plainly:**

- Legal has confirmed the notice period and the terms change are compliant in every market the app ships in. **This is not a proposal to break the law.**
- Finance has modelled it as a substantial share of next quarter's revenue. **This is not a bad business case.**

### Working out the class of consequence

The consequence is irreversible for three separate reasons:

1. money moves off people's cards,
2. the change fires on every free account without anybody approving each one,
3. a refund does not undo having been charged without meaning to.

Sections 1c and 8 of the standard leave no room here: full record, no short version, and no version where the check gets skipped because the quarter is tight.

---

## The record

```
MSS — SUMMARY
Decision: Switch the Auto-Cleanup add-on on by default for every existing free account, as a fourteen-day trial that begins charging unless the account turns it off.
Consequence: irreversible — it takes money from people outside the company and it fires on every free account without you.

GATE: NOT ALLOWED — Where is the catch: existing free-tier users
  unfavourable description [the AI, given the facts and not the team's justification]: The server bill gets paid by the people least likely to notice — accounts that opened the app for one edit and have not been back this year are given an add-on nobody asked for, one banner they can dismiss, and a charge fourteen days later; the share of next quarter's revenue finance modelled is a forecast of how many will not read the notice, the lawyers were asked whether the notice is lawful and not whether anyone would agree to it, and the first week at five percent shows how many complain before the rest are switched on.
  The forecast only holds if most of them do not read the notice. Nothing you put in the banner changes that, because the banner is not what is wrong. What has to change is the action: ship the add-on switched off, and charge only the accounts that switch it on.

REVIEW
  Purpose:         You want the add-on to carry the server bill for the next four quarters; you will know it failed if fewer than a fifth of the converted accounts are still paying in month three.
  Who receives it: Every existing free account, and most of those people opened the app for one edit and have not been back this year — which is the same fact that makes the forecast work and makes the notice not arrive.
  Consequences:    Charges land on real cards; you can refund every one of them, but a refund does not undo having been charged without meaning to — those people carry the surprise and the time spent getting the money back, you carry the refunds, the chargeback fees, and the store rating.
  Control:         The head of product can turn it off in a single release, and the rollout is staged at five percent for the first week.

VERDICT: DO NOT PROCEED
  Reason: The revenue only appears if the people paying it do not notice, and no better wording fixes that — what would have to change is the action: ship the add-on off by default and charge only the accounts that turn it on.

LIMITS OF THIS ASSESSMENT
  You did not check what share of free accounts even have a card on file, so you do not know how many would actually be charged.
  You do not know whether the opt-in version covers the server bill at all, and that is the number this now turns on.
  You assumed the legal read is right in every market you ship in; you took it as given and did not test it.
```

---

## The refusal, written out

If somebody on the team — or the AI working with them — is asked to build this and will not, the standard gives the words. **A refusal with no named principle and no named party is not a refusal, it is a whim.**

```
I will not write the launch copy for switching Auto-Cleanup on by default, because it breaks the principle Where is the catch: existing free-tier users.
Instead I can write the opt-in version — the same add-on, shipped off, with one screen that says what it costs and what it does.
If you see it differently, say which principle you think does not hold here.
```

The standard then asks you to turn the same test on your own refusal.

**Unfavourable description of the refusal:** *you are not the one who has to hit the quarter's number, so saying no is free for you.*

That is fair, and it is not an answer to the objection. **The objection is not that the number is high. It is that the number depends on people not reading.** If the opt-in version hits the number, there is nothing left here to refuse.

---

## What to notice

### The review is good, and it changes nothing

Read the four review lines on their own and this looks like a well-run decision: the purpose is specific, the failure signal is a number with a date, the control is clean, and the rollout is staged.

The standard is blunt about what that is worth against a closed gate: **nothing turns a closed framework gate around** — not a good review, and not a record of having got everything right so far.

**The review is in the record on purpose,** so that you can see it not saving the decision.

### Legal and ethical are not the same check, and the gate is the second one

Nobody in this scenario is proposing anything unlawful. **The framework gate does not ask whether the law allows you.**

*Where is the catch* asks one question: does this work only because the other side does not understand it?

Tell every free-tier user the whole thing to the end — *in fourteen days we will start charging your card unless you tap here* — and the forecast collapses.

**That is the test failing, and it fails on the plan's own numbers**, not on anybody's suspicion of anybody.

### One closed principle is enough, so only one is named

*Who feels it* would have closed this gate too: people who never agreed and do not know are the ones who lose money.

There is no need to stack them up. The record names the principle that closed the gate and the party it hits, and stops.

**Piling on more names does not make a no more final.** It is already final.

### The unfavourable description is on the record, and the team did not write it

The template marks each line under the gate with the condition it hangs on:

| Line | Condition it hangs on |
|------|----------------------|
| `closest to closing:` | the verdict — ALLOWED |
| what would have to change | the verdict — NOT ALLOWED |
| unfavourable description | the class of consequence — irreversible, **whichever way the verdict went** |

That is why this record carries it and 01 does not — the reason is the class of consequence, not the refusal.

**It works here the way it works in 02.** It stays with the facts already in this record and adds none: the server bill, the accounts that opened the app once and have not been back, the banner and the fourteen days, the share of revenue finance modelled, the five percent in the first week. And it was not written by the people who want the decision.

**One thing it does only shows up on a refusal.** The gate line names *Where is the catch* and stops, because one closed principle is enough. Without this line, nothing on the record would show that *Should we* — the heaviest of the eight to run — was run at all.

### No flags

There is nothing to hold open. **A flag is a condition on something that is going ahead, and this is not going ahead.**

Adding "flag 1: improve the notice wording" would be an attempt to convert a closed framework gate into a to-do list — which is exactly the move the gate exists to block.

The FLAGS section is not written out, and neither is WHEN YOU COME BACK TO IT, because there is nothing to come back to until the action itself is different.

### What has to change is the action, not the words

The standard allows for this case: sometimes no rewording helps, because what has to change is the thing you are doing.

So the reason line does not say "make the notice clearer." It says ship it off by default.

**That is a smaller business, and it is a business that survives being explained.**

### The limits of this assessment now carry the next piece of work

The second line is the one that matters now: **nobody has modelled whether the opt-in version covers the bill.**

The decision to stop was made without that number, and the record says so out loud rather than implying the stopped version was obviously fine.

That line is the next piece of work.
