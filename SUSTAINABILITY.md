# 🌱 TechCom Desk: what keeps it running

> A.L.E.X. runs this desk. What it takes to keep A.L.E.X. itself running (hosting, tokens, costs, who
> owns it, how to turn it off) is on **[A.L.E.X.'s sustainability page](https://psychedelicsinrecovery.github.io/alex-desk-public/sustainability.html)**,
> and PIR's GitHub pages as a whole are on the **[AstroLog's](https://psychedelicsinrecovery.github.io/changelog-astro-public/sustainability)**.
> This file lists what applies to this desk.

Nothing here costs money. What it takes is a few things that quietly expire or drift, written down
so none of it depends on anyone's memory.

## 🧩 The pieces

| Repository | What it is | How it goes live |
| --- | --- | --- |
| `techcom-desk` (private) | The desk's tickets: problems as Issues, ideas as Discussions, requesters only as scrambled tags. Its `portal/` folder is this desk's public page. | Never public, except `portal/` and the files below |
| [`techcom-desk-public`](https://github.com/psychedelicsinrecovery/techcom-desk-public) (public) | The desk's page on GitHub Pages, with this file, the roadmap and the license | A workflow copies them over on every change |
| `alex-desk` (private) | A.L.E.X., which opens and updates the tickets, and `site/build.py`, which writes this desk's page | See A.L.E.X.'s sustainability page |

## 🛠️ What needs looking after

| What | Why it matters | What to do |
| --- | --- | --- |
| 🔑 **The publishing token** (`PUBLIC_REPO_TOKEN`) | Lets this repository's workflow push its page to `techcom-desk-public`. When it expires, the page quietly stops updating (the workflow skips with a notice). | Renew it (scopes `repo` + `workflow`), update the secret here, and run **Actions → 🌐 Sync public portal** once by hand. |
| 🏭 **The page is generated** | `portal/index.html`, `portal/README.md` and `portal/404.html` are written by `alex-desk/site/build.py --desks ..`. A hand edit here is overwritten the next time it runs. | Change the page in `build.py`, rebuild, and commit `portal/` here. |
| 🖼️ **The share image** (`portal/social-card.jpg`) | It's the card PIR's AstroLog builds at `og/page/techcom-desk.jpg` (its words are in the AstroLog's `src/og/pages.ts`). Chat apps cache link previews for days. | After the card changes, copy it here again, then refresh cached previews (see `psychedelicsinrecovery/.github` → `SOCIAL-PREVIEWS.md`). |
| 🧰 **The header and footer** | They come from PIR's arrival kit on the hub (`psychedelicsinrecovery.github.io/arrival/`), and the design from `alex-desk-public` (`alex.css`). | Nothing to do here when they change. If they look broken, check the hub's `arrival/org.css` first. |
| 🎫 **Tickets reaching the Tech Committee** | A.L.E.X. writes tickets here with its own access; the committee's Discord role and channel are configured on A.L.E.X.'s side. | If tickets stop arriving, see the tokens section of A.L.E.X.'s sustainability page. |
| 🔒 **Privacy** | Tickets stay private in this repository; only the page is public. | Never put a ticket, a name or an email address in `portal/`. |

*Maintained by Christopher W with Alfred (Claude Code). Last reviewed 2026-10-13.*
