# Ambitious Science Teaching · Unit 1: Investigating Matter

OLX source for a scenario-based learning activity (SBLA) for **ELED 3261, Elementary Science Methods**, at the University of Memphis. It runs on [lo-blocks](https://github.com/olxhub/lo-blocks/).

**Live preview:** https://benspierce.github.io/ast2/ (a static build: answers stay in your own browser and nothing is collected, and the AI feedback step on the last screen is inactive there).

## What it is

A pre-service teacher on field placement meets with their methods instructor, Dr. Okafor, and four classmates to study the first four minutes of their cooperating teacher, Ms. Boyd, launching a fourth-grade unit on matter with a frozen Michigan lake as the anchoring phenomenon. Over one unit the candidate:

1. reads the school and the children before reading the lesson;
2. learns the framework's vocabulary (anchoring phenomena; kinds of teacher questions) by matching, then explains it in their own words;
3. reads the transcript closely: the scientific discourse in Ms. Boyd's questions, and her own unit and lesson plans against what a child actually said;
4. argues, with classmates who disagree with each other and with the course, about whose experiences the launch assumed (the critical and cultural reading of Ambitious Science Teaching);
5. examines their own assumptions about what makes a "good" phenomenon;
6. replays the launch as Ms. Boyd, making her decisions against the clock, and accounts for what their choices made possible and what they cost; and
7. plans a launch of the same science for the same room, as a lesson plan a substitute could run.

The course's four learning goals: understand how phenomena anchor science learning; examine how choosing and using a phenomenon is an equity decision; examine one's own assumptions and practice; and translate this into concrete, equity-oriented instructional designs.

The school is invented; the district, the numbers, the standards, and the storms are real.

## Layout

Everything is in `unit1-investigating-matter/`:

| File | What it holds |
|---|---|
| `manifest.yaml` | Title, namespace (`wp`), and the launch route. |
| `whose_phenomenon_sba_part1.olx` | The shell: the Course, the unit's screen order (with completion gates), and the Reference chapter. |
| `wp_session.olx` | The unit's screens and dialogue, the lesson-plan screen, and the print page. |
| `whose_phenomenon_activities_part1.olx` | The exercises: matching, checks, writing prompts, the transcript, and the transcript-marking task. |
| `wp_reference.olx` | Reference pages: the school, the class roster, Ms. Boyd's materials, the standards behind her plan, the frameworks, and the research evidence on both sides. |
| `replay/` | The replay: an introduction, one file per episode, the ending, the clock and "taken up" meters, and the debrief. |
| `artifact.olx` | "My Launch Study," the running record of the candidate's work. |
| `characters.cast` | The cast: the instructor, four classmates, the cooperating teacher, and the children of Room 14. |

Block ids use the prefix `wp_`, from the activity's working title, *Whose Phenomenon?*

## Running it

In a lo-blocks checkout, put `unit1-investigating-matter/` under `content/` (for example `content/sba/`), start the server (`npm run dev`), and open `http://localhost:8888/preview/wp/wp_sba_part1`.

A static build for subpath hosting:

```bash
npm run build
NO_SANDBOX=1 STATIC_BASE_PATH=/<subpath> ./node_modules/.bin/tsx scripts/build-static.ts \
  --manifest content/sba/unit1-investigating-matter/manifest.yaml
```

Keep the namespace `wp`: the in-text buttons that open Reference pages address them by namespaced id (for example `wp/wp_ref_materials`).

## Status

A working draft, under revision with the course instructor. The "Plan your own launch" screen is a draft for the instructor's revision. Known issues: the debrief's instructor path map is visible to students, and the AI feedback on the last screen needs a server with an LLM configured.

## License and credits

AGPLv3; see `LICENSE.TXT` and the additional terms in `NOTICE.TXT`. Credits are in `CONTRIBUTORS.TXT`.
