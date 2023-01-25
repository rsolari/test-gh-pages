# Deploy to Github pages from Github actions


I'm testing out a Github Action to delpoy to Github Pages on commit.

This repo is configured to deploy the `public/` directory using the "Static HTML By GitHub Actions" default action. 


### Steps
- put your HTML files in `public/`
- In the repository settings, `Settings` > `Code and Automation` > `Pages`, under `Build and Deployment" change the "Source" from `Deploy from a Branch` to `GitHub Pages`
- Go to `Actions` > `New Workflow` > `Pages` > `Static HTML` > `Configure`
- In the default YAML file, under `jobs.deploy.steps.path` change the `path` of the "Upload Artifact" job to `public/`
- Save the YAML file

On commit, the Github action should deploy the static HTML from `public` to github pages at https://YOURNAME.github.io/REPONAME/, e.g.  https://rsolari.github.io/test-gh-pages/
