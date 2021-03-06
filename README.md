[![Netlify Status](https://api.netlify.com/api/v1/badges/d5ba9070-f033-4b70-915b-7278fca41dd0/deploy-status)](https://app.netlify.com/sites/vuepress-blog-starter/deploys)
<a href="#" target="_blank">
  <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow.svg" />
</a>

# VuePress blog with Netlify CMS

> VuePress default blog theme template with netlify config for quick start

<a href="https://app.netlify.com/start/deploy?repository=https://github.com/p440davis/VuePress-Blog-with-Netlify-CMS&amp;stack=cms"><img src="https://www.netlify.com/img/deploy/button.svg" alt="Deploy to Netlify"></a>

## Demo site

[vuepress-blog-starter.netlify.com](https://vuepress-blog-starter.netlify.com/)

<a href="https://vuepress-blog-starter.netlify.com/"><img src="https://raw.githubusercontent.com/p440davis/VuePress-Blog-with-Netlify-CMS/master/blog/.vuepress/public/media/VuePress_%2B_Netlify_CMS.png" alt="" /></a>

## Features

### VuePress "best of both" static site generator

- Generates static html for every page so that your first page load is super fast
- Once loaded, the site runs as a Single Page App (SPA), making it super slick

### Default VuePress starter theme

- Navbar
- Homepage blog feed
- Page layout
- Sidebar with heading navigation
- Use Vue components within markdown to enhance your content
- Customise your site by [inheriting from this default theme](https://vuepress.vuejs.org/theme/inheritance.html) or [create your own from scratch](https://vuepress.vuejs.org/theme/writing-a-theme.html)

### Netlify's CMS integration

- User-friendly content editor with styled preview hosted at /admin on your website
- Git-powered editorial workflow manages content in your repo automatically
- Post collection configured so that you can start blogging content straight away

## Get started

### Deploy to Netlify

The best way to start is to hit this button:

<a href="https://app.netlify.com/start/deploy?repository=https://github.com/p440davis/VuePress-Blog-with-Netlify-CMS&amp;stack=cms"><img src="https://www.netlify.com/img/deploy/button.svg" alt="Deploy to Netlify"></a>

This is the fastest way to get your website going. You will initially be hosted on a random URL, but you can add your own domain name later in your "Domain settings" on Netlify.

### Using as a GitHub template

If you are not deploying to Netlify, click the "Use this template" button above to create your own repo from this template.

## Setup Netlify CMS

### Edit your admin config

Edit the `backend` config in `.vuepress/public/admin/config.yml` to point at your repo.

```
backend:
  name: github
  repo: username/repo
```

### Enable CMS login with GitHub OAuth

You can use [Netlify Identity](https://docs.netlify.com/visitor-access/identity/) to authenticate CMS users, but to start off, it's simplest to give yourself access with GitHub OAuth.

1. Go to your [developer settings on GitHub](https://github.com/settings/developers) and add a new OAuth app.
2. Enter the name and full URL of your Netlify site and this authorization callback URL:

```
https://api.netlify.com/auth/done
```

3. Click Register application to get your Client ID and Client Secret. You will need these in a moment.
4. In your site Settings, open 'Access control'. Under OAuth, click 'Install provider' and copy in the Client ID and Secret from [GitHub](https://github.com/settings/developers).

You should now be able to visit the /admin page on your website and login with GitHub.

## Install and develop on your computer

You will need Node installed locally.

```sh
npm i   # installs vuepress
npm run dev   # live development
```

### Build and deploy

```sh
npm run build   # production build in blog/.vuepress/dist
```

## Author

Pete Davis

- Website: [petedavis.dev](https://petedavis.dev)
- Github: [@p440davis](https://github.com/p440davis)

## Contribute

This template is default VuePress - so please give your [skills](https://github.com/vuejs/vuepress) or [money](https://opencollective.com/vuepress) to the [VuePress team](https://github.com/vuejs/vuepress).
