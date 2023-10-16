---
weight: 800
title: "Contributing"
description: ""
icon: "article"
date: "2023-10-15T15:13:44-03:00"
lastmod: "2023-10-15T15:13:44-03:00"
draft: true
toc: true
---

If you're new to **Masonite** I suggest you to first read the [Official Documentation](https://docs.masoniteproject.com/).
Masonite strives to have extremely comprehensive documentation 😃. It would be wise to go through the tutorials there.

Have questions or want to talk? Be sure to join the [Masonite Discord Community](https://discord.gg/TwKeFahmPZ).

## Develop instructions

To test the project locally, you just need to clone the repository and configure a basic .env just like any masonite project.

```bash
git clone https://github.com/eaguad1337/masonite-collapsar
```

## Install dependencies

```bash
python -m venv venv
source venv/bin/activate
python -m pip install -r requirements.txt
```

Create a simple .env
```bash
cp .env-example .env
```

Run migrations
```bash
python craft migrate
```

Build assets

```bash
npm install
npx vite build
```

Run the app
```bash
python craft serve
```

Visit [http://localhost:8000/collapsar](http://localhost:8000/collapsar) and you should see the dashboard and the User resource.
