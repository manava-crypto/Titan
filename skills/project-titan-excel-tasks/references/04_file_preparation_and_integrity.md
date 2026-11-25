# 04 · File preparation and integrity

From the task guide, section 7. These are conditions of acceptance, not style notes: a task cannot be taken forward until the sanitisation is done, and a file set that reads as machine-built is sent back.

## 7.1 Remove anything confidential or identifying

Client names, people, account numbers. The places it hides, all of which have to be checked and none of which show in the visible cells:

- hidden sheets, and hidden rows and columns;
- cell comments and notes;
- file metadata, including author, company, last-saved-by and the title;
- external links and defined names pointing at other files;
- data connections and query definitions;
- embedded objects, charts with cached source names, and pivot caches.

Sanitise consistently, so the task still works: a renamed entity has to be renamed everywhere it is referenced, or lookups break and the task becomes a puzzle about the renaming. And the expert has to have permission to share the material.

## 7.2 Say where each file came from

Either the expert's own sanitised work, or a named public source. A public source can still hold sensitive information, so it gets checked the same way before upload.

## 7.3 Keep inputs real

Messy is good: an export with new codes, a late adjustment, a changed template. Tidy inputs are where models already do well, so tidying the inputs usually removes the difficulty along with the mess.

## 7.4 Keep the inputs the expert's own

The guide's wording is that AI should not create or alter inputs, files or the prompt, and that reviewers check for it. In practice what matters at review is that the inputs read as a real export from real work: the expert's own figures, their field's codes and conventions, the mess a live file carries. Drafting help is fine; synthetic-looking data is what gets spotted. The signs reviewers read as generated are in the sweep below.

## 7.5 Use the Excel features and tools the job needs

If the job would reach for Solver, Power Query, pivot tables or macros, build the task around them and use a file format that supports them — .xlsm where there are macros. A task that needs a feature but ships in a format that cannot carry it fails at delivery, not at grading.

## 7.6 No artificial tricks

Inputs hidden in white font, meaningless tab names, bans on normal functions. These test whether a model spots a puzzle, not whether it can do the job. Leave them out.

## The sweep

Run all of it before judging a file set, and report what was checked as well as what was found.

- Open every sheet, including hidden ones, and unhide rows and columns.
- Read every comment and note.
- Read file properties: author, company, manager, title, last modified by, any custom properties.
- List external links, data connections, defined names and anything pointing outside the file.
- List embedded objects and images, and read any text in them.
- Check the renaming is consistent: every reference to a renamed entity resolves.
- Check the file format against the features the job needs.
- Check the number formats, dates and units are the ones a real export would carry, not retyped ones.
- Look for signs of generated content: perfectly uniform rows, dates on a constant spacing, round or repeating values, IDs that are sequential or hash-like, descriptive slugs that name the thing they identify, a status mix that never varies.

## Reporting a file finding

Say what was found, where it is, and what it does to the task. A client name left in the file properties is a blocking finding even though nothing on screen shows it. An inconsistently renamed entity is blocking because it changes what the task is testing. A white-font input is blocking because it makes the task a puzzle.

Give the exact change: the field, its current content, and what it should say. Where a value has to be invented to sanitise a real one, keep it in the shape the real data has — same length, same format, same code scheme — so nothing downstream breaks and nothing looks generated.
