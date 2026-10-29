# Working on the BrokerBroker help site

This repository is the user-facing help centre at **help.brokerbroker.app**. It is
a [Mintlify](https://mintlify.com) project: MDX pages with YAML frontmatter,
configured by `docs.json`. Mintlify builds and deploys it — there is no CI here
and no build step of ours.

**A push to `main` publishes.** There is no staging copy of this site. Treat every
commit as going live.

## Who reads this

Estate agents, not engineers. Many arrive from a link in the app, on a phone,
between viewings. Write for someone who has two minutes.

- Say what to do, in order, before explaining why.
- One page answers one question.
- Prefer the word a broker would use over the word the codebase uses.

## Terminology

Match what the pages already say. These were counted across the site, not
guessed — using the wrong one makes the docs read as though they describe
different software.

| Use | Never |
|---|---|
| **Groups** | Circles. The product renamed them; `circles.mdx` mentions the old name once, only to explain stale links |
| **your public card**, **your card** | Broker Card — it appears nowhere on this site |
| **BrokerBuddy** | the assistant, the bot, the AI |
| **Opportunities** | leads, prospects |
| **Matches** | suggestions, recommendations |
| **Vouches** | reviews, ratings, testimonials |
| **Deals** | transactions |
| **Buddy Score** | rating, score |
| **co-broke** | split deal, shared deal |
| **Buyer Finder Split Fee**, capitalised as a name | sub-agent fee, co-broke fee. The glossary keeps the old name once, so a broker who learned it can find the new one |

If you introduce a term that is not here, check how the app labels it first.

## Style

- Active voice, second person: "you".
- One idea per sentence.
- Sentence case for headings.
- Bold for UI elements: click **Settings**.
- Code formatting for file names, commands and paths.

## Language

Everything here is English — pages, headings, file names, alt text, commit
messages. That is the platform-wide convention, not a choice about this repo.

## Never publish

- Ticket codes, `linear.app` links, Sentry issue ids, or any internal tracker
  shorthand. A broker cannot decode them and they date the page instantly.
- Real broker or client names, addresses, phone numbers or emails. Redact
  screenshots before they land here — the data behind this product is personal
  data under UK GDPR and UAE PDPL.
- Internal URLs or anything under `admin.brokerbroker.app`.
- Fee percentages or commission figures unless the product itself shows them.
  They change, and a stale number in a help centre reads as a promise.

## Before committing

- `mint dev` renders locally; `mint validate` catches broken navigation, bad
  frontmatter and dead links.
- A page added to the repository but missing from `navigation` in `docs.json` is
  invisible. Adding the file is half the job.
- Check it on a narrow viewport. Most readers are on a phone.
