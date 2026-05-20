# Exam-timetable

This repository now hosts the exam countdown website at the repo root.

Files:
- `index.html` — app shell
- `styles.css` — UI styles
- `script.js` — app behavior

GitHub Actions is configured in `.github/workflows/pages.yml` to publish the root site on pushes to `main`.

## Usage

- Open `index.html` in a browser (or serve the folder with a simple static server).
- Add exams using the "Add Exam" button. Exams are stored in `localStorage` so they persist locally.
- Use the filter buttons to narrow the timeline by urgency or exam type.
- Toggle dark mode using the moon/sun button in the top-right; preference is saved.

## Improvements made

- Added accessibility landmarks, a skip link and improved focus styles.
- Replaced blocking `alert()` messages with a non-blocking aria-live toast.
- Fixed date calculation to use the current date at midnight for consistent day counts.
- Improved responsive layout and added prefers-reduced-motion support.

## Local testing

To serve locally (Python 3):

```bash
python3 -m http.server 8000
# then open http://localhost:8000 in your browser
```

If you'd like, I can also run a quick smoke test in a headless browser or add unit tests.