# Communications, Reimagined

An interactive Gallagher diagnostic designed to help communications leaders decide what their function should become next as AI changes how communication work is produced, understood and governed.

The app runs entirely in the browser and guides users through a short diagnostic before producing a tailored maturity profile, strategic questions and recommended next moves.

## What the diagnostic includes

* Three possible ambitions:

  * **Scale**: do today's work more efficiently
  * **Elevate**: do work that is worth more
  * **Reimagine**: redefine what the communications function is for
* 14 scored questions
* Six diagnostic dimensions:

  * Making work
  * Audience
  * Voice and counsel
  * Function shape
  * Human judgement
  * Guardrails
* Four maturity levels:

  * Exploring
  * Individual
  * Shared
  * Embedded
* A results dashboard with:

  * Overall score
  * Primary maturity level
  * Dimension profile
  * Strongest and weakest signals
  * Priority board questions
  * Recommended next moves
* An eight-question **Board lens** for wider strategic discussion

## Key features

* Runs as a single self-contained HTML file
* No installation or build process
* Responsive desktop and mobile layout
* Keyboard-supported diagnostic navigation
* Progress is saved automatically in the browser
* Users can resume an unfinished diagnostic
* Results can be copied as a shareable URL
* Results can be saved as a PDF through the browser print dialogue
* Results can be placed into a pre-addressed email
* Print-specific styling produces a cleaner PDF
* Reduced-motion preferences are respected

## Privacy and data

The app has no database and does not automatically send answers to a server.

Diagnostic progress is stored locally in the user's browser using `localStorage`.

When a user selects **Copy results link**, their answers and any optional identity information are encoded into the URL fragment after `#result=`. The information is not sent anywhere automatically, but anyone who receives that complete link can open the results.

The email button uses a `mailto:` link. It opens the user's default email application with the results inserted into a draft. It does not send the email automatically.

## Technology

The distributed app is already compiled and bundled into one HTML file. It includes:

* HTML5
* CSS
* JavaScript
* React 19
* Tailwind CSS
* Anime.js
* Embedded Gallagher logo assets

No Node.js packages, external scripts or runtime dependencies are required to host the supplied file.

## Repository structure

```text
communications-reimagined/
├── index.html
├── .nojekyll
└── README.md
```

The supplied HTML file must be renamed to `index.html` before publishing.

The `.nojekyll` file can be empty. It tells GitHub Pages to publish the files directly without trying to process the site as a Jekyll project.


## Updating the app

Because the distributed version is a compiled single-file application, small content or logic changes must be made inside `index.html`.

After updating it:

1. Commit the changed `index.html` file.
2. Push or upload the change to the `main` branch.
3. GitHub Pages will publish the updated version automatically.

For substantial future development, it would be better to keep the original source project alongside the compiled HTML rather than editing the minified bundle directly.

## Important configuration

The current version contains a fixed result-email recipient. This is used by the **Email results** button.

Changing that recipient requires updating the email name and address in the application code and rebuilding the source app, or carefully editing the bundled JavaScript inside `index.html`.

The app does not provide automatic email delivery. A real send-email function would require a backend service or third-party form provider.

## Browser support

Use a current version of:

* Google Chrome
* Microsoft Edge
* Mozilla Firefox
* Safari

The app depends on modern browser features including `localStorage`, the Clipboard API, URL fragments, `TextEncoder` and `TextDecoder`.

## Troubleshooting

### The site shows a 404 page

Check that:

* The file is named exactly `index.html`
* It is in the repository root
* GitHub Pages is publishing from `main` and `/ (root)`
* The Pages deployment has completed successfully

### The old version still appears

Refresh the page without using the cached copy:

* Windows: `Ctrl + F5`
* macOS: `Cmd + Shift + R`

### Progress will not save

Check that browser storage is enabled and that the site is not running in a heavily restricted private browsing environment.

### The PDF button does not download immediately

This is expected. **Save PDF** opens the browser print dialogue. Select **Save as PDF** as the printer or destination.

### The email button does nothing

The button depends on the device having a default email application configured for `mailto:` links.

### A shared results link exposes personal details

Optional name, role and organisation fields are included in the encoded results link. Do not include sensitive information before sharing the URL.

## Ownership

This repository contains a Gallagher-branded diagnostic. Confirm internal approval, brand requirements, data handling expectations and permission to publish before making the repository or website public.

## Licence

No open-source licence is included by default.

Unless Gallagher has approved another arrangement, treat the code, branding and diagnostic content as proprietary and for authorised use only.
