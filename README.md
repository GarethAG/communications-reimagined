# Communications, Reimagined

This folder is ready to host with GitHub Pages. The complete diagnostic is bundled into `index.html`, including its styling, logic, motion and Gallagher logo assets.

## Publish with GitHub Pages

1. Create a new GitHub repository.
2. Upload the contents of this folder to the repository root.
3. Open **Settings**, then **Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select the `main` branch and the `/ (root)` folder, then save.
6. GitHub will show the live address when publishing finishes.

## Included functions

- Number keys 1, 2, 3 and 4 select answers.
- Enter moves to the next question.
- Progress is stored in the visitor's browser.
- **Save PDF** opens the browser print dialogue with print-specific formatting.
- **Email results** opens a prefilled email containing the score and dimension breakdown.
- **Copy results link** creates a URL containing the completed result.

## Changing the email recipient

The current results recipient is `Gary_Moss@ajg.com`. Search for that address inside `index.html` and replace it if required.

## Technical notes

This is a static site. It does not need Node.js, a database, a build command or a server-side application. GitHub Pages can serve it directly.

