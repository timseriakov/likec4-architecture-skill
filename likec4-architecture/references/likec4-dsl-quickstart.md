# LikeC4 DSL Quickstart

Use this when creating or rewriting models.

## Top-level blocks

LikeC4 source uses one or more of:

- `specification` - define element/relationship/tag kinds
- `model` - define elements, hierarchy, and relationships
- `views` - define diagram projections

## Minimal working example

```c4
specification {
  element actor
  element system
  element container
}

model {
  user = actor "User"
  product = system "Product"
  web = container "Web App"
  api = container "API"

  user -> web "Uses"
  web -> api "Calls"
}

views {
  view context {
    include user
    include product
  }

  view containers {
    include user
    include web
    include api
  }
}
```

## Core syntax

### Element declaration

```c4
model {
  api = container "API" {
    technology "Node.js"
    description "Business logic and endpoints"
  }
}
```

### Nested elements

```c4
model {
  platform = system "Platform" {
    web = container "Web App"
    api = container "API"
  }
}
```

### Relationships

```c4
model {
  web -> api "Calls"
}
```

### Views and include predicates

```c4
views {
  view index {
    include *
  }
}
```

## Authoring rules

- Keep IDs stable once published (`api`, `billingWorker`, `ordersDb`).
- Prefer domain names over technical folder names.
- Use explicit relationship labels (`Publishes`, `Consumes`, `Reads/Writes`).
- Keep view scopes intentional; avoid giant all-in-one views.

## Official docs

- Intro: https://likec4.dev/dsl/intro/
- Specification: https://likec4.dev/dsl/specification/
- Relationships: https://likec4.dev/dsl/relationships/
- Views: https://likec4.dev/dsl/views/
