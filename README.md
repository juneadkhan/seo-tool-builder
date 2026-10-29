# SEO Tool Builder

**Give your coding agent a workflow for building useful free tools people can find through search.**

One Markdown skill, with a fictional worked example. It helps an agent research an opportunity, build a working calculator, converter or generator in your existing website, and decide which additional pages deserve to exist.

Adapted from the workflow I use to build free tools for my own product. This is a general-purpose extraction of that process, not a private application or a promise of the same growth.

## Install

Run inside the website repository you want to work on:

```sh
npx skills add juneadkhan/seo-tool-builder --agent claude-code --yes
```

For Codex, replace `claude-code` with `codex`. The Skills CLI requires Node/npm; the skill itself has no executable dependencies, API key or hosted backend. Installation adds the skill, not tool pages or analytics integrations. Your agent's existing tools, permissions, model access and usage limits still apply.

## Try it

Give your agent this prompt:

```text
Use seo-tool-builder in this repository. My product is [what it does] for
[who uses it]. Find useful free-tool opportunities connected to that audience.
Check current search results if you can and distinguish observed evidence from
guesses. Recommend one small first tool and an expansion plan. Do not edit files yet.
```

Then ask it to build your chosen tool. If you already know what to build:

```text
Use seo-tool-builder to build [tool] in this website using its existing stack
and design. Include a worked example, input validation, useful page content,
metadata and internal links. Check the calculation and mobile layout. Keep it
local and tell me what remains unverified before publishing.
```

Prefer a link to hand your agent? Use [the copy-paste setup prompt](SETUP-PROMPT.md).

## What you get

- A shortlist grounded in product fit, observed search evidence and build/upkeep cost.
- A functioning tool and useful explanation, with verified units and examples.
- Integration with the site's routing, metadata, links and sitemap conventions.
- An expansion plan based on distinct tasks and outputs, rather than a target page count.
- A record of the checks actually run and the limits of the available evidence.

Search Console and paid keyword services are optional. Public search research can provide qualitative evidence; the skill tells the agent to mark unavailable search volume, difficulty and analytics as unknown. Without web access, it labels opportunity ideas as hypotheses. Building a tool does not establish demand or guarantee indexing.

## Read it before using it

[SKILL.md](SKILL.md) is the complete workflow. [The example](references/worked-example.md) shows how a fictional file-transfer business might choose and validate an upload-time estimator. There is no embedded scraper, analytics connector or auto-publisher. The skill does not change an agent's permissions or confine its tools.

The software is free and MIT licensed. Model usage, browsing tools and any services you choose have their own costs. No account credentials or private code from the author's product are included or required.

## Validation

See [VALIDATION.md](VALIDATION.md) for the install and behavioral checks actually performed. These checks test packaging and a small local example, not search ranking or growth. The source post's business results are not a controlled evaluation of this extracted skill.
