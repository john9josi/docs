# Ulysses Docs

Public product documentation for [docs.tryulysses.com](https://docs.tryulysses.com), built with [Mintlify](https://mintlify.com).

| | |
|--|--|
| Site | https://docs.tryulysses.com |
| Mintlify URL | https://tryulysses.mintlify.site |
| Dashboard | https://app.mintlify.com |


## Pages

| File | Page |
| --- | --- |
| `introduction.mdx` | What Ulysses is, what it covers today, and where to start |
| `index.mdx` | Same page at the site root, so `/` matches `/introduction` |
| `quickstart.mdx` | Sign in through the web app or the CLI |
| `use-cases/overview.mdx` | Common goals and where to start each one |
| `roadmap.mdx` | Features in development |
| `concepts/overview.mdx` | Workspaces, projects, opportunities, awards, connections, and datasets |
| `guides/overview.mdx` | Index of guides |
| `guides/create-a-project.mdx` | Create a project or program in the web app or the CLI |
| `guides/match-opportunities.mdx` | Read stored opportunity matches |
| `interfaces/web-app.mdx` | Day-to-day work in the web app |
| `interfaces/cli.mdx` | CLI reference |
| `interfaces/mcp.mdx` | MCP (not yet available) |

## Local preview

Requires Node.js 20.17+.

```bash
npm i -g mint
mint dev
```

Preview at `http://localhost:3000`. Run `mint validate` before pushing.

## Publishing

Pushes to `main` deploy automatically via the Mintlify GitHub App. No separate Fly or CI deploy is required.

## Custom domain

`docs.tryulysses.com` is configured in Mintlify. DNS on Namecheap:

1. Verification **TXT** records (from the Mintlify custom-domain UI)
2. After both show verified: **CNAME** `docs` → `cname.mintlify.builders`

## AI tooling

- Install Mintlify’s writing skill: `npx skills add https://mintlify.com/docs`
- Admin MCP (edits / settings): `https://mcp.mintlify.com`
- Published docs expose `/llms.txt` for agents

Internal eng runbooks stay in `grand-harbor` — do not sync those here.
