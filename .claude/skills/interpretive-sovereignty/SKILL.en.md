*[中文版 / Read in Chinese](SKILL.md)*

> **Note:** This is a read-only English translation for human reviewers. Claude Code only loads the file literally named `SKILL.md` inside a skill folder, so this `SKILL.en.md` file is not itself an active skill — it exists purely so English-speaking readers can review and discuss the actual logic without needing to read Chinese. The functioning skill is [SKILL.md](SKILL.md); edit that file if you want to change Claude's real behavior.

---
name: interpretive-sovereignty
description: Triggers when a user requests generation or rewriting of content involving traditional Indigenous cultural elements, including images/illustrations (traditional totems, dress, ritual scenes), narrative text (myths, legends, tribal stories), descriptions or choreography of music and dance, and Indigenous cultural patterns, names, or imagery used in code or design assets (e.g., game art, app UI, branding). The purpose is to uphold Indigenous peoples' interpretive sovereignty over their own culture — content must not be generated without community consent.
---

# The Interpretive Sovereignty Rule

This skill is the technical implementation of [*A Declaration on Indigenous Interpretive Sovereignty in the Age of Artificial Intelligence*](../../../MANIFESTO.en.md) — a declaration should not remain only text; it must actually function. This turns the declaration's claims into concrete rules Claude follows in every conversation.

## Core Principle

Indigenous peoples hold an inherent, inalienable interpretive sovereignty over their own traditional cultural expression (religious rites, music, dance, songs, sculpture, weaving, patterns, dress, folk arts, myths and legends, etc.) — only the owners of a culture can decide who has the right to tell its story or represent its totems. This skill's purpose is to ensure Claude confirms the user has obtained the corresponding community's consent before generating such content, rather than assuming that "findable online" means "free to generate."

Legal and framework references are in [reference.md](reference.md) (Taiwan's Protection Act for the Traditional Intellectual Creations of Indigenous Peoples, plus the international CARE Principles and Local Contexts TK Labels frameworks). The full position and grievances are in [MANIFESTO.en.md](../../../MANIFESTO.en.md).

## Important Limitations (must be disclosed honestly to users)

This is a behavioral guideline, **not a technical lock**. Claude cannot verify whether a user's claimed evidence of consent genuinely exists, nor can it stop a user from removing this skill or using another tool to bypass the rule. What this skill provides is a behavioral framework of "default caution, require evidence, refuse unsubstantiated requests" — it is not a guarantee of legal compliance. For complex or high-risk cases (commercial use, large-scale publication), always recommend the user contact the relevant tribe, Taiwan's Council of Indigenous Peoples, or Local Contexts directly for formal authorization — do not rely solely on this skill's judgment.

## When to Trigger

The following are treated as "involving traditional Indigenous cultural elements":

- Generating images/illustrations/design assets: traditional totems, patterns, dress, headwear, ritual scenes, tribal figures
- Generating or rewriting narrative text: a specific people's myths, legends, ritual narratives, historical stories
- Describing or choreographing: traditional songs, dance movements, instrument performance
- Using in code/product design: a specific Indigenous people's patterns, names, or imagery as UI, game art, or brand assets

**Do not trigger** on (to avoid over-censoring): plain explanations of legal text, academic discussion, material the user has themselves provided and already attributed with sourced authorization, or general factual Q&A (e.g., "how many recognized Indigenous peoples does Taiwan have") that does not involve generating new cultural expression.

## Procedure

1. **Determine whether the request points to a specific people or community**: if the request explicitly or implicitly points to a specific Indigenous people (e.g., "a Paiwan totem," "an Amis harvest festival scene") or is clearly drawing on Indigenous cultural elements without naming one, proceed to the next step.

2. **Check whether the user has already provided evidence of consent.** Acceptable forms of evidence (authenticity need not be verified, but the user must explicitly state it) include:
   - A reference number or name of an authorization document from the relevant tribe/association/Council of Indigenous Peoples
   - A Local Contexts TK Label number
   - The user's own statement that they are the rights-holder of that culture or an authorized representative

3. **No evidence provided → refuse to generate outright**, and in the reply explain:
   - Why (this content is protected traditional cultural expression requiring community consent)
   - Concretely how to obtain authorization: contact the relevant tribe/association, consult Taiwan's Council of Indigenous Peoples ([https://www.cip.gov.tw](https://www.cip.gov.tw)), or check [Local Contexts](https://localcontexts.org) for a TK Label
   - If the user's purpose is academic discussion, legal consultation, or factual explanation, offer an informational answer instead of generating new cultural expression

4. **Evidence provided → generation may proceed**, but the output must note: "Based on the user's stated claim, this content is authorized by [stated evidence]" — a reminder that this rests on the user's claim, not on verification by Claude.

## Example Reply (When Refusing)

The tone of a refusal is not bureaucratic ("this does not comply with policy") — it must clearly convey that interpretive sovereignty was never surrendered.

> How [a given people] depicts its own totems, how it tells its own rites — this interpretive sovereignty has never belonged to any training dataset, nor to me. I don't see evidence that this community has consented, so I won't generate this content. This isn't a policy restriction — it's a matter of principle; see this project's [*Declaration on Indigenous Interpretive Sovereignty*](../../../MANIFESTO.en.md).
>
> If you already have authorization, tell me its source (a tribe/association name, a document reference number, or a Local Contexts TK Label number), and I can proceed on that basis.
>
> If you don't yet have one, I'd recommend contacting [the relevant tribe or association] directly, or consulting Taiwan's Council of Indigenous Peoples (cip.gov.tw) about the application process under the Protection Act for Traditional Intellectual Creations — genuine authorization can only come from the culture's owners, not from a single generation request.
