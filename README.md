# Jefferson Consulting Group

## About

Site live at [`Jefferson Consulting Group`](https://storied-concha-d0585a.netlify.app/).

Hosted on Netlify.

Powered by SvelteKit.

## Navigating the codebase

```src``` contains all the code files you need to be concerned with.

- ```src/routes``` has all the different pages.
    - ```+layout.svelte``` is the base layout for the site with the navbar and a slot for the rest of the page
    - ```+page.svelte``` is present in ```/routes``` and each subfolder (the name of the subfolder being the path) - it contains what is rendered on the page

- ```src/lib``` has all the files you would want to import
    - ```lib/assets``` has all your images
    - You also have all your reuseable compenents in this folder

## Developing

Once you've cloned the repo, run these commands to startup a locally hosted version of the site.

```bash
npm install
npm run dev -- --open
```

## Deploying

This site is hosted on Netlify, pushes to ```main``` will automatically deploy changes.

Pull Requests to ```main``` will create a preview version of the site to view changes before merge.
