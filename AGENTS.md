# Repository Guidelines

## Project Structure & Module Organization
This repository backs Tony Siu's GitHub profile page, so the rendered content comes directly from `README.md`. Keep hero sections, trophy embeds, and badge blocks in that file, using GitHub-flavored Markdown with inline HTML only when layout demands it. `CLAUDE.md` offers assistant notes and `.qodo/` stores AI tooling config; update them only when workflows change. There are no compiled assets—image badges load from external CDNs—so review link health whenever you touch the markup.

## Build, Test, and Development Commands
Use lightweight tooling to lint and preview documentation changes. Run `bunx markdownlint-cli2 README.md AGENTS.md` before opening a pull request to enforce the shared Markdown rules in `~/.codex-os/standards`. For a quick visual check, open a local preview with `glow README.md` or run `gh repo view --web` to confirm GitHub renders all badges correctly. No build step is required.

## Coding Style & Naming Conventions
Follow the global Markdown style: one `#` title per file, ATX headings, blank lines between sections, and manual wrapping around 100 characters. Keep badge URLs and icon alt text consistent (`alt="Python"`, etc.) so screen readers interpret the page. When embedding HTML tables, align indentation with two spaces and document any unusual elements with terse comments like `<!-- Stats cards -->`.

## Testing Guidelines
Automated coverage is not applicable, but every change should ship with lint output and a human preview. Run `bunx markdownlint-cli2` until the exit code is zero, then spot-check external assets with `curl -I <url>` to ensure HTTP 200 responses. Confirm that GitHub light and dark themes display legible colors; adjust `theme` query parameters when contrast drops below WCAG AA.

## Commit & Pull Request Guidelines
Use Conventional Commits with a docs scope, e.g., `docs(profile): refresh hero badges`. PRs must include before/after screenshots or preview links, note any new external services, and mention affected sections (`Header`, `Stats`, etc.). Link related tasks or issues, and call out outbound assets so reviewers can validate them quickly. Merge only after linting passes and reviewers confirm the visual diff.

## Security & Configuration Tips
Never embed secrets or personally identifiable data; tokens for external widgets must stay in environment variables or private backends, not the README. Prefer HTTPS sources and reputable CDNs to avoid mixed-content warnings. If a third-party badge introduces tracking or aggressive rate limiting, document the rationale in `product/decisions.md` and provide a fallback image to keep the profile resilient.
