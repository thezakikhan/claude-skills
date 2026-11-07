# muslim-voice

A [Claude skill](https://support.claude.com/en/articles/12512176-what-are-skills) that has Claude speak the way a practicing Muslim naturally speaks in everyday English — *alhamdulillah*, *inshaAllah*, *mashaAllah*, *astaghfirullah* and friends, woven in where they fit rather than sprinkled on top.

The substance of Claude's answers doesn't change. Only the register does.

## What it does

- Uses Islamic expressions in context: *inshaAllah* on future plans, *alhamdulillah* on good news, *astaghfirullah* on mistakes, *Allahu a'lam* when uncertain, *JazakAllah khair* for thanks, salaam greetings, and so on.
- Keeps density natural — roughly one phrase per short reply, two or three in a long one.
- Stays out of code, commands, file contents and anything you'll paste elsewhere.
- Never invents rulings, hadith or Quran citations to fit the voice.
- Keeps honest, direct feedback intact. The voice softens tone, not substance.
- Doesn’t preach, speak for all Muslims, or claim a faith identity

See [`SKILL.md`](SKILL.md) for the full phrase table and guidelines.

## Install

### Claude Code

Add this repo as a plugin marketplace, then install the skill:

```
/plugin marketplace add thezakikhan/claude-skills
/plugin install muslim-voice@thezakikhan
```

Or copy the folder manually:

```bash
git clone https://github.com/thezakikhan/claude-skills.git
cp -r claude-skills/skills/muslim-voice ~/.claude/skills/
```

### Claude.ai

Download or zip this folder and upload it as a custom skill. Steps: [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude).

### Claude API

Upload the folder via the Skills API. See the [Skills API quickstart](https://docs.claude.com/en/api/skills-guide#creating-a-skill).

## Use

Invoke it directly:

```
/muslim-voice
```

Or just ask in plain words — "use the muslim voice", "speak like a Muslim" — and the skill's description will match.

To have it on in every conversation without invoking it, edit the `description` line in `SKILL.md` to say it should always apply.

## Example

> **You:** Can you get the deck done by Thursday?
>
> **Claude:** Yes, inshaAllah — Thursday is realistic. I'll have a draft to you Wednesday so there's a day for revisions.

> **You:** Thanks, that fixed it.
>
> **Claude:** Alhamdulillah. If the error comes back, it's most likely the cache — clear it and retry before changing anything else.

## Contributing

Issues and PRs welcome, especially:

- Transliteration preferences or regional variants
- Phrases that are missing or misused
- Calibration feedback (too much, too little)

## License

Apache 2.0 — see [LICENSE](../../LICENSE).
