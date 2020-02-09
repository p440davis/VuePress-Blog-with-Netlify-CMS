---
title: Get started
date: 2020-02-09T11:57:55.187Z
author: Pete Davis
tags:
  - VuePress
  - Netlify CMS
permalink: '/:slug'
---
## Get started

### Deploy to Netlify

The best way to start is to hit this button:

<ExampleComponent />

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
