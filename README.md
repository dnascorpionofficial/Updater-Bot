# Updater Bot — Changelog

Join Telegram : [Integrity Root Channel](https://telegram.me/integrity_root_channel)

A Telegram bot that watches GitHub projects for new releases and new builds, picks the right file, and posts it to your Telegram channels and groups together with a readable changelog, source, report support, time etc.

---

### v106 — Oct 9, 2026
- The bot now reports whether it is actually working, not just whether it is online. A bot that freezes is noticed and restarted automatically.
- Bring back AI Agents with updated infrastructure
- Migrated keybox code to seperate thread & Hided key code from AI Agents.

`This method isn't worth`
- I will remove either keybox elements or AI Agents from monitoring after some days of testing

### v105 — Oct 4, 2026
- AI Agents flagging the keybox updates that causing bot delays & some internal issues,So Disabled AI Agents.

### v104 — Oct 4, 2026
- Fixed duplicate posts after a slow upload. When an upload takes too long to confirm but the file did reach the channel, the bot now recognizes it right away and does not post it again.
- Fixed the wrong post being matched when two projects have similar names.
- Posts with several files now keep every confirmed file.

### v103 — Oct 1, 2026
- Fixed a release being posted twice when Telegram's confirmation was delayed.
- "Auto Delete Old Post" now removes the old post only after the new one is confirmed.

### v102 — Sep 15, 2026
- Fixed duplicate posts during GitHub outages. Saving now retries automatically, and the bot keeps track of what it has already posted even when saving fails for a while.

### v101 — Sep 15, 2026
- "Auto Delete Old Post" now also removes the old copy of the post in the linked discussion group, not just in the channel.

### v100 — Sep 4, 2026
- Files larger than Telegram's 50MB upload limit are skipped straight away instead of being retried over and over. This fixed repeated restarts caused by oversized files.

### v99 — Aug 26, 2026
- Smarter file picking: files marked "legacy" are now less likely to be chosen over the main build.

### v98 — Aug 26, 2026
- Renaming a repo keeps its history instead of clearning - stale datas.
- Forced checks now fill in missing details for builds that were already posted.

### v97 — Aug 25, 2026
- Build checks are faster and more reliable. Only successful builds are considered, so failed or cancelled builds can no longer push the last good build out of view.

### v96 — Aug 25, 2026
- Fixed the bot sometimes re-checking old builds again and again.

### v95 — Aug 23, 2026
- The changelog page account is now refreshed only when page creation keeps failing (5 failures in a row), instead of on a fixed schedule.

### v94 — Aug 23, 2026
- Every update now gets its own fresh changelog page, so an older post always keeps showing the changelog it was posted with.
- Fixed an older post's changelog changing even when the newer post failed to send.

### v93 — Aug 23, 2026
- Builds that are wrapped in an extra zip file are now found and posted correctly.

### v92 — Aug 23, 2026
- Posted module files are now exactly the same as the original from GitHub, so the checksums match.

### v91 — Aug 22, 2026
- Fixed some projects being fully re-scanned on every check. Unchanged projects are now skipped quickly.
- Improved bug hunting with monitoring AI Agents.

### v90 — Aug 22, 2026
- Added Gemini as the first translation option for non-English changelogs. If it is unavailable, the bot moves on to the next option automatically.
- Translations are checked so that refusals or extra comments never end up in a post.

### v89 — Aug 22, 2026
- The owner now gets a one-time alert when the DeepL translation quota is almost used up.

### v88 — Aug 17, 2026
- Added DeepL as a more reliable translation option for non-English changelogs.

### v87 — Aug 13, 2026
- Fixed stray tags showing up in changelog pages when release notes used collapsible sections.
- Fixed `\n` showing up as text instead of a line break.
- Fixed changelogs sometimes being posted untranslated when the translation services were busy.

### v86 — Aug 11, 2026
- Fewer false "unreachable" alerts when the service is just slow to respond.
- The bot now retries automatically when it cannot connect to Telegram at startup.
- Integrated 7 AI Agents for monitoring.

### v85 — Aug 11, 2026
- More time is allowed for release and build checks, which fixed "timed out" errors while GitHub was slow.

### v84 — Aug 11, 2026
- Refreshed post icons: 📦 before the title, 🔊 for notes, and ℹ️ for README.

### v83 — Aug 11, 2026
- Fixed the same file being posted several times in a row when Telegram's confirmation was lost.
- Larger files now get more time to upload.

### v82 — Aug 8, 2026
- Fixed translated changelogs being cut off in the middle.

### v81 — Aug 8, 2026
- Faster posting with fewer redundant saves.

### v80 — Aug 7, 2026
- Fixed ID numbers (such as security advisory IDs) and usernames being turned into commit links by mistake.

### v79 — Aug 7, 2026
- Builds with nothing usable inside are no longer downloaded again on every check.

### v78 — Aug 7, 2026
- Fixed the first issue number in a list, like (#3, #4, #5), not becoming a link.

### v77 — Aug 3, 2026
- Fixed ordinary words such as "feedback" being partly turned into commit links.

### v76 — Aug 1, 2026
- Fully removing a project now also clears its leftover changelog data.

### v75 — Jul 21, 2026
- Add/Edit Repo instructions now show a tap-to-copy example for the bug-report link, with each step laid out as its own block.

### v74 — Jul 20, 2026
- The bot now notices when GitHub is having problems and waits instead of failing. Admin actions ask for confirmation first.
- The status panel shows the current GitHub status.
- Projects are no longer removed by mistake during a GitHub outage.

### v73 — Jul 14, 2026
- Fixed the same release being posted again and again.

### v72 — Jul 14, 2026
- All Telegram links now use `telegram.me`.

### v71 — Jul 10, 2026
- New **Select Description Method** menu with four options: Telegraph page with description, Telegraph page only, description only, or no description.
- Telegraph pages now keep your links and formatting (bold, italic, underline, strikethrough, code, quotes).
- You can customize the Telegraph link line shown in a post.
- Fixed email addresses being shown as @mentions.

### v70 — Jul 8, 2026
- Admin panel now matches each admin's role, with a simpler layout for normal admins.
- Normal admins can use Default Post Mode for the chats assigned to them.
- Added an approval step with a one-time access code for sends from admins who are not trusted, and a new **Trusted** switch to skip it.
- Fixed bug-report links without `https://` not becoming clickable.
- Repo Manager can now name the platform for "other" bug-report links.
- Notifications with special characters now always arrive.

### v69 — Jul 8, 2026
- Faster, with fewer requests to GitHub.
- New switch to turn post logging on or off.
- Failed Logs now shows only real problems.

### v68 — Jul 6, 2026
- Fewer repeated requests when settings are saved and loaded.

### v67 — Jul 5, 2026
- New bug-report flow when posting: choose the type and add a link.
- Links and usernames you type are cleaned up automatically.
- Posts show a "last updated" note on the changelog page.
- Posts include an install note: "Extract zip to install apk", "Flash in root manager", or "Load via KernelPatch".
- Missing repo details are filled in automatically.

### v66 — Jul 3, 2026
- Fewer unnecessary updates and requests.
- Owner alerts now start earlier, at the second failed check, and a project is removed only after four failed checks.

### v65 — Jul 2, 2026
- Minor update.

### v64 — Jul 1, 2026
- Proper thumbnail handling: transparent images, sizes and file weight are now fixed, so thumbnails show instead of a blank preview.

### v63 — Jul 1, 2026
- Behind-the-scenes cleanup: the code was tidied and old one-time update steps were removed, so the bot runs lighter.

### v62 — Jun 30, 2026
- Fixed reactions landing on the wrong file when two files are posted together.
- Re-run builds on GitHub are now handled correctly.

### v61 — Jun 30, 2026
- Two quick messages from the same admin are now handled in order.
- Fixed "message is not modified" errors.
- Fixed the Add Admin panel closing unexpectedly.

### v60 — Jun 30, 2026
- `/status` now shows the date the bot first launched instead of time since the last restart.

### v59 — Jun 30, 2026
- Fixed leftover prompt messages staying in the chat after a menu expired.

### v58 — Jun 29, 2026
- Pull-request builds now show the pull request title in the summary.

### v57 — Jun 29, 2026
- Menus left unfinished for 10 days are now cleaned up automatically.

### v56 — Jun 28, 2026
- Relative links in release notes now point to the right place.
- Better protection against reposting everything when GitHub is temporarily unreachable.
- Very short file names are now padded so they are easier to identify.

### v55 — Jun 28, 2026
- Boost/Cheer buttons now vary in style and message.
- A problem with the share button no longer stops a post from going out.

### v54 — Jun 26, 2026
- New **Custom Post Mode** to send your own message, with photo and formatting, that is not tied to a release.
- Admin panel reorganized into clear sections.
- Every step now has a Cancel button.
- Richer chat status reports.

### v53 — Jun 25, 2026
- Fixed unfinished builds being picked before finished ones.

### v52 — Jun 25, 2026
- GitHub usage and remaining limit are now shown in the status panel.
- Saving is safer when more than one bot instance is running.

### v51 — Jun 24, 2026
- Fixed posts from admins with "Sign Messages" turned on being missed.
- Fixed starting one flow wiping another in-progress flow.
- New repos get auto-clean settings right away.
- History is kept when a project switches between releases and builds.

### v50 — Jun 23, 2026
- Added BOOST and DONATE buttons to every post, plus several footer styles.
- New panel showing which projects currently have no usable build.
- Editing a project's link no longer breaks its post history.

### v49 — Jun 20, 2026
- More reliable translation, with better language detection (Arabic, Thai, Chinese) and support for long lines.
- Zip files that contain a module inside are now opened and handled.

### v48 — Jun 11, 2026
- Changelogs written in other languages are now translated to English automatically.

### v47 — Jun 10, 2026
- Auto-reactions: the bot adds a reaction to its post.

### v46 — Jun 8, 2026
- More reliable changelog pages, with nothing recreated when there is nothing new.

### v45 — Jun 5, 2026
- Small formatting fix for changelog pages.

### v44 — Jun 5, 2026
- Changelogs now open as a clean Telegraph page, with links, bold text, code, lists, issue numbers and commit links.

### v43 — May 8, 2026
- Messages that cannot be deleted are now handled by a helper account that retries up to 3 times.

### v42 — May 8, 2026
- New `/setthumb` command to set the thumbnail.

### v41 — May 8, 2026
- Posts with several files are now tracked correctly.
- Owner alerts now say whether a delete failed or the message was too old to delete.

### v40 — Apr 24, 2026
- Minor update.

### v39 — Mar 29, 2026
- Fixed removing a project from one chat removing it from every chat.

### v38 — Mar 22, 2026
- Owner alerts now include a clickable link to the message.

### v37 — Mar 10, 2026
- Small tweaks.

### v36 — Mar 9, 2026
- Small tweaks.

### v35 — Mar 7, 2026
- File picking simplified into the single name-based ranking introduced in v33.

### v34 — Mar 6, 2026
- The version number is now read from the file name when the tag has none.

### v33 — Mar 5, 2026
- Smarter file picking based on the file name (release, stable and so on rank higher, debug lower).
- Alerts for builds with no usable file are sent only once.

### v32 — Feb 10, 2026
- Telegram sending problems are now sorted into clear types (temporary network issues, rate limits, permission problems, and serious errors), so each one is handled properly.

### v31 — Feb 10, 2026
- Broken projects are removed automatically after repeated failures, with owner alerts.

### v30 — Feb 10, 2026
- Files already posted are no longer downloaded again.

### v29 — Feb 9, 2026
- Small follow-up improvements to the v28 error handling.

### v28 — Feb 9, 2026
- Failed downloads and sends are handled better: temporary problems retry, permanent ones stop.

### v27 — Feb 4, 2026
- Fixed duplicate scheduled checks.

### v26 — Feb 4, 2026
- Changing the check interval now takes effect immediately.

### v25 — Feb 3, 2026
- Follow-up improvements to the v24 update.

### v24 — Feb 3, 2026
- APK files are sent inside a zip so Telegram shows the thumbnail.
- Older chats are updated automatically with the newer settings.

### v23 — Feb 1, 2026
- Minor improvements.

### v22 — Feb 1, 2026
- Fixed display of the auto clean and deleter status.

### v21 — Jan 31, 2026
- Fixed the scheduler starting twice.

### v20 — Jan 31, 2026
- New **Schedule Settings** menu to change how often releases and builds are checked.

### v19 — Jan 31, 2026
- A stuck check can no longer crash the bot, and checks now reschedule themselves.

### v18 — Jan 31, 2026
- Added GitHub API settings and a stricter date format.

### v17 — Jan 30, 2026
- Small cleanup.

### v16 — Jan 30, 2026
- Status now shows how long ago the last check ran and when the next one is due.

### v15 — Jan 30, 2026
- Cleaner Direct Send prompts, and a flow can now be cancelled at any step.

### v14 — Jan 29, 2026
- New **Direct Send**: upload a file, rename it, pick the chats, and send.

### v13 — Jan 29, 2026
- Minor behind-the-scenes update.

### v12 — Jan 29, 2026
- Shows a "please wait" message while the bot is busy.

### v11 — Jan 29, 2026
- Added the Add Admin flow.

### v10 — Jan 29, 2026
- Fixed repo lists showing projects that are not assigned to the chat.

### v9 — Jan 29, 2026
- Repo lists are now sorted alphabetically and split into pages.

### v8 — Jan 29, 2026
- New Auto Clean on/off buttons per project.
- Long status messages are split up and removed automatically.

### v7 — Jan 28, 2026
- The new post is sent first, and the old one is deleted only after that succeeds.

### v6 — Jan 28, 2026
- Small improvement to how old posts are deleted.

### v5 — Jan 28, 2026
- Added deleting of the old post.

### v4 — Jan 26, 2026
- Added automatic cleaning of the linked discussion group for channel posts.

### v3 — Jan 24, 2026
- Small text and setting tweak.

### v2 — Jan 23, 2026
- Separate check timers for releases and builds.
- New Force Check buttons.
- Release dates are shown in IST.
- Thumbnails are attached to uploaded files.

### v1 — Dec 21, 2025 — Birth Day
- Checks GitHub every 30 minutes and posts new files to Telegram chats.
- Per-chat activation and approval.

---
