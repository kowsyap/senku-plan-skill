# Senku plan skill

Get a workout plan into the [Senku](https://github.com/kowsyap/project-senku)
iPhone app with any AI:

- **Make** a plan from a few questions: goal, days a week, time, equipment,
  experience.
- **Convert** a plan you already have: Excel, PDF, Word, a photo or text.

Both give you one `.json` file, with every exercise matched to Senku's own
list, that Senku imports in a tap.

## Get it

**[Download senku-plan.zip](https://github.com/kowsyap/senku-plan-skill/releases/latest/download/senku-plan.zip)**,
the latest version, and keep it zipped.

### Claude (web or desktop)

Custom skills need a paid plan (Pro, Max, Team or Enterprise) with code
execution on.

1. Open **Settings → Capabilities**. Make sure code execution and file
   creation are on.
2. Under **Skills**, choose **+ → Upload a skill** and pick `senku-plan.zip`.
   (Claude moves these menus now and then; look for *Skills* in Settings.)
3. In a new chat, type **`/senku-plan`** and ask for a plan, or attach yours.

### Claude Code

Unzip it into `~/.claude/skills/`, so the file is at
`~/.claude/skills/senku-plan/SKILL.md`. Then type `/senku-plan`.

### Other AIs

- **Skills supported** (Codex, Copilot, Cursor and similar): put the
  `senku-plan` folder in the tool's skills directory.
- **Chat only** (ChatGPT, Gemini…): paste
  [`prompt-make.md`](senku-plan/prompt-make.md) to make a plan, or
  [`prompt.md`](senku-plan/prompt.md) to convert one. The Senku app gives you
  the same prompts, with your own exercises added, under
  **Workout → Your Week → Import a plan**.

## Import into Senku

1. Get the `.json` onto your iPhone: AirDrop, Files or Mail.
2. In Senku, press and hold the **SENKU** logo for a second, or use **Import
   plan** on the Import a plan page.
3. Check the preview and tap **Replace**. Only your plan changes.

More detail, the script and worked examples: [`senku-plan/README.md`](senku-plan/README.md).

## Versions

Each release follows a change to Senku's exercise list or to the skill. Plans
carry the exercise list's version, and Senku tells you on import if yours was
made from an older one: download the latest zip and make it again.

MIT licence.
