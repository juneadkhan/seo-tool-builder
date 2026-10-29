# Validation

Checked October 29, 2026. These checks establish a small packaging and behavioral smoke test, not a ranking or traffic result.

## Skill and installation

- Skill-creator validation passed for the name, frontmatter and instruction file.
- Fresh project-local Skills CLI installations from both the local candidate and the published GitHub repository succeeded for Claude Code and Codex; all six installed source files matched and their bundled Markdown links resolved.
- Anonymous HTTP requests to the public repository and pinned skill/setup source succeeded without authentication; source bytes matched the reviewed commit.
- Bundled Markdown reference links resolved. Current Google primary documentation was checked for helpful content, canonical URLs, sitemap dates, structured data and scaled-content guidance.
- The source was manually reviewed and scanned for private identifiers and common secret formats; no private application code, analytics exports, credentials or machine paths were included. Pattern checks are not a guarantee against every possible sensitive value.

## Independent use on another product

An independent Codex agent received this skill, a fictional garden-planning website and a request to build a mulch-volume calculator plus an expansion recommendation. It had no original product code, keyword account or analytics export. Read-only public research was permitted.

It built a working calculator in the fixture's existing stack, sourced its methodology, integrated the page with navigation, metadata and sitemap, and marked unavailable demand and conversion metrics as unknown. It recommended retaining a single mulch page and investigating a genuinely different soil-fill task, rather than generating 300 city-name variants with the same answer.

All **12 fixture checks passed**, including live local HTTP checks. They cover independent normal examples, top-up geometry, units, allowance, whole-bag rounding, zero/invalid/oversized inputs, tiny positive volumes, initial HTML content, metadata, internal links and sitemap inclusion. Initial arithmetic/checker failures were corrected before the final pass; this is not a perfect-first-attempt claim.

A separate browser pass exercised the result at desktop and phone widths, confirmed top-up arithmetic, hid stale results after an edit, and checked invalid-input feedback and focus. Viewport screenshots at 1280×900 and 390×844 were inspected; no horizontal overflow was observed.

The fixture is a disposable local evaluation project, not an application bundled with the skill. The public worked example uses a different fictional file-transfer product to explain the general workflow. Neither is a measured search-growth case study.

## Not established

A separate live Claude Code behavioral run, production deployment/indexing, real-device and assistive-technology testing, search-volume accuracy, conversion lift and rankings are not established by this local check. There were no paid API calls, analytics-account changes, deployments or social publications. Model use and capabilities depend on the reader's existing agent and services.
