# Locales manager repository template

> [!NOTE]
> This is a template repository that you can use freely, make sure all data is updated in the various paths to work properly. 

## Setup

1. Use the template or download the code
2. Navigate to the workflows folder
   ```bash
   cd .github/workflows
   ```
3. Replace `Maximus7474/locales-manager-template` with your username / organisation name and repository name
    Not doing so will make the two main workflows not available.
4. Update this file to remove the usage instructions (doubt you'll want to keep them)
5. Update the locale files in the various folders
6. Update the static data in `.github/scripts/data.js`

## Features
* JSON formatting using [prettier](https://www.npmjs.com/package/prettier)
  * This is run on all forked repositories to keep the structure clean.
  * Triggered by workflow -> `.github/workflows/prettier.yaml`
* Pull Request validation
  * Compares the changed files found within the PR with the default locale (defined in `.github/scripts/data.js`)
  * Can handle multiple changed files across multiple resources
* Readme Recap updating
  * Demo visible below, will update a markdown table indicating which locales are up to date or missing for each resource
  * Runs on push to the main branch
  * Triggered by workflow -> `.github/workflows/update-readme-recap.yaml`

## Additional features

I have also created a [github action](https://github.com/Maximus7474/locale-manager-action) that links to this repository structure, to pull updated changes to the json files to the closed source project. Making it an easy system to implement into your CI/CD pipeline making your project easier to contribute to by your community without having the hassle of manually updating the files.

---

# Locales repository

This repository contains all the locale files for the various scripts.

If you want to contribute to maintaining these locales up to date, please refer to the [Contributing Guidelines](./CONTRIBUTING.md) to maintain a well structured repository.

<!-- start_recap -->
| Locale | [resource_1](https://creations.mtdv.me/watch?v=Z5OI9Df2fY) | [resource_2](https://creations.mtdv.me/watch?v=Z5OI9Df2fY) |
|--------------|--------------|--------------|
| German (de) |  | ✅ |
| English (en) | ✅ | ✅ |
| Spanish (es) |  | ❌ |
| French (fr) | ✅ |  |
<!-- end_recap -->

Icon information:
* ✅ - Up to date
* ❌ - Incomplete
