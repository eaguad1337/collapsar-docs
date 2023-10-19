---
weight: 10
title: "Quickstart"
description: "A guide to getting up and running with Collapsar"
icon: "rocket_launch"
date: "2023-10-15T15:11:11-03:00"
lastmod: "2023-10-15T15:11:11-03:00"
draft: false
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
pip install collapsar
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

## Publish the assets

```bash
python craft collapsar:install
```

## Create a resource

Use the following command to create your resources, where `MyModel` is the class name of your [Masonite Model](https://orm.masoniteproject.com/models).

```bash
python craft resource MyModel
```

Your new resource will be placed in `app/collapsar/resources/MyModelResource.py` with a base configuration.

```python
from collapsar import Resource
from collapsar.IdField import IdField

from app.models.MyModel import MyModel

class MyModelResource(Resource):
    """MyModel Resource."""

    title = "MyModel"
    model = MyModel

    @classmethod
    def fields(cls):
        """Return the fields of the resource."""

        return [
            IdField("Id", "id").readonly().sortable(),
        ]
```

Great! From now on, you can add [Fields](/docs/fields), [Validations](/docs/validation) or define your Field [Visibility](/docs/visibility)

To see your dashboard, visit [https://localhost:8000/collapsar](https://localhost:8000/collapsar)