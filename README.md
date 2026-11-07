# Claude skills by Zaki Khan

A collection of [skills](https://support.claude.com/en/articles/12512176-what-are-skills) for Claude — folders of instructions Claude loads to do a specific kind of task well. Each skill lives in its own folder under [`skills/`](skills) and can be installed on its own.

I'm a fractional head of product and coach PMs and designers. Most of what lands here will be product-management skills — the frameworks and reviews I actually use with teams — plus the occasional one that's just for me.

## Skills

| Skill | What it does |
|---|---|
| [muslim-voice](skills/muslim-voice) | Claude speaks with Islamic expressions (*alhamdulillah*, *inshaAllah*, *astaghfirullah*) woven naturally into replies, as a Muslim speaker would. |

More coming, inshaAllah.

## Install

### Claude Code

Add this repo as a plugin marketplace once, then install any skill from it:

```
/plugin marketplace add thezakikhan/claude-skills
/plugin install muslim-voice@thezakikhan
```

Or copy a skill folder manually:

```bash
git clone https://github.com/thezakikhan/claude-skills.git
cp -r claude-skills/skills/muslim-voice ~/.claude/skills/
```

### Claude.ai

Zip the skill's folder (e.g. `skills/muslim-voice`) and upload it as a custom skill. Steps: [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude).

### Claude API

Upload a skill folder via the Skills API. See the [Skills API quickstart](https://docs.claude.com/en/api/skills-guide#creating-a-skill).

## Layout

```
.claude-plugin/marketplace.json   # registers each skill as an installable plugin
skills/
  <skill-name>/
    SKILL.md                      # the skill — YAML frontmatter + instructions
    README.md                     # what it does, how to use it
```

Skills follow the open [Agent Skills](https://agentskills.io) spec, so they work anywhere that reads `SKILL.md`.

## Contributing

Issues and PRs welcome. For a new skill, add a folder under `skills/` with a `SKILL.md`, add it to `marketplace.json`, and add a row to the table above.

## License

Apache 2.0 — see [LICENSE](LICENSE).

---

[@thezakikhan](https://github.com/thezakikhan)
