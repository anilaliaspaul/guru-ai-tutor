# GURU Roadmap

This roadmap describes possible directions for the open-source GURU skill. It is a planning document, not a promise that every item is implemented or has a delivery date. Priorities may change based on learner feedback, maintainer capacity, and the capabilities of supported AI hosts.

## Current release: v1.0

The current release provides a platform-neutral teaching framework with: 

- Personalised learner intake, including optional special instructions.
- Six complementary teaching methods.
- Adaptive learning roadmaps and diagnostic assessment.
- Mandatory revision after each module.
- Cumulative progress tests every seven calendar days.
- A comprehensive final assessment and mastery rubric.
- Missed-work recovery and learner-controlled sessions.
- Scheduling and calendar workflows that use host integrations when available, with explicit capability limits.
- Date-aware syllabus and exam-model review instructions that require authoritative verification.

## Near-term priorities

### 1. Reliability and documentation

- Validate the skill structure against supported Agent Skills host conventions.
- Keep the canonical skill and Claude Code/Codex discovery copies synchronised.
- Improve installation, troubleshooting, and example-session documentation.
- Add repeatable checks for required teaching stages, assessment cadence, and scheduling safety rules.

### 2. Teaching quality validation

- Test GURU with learners studying unrelated subjects, not only software or AI certifications.
- Evaluate whether diagnostic questions reveal genuine knowledge gaps.
- Assess the usefulness and workload of module revisions and weekly tests.
- Refine mastery criteria so they reflect demonstrated ability rather than lesson completion.

### 3. Host compatibility

- Document differences between Claude Code, Codex, and other compatible hosts.
- Test tool-dependent workflows only where the host actually exposes the required tools.
- Make fallbacks explicit when calendar, scheduler, notification, voice, or web access is unavailable.

## Longer-term ideas

These are exploratory and are **not features of the current skill release**:

- Optional reusable assessment templates for different learning domains.
- Learner-owned progress export/import formats.
- Shared progress continuity across AI platforms through an external storage integration.
- A standalone GURU learning application with independent scheduling and notifications.
- Email assessment reports, learning cohorts, study groups, and course-specific leaderboards.
- Privacy-conscious peer comparisons based on comparable assessments and demonstrated improvement.

## Product principles

1. **Learning before engagement:** optimise for understanding and transfer, not time spent in an app.
2. **Evidence before mastery claims:** require explanations, practical work, and assessment evidence.
3. **Source transparency:** verify changing syllabuses and policies against authoritative sources and record when they were checked.
4. **Learner control:** make schedules, reminders, and learning pace explicit and adjustable.
5. **Privacy by default:** do not expose learner records or assessment results to other people without clear consent.
6. **Honest capability boundaries:** a skill alone cannot guarantee background execution, push notifications, calendar writes, email delivery, or cross-platform persistence. Those require host integrations or separate software.
7. **Subject independence:** avoid hard-coding GURU to a particular vendor, exam, profession, or language.

## How to influence the roadmap

Open an issue with the learning problem, the expected outcome, and an example of how the proposed change would help. Bug reports should include the host, relevant skill version, and a minimal reproduction where possible. Do not include private learner records, credentials, or confidential assessment material.
