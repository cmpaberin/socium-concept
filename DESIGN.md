# Socium — design system

Pre-contract mockup for **Socium** (socium.team). Vertical: B2B tech staffing / offshore
delivery. Built 2026-09-08 by LocalEnhance for the Thursday 10 Sep scoping call with
Thomas Chapman (Managing Director and co-owner) and Grace Zulueta (Client Partner).

Everything below is measured off their own live assets. Nothing is invented.

## Where the direction came from

Their brand mark is a network polyhedron in an orange-to-amber gradient
(`assets/mark.png`, pulled from their site icon). Their homepage hero is a dark circuit-board
render lit in the same orange (`assets/tech-specialists.jpg`), and their section bands use a
near-black hexagon honeycomb with orange glow (`assets/mark-hex.png`). The wordmark sets
"Socium" in a bold transitional serif over "Teams Done Differently", wide-tracked.

So the palette is not a judgement call: white page, near-black photographic bands, one orange.

## Tokens

| Token | Value | Source |
|---|---|---|
| `--bg` | `#FFFFFF` | their page ground |
| `--surface` | `#F5F5F5` | measured, `#f6f6f6` in their stylesheet |
| `--ink` | `#2D2D2D` | measured, their body and heading colour |
| `--brand` | `#FD6F06` | measured, 43 occurrences on the homepage |
| `--dark` | `#0A0A0A` | measured, their hero and band ground |

Five colours. `#ED8727` appears only inside the mark's gradient, never as a flat fill.

**Deviation, deliberate:** their own buttons put white text on `#FD6F06`, which measures about
3:1 and fails WCAG AA. Buttons here use `#2D2D2D` on the orange instead, about 7:1. Worth
raising on the call, because accessibility appears in enterprise vendor questionnaires.

## Type

Montserrat (display and UI) + Roboto (body). Both are already loaded on socium.team, so this
is their stack, not a substitution. PT Serif Bold appears in exactly one place, the wordmark
lockup, to reproduce the serif in their logo. That is a logo reproduction, not a third type role.

Nav is Montserrat 600 uppercase at `0.08em`, matching their header.

## Spacing

4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 96 / 128. No in-betweens.

## Motion budget

- Scroll-reveal fade-up, 90ms stagger, on every section.
- Exactly ONE ambient element: a slow orange glow drift behind the hero chip. Nothing else
  moves on its own.
- Hover: image `scale(1.04)`, card lift `-6px`.
- Count-up on the trust strip, once on first viewport entry.
- All gated behind `prefers-reduced-motion`.

Signature feature stack, decided explicitly rather than defaulted:

- **Higgsfield motion** — yes for the paid build, no for this mockup. Their circuit render is
  lit for it and a 4 second cinemagraph of the board would carry the hero. About $0.10. Held
  back so a mockup does not spend budget before the deal.
- **Scroll-cinema** — no. It needs one hero object on a clean ground. Their asset library is
  renders and rooms, not a single product.
- **AI concierge** — yes, propose it. Two real jobs to do: answer buyer questions about the four
  engagement models and cost bands, and answer candidate questions about open roles. Rule-based
  tier is free and reads from the same content.

## Imagery rules

Their own assets only. Dark circuit renders, hexagon textures, their real team photographs,
their real service icons. No stock, no AI illustration, no generic office handshakes.

## Fact ledger

One row per claim that appears on the page.

| Claim on page | Source |
|---|---|
| London, Dubai, Manila | socium.team, offices listed site-wide |
| Four NEO, 4th Avenue, BGC, Taguig, Metro Manila | Socium Staffing Solutions Inc., Bossjob company profile |
| 51 to 100 staff in the Philippines | Bossjob company profile |
| 100 to 200 staff group-wide, HQ London, 8 years | LinkedIn company page |
| 28 named staff across Perm, TaaS, RPO, enterprise support | socium.team/philippines-team/ |
| Four service lines and their descriptions | socium.team/1-solutions-new-2025/ |
| TaaS 50 to 60% cost saving | socium.team, TaaS description |
| 61% / 79% / 68% market statistics | socium.team, their own solutions page |
| 90% retained client base | socium.team, their own graphic `90-Retained-Client-Base.png` |
| Client names: Aveva, Virgin, Intuit, Medtronic, bolttech, TravelPerk, Preqin, King, Adevinta, AltoVita, Noah, Onto, Oliva, GPI | socium.team/clients/ and their nine case-study pages |
| Great Place To Work certified, Philippines | greatplacetowork.com.ph/companies/socium/ |
| Java Developer, PHP 100,000 to 200,000 per month, hybrid Taguig, 5 to 10 years | Bossjob live listing |
| Backend Developer, PHP 90,000 to 150,000 per month, hybrid Makati, 5 to 10 years | Bossjob live listing |
| Thomas Chapman, Managing Director, Permanent and APAC | LinkedIn |
| Named team members and titles | socium.team/philippines-team/ |

Four job rows are marked **Example listing** in the interface and in their description text.
They are layout demonstrations, not Socium vacancies. Only the two Bossjob roles are marked live.

## Pre-contract gate

Applied per `references/pre-contract-preview.md`:

- Fixed confidentiality chip, bottom-left, naming Socium and the build date.
- `<meta name="robots" content="noindex, nofollow">` in the head.
- `robots.txt` blanket disallow on the host.
- Repo README states plainly that this is unofficial and unaffiliated.

Comes off when a contract is signed, at which point the production gates in `acceptance.md`
apply instead, including a real indexing decision.
