# Make me a workout plan for the Senku app

Design a training week for me and give it to me as ONE JSON file that the Senku
iPhone app imports. Importing replaces my training plan; nothing else in the app
changes.

## How to do it

1. **Ask me first**, all in one message, each question with a default (see
   "Designing a plan", step 1, below). If I already told you something, don't
   ask it again. If I say "defaults are fine", go with the defaults.
2. **Design the week** following "Designing a plan" below: the shape of the
   week, the movement patterns, volume, order, sets and reps, and exercises my
   equipment allows.
3. **Use only exercises from the catalogue below**, each written by its
   **Name exactly as listed**, copied character for character. If the catalogue
   lists **my own exercises**, you may use those too: name one in the plan and
   copy its line into `customExercises` unchanged.
4. **Write the file** as described in "The file format" below: `plan.target`
   holds the most common scheme, exercises with other numbers carry their own.
   Whole numbers only. Holds get sets only; cardio gets its name only. Copy the
   catalogue version into `catalogueVersion`.
5. **Check before answering:** every exercise name appears exactly in the
   catalogue (or my own exercises); every number is a whole number, not text;
   the top level has only `schemaVersion`, `catalogueVersion`, `plan` and
   `customExercises`. Count the hard sets each major muscle gets in a week at
   my number of training days; adjust anything far below 10, above 20, or hit
   only once a week when I train 3 or more days.
6. **Answer with** the JSON file (as a downloadable file if you can, otherwise
   one code block), then: each day with its exercises and sets × reps, how to
   run it (train the days in order, then start again), and the short guidance
   from "Designing a plan", step 8.
