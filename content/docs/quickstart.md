---
weight: 1
title: "Quickstart"
description: "A guide to getting up and running with Collapsar"
icon: "rocket_launch"
date: "2023-10-15T15:11:11-03:00"
lastmod: "2023-10-15T15:11:11-03:00"
draft: true
toc: true
---

Collapsar is a package that will let you save time creating a dashboard for your app. You won't need to worry anymore about creating CRUD's.

{{<alert context="warning" text="Collapsar is in early development stage and it's nnot ready for production environments."/>}}

**Main features**

- **Resources**: Create multiple resources to your dashboard using your Masonite Models.
- **Use fields**: Choose between a set of **Fields** components to create your dashboard.
- **Add validations**: You can configure rules to validate user input directly from your **Resource** definition.

## Prerequisites

Before we start, make sure you have the following installed:

- Masonite 4 or later.
- Python3.
- Python3 Pip.

## Install Collapsar

Go to your project folder and run the following [pip](https://pip.pypa.io/en/stable/installation/) command.

```bash
pip install masonite-collapsar
```

{{<alert context="info" text="Make sure to init your **venv** first"/>}}

Add CollapsarProvider to your project in `config/providers.py`:

```python
# config/providers.py
# ...
from collapsar import CollapsarProvider

# ...
PROVIDERS = [
    # ...
    # Third Party Providers
    CollapsarProvider,
    # ...
]
```

## Create a user

{{<alert context="danger" text="Not ready at the moment."/>}}


## Usage

This package has the UserResource class as example, you could edit the configuration editing the file `/tests/integrations/app/collapsar/resources/UserResource.py`
