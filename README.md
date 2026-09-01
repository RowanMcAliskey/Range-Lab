[README.md](https://github.com/user-attachments/files/31709184/README.md)
# Range Lab

Range Lab is a mobile-first golf practice app designed to make range sessions feel more like playing golf.

Instead of repeatedly hitting the same club, Range Lab gives each ball a club, a personalized target distance, and a clear shot intention. The golfer hits it once, records the result if desired, resets, and moves on.

**Hit a shot. Live with it. Move on.**

## Features

- Random Practice and course-style practice modes
- Personalized club selection and carry distances
- Fundamentals and Advanced shot calls
- Optional direction, contact, flight, shape, and strike feedback
- Configurable reset time between shots
- Automatic recovery of interrupted sessions
- Session history, practice trends, and pattern detection
- CSV export
- No accounts, advertisements, or external tracking

## Run the App

Open `range_lab.html` in a browser. There is no build step, framework, or dependency installation.

The file can also be hosted as a static site through GitHub Pages.

## Data and Privacy

Practice data is stored locally in the golfer's browser using IndexedDB, with a local-storage fallback. Data does not sync between devices. Clearing browser site data may remove saved sessions, so users should export a CSV if they want a backup.

## Project Structure

The complete app is contained in one file:

`range_lab.html`

It includes all HTML, CSS, JavaScript, shot-generation logic, storage, and analytics.
