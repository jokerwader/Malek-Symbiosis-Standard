![MSS](assets/mss-logo.png)

# Malek Symbiosis Standard

**A standard for checking decisions before they affect other people.** Version 4.5.0. Author: Mateusz Małek.

Polski: [README.pl.md](README.pl.md) · Licence: [CC BY-SA 4.0](LICENSE.md)

---

## What MSS is

MSS is a set of questions you ask before making a decision that can affect another person.

You can use it yourself or with an AI. It works especially well with an AI because the model can ask questions you may not think to ask about your own decision.

MSS is not software, a score, a certificate, or a training course. It is a written procedure. It does not replace legal advice.

---

## Where it came from

We first wrote MSS as a working tool for one person using AI. We noticed a common problem:

**An AI usually does what you ask.** It works quickly and rarely asks uncomfortable questions unless you tell it to. A harmful decision can therefore look sensible, profitable, and urgent when nobody challenges it.

Early versions used scores, percentages, limits, and weights. We removed them. A high business score could cancel out a low ethical score and make a harmful decision look acceptable.

MSS now uses eight questions. Each question can stop the decision. A good result in one area cannot cancel a failure in another.

The name refers to **symbiosis**. You bring the facts and responsibility. The AI brings questions and a different point of view. Both follow the same rules.

MSS is used in production on Fibid.pl, Frostbox.pl, AutoQuote.pl, and by several business agents.

---

## What MSS is for

The goal is simple: **do not let a decision that harms somebody pass unnoticed.**

MSS asks you to do three things:

1. **Name the people affected.** Do not hide them behind words such as “the market” or “users”.
2. **Check whether they can refuse.** A formal right to say no is not enough if saying no would cost them much more than accepting.
3. **Leave a written record.** Another person should be able to see who was affected, what was checked, and what remains unknown.

MSS cannot guarantee an ethical decision. It makes missing facts and ignored people easier to see.

---

## How it works

| Step | What you ask |
|---|---|
| **1. Consequence** | Can the result be undone safely? |
| **2. Framework gate** | Do all eight required principles allow the decision? |
| **3. Review** | Is the decision useful, clear, controlled, and consistent? |
| **4. Flags** | What must be checked, by whom, and by when? |
| **5. Verdict** | Proceed, wait until flags are closed, or do not proceed? |
| **6. Limits** | What could not be checked before the decision? |

The order matters. First check whether the decision is allowed. Then check whether it is worth doing. Finally, state what you still do not know.

For a reversible decision, the written result can be short. An irreversible decision needs a full record.

---

## Start here

You do not need to read every file.

- To try MSS in a chat, follow [Using MSS with Claude](guides/USE-WITH-CLAUDE.md).
- To read every rule, open [STANDARD.md](standard/STANDARD.md).
- To tell a model when to start an assessment, use [MODEL-INSTRUCTION.md](standard/MODEL-INSTRUCTION.md) together with the standard.
- To see complete examples, open [examples/](examples/).
- To test whether different models understand MSS in the same way, open [tests/](tests/).

Other useful files:

- [DIAGRAMS.md](guides/DIAGRAMS.md) — four diagrams of the procedure;
- [NAME-USAGE.md](guides/NAME-USAGE.md) — when you may say “MSS-compliant”;
- [CONTRIBUTING.md](CONTRIBUTING.md) — how to report a problem or propose a change;
- [CHANGELOG.md](CHANGELOG.md) — what changed between versions.

---

## What is published

This repository contains the complete MSS rules and procedure. They are not a demo or a reduced version.

Our applications add product-specific data, roles, tools, and workflows. That product layer is not included because it only makes sense inside those applications. You can build your own layer around the same published rules.

---

## Licence and name

You may copy, change, and use the text commercially under [CC BY-SA 4.0](LICENSE.md). You must credit the author and keep the same licence.

Use the phrase **“MSS-compliant”** only when all eight framework-gate principles are implemented without exceptions. If you use only part of MSS, say **“based on MSS”** and list what you left out. See [NAME-USAGE.md](guides/NAME-USAGE.md).

Author: **Mateusz Małek** · Citation: [CITATION.cff](CITATION.cff)
