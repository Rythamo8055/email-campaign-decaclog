# DEVLOG — email-campaign-decaclog

> Living log of every decision & conversation summary with timestamps.  
> **Repo:** https://github.com/Rythamo8055/email-campaign-decaclog  
> **Rule requested by user (2026-08-25):** From now on + retroactively, every decision/summary gets logged here with timestamps (UTC + IST). Single source of truth beside `DECALOG.md`.

## Format
```
[UTC] | [IST] | Decision | Summary | Files | Commit
```

---

### 2026-08-25 — Initial Build

#### [2026-08-25T14:27:36Z] — 19:57 IST — Decision: Create repo `email-campaign-decaclog`
- **Conversation summary:** User provided 3 YouTube transcripts (1) I tried every FREE email tool `U81KcSh96SY`, (2) I Sent 1B Emails `WKxqjIE2vto`, (3) 7h Cold Email Course `DDGcd1JoJV0` + asked to extract main points as bullet points in single file and push via `gh` to GitHub under `/1st mail campain`.
- **Decision:** Create new public repo via `gh repo create email-campaign-decaclog --public --description "Decalog + Campaign Bible..."`.
- **Outcome:** Repo created at https://github.com/Rythamo8055/email-campaign-decaclog (clone_url same). Verified with `gh repo view`.
- **Files:** (repo init, no files yet)
- **Commit:** — (gh create)

#### [2026-08-25T14:29:00Z] — 19:59 IST — Decision: Write single-file bible `DECALOG.md:1`
- **Conversation summary:** Synthesize all 3 long transcripts into one bullet-only file usable as campaign playbook (warm newsletter + cold outbound + deliverability).
- **Decision:** Create `DECALOG.md` with 6 sections: §0 HowToUse, §1 Free Tools (40→17→8 + 8 tool ratings), §2 1B Emails 7 Lessons, §3 Cold Masterclass 3 Pillars + full technical/list/offer/copy/analytics/managing/scaling/Clay/signals/reply/omnichannel/future, §4 Decalog 10 Commandments + checklist, §5 copy templates, §6 resources. Chose bullet hierarchy, kept affiliate/resource links, kept file under 50KB for portability.
- **Outcome:** File written, 547 lines, 44344 bytes. Verified with `wc -l` + `ls -lh`.
- **Files:** `DECALOG.md:1`
- **Commit:** `22dc206` — `feat: decalog + main-tail single-file bible from 3 transcripts...`

#### [2026-08-25T14:33:37Z] — 20:03 IST — Decision: Start maintaining DEVLOG.md (this file)
- **Conversation summary:** User clarified: “now from now on and also before we need to make a devlog also like you need to update that when we make any decission of summary of our conversation with time stamps”.
- **Decision:** Create `DEVLOG.md:1` as living log, retroactively document prior decisions (repo creation + DECALOG write) with UTC/IST timestamps derived from `git log --date=iso` (2026-08-25T14:27:36Z) and `date -u`. Define format, auto-update rule for future. Push to same repo.
- **Outcome:** This file created. Next pushes will append new entries.
- **Files:** `DEVLOG.md:1` (new), `DECALOG.md:1` (unchanged)
- **Commit:** `ddc7f0a` — `feat: add DEVLOG with retroactive + live timestamped decision log`

---

## How logging works going forward
- Every assistant turn that makes a decision (new file, edit, repo/gh action, summary) → append new row here BEFORE `git push`.
- Timestamp source: `date -u +"%Y-%m-%dT%H:%M:%SZ"` and IST (`date`).
- Keep reverse chronological or chronological (chosen: chronological with newest at bottom).
- No deletion of old rows — append-only.

## Pending
- [ ] Add GitHub Action to enforce DEVLOG update on each push (optional)
- [ ] Mirror DEVLOG to `docs/DEVLOG.md` if repo grows beyond single file

---
*Last updated: 2026-08-25T14:33:37Z — commit ddc7f0a*
