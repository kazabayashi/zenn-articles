# AGENTS.md — zenn-articles

This repository stores Zenn articles for the `@carapace` account.

## Standard Article Flow

1. Create new articles under `articles/<slug>.md`.
2. The slug must use only `a-z`, `0-9`, `-`, and `_`, and must be 12 to 50 characters long.
3. Every article must include Zenn frontmatter:
   - `title`
   - `emoji`
   - `type: "tech"`
   - `topics`
   - `published`
4. New drafts must always start with `published: false`.
5. Pushing `published: false` sends the article to Zenn as a draft. The human reviews it in preview.
6. Only after the human explicitly approves publication may `published: true` be used.
7. Codex must not switch an article to `published: true` on its own. Final publication is always a human decision.

## Content Rules

- Do not include private product names, company names, industry details, personal information, or internal identifiers.
- Do not mention Stayble.
- The maker may be described only as "日本の一経営者であり、一クリエイター".
- Do not describe the maker as "non-engineer" or say that the product was "made with AI".
- When an article includes current AI industry facts, dates, numbers, model names, regulations, or company actions, prompt the human to verify that the facts are still current before pushing.
- Do not add unverified numbers, dates, names, or claims.

## Operating Principle

Codex prepares drafts. The human reviews, approves, and publishes.
