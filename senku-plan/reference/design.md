# Designing a plan

How to build a week from scratch when there is no plan to convert. The result
is the same file as a conversion, in the same format, with every exercise named
exactly as the catalogue lists it.

These are mainstream, well-tested starting points, not the only right answers.
A sensible plan the person will follow beats a perfect one they will not.

## 1. Ask, once

Ask everything in **one message**, each with a default, so a reply of "defaults
are fine" is enough. Skip anything you were already told.

| Question | Choices | Default |
| --- | --- | --- |
| Main goal | build muscle · get stronger · general fitness · lose fat | build muscle |
| Days a week | 2 to 6 | 4 |
| Time per session | 30 · 45 · 60 · 75+ minutes | 60 |
| Equipment | full gym · home with dumbbells (and a bench?) · bodyweight only | full gym |
| Experience | new (under 6 months) · some (6 months to 2 years) · lots | some |
| Avoid | injuries, painful movements, exercises they dislike | none |
| Focus | muscles they want more of, if any | none |

If they mention **pain now, chest pain, dizziness, pregnancy, a heart or other
medical condition, or being under 18**, say plainly that they should check
with a doctor before training hard, and keep the plan conservative.

## 2. Pick the shape of the week

Senku lists each **distinct** day once and the person picks one each time they
train, cycling through. So a six-day push/pull/legs is three days in the file.

| Days a week | Shape | Days in the file |
| --- | --- | --- |
| 2–3 | Full body | 2 (A, B) for 2 days; 3 (A, B, C) for 3 days |
| 4 | Upper / Lower | 4: Upper A, Lower A, Upper B, Lower B |
| 5 | Upper / Lower + Push / Pull / Legs | 5: Upper, Lower, Push, Pull, Legs |
| 6 | Push / Pull / Legs, twice | 3: Push, Pull, Legs (or 6 with A/B variants for variety) |

Prefer A/B variants over identical repeats when there is room: the same muscles
with different exercises spreads the work across angles.

Tell the person how to run it in the app: "Train them in order and start again
at the top."

## 3. Cover the basics every week

Across the week, include at least one of each movement pattern:

- **Squat** (squat, leg press, split squat, lunge)
- **Hinge** (deadlift, Romanian deadlift, hip thrust, back extension)
- **Horizontal push** (bench, push-up, chest press)
- **Horizontal pull** (rows)
- **Vertical push** (overhead press)
- **Vertical pull** (pulldown, pull-up)

Then add isolation work for what those miss: side and rear delts, biceps,
triceps, calves, hamstring curls, abs.

## 4. Volume and frequency

- Aim for each major muscle (chest, back, shoulders, biceps, triceps, quads,
  hamstrings, glutes) to be trained **twice a week** where the days allow.
- Aim for roughly **10–20 hard sets per muscle per week**. Beginners can start
  nearer 8; more is not better past about 20.
- **Exercises per session** from the time available, at about 3 sets of each:

| Time | Exercises |
| --- | --- |
| 30 min | 3–4 |
| 45 min | 4–5 |
| 60 min | 5–6 |
| 75+ min | 6–8 |

Check the week with `python3 scripts/senku_plan.py volume FILE --days-per-week N`.
It counts weekly sets per muscle from the catalogue's own muscle data and flags
what is under-trained, over-trained or hit only once.

## 5. Order within a day

1. The heaviest compound first (squat, deadlift, bench, row).
2. Other compounds.
3. Isolation.
4. Abs, carries or conditioning last.

Do not put two hard exercises for the same small muscle back to back unless the
day is built around it.

## 6. Sets and reps by goal

| Goal | Big compounds | Other compounds | Isolation |
| --- | --- | --- | --- |
| Build muscle | 3 × 6–10 | 3 × 8–12 | 3 × 10–15 |
| Get stronger | 4 × 3–6 | 3 × 6–8 | 3 × 8–12 |
| General fitness | 3 × 8–12 | 3 × 8–12 | 2–3 × 12–15 |
| Lose fat | as build muscle; keep the heavy work, it keeps the muscle | | |

Put the most common scheme in `plan.target` and give only the others their own
numbers. Ranges suit Senku: when every set reaches the top at one weight, the
app suggests the next weight up and the range starts again. That is the whole
progression, so there is nothing else to write.

Beginners: 2–3 sets per exercise, fewer exercises, and more machines and
dumbbells than heavy barbell lifts.

## 7. Choosing exercises

- **Only from the catalogue**, by full Name, and only ones the equipment allows:

| Equipment answer | Use exercises with equipment |
| --- | --- |
| Full gym | anything |
| Home with dumbbells | `dumbbell`, `bodyweight` (and `kettlebell` if they have one). Bench exercises only if they have a bench. |
| Bodyweight only | `bodyweight` |

- Respect **avoid**: no exercise that loads the injured area, and say what you
  swapped.
- Add one extra exercise (or 2–4 sets) for a **focus** muscle, not a whole day.
- Prefer exercises most gyms have. Don't build a home plan around a pull-up bar
  unless they said they have one; use a row instead.
- Holds (plank, dead hang) and cardio go at the end. Cardio is named only, no
  numbers.

## 8. Hand it over

Besides the file and a list of each day with its exercises and sets × reps,
add short, practical guidance Senku does not store:

- **Rest:** about 2–3 minutes after heavy compounds, 1–2 after the rest. (Senku
  can start a rest timer after each set: Workout → Your Week → Rest.)
- **Effort:** finish most sets with about 1–3 good reps left in the tank.
- **Starting weights:** pick a weight that reaches the bottom of the range with
  good form; the app takes it from there.
- **Stop and see a doctor** for chest pain, fainting, or sharp joint pain.

Keep it to a few lines. This is not medical advice and should not read like it.
