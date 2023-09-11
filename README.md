# LLM generated website for a documentary movie

[![Gana tu espacio | Grafiti & Arte urbano mexicano](./images/header.es.1920.jpg)](http://ganatuespacio.art)

## Getting started

Requirements: [Git](https://git-scm.com/downloads), [Node.js](https://nodejs.org/en/download/current), [Codeium](https://codeium.com/download) for [VSCode](https://code.visualstudio.com/Download) (or your preferred editor)

### Opening local version

1. [Fork](https://github.com/iki/ganatuespacio/fork) this repository

2. Clone the forked repository to your machine

   ```sh
   git clone https://github.com/YOUR-GITHUB-ID/ganatuespacio
   ```

3. Run any local development http server like VS Code [Live Server](https://github.com/ritwickdey/vscode-live-server) or Node [live-server](https://github.com/tapio/live-server):

   ```sh
   npx live-server
   ```

### Editing

1. Edit [`index.html`](./index.html)
2. Check the result in your browser
3. If any changes are needed, repeat from step 1
4. Update localized versions

### Editing via LLM

1. Edit the [prompt](./prompt.md) and paste it to Codeium sidebar in your editor
2. Replace [`index.html`](./index.html) content with the generated output
3. Check the result in your browser
4. If any changes are needed, update the prompt in Codeium sidebar and repeat from step 2
5. Update the [prompt](./prompt.md) to match the last Codeium prompt from step 4
6. Update localized versions

### Submitting changes

1. Make sure that the site works locally as expected
2. Make sure that all content files are updated:

   - `prompt.md` - updated LLM prompt (if used)
   - `index.html` - generated webpage (`en`)
   - `es/index.html` - generated webpage (`es`)
   - `cs/index.html` - generated webpage (`cs`)

3. [Create a branch](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-branches) named `feat/NAME`, where `NAME` is a short descriptive name using lowercase and dashes like `add-awards`

   ```sh
   git checkout -b feat/NAME
   ```

4. [Commit](https://github.com/git-guides/git-commit) the changes with description `feat: DESCRIPTION`, where `DESCRIPTION` is a short one-line description in imperative mode like `Add awards`

   ```sh
   git add prompt.md index.html es/index.html cs/index.html
   git commit -m "feat: DESCRIPTION"
   ```

5. [Push](https://github.com/git-guides/git-push) the branch to your forked repository

   ```sh
   git push origin feat/NAME
   ```

6. [Create a Pull Request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork) to the main repository

   Open https://github.com/YOUR-GITHUB-ID/ganatuespacio/compare/feat%2fNAME...iki:ganatuespacio:main

## Watch the trailer

[![Watch the trailer](https://img.youtube.com/vi/-MFLoG6FGuw/maxresdefault.jpg)](https://youtu.be/-MFLoG6FGuw)

![Take your space | Mexican graffiti and urban art](./images/header.en.1920.jpg)
