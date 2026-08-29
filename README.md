# Nervous System Studio

A set-and-setting personalization tool (research preview). Single-file, dependency-free
web app deployed as a static site via Vercel. Profile and logs live in `localStorage`;
there is no account server.

## The part that matters

The app reads self-reported logs and offers observations about your environment. That is one
step away from a horoscope, and what separates them is a set of published rules about when
the tool is allowed to speak. `#/method` sets them out in full, with the numbers the engine
actually uses:

| Guard | Value | Why |
|---|---|---|
| Minimum entries before any comparison | 4 | Short series are dominated by the day; extreme first entries rebound on their own |
| Minimum entries per compared group | 2 | A comparison where one side happened once is a single evening with a label on it |
| Minimum difference on the 0–10 scale | 1.5 | Self-report drifts by about a point without anything changing |
| Maximum observations shown at once | 4 | Check enough pairs and some clear any threshold by chance |
| Confidence grade | Preliminary / Emerging / Moderate | 3-per-group and 8 total for Emerging; 5 and 12 for Moderate; Moderate is the ceiling |

Every surfaced observation now carries a **How this was computed** disclosure: the two groups,
their entry counts, their means, the difference against the floor, the rule that produced the
grade, how fragile it is (the score one further entry would have to fall below for the
observation to disappear), and what would raise its grade.

## What was added

- `#/method` — the guards explained with sources, a worked example on nine entries where the
  correct answer is that nothing is shown, and a live readout of your own data against the rules.
- A substantial journal empty state: what an entry captures, why in-the-moment logging matters,
  and the four-entry path to a first comparison.
- A readiness ladder on the dashboard.
- Export logs as JSON (carrying the thresholds and interpretation rules with them) or CSV,
  and re-import a previous export. All local: `Blob` out, `FileReader` in, no request.
- A labelled ten-entry sample set so the method can be inspected without waiting a fortnight.

## Evidence

`Nervous-System-Studio-Research-Dossier.md` is the graded evidence base. Method-page citations:
Barnett et al. 2004 (regression to the mean), Shiffman et al. 2008 (EMA), Benjamini & Hochberg
1995 (multiple comparisons), Harkin et al. 2016 (monitoring effects), and the What Works
Clearinghouse Procedures and Standards Handbook v5.0 (single-case designs require at least
three demonstrations of an effect at three different points in time).
