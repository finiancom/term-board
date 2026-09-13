# Term Board

A free, local-first semester organizer. Track your courses, assignments, exams, and weekly class schedule in one page — no account, no server, no cost.

## Why

Most of what matters during a semester boils down to one question: *what do I need to know right now?* Term Board is built around that — a "right now" strip always shows your current or next class and the next thing due, a weekly time-grid shows your recurring lectures/exercises/seminars, and a month view is there when you need to plan further out.

## Features

- **Courses** — name, code, color, instructor, and an exam style box (bonus points and midterms, each with optional details, plus the final exam's type — session examination, end-of-semester exam, or graded coursework — and date).
- **Materials, organized** — slides, problem sets, solutions, reading, and recordings are grouped into sections instead of one flat list, and each one gets a to-do / in-progress / done status you click to cycle — handy for tracking your way through a pile of exercise sheets independent of any due date.
- **Deadlines & exams** — assignments, exams, quizzes, projects, and readings, each with a due date/time and notes. Overdue and due-soon items are called out automatically.
- **Study sessions** — plan a block of time to study, with or without tying it to a course. Shows up on the week calendar, in its own "Study" tab, and in the "right now" strip when one's in progress or coming up.
- **Weekly schedule** — give each course recurring lesson blocks (lectures, exercise classes, seminars — whatever labels your program uses) and see them laid out in a real weekly time grid.
- **Semester setup** — enter your term's start/end dates, exam period, and breaks once; the app then knows what week it is, and quietly skips recurring lessons outside the term and during declared breaks or the exam period, instead of showing them every single week forever. A "Fill from a preset" dropdown can fill all of this in for ETH Zürich's published semesters (hand-updated in the code, not fetched live) — or just fill it in manually for any other school.
- **Month & week calendar views**, with a course-specific view when you drill into one course.
- **Local folder connection** *(Chrome/Edge on desktop)* — point a course at a real folder on your computer and browse its files right there, using the browser's native File System Access API.
- **Local-only storage** — everything is saved in your browser via `localStorage`. Nothing is sent to a server, because there is no server. Export a JSON backup any time and import it elsewhere (or on the same device after clearing browser data).
- **Import a schedule from `.ics`** — parses a calendar file you already downloaded (e.g. ETH Zürich's myStudies "Add to calendar" export) entirely in your browser, no network call. Recurring weekly lectures/exercises become courses with a weekly schedule already filled in (grouped by course number when the title has one); one-off events like exams are left alone. Re-importing updates existing courses instead of duplicating them.

## Using it

Pick whichever is easiest:

- **Just open it.** Download `index.html` and double-click it. Everything runs from the file itself.
- **GitHub Pages.** Fork/clone this repo, enable Pages on the `main` branch, and you'll have a URL you can open from any device (each device keeps its own local data — see Data & privacy below).
- **Any static host.** It's one self-contained HTML file — Netlify, Vercel, a personal server, anywhere that serves static files works.

No build step, no dependencies to install, no signup.

## Data & privacy

Term Board stores everything in your browser's `localStorage` — courses, items, your semester setup. That means:

- Your data never leaves your device.
- It does **not** sync across browsers or devices automatically. Use **Export backup** (in the sidebar) to download a JSON file, and **Import backup** to load it somewhere else.
- Clearing your browser's site data for this page deletes everything — export first if that matters to you.
- The optional local-folder connection uses the browser's File System Access API, which is currently supported in Chromium-based browsers (Chrome, Edge) on desktop. It isn't available in Safari or Firefox; the app just hides that feature there.

## Contributing

It's a single HTML file (`index.html`) — all CSS and JavaScript inline, no build tooling. Open a PR with fixes or features; it's meant to stay dependency-free and easy to fork for your own school's conventions.

## License

MIT — see [LICENSE](LICENSE). Free to use, modify, and redistribute.
