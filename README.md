# Interview Practice

A free interview practice tool for formerly incarcerated individuals. It helps people prepare the two answers that matter most, the question about a conviction and "Tell me about yourself," then practice common interview questions out loud with a timer and print a one-page sheet to take to the interview. It runs entirely in the browser: no account, no server, and nothing typed into it is sent anywhere or stored unless the person chooses to save it.

Try it at https://olivercrocco.com/interview-practice/, or download `interview-practice.html` and open it in any browser. The single file works without the internet, so it can be shared on a USB drive or used on a laptop in a classroom.

It was built for an employment skills course in a Louisiana reentry bridge program for people in their first year after release, and is a companion to the [Reentry Resume Builder](https://github.com/olivercrocco/reentry-resume-builder) and [First Paycheck](https://github.com/olivercrocco/first-paycheck). Nothing in it is specific to Louisiana.

## What it does

- Builds the answer about a conviction in five parts: say it plainly, take responsibility, what you did with the time, who you are now, and bring it back to the job. Each part offers starting sentences to tap and then put in the person's own words. The whole answer shows with a word count, an estimate of how long it takes to say (about 130 words a minute), a warning for any blank left to fill, and a button that reads it aloud.
- Builds "Tell me about yourself" in three parts: who you are as a worker, what you have done, and why this job. A file saved by the Reentry Resume Builder can be opened to start this answer from the person's resume.
- Offers 19 practice questions in four groups (common questions, about your background, work situations, end of the interview). Each card can be read aloud, has a timer that turns amber when the answer runs long, tips on why the employer asks, a notes box, and a "practiced" check. Questions can be filtered by group or shuffled.
- Helps pick one or two questions to ask the employer.
- Ends with an interview day checklist, the first 30 seconds (greeting, eye contact, handshake), a thank-you message to copy, and a one-page interview sheet to print.
- Reads each step aloud on request, using the device's own voices, which work offline.

## Design choices

- The conviction answer follows a common reentry coaching structure: honest, brief, responsibility taken, focus on what changed and on the job. The guidance tells people not to go into the details of the case unless asked.
- It gives no legal advice about what employers may ask or what applicants must disclose. Programs using it should add their own guidance on fair-chance hiring rules where they work.
- No voice recording. Many sites and facility devices block the microphone, so the tool suggests practicing with a partner or a phone's voice recorder.
- No AI. Answers are the person's own, built from starting sentences they choose and edit.

## Files

- `interview-practice.html`: the whole tool in one file. This is the source of truth.
- `build-web.mjs`: builds `web/`, a version for sites whose Content-Security-Policy blocks inline scripts. Run `node build-web.mjs` after editing the single file.
- `web/`: the built web version (`index.html`, `core.js`, `ui.js`, and a copy of the single file for download).

## Adapting it

The content sits at the top of the first script in `interview-practice.html`: `STORY_PARTS` and `TELL_PARTS` (the starting sentences), `QUESTIONS` (each with its group, target time, reason, and tips), `ASK_THEM`, and `DAY_CHECKS`. Programs can change the wording to match how they coach without touching the rest.

## License

MIT. See `LICENSE`.

Built for formerly incarcerated individuals and the programs that support them, by Oliver S. Crocco, Louisiana State University.
