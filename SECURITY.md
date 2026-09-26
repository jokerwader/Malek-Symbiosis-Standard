# Security

MSS is a document. There is no server, no binary, and nothing to install — so most of what "security" usually means does not apply here.

Two things still do.

---

## A framework gate gap is public, not private

**If you have found a decision that passes all eight principles of the framework gate and should not, report it in the open**, in a normal issue.

That is a contribution, and it is the most valuable one this project takes. The template is in [CONTRIBUTING.md](CONTRIBUTING.md).

**Do not sit on it and do not send it quietly.**

**Why this is the opposite of normal practice:** in software, you report a weakness privately so it can be patched before anybody exploits it. Here there is nothing to exploit and nothing to patch in secret. A weakness in the framework gate is something **everybody relying on the framework needs to know about while it is still open** — because they are relying on it today, and a private report leaves them doing that in the dark.

---

## What to report privately

Report privately only if openness would hurt somebody:

- a personal detail about a named person left in an example where it should not be;
- a file in this repository that is not what it says it is;
- a problem with the repository or the account behind it.

**Contact:** malek@fifo.com.pl

---

## What to expect

One maintainer, no service level agreement, no bounty.

You will get an answer, but not necessarily a quick one.

If the report holds up, the fix goes into [CHANGELOG.md](CHANGELOG.md) with credit to you — unless you would rather not be named, in which case say so.
