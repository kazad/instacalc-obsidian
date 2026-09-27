# Instacalc for Obsidian (beta)

Calculations, units, charts and LaTeX that compute, right in your notes.
Write `rent = $1,850/month` on one line and `rent * 12` on the next; the
answers appear beside what you typed and update as you edit.

[![A one-minute tour: a trip budget that computes, drag-to-explore, goal seek, charts, LaTeX that evaluates, and stateless share links](media/tour.gif)](media/tour.mp4)

*One-minute tour ([full-quality video](media/tour.mp4)).*

- Natural-language math: percentages, units, currencies, dates
- Variables that flow across a note's calculation blocks
- Charts and plots from the numbers you already wrote
- `$$ ... $$` LaTeX blocks that evaluate, not just render

This repository holds the plugin's **release builds and install notes only**.
It is where testers install from; development happens elsewhere.

## Install with BRAT (recommended)

BRAT (Beta Reviewers Auto-update Tester) installs the beta and keeps it up to
date automatically.

1. In Obsidian, open **Settings > Community plugins**. If the vault is in
   Restricted Mode, turn it off.
2. Click **Browse**, search for **BRAT**, install it and enable it.
3. Open **Settings > BRAT** and click **Add beta plugin**.
4. Paste `kazad/instacalc-obsidian` and click **Add plugin**.
5. Back in **Settings > Community plugins**, enable **Instacalc**.

BRAT checks for new versions when Obsidian starts (and on demand from its
settings), so you will get each new beta without doing anything.

## Manual install (fallback)

1. Open the [latest release](https://github.com/kazad/instacalc-obsidian/releases)
   and download `main.js`, `manifest.json` and `styles.css`.
2. Put them in `<your vault>/.obsidian/plugins/instacalc/` (create the folder
   if it does not exist; `.obsidian` is hidden in most file browsers).
3. Restart Obsidian, or reload plugins, then enable **Instacalc** in
   **Settings > Community plugins**.

Each release also carries a zip with the same three files in an `instacalc/`
folder, which you can unzip straight into `.obsidian/plugins/`.

A manual install does not update itself; repeat these steps for a new version.

## Sending feedback

From inside a note, open the Instacalc toolbar's **"..."** menu and choose
**Send feedback**. It goes straight to the Instacalc team, and that is the
fastest way to report a wrong answer, a rendering glitch or an idea.

To ask a question, share a note, or discuss an idea in the open, use
[Instacalc Discussions on GitHub](https://github.com/kazad/instacalc/discussions), the community for Instacalc on the web and in Obsidian.

## Requirements

Obsidian 1.4.0 or newer, desktop or mobile.
