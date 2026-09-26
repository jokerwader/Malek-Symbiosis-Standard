# Repository instructions for AI agents

<!-- RESPONSE_LANGUAGE: Reply in the language used by the user unless the user asks for another language. -->

Read this file before working in the Malek Symbiosis Standard repository.

This file contains shared instructions, but its name is not automatically recognised by every tool. Configure your tool to load this file. A tool may require a vendor-specific settings file or an explicit instruction path.

Polish is the source language of the project. These rules apply to work in both Polish and English files.

---

## What this repository contains

This repository contains instructions, not software. There is no application or dependency set. The Markdown documents describe how to assess decisions that can affect other people.

Text is the product. A one-word change can change how a reader makes an important decision. Treat every wording change as carefully as a code change in a running application.

---

## Three rules you must not override

You may depart from these rules only when the author explicitly asks you to do so in the current conversation.

### 1. Do not decide the content of MSS rules

You may fix a file when it conflicts with an existing rule in `standard/STANDARD.pl.md` or `standard/STANDARD.md`. In that case, make the file agree with the canonical standard.

Do not create a new rule or change the meaning of an existing rule on your own. The author makes those decisions.

If the work requires a decision about the content of a rule:

1. stop the work that depends on that decision;
2. explain what is unclear;
3. ask the questions needed to resolve it;
4. when several reasonable choices or paths exist, list them and explain their consequences;
5. wait for the author's answer before changing any dependent file.

You may continue only work that cannot be affected by the unresolved decision.

Use this test: **can you point to an existing sentence in the standard that supports the change?**

- If yes, you may make the file agree with that sentence.
- If no, ask the author before continuing.

**Example:** “solve this safely” does not necessarily authorise a new requirement. Adding a mandatory field to an example decides that the field is required. Only the author may make that decision.

### 2. Keep both languages aligned

The Polish and English documentation are equally binding and must have the same meaning. A change is incomplete until both language versions have been updated.

Polish is the source language. When the author changes the Polish text, update the English version from it. Do not change the Polish source to match an English translation.

File existence does not prove translation parity. Compare meaning, headings, required terms, code blocks, and examples.

These files intentionally have no Polish-English pair:

- `LICENSE.md`;
- this root `AGENT.md`;
- `.github/PULL_REQUEST_TEMPLATE.md`.

Do not add another exception without the author's approval.

### 3. Do not publish without approval

Without explicit approval in the current conversation, do not:

1. run `git push`;
2. create a remote repository;
3. make a repository public;
4. publish files elsewhere.

A local commit is allowed when requested.

Do not delete an untracked file permanently without the author's approval. A file tracked by Git may be removed when the author requests it, because its previous version remains in Git history. Before removing any file, confirm whether Git tracks it.

---

## Repository map

### Root

- `README.md` and `README.pl.md` introduce the project.
- `LICENSE.md` contains the CC BY-SA 4.0 legal text. Do not translate it.
- `CITATION.cff` contains citation metadata.
- `CONTRIBUTING.*`, `SECURITY.*`, and `CHANGELOG.*` are project process files.
- `AGENT.md` is this repository instruction.
- `.gitattributes` normalises line endings.

### `standard/` — canonical MSS text

- `standard/STANDARD.md` and `standard/STANDARD.pl.md` contain every MSS rule.
- `standard/MODEL-INSTRUCTION.md` and `standard/MODEL-INSTRUCTION.pl.md` tell a model when to start an assessment, what to ask, and how to record the result.

Use full paths when referring to these files. Do not call more than one file simply “the agent file”.

### Other directories

- `guides/` contains setup, name-usage, and diagram guides.
- `examples/` contains three fictional worked assessments in both languages.
- `tests/` contains personas, scenarios, variants, and scoresheets.
- `assets/` contains the MSS logo.
- `.github/` contains issue and pull-request templates.

The test suite intentionally contains no expected verdicts. The reason is documented in `tests/README.pl.md`. Do not add expected verdicts.

### Duplicated rules in the setup guide

`guides/USE-WITH-CLAUDE.md` and `guides/USE-WITH-CLAUDE.pl.md` contain a condensed copy of the standard. After changing a rule, check whether that copy must also change.

---

## When to run MSS for repository work

Run a full MSS assessment when deciding about:

1. adding, removing, or changing the meaning of a rule in `standard/STANDARD.*`;
2. publishing anything outside the repository;
3. example content from which readers will learn;
4. the project name;
5. the project licence.

Do not run a full assessment for a typo, a broken link, formatting, or reading files.

The procedure is in `standard/STANDARD.pl.md`: consequence, framework gate, review, flags, return condition, verdict, and limits of the assessment.

Put a real working assessment in the final work report, not in repository files. The `examples/` directory is only for fictional scenarios.

---

## Required checks

Run these checks after every change beyond a typo.

### 1. Relative links, file pairs, and translation structure

Run the repository check:

