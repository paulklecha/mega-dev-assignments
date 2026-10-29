# S01E03 · what it shows

Re-triage of support ticket **#4471** ("dates parse mm/dd in eu locales"), filed by the desk as
one known bug. Working from the desk's kb export, #4471 actually holds **two** distinct bugs.

## Tickets (GitHub issues in this repo)

- [#1 · parser reads dates month-first — **379 reports**](../../issues/1)
- [#2 · booking-v3 form hint (MM/DD/YYYY) stores wrong date — **33 reports**](../../issues/2)

379 + 33 = **412** unique reports (427 export rows − 15 duplicate ids).

## The page

- Source: `support-kb/src/routes/kb/incidents/4471-two-problems/+page.svx`
  (signed; frontmatter `signature:` and `<RenderStamp {signature} />`, per the kb README).
- As the desk will see it: `rendered/4471-two-problems.html`.

## How the counts were computed

The cause of each report is computed from the tenant's locale and booking form using the kb's
own `support-kb/src/lib/kb/causes.ts`, not from intake's tag (which disagreed on 38 reports).
`support-kb/` is the desk's kb export with the new page added.
