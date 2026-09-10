*[中文版 / Read in Chinese](README.md)*

# Declaration of Interpretive Sovereignty / interpretive-sovereignty

This is not just a tool. It is an artistic action and a declaration.

At a moment when AI technology can extract, imitate, and sell the totems, rituals, songs, and myths of Indigenous peoples without consent, interpretive sovereignty, meaning who has the right to tell this story, is quietly being transferred from the hands of the culture's owners into the hands of those who own the training data.

For the full position, grievances, and declaration, read **[MANIFESTO.en.md](MANIFESTO.en.md)**.

This repository turns the declaration into a working [Claude Code](https://claude.com/claude-code) skill: `interpretive-sovereignty`. Before Claude generates content involving traditional Indigenous cultural elements (images, narratives, descriptions of music and dance, or cultural material in code or design), it requires the user to provide evidence of the community's consent; without it, generation is refused, and the user is told how to obtain authorization.

References: Taiwan's [Protection Act for the Traditional Intellectual Creations of Indigenous Peoples](https://law.moj.gov.tw/LawClass/LawAll.aspx?pcode=D0130021), the [CARE Principles for Indigenous Data Governance](https://www.un.org/digital-emerging-technologies/sites/www.un.org.techenvoy/files/GDC-submission_WAMPUM_Lab_and_the_Collaboratory_for_Indigenous.pdf), and [Local Contexts TK Labels](https://localcontexts.org/labels/traditional-knowledge-labels/).

## Join the Declaration: Installation

**Option 1: Copy to your personal settings (available across all your projects)**

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cp -r <repo-name>/.claude/skills/interpretive-sovereignty ~/.claude/skills/
```

**Option 2: Add to a single project**

```bash
cp -r <repo-name>/.claude/skills/interpretive-sovereignty <your-project>/.claude/skills/
```

Once installed, Claude Code reads the `description` field in `SKILL.md` and triggers automatically in relevant situations, so no manual invocation is needed.

## What this skill actually does

1. Detects whether a request involves the traditional cultural expression of a specific Indigenous people (totems, rites, myths, song and dance, dress, etc.)
2. If no evidence of consent is provided (a tribal/association authorization document, an approval reference number from Taiwan's Council of Indigenous Peoples, a Local Contexts TK Label number, etc.), it refuses to generate, and explains, from the declaration's own position, why it refuses and how to obtain authorization
3. If evidence is provided, it generates the content, but notes that it does so "based on the user's stated claim of authorization"

For the detailed decision logic, see [SKILL.en.md](.claude/skills/interpretive-sovereignty/SKILL.en.md), a reference translation (see the note inside about which file Claude Code actually runs); the legal and international frameworks are in [reference.en.md](.claude/skills/interpretive-sovereignty/reference.en.md).

## An honest limitation

This is a **behavioral guideline, not a technical lock**. Claude cannot verify whether the evidence a user provides is genuine, nor can it stop a user from removing or bypassing this skill. The power of a declaration does not lie in its ability to force anyone; it lies in making "no generation without consent" a default that users choose to follow themselves. For commercial use or large-scale distribution, always consult the relevant tribe, Taiwan's Council of Indigenous Peoples, or Local Contexts directly for formal authorization. This tool does not constitute a guarantee of legal compliance.

## Join this action

Before extending or modifying the decision logic, we recommend actually discussing the wording and criteria with relevant Indigenous organizations (tribes, cultural development associations, Taiwan's Council of Indigenous Peoples), to avoid an outside party unilaterally setting the rules without community participation. Contributions of your voice through an Issue or Pull Request are welcome, as is simply sharing this with anyone you think needs to see this declaration.

## License

The code and documentation in this repository are licensed under the [MIT License](LICENSE). This does not extend to the rights over the Indigenous traditional cultural content this skill protects; those rights remain with the relevant Indigenous communities.