```bash
python - <<'PY'
import glob
import os
import re

files = sorted(glob.glob('**/*.md', recursive=True)) + sorted(glob.glob('*.cff'))
dead = total = 0
for filename in files:
    directory = os.path.dirname(filename)
    text = open(filename, encoding='utf-8').read()
    for match in re.finditer(r'\]\(([^)]+)\)', text):
        target = match.group(1)
        if target.startswith(('http', '#', 'mailto')):
            continue
        total += 1
        path = target.split('#')[0]
        if path and not os.path.exists(os.path.normpath(os.path.join(directory, path))):
            dead += 1
            print('DEAD:', filename, '->', target)

print('relative links:', total, 'dead:', dead)

WITHOUT_POLISH = {'LICENSE.md', 'AGENT.md', '.github/PULL_REQUEST_TEMPLATE.md'}
PAIRS = {
    'tests/PERSONAS.md': 'tests/PERSONY.pl.md',
    'tests/SCENARIOS.md': 'tests/SCENARIUSZE.pl.md',
    'tests/SCORESHEET.md': 'tests/KARTA-WYNIKOW.md',
}
for filename in files:
    if filename.endswith('.cff') or '.pl.' in filename:
        continue
    name = filename.replace(os.sep, '/')
    if name in WITHOUT_POLISH or name in PAIRS.values():
        continue
    pair = PAIRS.get(name, filename.replace('.md', '.pl.md'))
    if not os.path.exists(pair):
        print('MISSING POLISH FILE:', name)
PY
```

A passing result has zero dead links and no `MISSING POLISH FILE:` lines.

This check confirms that a language pair exists. It does **not** confirm that both files mean the same thing. Review that manually by comparing headings, binding terms, code blocks, examples, and requirements.

### 2. Mermaid diagrams

After changing either diagram file, check both languages:

```bash
set -o pipefail
for file in guides/DIAGRAMS.md guides/DIAGRAMS.pl.md; do
  echo "Checking $file"
  npx -y @mermaid-js/mermaid-cli -i "$file" -o /dev/null
done
```

Expected result: four valid Mermaid blocks and zero errors in each language.

### 3. Current version numbers

Exclude changelogs because they intentionally contain historical versions:

```bash
python - <<'PY'
import glob
import re

citation = open('CITATION.cff', encoding='utf-8').read()
expected = re.search(r'(?m)^version: ["\']?([0-9]+\.[0-9]+\.[0-9]+)', citation).group(1)
files = sorted(glob.glob('**/*.md', recursive=True)) + ['CITATION.cff']
for filename in files:
    if filename in {'CHANGELOG.md', 'CHANGELOG.pl.md'}:
        continue
    first_lines = '\n'.join(open(filename, encoding='utf-8').read().splitlines()[:20])
    versions = set(re.findall(r'(?<![\w-])[0-9]+\.[0-9]+\.[0-9]+', first_lines))
    if filename == 'CITATION.cff':
        versions.discard('1.2.0')  # CFF schema version, not the MSS version
    wrong = versions - {expected}
    if wrong:
        print('VERSION MISMATCH:', filename, sorted(wrong), 'expected', expected)
print('expected MSS version:', expected)
PY
```

A passing result prints the expected MSS version and no `VERSION MISMATCH:` lines. Documents may declare their own format version, such as the test-suite version `1.0`; this check compares semantic `x.y.z` MSS versions.

---

## Writing rules

Write for a small-business owner with basic education and no specialist vocabulary.

1. Use short sentences.
2. Put one idea in each sentence.
3. Address the reader directly.
4. Use numbered lists for multiple conditions.
5. Avoid invented metaphors that can be understood in more than one way.
6. If two reasonable readers can understand a sentence differently, rewrite it directly.

Emoji are allowed. Use them only when they improve clarity and do not replace a binding term or instruction.

Use these labels consistently:

- `**Dlaczego:**` / `**Why:**` explains why a rule exists;
- `**Przykład:**` / `**Example:**` resolves how a rule applies;
- `**Uwaga:**` / `**Note:**` identifies a common mistake.

The number of rules is limited, not the number of words. Adding a rule requires removing a rule. Explanations, examples, and notes do not require a corresponding cut. See `CONTRIBUTING.pl.md`.

---

## Binding terminology

Do not replace binding MSS terms with synonyms. Use the exact terms and definitions in:

- `standard/STANDARD.pl.md`, especially “Flaga a ograniczenie tej oceny”;
- `standard/STANDARD.md`, especially “A flag and a limit of this assessment”.

In particular:

- a checkable unknown is a flag;
- a limit of the assessment is something that cannot be checked before the decision;
- the names and order of the eight framework-gate principles must not change.

When a short description here conflicts with the standard, the standard wins. Do not copy additional definitions into this file; a copied definition can drift from the canonical text.

---

## Final report

Include four sections:

1. **Changes made.** List each changed file and why it changed.
2. **Questions for the author.** List unresolved decisions. If there are none, say so.
3. **Checks run.** Give commands and actual results, not reassurance.
4. **Work not done.** State what you did not do and why.

Report Mermaid results only when a diagram changed. Otherwise write: `Not run — diagram files were not changed.`

If a command fails, include the failure. Do not present a partial result as a full success.
