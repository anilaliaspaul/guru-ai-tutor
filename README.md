<!-- GURU logo -->
<p align="center">
  <img src="skills/guru/assets/guru-logo.png" alt="GURU – Your Personal AI Learning Mentor" width="820">
</p>

<h1 align="center">GURU – Your Personal AI Learning Mentor</h1>
<p align="center"><strong>Learn. Practise. Revise. Master.</strong></p>
<p align="center">First public release: <strong>v1.0</strong></p>

GURU is a reusable, subject-independent AI tutor skill. It helps learners build genuine understanding and independent competence in **any subject**: software engineering, AI, professional certifications, languages, leadership, academic topics, or practical skills.

It is designed to work with **Claude Code**, **ChatGPT Codex**, and other compatible Agent Skills hosts.

## What makes GURU different?

GURU is not an answer generator. It is a structured teaching framework that makes the learner do the thinking, practise the skill, explain their reasoning, and demonstrate mastery.

- Personalised learning paths based on the learner's goal and current level.
- Beginner-friendly intake with free-text teaching language preferences and optional special instructions.
- Date-aware course updates: verify syllabus or exam-model changes against authoritative sources before updating the roadmap and assessments.
- Six teaching methods: high-leverage learning, realistic error simulation, plain-language translation, adaptive roadmap design, hidden-gap diagnosis, and Feynman-style explanation.
- Structured revision after **every module**.
- Cumulative progress test every **7 calendar days**.
- Comprehensive final assessment at course completion.
- Unlimited sessions per day and no arbitrary four-hour or daily lesson cap.
- Missed lessons and tests are carried forward rather than silently skipped.
- Learner-controlled start, pause, resume, and additional sessions.
- Scheduled lesson preparation with a mobile-ready notification workflow where the host supports push notifications.
- Calendar-based recurring study sessions, module revisions, weekly tests, and final assessments.
- Natural-language schedule management: start now, move a lesson, schedule a weekly test, show the learning calendar, and pause notifications.

## Repository structure

```text
guru-ai-tutor/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── ROADMAP.md
├── .gitignore
├── skills/
│   └── guru/
│       ├── SKILL.md
│       ├── agents/
│       │   └── openai.yaml
│       └── assets/
│           ├── guru-icon.png
│           ├── guru-icon.svg
│           ├── guru-logo.png
│           └── guru-logo.svg
├── .claude/
│   └── skills/
│       └── guru/
│           └── SKILL.md
└── .agents/
    └── skills/
        └── guru/
            └── SKILL.md
```

`skills/guru/SKILL.md` is the canonical source. The `.claude/skills` and `.agents/skills` copies make the repository directly discoverable when cloned and opened as a project in Claude Code or Codex. Keep all three copies in sync when publishing updates.

## Install in Claude Code

### Global installation

```bash
npx skills add https://github.com/anilaliaspaul/guru-ai-tutor --skill guru -a claude-code -g
```

### Project installation

Clone the repository and open it in Claude Code. The included `.claude/skills/guru/` folder makes GURU available to that project.

### Manual global installation

Copy `skills/guru` to `~/.claude/skills/guru` on macOS/Linux, or `%USERPROFILE%\.claude\skills\guru` on Windows.

## Install in ChatGPT Codex

### Personal/global installation

Copy `skills/guru` to `~/.agents/skills/guru` on macOS/Linux, or `%USERPROFILE%\.agents\skills\guru` on Windows.

### Project installation

Clone the repository and open it in Codex. The included `.agents/skills/guru/` folder is the repository-level discovery location.

Codex can also install skills from external repositories using its built-in `$skill-installer`. In Codex, invoke `$skill-installer` and provide the public GitHub repository URL:

`https://github.com/anilaliaspaul/guru-ai-tutor`

Then specify the skill path: `skills/guru`.

If a newly added skill does not appear, restart Codex and inspect available skills with `/skills`.

## Use GURU

- Claude Code: `/guru`
- Codex: `$guru`
- ChatGPT desktop skill picker: `@GURU` where custom skills are enabled.

Example:

> Use GURU. I want to learn cloud architecture. Help me define my goal, assess my current level, and create a learning plan.

GURU collects the learner's requirements, clarifies anything ambiguous, assesses current knowledge, and builds an adaptive roadmap.

## Learner setup

GURU collects **eight required inputs and one optional input**. It reuses information the learner has already provided and asks only for details that are missing or unclear.

1. **Skill or subject.**
2. **Final goal** or measurable outcome.
3. **Target completion date**, or an explicit no-deadline choice.
4. **Daily study-time target** in minutes. This is a planning estimate, not a cap on lesson length or sessions.
5. **Teaching language**, in free text; any language or combination is accepted.
6. **Teaching mode:** Voice, Text, or Both, subject to host capabilities.
7. **Daily lesson-material preparation/notification time and timezone**, or no scheduled notification.
8. **Preferred study days/time windows and calendar block duration**, or no calendar events. This is separate from the preparation/notification time.
9. **Other special instructions (optional):** for example, a future syllabus change, required official sources, accessibility needs, workplace constraints, or topics to prioritise or avoid.

For dated syllabus or exam-model changes, GURU creates a review checkpoint, checks authoritative sources on or after the specified date, and updates the roadmap and assessments only when the change is verified. If it cannot verify the change, it reports that limitation and retains the last verified material.

If an answer is unclear, GURU asks again rather than guessing. The optional field never blocks the learner from proceeding.

## Assessment commitments

| When | Required activity |
|---|---|
| After every module | Structured revision and gap repair |
| Every 7 calendar days | Cumulative progress test |
| At course completion | Comprehensive final assessment |

A lesson is not complete merely because the content was delivered. GURU requires evidence of understanding and application.

## Compatibility notes

- The core `SKILL.md` follows the Agent Skills format and stays platform-neutral.
- `agents/openai.yaml` provides optional OpenAI/Codex UI metadata and branding.
- Claude Code uses the standard skill folder and does not require `openai.yaml`.
- The repository includes native discovery folders for Claude Code and Codex.
- Background lesson preparation and mobile push notifications require a host scheduler, supported mobile app, and notification permission. A skill alone cannot send popups.
- Calendar creation and editing require a connected calendar integration with appropriate access. GURU asks for approval before creating the initial calendar plan.
- Preparation time, study appointment time, and ready-notification delivery are separate. The skill never claims a popup was seen or an event was written unless the host confirms the action.
- GURU understands natural-language commands to start now, move a lesson, schedule a weekly test, show the learning calendar, and pause notifications for a week.

## Contributing

Issues and pull requests are welcome. Keep the core tutor instructions platform-neutral and update the platform-specific metadata or discovery copies when needed.

## License

MIT. See [LICENSE](LICENSE).
