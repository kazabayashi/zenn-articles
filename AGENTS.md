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

## Draft File Rules

- Always save article drafts as `.md` files instead of relying on chat output for copying.
- Use `articles/<slug>.md` for Zenn Japanese drafts.
- Use `dev-articles/<slug>-en.md` for dev.to English drafts unless the human specifies another path.
- Avoid presenting full article bodies only in chat because terminal/browser soft wrapping can introduce unwanted line breaks when copied.

## Cover Image Rules

- Create a cover image / OGP image for future Zenn and dev.to articles when practical.
- Keep the Carapace visual style: dark terminal/code-editor background, quiet green terminal accent, restrained and trustworthy tone.
- Prefer deterministic SVG/HTML/CSS when text accuracy matters. Verify exact spelling of product and company names such as `Carapace` and `Anthropic`.
- Use a wide cover ratio suitable for dev.to and reusable for OGP, approximately `1000x420`.
- Do not make the cover visually noisy; the headline should be short, readable, and aligned with the article's main idea.
- Do not include `cover_image` in dev.to article frontmatter. dev.to accepts only network URLs such as `https://...`; local relative paths such as `/images/example.png` cause a `main_image: is not a valid URL` error.
- For dev.to articles, Codex should still prepare the thumbnail image file (`.png`) for the human, but the human uploads it manually in the dev.to editor with the "Upload Cover Image" button.
- Zenn is different: because Zenn uses GitHub-linked repository assets, Zenn article frontmatter may include an image reference when needed.

## Content Rules

- Do not include private product names, company names, industry details, personal information, or internal identifiers.
- Do not mention Stayble.
- The maker may be described only as "日本の一経営者であり、一クリエイター".
- Do not describe the maker as "non-engineer" or say that the product was "made with AI".
- When an article includes current AI industry facts, dates, numbers, model names, regulations, or company actions, prompt the human to verify that the facts are still current before pushing.
- Do not add unverified numbers, dates, names, or claims.

## Operating Principle

Codex prepares drafts. The human reviews, approves, and publishes.
