---
name: competitor-analysis
description: >-
  Compare how other products handle a flow or screen. Use when the user asks
  how competitors do this, how other apps do this flow or screen, let's see
  other competitors, compare this screen, competitor flow, competitor screen,
  or wants a competitive analysis of a UI flow. Collect public screens, write
  highlights per competitor, and lay the screens on a local Twombly canvas.
---

# Competitor analysis

Collect public screens for one flow, note what stands out for each competitor, and place the images on a local Twombly canvas.

Do not start Mobbin, store lookups, or the canvas until the user has confirmed the choice list in section 1. A request that answers some questions is not that confirmation.

## 1. Ask, then confirm

One short round. Ask only what the message left open. Skip a question already answered. Then stop and show the choice list. Wait for an explicit yes before collecting. Do not treat "proceed" as covering a choice you have not written down.

Ask, in this order:

1. **Pattern or comparison.** Examples of a pattern, or a comparison against a product they ship? If they name no product, do not block on a name. Ask the category and the job instead: shopper checkout, subscription paywall, account billing, or whatever fits.
2. **What counts.** Where the pattern starts and stops. Spell out the close calls: one page with several sections, a page that numbers two steps on the same screen, express pay alone (Apple Pay, Shop Pay), a checkout builder, an admin screen. Ask which of those are in.
3. **What to exclude.** A rule, not a vibe. Name the platforms, payment hosts, and screen types to skip. "Not Shopify" means Shopify-hosted checkout and Shop Pay, including brands that are not Shopify themselves. Login-walled captures are always out.
4. **Who is in the flow.** Guest, or a returning customer with a saved address and card? Say which, because one-step pages often exist only for the saved-payment case.
5. **Surfaces when they disagree.** If iOS is one sheet and the website is a wizard, include only the matching surface, or show both and label the mismatch? Ask this instead of assuming web and mobile whenever both exist.
6. **How much of the flow.** Entry (product, cart, or plan), the pay screen, and confirmation, or only the pay screen? That choice sets the canvas rows.
7. **Region and age.** Which storefront, and whether an older public capture is fine. Skip this only when they already said any public example is enough.

**Competitors.** If they are comparing a product they ship and name no rivals, propose 4 to 6 and wait. If they asked for examples of a pattern and named no rivals, do not wait on a list. Pick 4 to 6 that match the rules above, put those names in the choice list, and wait for the yes on that list.

**Confirm before every run.** After the answers, send one recap of every choice you are about to use, including defaults you filled in. Cover the job, what counts, exclusions, guest or saved payment, surfaces, how much of the flow, region and age, and the product list. Wait for the user to confirm or correct it. If they correct one line, update the list and confirm again. Only then collect.

## 2. Collect screens

Mobbin first. Then public store listings where Mobbin is thin. Then the competitor's public site when the flow is on the web or the other sources do not show it. Save image files. Do not invent screens, describe a screen you did not retrieve, or capture anything behind a login.

### Mobbin

Search Mobbin for the flow on the chosen platform and save the matching production screens for each confirmed competitor.

If the Mobbin tools are not authenticated, stop. Authenticate Mobbin and wait. Do not fill the gap with guessed screenshots.

### App Store and Google Play

Use public listing screenshots only when Mobbin has little or nothing for that competitor and that flow. Match the same flow. Skip login-walled or paywalled captures.

### Public sites

When the flow is on the web, or Mobbin and the store listings do not show it, open the competitor's public site and capture the matching pages. Marketing pages, docs, and logged-out product pages count. Skip anything behind a login. Save still images of the relevant screens, not a crawl of the whole site.

Say which competitor was skipped and why.

If a screen forces a new call during the run, stop and confirm it before continuing. That includes dropping a product because the flow is multi-step, swapping in a replacement, keeping only one platform when web and mobile disagree, or treating a numbered single page as in or out. Add the change to the choice list and wait for a yes. Do not quietly revise the set.

## 3. Highlights

For each competitor, write 3 to 5 notes:

- What the screen is doing.
- The pattern: layout, steps, empty state, or paywall.
- One thing that stands out.

Tie the notes to the comparison point from the clarifying round. These notes go on the frame caption and in the chat reply.

## 4. Twombly canvas

Frames are static images only. Add only files that are safe to leave the machine.

Use a local canvas. Do not use the hosted Twombly plugin, `https://twombly.app/mcp`, `open_canvas`, or `add_frames`. Those open the signed-in account. Do not run `twombly login`, `twombly upgrade`, `twombly share`, or `twombly join`. Do not hand the user a `twombly.app` link.

### Open the local canvas

From the project directory, run every command as `npx -y twombly@latest <command>`. Read `npx -y twombly@latest guide` once if the command shape is unclear.

1. `npx -y twombly@latest init --name "<short job name>" --no-open`
2. Open the `local` address from that result beside the chat. That address is on this machine (`localhost`). If the result also has a hosted `link`, ignore it.
3. Add each saved image with `npx -y twombly@latest add <image> --title "<competitor> <screen>" --level image --width <px> --height <px>`. Put one step on each row: the first image of a new step gets `--new-row`. Competitors stay in the same column order on every row.
4. `npx -y twombly@latest show`, then `npx -y twombly@latest done`.

If the local server cannot start, say so and stop. Do not fall back to the hosted account.

### Layout

One canvas. One column per competitor. One row per step in the flow, in the same order for every column.

- Frame title: competitor name plus screen name.
- Caption: that competitor's highlights. Twombly image frames have no caption field, so put the highlights in the chat reply and in the frame title only when a short label fits.

The canvas the user opens is the local address. Do not describe it as a hosted link.

## 5. Reply

Lead with the local canvas address. Then the highlights, grouped by competitor. Name anything skipped. Do not make a slide deck.
