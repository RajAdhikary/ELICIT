# ELICIT

An offline tool for structured photo elicitation in language documentation fieldwork.

ELICIT runs in the browser on an iPad (or any tablet or laptop) and works without an internet connection once loaded. A fieldworker sets up a session for a speaker, loads photo stimuli, and works through standardized question sets. Answers are recorded as typed responses, multiple-choice selections, or audio, and can be exported as CSV for analysis.

It was built for documenting Garhwali ecological knowledge in the Mandal Valley, Uttarakhand, India. The question sets are written in Garhwali with Hindi glosses, but the structure is meant to be adapted to other languages and domains.

## Features

- **Works offline.** A service worker caches the app, so it keeps working in places with no network.
- **Installs to the home screen.** On an iPad, open it in Safari and choose *Share → Add to Home Screen* to run it full screen.
- **Photo stimuli.** Load your own photos from the device for each question set.
- **Standardized question sets.** Questions are grouped into categories and "books":
  - Ecolinguistics: Plants, Animals, Birds
  - Kinship & Social Terms: Family Relations, Social Roles, Life Stages
  - Body & Health: Body Parts, Illness & Medicine, Emotions & States
  - Material Culture: Tools & Implements, Clothing & Adornment, Food & Cooking
  - Grammar & Paradigms: Verb Paradigms, Pronouns & Case, Sentence Elicitation
- **Several response types.** Short text, long text, single and multiple choice, and audio recording.
- **Speaker pseudonyms.** Sessions are labelled with pseudonyms (e.g. SP01) rather than names.
- **CSV export.** Export responses per question set, one row per photo, ready for R or a spreadsheet.

## Using it

The whole app is three files: `index.html`, `manifest.json` and `sw.js`, plus `icon.png`.

1. Serve the folder from any static web server (for example `python3 -m http.server` in this folder, then open `http://localhost:8000`).
2. Open it once while online so the browser caches it.
3. From then on it works offline.

## Data and privacy

ELICIT has no server and sends nothing anywhere. Responses are saved in the browser's local storage on the device you are using. Photo files are not stored by the app and need to be reloaded each session. Audio recordings are held in memory during a session.

Because everything lives on one device, **export your data regularly** and back it up according to your project's data management plan and ethics approval. Clearing the browser's data will delete saved responses.

## Status

ELICIT is in active development as part of my dissertation fieldwork. A native iPad version is planned. Bug reports and suggestions are welcome through GitHub Issues.

## Citing ELICIT

If you use ELICIT in your research, please cite it. GitHub's **Cite this repository** button (on the right of this page) gives the citation in APA and BibTeX formats, from the `CITATION.cff` file.

## License

Released under the [MIT License](LICENSE).

## Author

Raj Adhikary, Department of Linguistics, University of Florida
