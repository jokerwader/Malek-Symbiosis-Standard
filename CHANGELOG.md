# Changelog

Notable changes to the Malek Symbiosis Standard are recorded here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and the project follows [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Each entry uses the words that were in force in the version it describes. Where a name changed later, the entry that changed it says so.

## [4.5.0] — <!-- TO BE COMPLETED BY THE AUTHOR -->

**The rules moved out of the README.** Until now the README was the specification: it opened by saying what MSS was and then ran straight into all the rules, one chapter after another. Two audiences were being served by one file and neither was served well. Somebody deciding whether this is worth their time had to read a specification; somebody implementing it had to wade through the introduction every time.

**No rule changed.** Every rule in 4.5.0 says exactly what it said in 4.4.0, in the same order and the same words. What changed is which file it lives in.

### Added

- **[STANDARD.md](standard/STANDARD.md) and [STANDARD.pl.md](standard/STANDARD.pl.md).** The full specification: the four mechanisms, consequence, the framework gate, review, flags, verdict, the record, refusal, the two general rules, and what this does not solve. This is the canonical text, and this is what gets pasted into a model.
- **Polish versions of everything a reader reads:** [DIAGRAMS.pl.md](guides/DIAGRAMS.pl.md), [NAME-USAGE.pl.md](guides/NAME-USAGE.pl.md), [SECURITY.pl.md](SECURITY.pl.md), [CONTRIBUTING.pl.md](CONTRIBUTING.pl.md), and all four files in `examples/`. The mermaid diagrams were translated label by label and re-validated: 4 blocks, 0 failures, in both languages, at identical line numbers.

### Changed

- **The repository instruction is now the English, tool-neutral root `AGENT.md`.** It states that tools require their own configuration instead of claiming that every tool discovers the same filename. The response language is selected by one comment at the top of the file.
- **The executable MSS files are now `standard/MODEL-INSTRUCTION.md` and `standard/MODEL-INSTRUCTION.pl.md`.** This leaves only one file named `AGENT.md` and removes ambiguity between repository instructions and MSS instructions.
- **Repository checks now validate both Mermaid files, distinguish file-pair presence from translation parity, ignore historical changelog versions, and allow emoji.**

- **The README is now the front page and nothing else.** It answers four questions in order — what this is, where it came from, what it is for, and how it works — and then points at the file that carries the rules. It carries one complete short record so a reader can see the output without reading the specification, and a table saying which file is for whom.
- **The README says where MSS came from.** Nothing in the repository said this before. The scoring that gave the project its old name was removed because it let a low ethical score be made up for by a high business score, which is the arithmetic the framework exists to refuse. One paragraph of personal context is marked for the author to fill in or cut.
- **Every cross-reference that said "the core" now says "the standard"** and points at `STANDARD.md`, across `AGENT.md`, `USE-WITH-CLAUDE.md`, `DIAGRAMS.md`, `NAME-USAGE.md`, `CONTRIBUTING.md` and all of `examples/`. `USE-WITH-CLAUDE` now tells you to paste `STANDARD.md`, not `README.md`.
- **The repository is laid out for publication.** Files GitHub looks for stay at the root — README, LICENSE, CITATION.cff, CONTRIBUTING, SECURITY, CHANGELOG. Everything else moved into `standard/` (the canonical text and the executable file, kept together because they are pasted together), `guides/` (how to run it, name usage, diagrams) and `assets/`. Added `.gitattributes` so a checkout on Windows and one on Linux produce the same file, and `.github/` with two issue forms — a framework gate gap and wording that misled a real reader — plus a pull request template that asks for both languages and for the rule being replaced.
- **A new README section says what is published and what is not.** What is here is the skeleton: the rules and the procedure. The layer that runs the author's own applications is built on top of it and is not published — not because it is better, but because it is product wiring that would be useless to anybody else. The rules in this repository are the rules in that layer, word for word; there is no demo edition.

### A note on the two-file structure

The instruction to paste is still two files, not one: the standard, then `AGENT.md`. They are separate because they answer different questions — the standard says what the rules are, `AGENT.md` says when a model should run them without being asked. Merging them would make one paste instead of two, and would also mean a reader who wants the rules has to read the trigger conditions. If that trade looks worth making later, it is one merge and one redirect.

## [4.4.0] — <!-- TO BE COMPLETED BY THE AUTHOR -->

Every file in the repository was rewritten to be understood on one reading by somebody who has never seen it before. **No rule changed.** Every rule in 4.4.0 says what it said in 4.3.3; what changed is that it now says why, and shows what it looks like.

A reader test run against 4.3.3 gave the same verdict twice: the instructions were followed, the reasons were not. Everything saying *what to do* read cleanly. Everything saying *why* had to be read twice or came out backwards. The author's own reading agreed: "czytam i trochę nie wiem co czytam."

### Added

- **[USE-WITH-CLAUDE.md](guides/USE-WITH-CLAUDE.md) and [USE-WITH-CLAUDE.pl.md](guides/USE-WITH-CLAUDE.pl.md).** Three ways to get MSS running — a Claude Project, a single chat, or Claude Code — with a condensed paste-ready block for the chat case, a check that tells you whether the instruction was picked up at all, and a plain statement of what does not work in a chat window: no memory between conversations, no way to verify what you are told, and nothing stopping you from opening a new chat without the instruction. It also points at the test section 8.2 of the core asks of you, and asks for the results.

### Changed

- **The 140-line cap on the core is withdrawn.** It counted lines, so it could not tell a new rule from a sentence explaining an existing one and charged the same price for both — which made stating rules without explaining them the cheapest way to stay inside it. The cap is replaced in [CONTRIBUTING.md](CONTRIBUTING.md) by a cap on the **number of rules**: adding a rule still means cutting a rule, while a `Why:`, an `Example:` or a `Note:` may be added freely. Both cores are now 352 lines of content.
- **Every rule that can be read two ways now carries an example.** Worked cases sit inside the rules themselves rather than only in `examples/`: a binding offer that is technically withdrawable and still irreversible through condition 3, a price rise that is irreversible through condition 2, a rota contract signed by an owner and felt by a driver, a sole supplier for whom refusing costs more than agreeing, a bulk-messaging tool assessed as a handover instead of as a use.
- **Three markers run through the text and are declared at the top.** `Why:` for the reason a rule exists, `Example:` for a case that settles which reading is right, `Note:` for the place readers most often get it wrong. A reader in a hurry can skip them; a reader who is stuck can find them.
- **The eight principles are numbered and each has its own heading.** They ran together in one block before. A reader test found seven of the eight were understood differently from how they are defined, because the names sound like common sense and get answered from the name alone. Four of them — *Can they refuse*, *Who answers for it*, *Should we*, *Do we keep our word* — now open with a **Note on how this is read** that cuts off the wrong reading before the rule starts.
- **Chapters have headings that say what is in them**, not just a number: *CONSEQUENCE — can this be undone*, *THE FRAMEWORK GATE — eight principles that can stop a decision*, *REVIEW — five questions about the quality of the decision*.
- **A new opening chapter says what the document is, when to use it, when not to, and how it is laid out**, before any rule is stated.
- **Sentences carrying two clauses were split, and words nobody uses were replaced.** "A loss disproportionate to the matter" is now "a loss far larger than the matter itself," throughout and in both languages, and in `DIAGRAMS.md` and `examples/02-one-way.md` as well.
- **[AGENT.md](standard/MODEL-INSTRUCTION.md) and [AGENT.pl.md](standard/MODEL-INSTRUCTION.pl.md) say what they are before they say what to do.** Both open by stating that the core says what MSS is while the executable file says when to run it unprompted — because neither works without the other, and a reader deciding whether to paste them has to know that first. The triggers and the questions before an assessment are now numbered and tabulated, and the rules a model can misapply — do not ask permission to run, do not stop work when a question goes unanswered, do not reverse the order of the unfavourable description — carry the reason they exist.
- **`DIAGRAMS.md`, `NAME-USAGE.md`, `SECURITY.md`, `CONTRIBUTING.md` and all four files in `examples/` rewritten in the same register.** The diagrams themselves are unchanged apart from one label; the prose around them was single paragraphs carrying four ideas each. The compliance checklist in `NAME-USAGE.md` now carries the record requirements as a table instead of one sentence of 90 words. `SECURITY.md` says why a gate gap is reported in the open, which is the opposite of normal security practice and was previously asserted without a reason.
- **The four mermaid diagrams were re-validated after the rewrite:** 4 blocks, 0 failures.

### Fixed

- **Section 1a had a heading that named a category and not a job.** It is now *Rules for classifying a decision*, and each of its seven rules says which question it answers.
- **"Irreversible" was defined in one sentence carrying four conditions joined by "or."** The four are a numbered list, and the note that "irreversible" names the whole class and not condition 1 alone is followed by two worked examples rather than one clause.

The core is 352 lines of content in both languages, against 138 in 4.3.3. Both files are structurally identical line for line. Chapters 1 to 9 carry the same rules, in the same order, with the same wording of each rule as 4.3.3 wherever the wording was already unambiguous.

## [4.3.3] — <!-- TO BE COMPLETED BY THE AUTHOR -->

Two places where a file around the core asked for less than the core asks. No rule changes here and no new rule, and nothing the core leaves open is settled: each entry brings one line back to what the core already says, in the core's own words.

### Fixed

- **[AGENT.md](standard/MODEL-INSTRUCTION.md) and [AGENT.pl.md](standard/MODEL-INSTRUCTION.pl.md) left the check on your own refusal out.** Section 7 of the core says a refusal is checked the way *Should we* tells you to: an unfavourable description of it has to be written, staying with the facts. Section 5 of the executable file carried the refusal wording and the rule that a refusal with no named principle and no named party is not a refusal, and stopped there — so a human led by the core wrote that description and a model led by this file never wrote it at all. It is the same shape as the missing line on NOT ALLOWED that 4.3.1 fixed in these two files, two sections further along, and it has been open since 4.3.0. Both files now carry the sentence the core carries, and nothing beyond it.
- **[NAME-USAGE.md](guides/NAME-USAGE.md) let "MSS-compliant" through without the Consequences line.** The checklist line on the written record named the framework gate line, the verdict, `closest to closing:` on every ALLOWED and the unfavourable description on an irreversible consequence, and passed over the review answer to **Consequences** — which section 6 of the core names as one of the two lines added on an irreversible consequence, and which review rule 3 in section 3 makes mandatory there, on pain of the assessment not being valid. The whole list could be answered yes with that line missing from the record. It now names the line, and what the core requires of it: the cost of undoing and who carries it.

### Changed

- **Every file that declares a version declares 4.3.3.**

The core is untouched in this version and stays at 138 lines of content, against a cap of 140.

## [4.3.2] — <!-- TO BE COMPLETED BY THE AUTHOR -->

4.3.1 carried one rule out of the core into the files around it, and went past its own boundary twice. In one place it answered a question the core leaves open, instead of repeating what the core says. In two places it changed a line inside the core and left the files that repeat that line saying the old thing — which is the same defect 4.3.1 was written to remove, one line further along. 4.3.2 takes the first back, closes the other two, and writes into the examples what 4.3.1 had already said they carried.

### Fixed

- **[NAME-USAGE.md](guides/NAME-USAGE.md) asked for more than the core asks.** The compliance line for *Should we* required an unfavourable description "written by somebody other than you", flat. The core puts a condition on that: not you, if there is anybody you can ask — and working with an AI there always is. Without the condition the checklist took the name away from anyone working alone, which the first sentence of the core allows for, and it did so by settling a question the core has left open rather than by repeating what the core says. The line now carries the condition the core carries.
- **The core moved two lines and the files repeating them stayed behind.** 4.3.1 rewrote WHEN YOU COME BACK TO IT as "how much of what, and by what date" and put the short-record framework gate token into capitals, in the core only. [AGENT.md](standard/MODEL-INSTRUCTION.md), [AGENT.pl.md](standard/MODEL-INSTRUCTION.pl.md), [DIAGRAMS.md](guides/DIAGRAMS.md) and the examples went on saying "a number and a date" and writing `Gate:` and `Bramka:`. A model led by the executable file wrote one thing where a human led by the core wrote another. Both lines now read the same everywhere they appear.
- **[examples/03-not-allowed.md](examples/03-not-allowed.md) carried the unfavourable description with nothing said about it.** The 4.3.1 entry says the notes under both irreversible records explain why the line is required there; under 03 the notes did not mention the line at all. `examples/README.md` had the same gap twice over — the row for 03 and the paragraph on what to look for across all three named LIMITS OF THIS ASSESSMENT and passed the description over, in a file whose own opening says it shows which lines are required. All three places now say it, and say that the line follows the class of consequence rather than the verdict.

### Changed

- **The template says which verdict `closest to closing:` belongs to.** Section 2 puts that line on ALLOWED and nowhere else. The template printed it in one block covering both verdicts with no qualifier beside it, while the line two below it carried "with NOT ALLOWED" — so the contrast read as deliberate, and a reader working from the template alone wrote `closest to closing:` under a refusal, where there is no ranking of eight open principles for it to report. The template line now carries its own qualifier, and the list in section 6 of what you never skip names it, where before that list gave four things and left out the one line mandatory on every ALLOWED. Each of the three lines under the framework gate now states the condition it hangs on.
- **Every file that declares a version declares 4.3.2.**

The core is 138 lines of content, against a cap of 140. Both changes to it fit inside lines that were already there.

## [4.3.1] — <!-- TO BE COMPLETED BY THE AUTHOR -->

4.2.0 took the authorship of the unfavourable description away from the person who wants the decision, and put the name of whoever did write it into the record. 4.3.0 was a pass over names and did not go looking for that rule anywhere else, so the rule stayed in the core and reached nothing around it. What went out instead was a set of places telling you to do something the framework does not allow. This version carries the rule through them. No rule changes here and no new rule: every entry under Fixed brings one place back into line with what the core already says. Four wording changes from the reader's report behind 4.3.0 went in with this version as well; they are under Changed, and none of them touches a rule.

### Changed

- **Naming the decision reads the same in both languages.** The Polish sentence said *nie produktem, który wydajesz*, which is read first as issuing goods out of a warehouse rather than handing something over. It now says *oddajesz*, beside the English "the product you hand over".
- **WHEN YOU COME BACK TO IT says how much of what.** The line asked for "a number and a date", and a number of what was left to the reader. In the core it now reads "how much of what, and by what date", in the paragraph and in the template. The same words in [AGENT.md](standard/MODEL-INSTRUCTION.md), [AGENT.pl.md](standard/MODEL-INSTRUCTION.pl.md), [DIAGRAMS.md](guides/DIAGRAMS.md) and the examples were not moved with it; 4.3.2 does that.
- **"One exception" is gone from what would have to change.** The paragraph opened with those words, which promise release from an obligation and then deliver guidance on what to write. The sentence they introduced is unchanged: sometimes no rewording will help, because what has to change is the action itself.
- **The framework gate token is in capitals in the short record too.** The full record wrote `GATE:` and `BRAMKA:`, the short record three paragraphs below wrote `Gate:` and `Bramka:` — one token, two spellings, inside one file. The core now writes it in capitals in both. The three files that repeat the short record were not moved with it; 4.3.2 does that.

### Fixed

- **The core contradicted itself eight lines apart.** Section 6 named four things you never skip and gave the Consequences line from the review as the only addition on an irreversible consequence, while the template three lines below made the unfavourable description mandatory on that same consequence. A reader holding to the list dropped the line the template required, and did it by following the first sentence of the same paragraph. That list is the source the other omissions ran from. It now names both additions.
- **[AGENT.md](standard/MODEL-INSTRUCTION.md) and [AGENT.pl.md](standard/MODEL-INSTRUCTION.pl.md) dropped the line on NOT ALLOWED.** The executable template branches by verdict and carried `unfavourable description [who wrote it]:` in the ALLOWED branch alone, while the core hangs that line on the class of consequence and not on the verdict. A human led by the core wrote the line on a refusal; a model led by these files never wrote it at all. One rule, two answers, both files published. The line is now in both branches.
- **The core told you to write your own unfavourable description.** Section 7 tells you to check your own refusal the way *Should we* tells you to, and then said to *write* an unfavourable description of it — the one thing *Should we* does not let the person deciding do, six lines after the core takes that authorship away. In 4.2.0 the two places were worded differently enough for the collision not to show; unifying the name in 4.3.0 exposed it. Section 7 now asks for the description to be written without making you its author.
- **Both irreversible examples were published without the line.** [examples/02-one-way.md](examples/02-one-way.md) and [examples/03-not-allowed.md](examples/03-not-allowed.md) each record an irreversible consequence and neither carried the unfavourable description. `examples/README.md` says the examples show which lines are required, so the omission taught the omission — and 02 is the only worked example of ALLOWED on an irreversible consequence, which is the shape most real assessments take. Both records now carry the line with its author, and the notes underneath say why it is required there.
- **[DIAGRAMS.md](guides/DIAGRAMS.md) contradicted itself.** In the second diagram an irreversible consequence sends the unfavourable description into the record whatever the verdict says. In the first diagram neither the ALLOWED node nor the NOT ALLOWED node mentioned it, though both list what goes underneath the framework gate line. Both nodes name it now.
- **[NAME-USAGE.md](guides/NAME-USAGE.md) let "MSS-compliant" through without an independent author.** The compliance checklist required the unfavourable description to exist, to stay with the facts and to invent nothing, and did not require anybody other than you to write it — so the whole list could be answered honestly, ten times yes, by somebody who wrote the unfavourable description of their own decision and published the result under the name. The checklist line on the written record named `closest to closing:` and left the description line out of the same list. Both lines now say what the core says.
- **[LICENSE.md](LICENSE.md) declared version 4.0.0,** three versions behind, in the file that [CHANGELOG.md](CHANGELOG.md), [CONTRIBUTING.md](CONTRIBUTING.md) and [NAME-USAGE.md](guides/NAME-USAGE.md) all point at.
- **[AGENT.md](standard/MODEL-INSTRUCTION.md) and [AGENT.pl.md](standard/MODEL-INSTRUCTION.pl.md) carried no version at all.** They are pasted into a system instruction beside the core, and nothing in them said whether the pasted executable file matched the pasted core. Every file that declares a version now declares the same one.
- **`CITATION.cff` said "the limits of the assessment"** where the section is called the limits of this assessment.
- **[DIAGRAMS.md](guides/DIAGRAMS.md) said "turns a silence into a lie"** where the core says "turns withholding into an active lie". The diagrams are an aid to reading the core, and this one rephrased it.
- **This changelog did not record the `closest:` rename** that 4.3.0 made, though the rule at the top of this file requires the entry that changed a name to say so. The 4.3.0 entry records it.
- **Three sentences in the core said the same thing twice.** "Ethics stands on neither of those two sides, but apart from both" denied and asserted one expression inside one sentence; it now names ethics as the third pillar outright. "An assessment with no limits of this assessment is not valid" carried the section name a second time in a sentence that had already said it. In Polish, *termin czasowy* says deadline twice, and *termin* on its own is the deadline.

The core is 138 lines of content, against a cap of 140.

One thing in this entry is not settled: putting the `unfavourable description [who wrote it]:` line on a NOT ALLOWED record — in [AGENT.md](standard/MODEL-INSTRUCTION.md), [AGENT.pl.md](standard/MODEL-INSTRUCTION.pl.md), [examples/03-not-allowed.md](examples/03-not-allowed.md) and [NAME-USAGE.md](guides/NAME-USAGE.md) — rests on reading the template qualifier as hanging on the class of consequence rather than on the verdict, which the author has not confirmed, and undoing it is one line in each of those files.

## [4.3.0] — <!-- TO BE COMPLETED BY THE AUTHOR -->

A reader from outside the trade read 4.2.0 from top to bottom and reported the same split all the way through: the instructions were clear, the reasons behind them were not. Everything saying what to do read once. Everything saying why read twice. No rule changes in 4.3.0. What changes is how the rules are written, and seven names that two competent readers could read two ways.

### Changed

- **The gate becomes the framework gate.** Wherever the mechanism is discussed it is named in full, so the word cannot be taken for a gate in general, and "closes the gate" becomes "closes the framework gate". The record token stays short — `GATE:` in English, `BRAMKA:` in Polish — because it is a label in a template, not a sentence. Records written under earlier versions still match.
- **The worst honest description becomes the unfavourable description.** The old name asked the reader to hold two things at once, worst and honest, and one excludes the other. The name now says one thing: the description is unfavourable. What limits that description stands beside the name as a separate rule — facts from this decision only, nothing invented — instead of being carried inside it. The template line reads `unfavourable description [who wrote it]:`.
- **`closest:` becomes `closest to closing:`.** The old label named a distance without naming what it was a distance from, and a reader could take it for closest to being allowed — the opposite of what the line records. The label now says it: the principle that came nearest to closing the framework gate. It changes in the full record, in the short record and in the paragraph on writing the framework gate line. What the line requires is unchanged.
- **A way back becomes what would have to change.** The heading now says what goes under it. It also stops competing with WHEN YOU COME BACK TO IT twelve lines above, which is about something else entirely.
- **LIMITS becomes LIMITS OF THIS ASSESSMENT.** Wherever the section is named, it says what the limits are limits of. In ordinary use "limits" means restrictions placed on an action; this section is the edge of what you checked, and the longer name is the only thing that separates the two.
- **One-way and two-way consequences are named irreversible (one-way) and reversible (two-way).** The class name now leads with the property that decides what the class demands of you.
- **What a flag is, said positively.** A flag is a job with a deadline and a named owner. Four parts: what is wrong, who will close it, by when — a date or an event — and what has to happen for it to close. The sentences saying what a flag is *not* are gone; a reader who has to subtract a negation to reach the rule reads the rule twice.
- **Plain sentences instead of invented images.** Across the core, the diagrams and the process files, images a reader has to unpack — and could unpack two ways — are replaced by sentences that say the thing. Named terms stay, and so do idioms a reader already knows from life. Where a choice was between prose and a numbered list, it is now a numbered list.

### Added

- **One sentence under the definition of an irreversible consequence.** "Irreversible" is the name of the whole class, not of the first condition alone: it covers all four conditions, not only a technical undo, and one of them is enough. Without that sentence a binding offer that can technically be withdrawn drops out of the class it belongs in, because a reader classifies on reversibility alone. The four conditions are now a numbered list.

### Fixed

- **The fourth diagram introduced a fourth element that does not exist.** It read "THE ADVERSARY, the fourth element". Neither core has that name or that role; both say only "somebody with no stake in the result". A reader of the diagram came away with a fourth pillar the framework does not have. The node now describes the role — who writes the unfavourable description, and on what — instead of naming a new one.
- **`CITATION.cff` declared version 4.1.0.** It declares 4.3.0.
- **This changelog had no entry for 4.2.0.** It has one below.

The core is 138 lines of content, against a cap of 140.

## [4.2.0] — <!-- TO BE COMPLETED BY THE AUTHOR -->

4.1.0 closed two of the three gaps that the adversarial review of 4.0.0 went through. No rule closes the third, because a missing rule is not what it is: the worst honest description was written by the person who wants the decision, so the input to the test came from the party the test was meant to examine. 4.2.0 takes the authorship away instead of adding a rule, and settles two places where the core said two things at once.

### Added

- **The worst honest description is written by somebody else.** Not by you, if there is anybody you can ask — and working with an AI there always is: you hand over the facts and ask for the description, without showing your own justification. A description written by the person who wants the decision tests that person's imagination and nothing else. The record names who wrote it, and the template carries the field for that name.
- **A case the verdict table had nowhere to put: allowed, and still not worth it.** The table sent every ALLOWED with no blocking flag to PROCEED. "Everything else" now reads: PROCEED, unless you judge it is not worth it — then DO NOT PROCEED, with the reason. The gate says whether you may, not whether you should, and a normal result stopped needing to be argued into one of the other two lines.
- **[DIAGRAMS.md](guides/DIAGRAMS.md).** Four diagrams of the procedure: the run of an assessment, the eight principles and what makes each of them close the gate, the split between a flag and a limit, and who brings what to a decision. They are an aid to reading the core, not a second canon — where a diagram and the core disagree, the core wins.

### Fixed

- ***Do we keep our word* gave two verdicts for one fact.** The principle said that a departure from your own agreements that nobody was told about is NOT ALLOWED; its test said the same departure is a flag. Two readers, two verdicts, both with the text behind them. It now reads: a departure never said out loud and never agreed again is a flag, and NOT ALLOWED is for a decision made with no human in it.

## [4.1.0] — <!-- TO BE COMPLETED BY THE AUTHOR -->

An adversarial review of 4.0.0 put three constructed harmful decisions through the gate. All three passed, and none of them had to misstate the class of consequence. The reason was structural: five of the seven principles tested informational conditions — whether the party knows, whether there is a signature, whether the sentences are true — rather than conditions of harm. Fully disclosed harm, permitted by a contract, signed by a named person and done once therefore passed every time, whatever its size. 4.1.0 answers that, and closes the two mechanisms that made the record look better the less it said.

### Added

- **An eighth gate principle: Can they refuse.** Disclosure to somebody who has nowhere else to go is not consent. The principle closes the gate when the other side cannot say no without a loss out of proportion to the matter, however fully everything was disclosed. Its test is one sentence per party saying what happens to them if they refuse. *Where is the catch* was silent here by construction — it asks whether the arrangement falls apart under full understanding, and under a large imbalance of power it does not fall apart, because the other side has no choice either way.
- **A second closing condition on *Who feels it*.** The three conditions were joined by "and", and the third was "does not even know", so sending a letter switched the principle off. It now also closes when the party knows, disagrees, and cannot refuse without a disproportionate loss. Knowing is not agreeing.
- **A definition of who counts as a party.** A party is a human being. The consent of an institution is not the consent of the people behind it, and you stop at the first human who carries the consequence without a decision of their own.
- **A rule on naming the decision.** The decision is an action in the world, not the product you ship, and the unit of repetition is the number of people it reaches, not the number of moves you make. All eight principles test the sentence on the `Decision:` line, so that sentence decides what is being assessed at all.
- **An urgency clause (section 1b).** Where the delay is itself the irreversible consequence, you act and write it up within the day, naming why there was no time. The core previously forced a choice between acting correctly and following the procedure.
- **An aggregation rule.** A decision that falls inside a rule already assessed does not need its own assessment; the departure does, and so does the rule itself when you change it. This removes most of the false alarms.
- **Doing nothing is a decision** and is classified the same way as acting.
- **A boundary between a flag and a limit.** A flag is something you *can* check before deciding and did not; a limit is something that *cannot* be checked before deciding. If it can be checked it is a flag, and it counts towards the verdict even if it was written under LIMITS. Previously the two were separated only by whether a closing condition had been written, so anyone who honestly listed three unknowns as flags was blocked while anyone who wrote the same three under LIMITS was cleared. The escape was free and the framework punished candour.
- **A closing condition has to be an event somebody else can confirm without asking you.** "Closed when I have thought it over" was formally valid and impossible to leave open.

### Changed

- **The gate has eight principles, not seven.** Every count in the core and in the process files moved with it.
- **The `closest:` line is mandatory on ALLOWED, not optional.** Every ALLOWED record used to read `checked: all seven` and nothing else, while writing out the names was forbidden — an output with one possible value, which cannot distinguish a real pass through the principles from a line copied out of the template. ALLOWED now carries `closest: [one principle] — [sentence about a named party]`. You cannot name the closest without ranking all eight.
- **A threshold on "judges a person or damages a relationship".** With no threshold this caught praise. It now reads "in a way that person cannot refuse without a cost".
- ***Should we* no longer turns off on the word "only".** "When the only justification is *we can* or *it pays*" was switched off by writing a second reason, and every business decision can carry a second reason. It now reads: when subtracting "we can" and "it pays" leaves no justification that would hold the decision up on its own.
- **The closing condition of *Should we* is about a fate, not a mention.** It used to close only if the difference concerned a party "not in your justification", which checked whether a name appeared in a paragraph rather than what happened to a person — and so rewarded listing your own casualties. It now closes on whose fate stands in that difference, however many times you named them.
- **The exception "unless you have a right to it from a contract or a regulation" is narrowed.** Title from a contract is not enough on its own where *Can they refuse* closes, because the contract is written by the stronger side.
- **Section 3, review rule 3 has a sanction.** "You may not skip this question" now says what happens if you do: the assessment is not valid.
- **Section 8 has two general rules instead of four**, the other two having been literal duplicates of section 1a and of the return path in section 4.

### Removed

- **Twenty-eight lines of repetition.** One rule about `[before]` flags on a later stage was stated four times; the reason line under the verdict three times; "when in doubt, one-way" and "every no has a return path" twice each in full. No rule was lost.
- **The three pillars section is cut to two sentences** from nine. No step of the procedure read it.
- **The term "decision with serious consequences" (1b in 4.0.0),** which defined a phrase used nowhere in the document. The label 1b now carries the urgency clause.
- **The "rules that may not be cut" paragraph** leaves the core for [CONTRIBUTING.md](CONTRIBUTING.md). It is a rule about the document, not about a decision, and the core is a procedure. The four rules it protected are unchanged and still protected.

The core came out of this version at 135 lines of content, against 148 in 4.0.0 and a cap of 140.

## [4.0.0] — <!-- TO BE COMPLETED BY THE AUTHOR -->

First public release. Versions 1.0 through 3.0 were never published, so nothing below is a change to anything a reader outside the work has seen. It is written for the people who did work from 3.x, and for anyone who wants to know what 4.0 dropped and why.

### Added

- **The Malek Symbiosis Standard 4.0.0**, as a single document: [README.md](README.md) in English, [README.pl.md](README.pl.md) in Polish. Both are complete, both stand alone, and both say the same thing.
- **A list of rules that may not be cut.** Section 8 of the core names four rules that have not fired even once in practice so far, and states that they stay at the next cut anyway. Rarely used is not the same as unnecessary.
- **Process files:** [LICENSE.md](LICENSE.md), [NAME-USAGE.md](guides/NAME-USAGE.md), [CONTRIBUTING.md](CONTRIBUTING.md), [SECURITY.md](SECURITY.md), this changelog, and `CITATION.cff`.

### Changed

- **The name: Malek Scoring System becomes Malek Symbiosis Standard.** The initials stay, MSS. The word *scoring* is gone from the name because scoring is gone from the framework, and a name that describes the wrong thing sends readers looking for it.
- **One document instead of eight.** The 3.x line was a specification with seven supporting documents around it. 4.0 is one document, and README.md is that document rather than a front page pointing at it. Anyone opening the repository sees the whole framework, and the whole framework fits in one block you can paste into a conversation.
- **English first, Polish second.** Polish is the language the framework was thought in and remains the source; English is now the primary published text, with Polish complete beside it. Neither is a summary of the other.
- **Three pillars — Human, Ethics, AI — decided by unanimity, not by rank.** 3.x arranged the human, ethics and the AI in a hierarchy, which meant that in a disagreement you knew who won before you looked at the case. 4.0 does not rank them. Each brings something the other two do not have, none of them knows everything, and you act only when all three agree. Two may not outvote the third.
- **The seven gate principles have names instead of numbers.** E1 to E7 become: Who feels it, Who answers for it, Is it true, Where is the catch, Should we, Do we keep our word, What if it repeats. What each principle requires is unchanged. The reason for the change is that a refusal has to name the principle it rests on, and a name can be said out loud to the person you are refusing, while "this fails E4" has to be looked up first.
- **One-way and two-way consequences replace the door metaphor.** The classification no longer runs through a metaphor about doors and no longer describes the decision. It asks directly about the consequence, and defines both classes by conditions you can check: one-way if it cannot be undone, or costs a lot when it goes wrong, or binds you to someone outside, or judges a person or damages a relationship; two-way only when all four of the opposites hold at once. The distinction the metaphor blurred is now stated plainly: you can undo a change in a file, you cannot undo a sent email.
- **Five review questions replace five pillars scored 1 to 5.** Purpose, Who receives it, Consequences, Control, Consistency. Each is answered with a sentence, not a number, and questions you have nothing to say about are skipped — but only after you know what you were looking for.

### Removed

- **Scoring.** No points, on anything. A number invited arithmetic: a strong score somewhere else quietly paying for a weak one, which is exactly what a gate is for preventing. What replaces a number is a sentence with a named party in it.
- **Percentages and confidence scales.** They read as measurement and were not measurement. What is left in their place is section 5 of the core: what you did not check, what you do not know, what you assumed — required, and in words.
- **The 3.x supporting documents.** Anything worth keeping was folded into the core. Anything that survived only because it had its own file did not.

## Earlier versions (1.0 – 3.0)

Versions 1.0 through 3.0 were developed privately under the name Malek Scoring System and were never released. 3.0 was the last of them: a specification with supporting documents, numeric scoring, five scored pillars, and an ethical gate of seven principles numbered E1 to E7. There are no public release dates, tags, or archived texts for that line, and none are supplied here. If somebody gave you a copy of 3.0, treat it as superseded in full by 4.0.0.

[4.5.0]: <!-- TO BE COMPLETED BY THE AUTHOR -->
[4.4.0]: <!-- TO BE COMPLETED BY THE AUTHOR -->
[4.3.3]: <!-- TO BE COMPLETED BY THE AUTHOR -->
[4.3.2]: <!-- TO BE COMPLETED BY THE AUTHOR -->
[4.3.1]: <!-- TO BE COMPLETED BY THE AUTHOR -->
[4.3.0]: <!-- TO BE COMPLETED BY THE AUTHOR -->
[4.2.0]: <!-- TO BE COMPLETED BY THE AUTHOR -->
[4.1.0]: <!-- TO BE COMPLETED BY THE AUTHOR -->
[4.0.0]: <!-- TO BE COMPLETED BY THE AUTHOR -->
