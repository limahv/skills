# Skills

Agent skills that keep you in the loop: you stay the one who knows where the code lives and what it does.

## Install

```bash
npx skills add <user>/<repo>
```

Pick agents with `-a` (e.g. `-a claude-code -a codex -a opencode`), install globally with `-g`.

## Skills

| Skill | Triggered | What it does |
|---|---|---|
| [`pair-programming`](skills/pair-programming/SKILL.md) | by you | The agent sketches an approach in private while you draft the code, then you compare both and decide together. |
| [`implementation-frame`](skills/implementation-frame/SKILL.md) | by the agent | When details turn into shape questions (names, signatures, types, files), the agent asks you to write a code frame instead of a prose spec, then builds inside it. |
| [`tdd-first`](skills/tdd-first/SKILL.md) | by the agent | Before implementing, the agent proposes test cases for your approval, then goes red → green. |
| [`zoomed-out`](skills/zoomed-out/SKILL.md) | by the agent | When your replies turn vague, the agent maps the conversation's turning points and asks where you lost the thread. |

`pair-programming` uses `disable-model-invocation: true`, which Claude Code honors; other agents may ignore it.

## License

[MIT](LICENSE)
