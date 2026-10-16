# Lab 2.5 Self-archiving and defensible timestamping

| Duration | Type | Running case | Assessed |
| --- | --- | --- | --- |
| 15 minutes | Individual | No | No |

## Aim

Capture a dynamic page with infinite scroll, produce a defensible archived copy with a hash and timestamp, and document the method well enough for someone else to repeat it.

## Outcome

An **archived artefact** (screenshot, saved page and hash file) with an **integrity record**.

## The analogy: the photo with today's newspaper

Hostage photos used to hold up that day's newspaper to prove when they were taken. Your capture needs the same: a way for a stranger to believe this was taken at this time, from this page, and not edited since.

## What you need to do

- [ ] Open the sandbox feed page that loads more content as you scroll
- [ ] Scroll to the depth stated in the brief
- [ ] Capture a full-page screenshot and a saved copy of the page
- [ ] Hash both files and record the time, URL and method
- [ ] Write the integrity record

**Deliverable:** `selfarchive/` folder with `.png`, `.html`, `.sha256` and `method.md`.

## What the instructor sets up beforehand

- A sandbox page with infinite scroll and an expandable section (the "interactive content")
- The target depth (for example, the 40th item) in the brief
- A reliable time source shown on the room screen

## Before you start

- Read [S2 Web archiving and persistence](../sessions/s2-web-archiving.md), self-archiving and dynamic content sections.
- **Tools:** Firefox `case-running` with Hunchly; terminal.

## Rules for this lab

- Use only the sandbox page.
- Record exactly what you did, including what you clicked.

## Steps

### Step 1: Prepare (2 min)

1. Make a folder: `mkdir -p ~/cases/CASE-2026-001-running/03-evidence/selfarchive`
2. Note the current time in SGT and UTC from the room clock and from `date -u` in the terminal.

### Step 2: Load the full content (4 min)

1. Open the sandbox page. Dismiss the consent banner and note that you did.
2. Scroll until the 40th item has loaded. Expand any collapsed sections.
3. Count the items visible so you can state it in your record.

### Step 3: Capture (4 min)

1. In Firefox press Ctrl + Shift + S and choose **Save full page** to create a PNG.
2. Press Ctrl + S and save the page as **Web Page, complete** (`.html`).
3. Confirm Hunchly recorded the page as well.

### Step 4: Hash and record (5 min)

```bash
cd ~/cases/CASE-2026-001-running/03-evidence/selfarchive
sha256sum *.png *.html | tee capture.sha256
date -u +"%Y-%m-%dT%H:%M:%SZ" >> method.md
```

Open `method.md` and write: URL, time (SGT and UTC), browser and version, profile, steps you took (consent banner dismissed, scrolled to item 40, expanded section X), number of items visible, file names, and the hash values.

## Worked example

```markdown
URL: https://sandbox.example/feed
Captured: 2026-11-04 10:12 SGT (02:12 UTC)
Browser: Firefox 1xx, profile case-running
Steps: dismissed cookie banner; scrolled to item 40; expanded "Show replies" on item 3
Visible items: 40
Files: feed-full.png, feed.html
SHA-256: <value>
```

## Common mistakes

- Capturing before the content loads, so only the first screen is saved.
- Leaving out the time zone.
- Editing the saved file afterwards, which invalidates the hash.

## If you finish early

Repeat the capture 10 minutes later and compare the two hashes. Explain in two lines why they differ even when the visible content looks the same.

## Summary

A defensible capture records the page, the method, the time and the integrity of the files. Anyone should be able to repeat what you did and check the hashes match.

## Carries forward

- Every important live capture from now on follows this pattern.
- Lab 2.8 asks for a method note on each item you verify.
