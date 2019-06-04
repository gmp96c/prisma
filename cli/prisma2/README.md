# Prisma 2 CLI architecture

```

 ┌────────┐ exposes `prisma` cli
 │ prisma │◀─────────────┐
 ▲────▲───┘◀────────┐    │
 │    │             │    │
 │    │             │    └─────────────┬───────────────────────┐
 │┌───┴──────────┐  ├────────────────┐ │ @prisma/introspection │
 ││ @prisma/lift │  │ @prisma/photon │ └───────────▲───────────┘
 │└──────▲───────┘  └──────────▲─────┘             │  core + cli
 │       │ core + cli          │ core + cli        │
 │       │                     │                   │
 │       │                     │                   │
 ├───────┴──────┬──────────────┴───────────────────┘
 │ @prisma/cli  │
 └──────────────┘
    cli utils
```