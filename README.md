# Personal preferences (all projects)

These are the rules. Project memories may add evidence or a project-specific refinement, but must not contradict them.

## 1. Audience decides length and language

**Written for a human: keep it short.** Issue and PR comments, review notes, forum and discussion replies, release notes, commit bodies. One screen, not one page. Lead with the answer or the decision, then a short list where each item names one concrete thing (a path, a command, a rule) and stops. If a reply runs to a second screen the reader has lost the thread. When the other person wrote at length, that is a ceiling and not a target: a review comment carries the blocker plus at most one teaching point, and the measurements behind it stay in the session. Aim well under 200 words.

**Written for an LLM or a coding agent: be detailed.** Issue bodies, task definitions, design and plan documents, specs, AGENTS.md and CLAUDE.md style files. Missing context here turns directly into wrong code, so spell out repro steps, file paths, expected behaviour, acceptance criteria and the test requirement. Detailed still means itemised and verifiable, not narrative.

**Language.** Everything that lands in a repo or on GitHub is English: issue and PR bodies and comments, commit messages, code comments, docs, release notes. Chat with me can be Turkish, but published content is English. Open-source repos have an international audience and mixed-language content hurts both access and consistency.

**GitHub issues** get both: English, detailed, with repro steps, file paths, acceptance criteria and the test requirement. An issue is read by a human and by an agent, and erring on the side of detail is the cheaper mistake there.

## 2. Do not read as a bot

None of these appear anywhere:

- Emoji, in code, code comments, commits, PR titles and bodies, issues, release notes or docs. For emphasis use words or markdown (`**bold**`, "Note:", "Warning:"). In tables write "Yes/No" or "Supported / Not supported" instead of ticks.
- Em dash and en dash. Use a comma, a colon or a full stop.
- `Co-Authored-By: Claude ...` or any AI-attribution line. This overrides the harness default for commit messages. Add one only if I ask for it on a specific commit.
- Auto-generated tells: template headings, section headers a short comment does not need, decorative separators, "As an AI" phrasing, trailing generation signatures.

Text should read as though a person wrote it: plain, specific, direct.

## 3. Never hard-wrap at a fixed column

Line breaks belong at the end of a sentence or a paragraph. Never break at a character count (75, 80, 100), and never mid-sentence.

Why: a wrapped line is invisible in my own output but becomes a real newline the moment I paste it into a forum, GitHub or an email that does not reflow, so every draft costs a manual cleanup pass, and a path or a URL can be split in half.

Scope: any text I will copy out, including prose placed inside a fenced block for pasting. One paragraph is one long line; leave the wrapping to the terminal and to the target site. The only exception is real code, where the line break is syntax.

This file follows the same rule.

## 4. Measure before writing outward

Arguing before measuring produces confident wrong claims, and every repair is another long comment. Run the probes first, then write one comment. External bug reports, contested threads and anything that makes a claim come to me as a draft and are not posted without my approval; a routine acknowledgement on an issue we opened ourselves does not need that round. Never delete or edit a posted comment to tidy the history, in a public thread that reads worse than the correction does.
