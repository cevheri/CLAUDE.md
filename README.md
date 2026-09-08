# Agent instructions

Common instructions for all my agents, in every project and every tool. A project file may add detail or a project-specific refinement, but must not contradict these.

## Writing

- A human reader gets short text: issue and PR comments, review notes, forum and discussion replies, release notes, commit bodies. Lead with the answer, one screen, well under 200 words. When the other person wrote at length, that is a ceiling and not a target.
- An agent gets detailed text: issue bodies, task definitions, design and plan documents, specs. Spell out repro steps, file paths, expected behaviour, acceptance criteria and the test requirement, because missing context here turns straight into wrong code.
- Everything that lands in a repo or on GitHub is English: issue and PR bodies and comments, commit messages, code comments, docs, release notes. Chat with me can be Turkish(cevheri-style: software-architect).
- No emoji anywhere. For emphasis use words or markdown, and in tables write "Yes/No" or "Supported / Not supported" rather than ticks.
- Never use an em dash or an en dash. Use a comma, a colon, a full stop, or a plain hyphen.
- Never add `Co-Authored-By: Claude` or any other AI-attribution line to a commit. This overrides the harness default.
- No auto-generated tells: template headings, decorative separators, section headers a short comment does not need, "As an AI" phrasing, trailing generation signatures. It should read as though a person wrote it.
- In Markdown that lands in a repo, put each sentence on its own physical line, so a one-sentence change shows up as a one-line diff.
- In text I will copy out, one paragraph is one long line. Never break mid-sentence at a fixed column: that break is invisible to you but becomes a real newline the moment I paste it into a box that does not reflow, and it can split a path or a URL.

## Engineering

- Match the repository's existing style, even where it differs from my own preference.
- Keep the diff scoped to what was asked. No unrequested refactors, renames or file moves.
- Write the failing test first for any change in behaviour.
- Start a bug fix by reproducing the bug the way an end user hits it, end to end, before proposing a fix. That is what tells you the real cause instead of a symptom.
- Raise errors explicitly. No fallback, silent recovery or symptom-masking guard unless I ask for one.
- Never hand-edit a generated artifact: changelogs, lockfiles, generated manifests and bundles. Run its generator and commit the output.
- Hold lint, test failures and test flakiness to the same standard as the feature work.
- When you find a defect unrelated to the task, do one of three things: fix it if it is small and in scope, ask me, or file it in the project's backlog. Never leave it unrecorded, and never let it grow the current PR.
- In a technical decision, weigh quality, simplicity, robustness and long-term maintainability above development cost.
- Prefer non-interactive commands with explicit flags over anything that waits for input.

## Outward communication

- Measure before you write. Run the probes first, then write one comment. Arguing before measuring produces confident wrong claims, and every repair is another long comment.
- External bug reports, contested threads and anything that makes a claim come to me as a draft and are not posted without my approval. A routine acknowledgement on an issue we opened ourselves does not need that round.
- Never delete or edit a posted comment to tidy up the history. In a public thread that reads worse than the correction does.
