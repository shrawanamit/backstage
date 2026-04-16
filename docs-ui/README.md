# Backstage UI Docs

Backstage UI Docs is the documentation website for the Backstage internal UI library (`@backstage/ui`).  
The site provides an overview of the design system, reusable UI components, and usage guidelines for Backstage.

You can view the live website here:  
👉 https://ui.backstage.io

---

## Running the Site Locally:

The documentation site is built with **Next.js** and hosted on **GitHub Pages**.

To run the site locally:

```bash
yarn start
```

## Deployment:

Deployments are fully automated and triggered when a pull request is merged into the `master` branch. The site is hosted on GitHub Pages.

## Maintaining Component Changelogs:

After each `@backstage/ui` release, run `yarn sync:changelog` to keep component changelogs in sync with the documentation.

This script:

- Parses `packages/ui/CHANGELOG.md` for new versions
- Extracts entries tagged with "Affected components: ..."
- Updates `src/utils/changelog.ts` with new entries
- Handles both component-specific and general package changes

After running, review the changes in `src/utils/changelog.ts` and commit them.

## Preview changes before writing:

To preview the changelog updates without modifying any files, run:

```bash
yarn sync:changelog:dry-run
```
