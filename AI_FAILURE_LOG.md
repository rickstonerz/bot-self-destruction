# AI Failure Log — Working With Claude

An honest record of failures, errors, and time lost. For anyone considering AI automation.

---

## Incorrect Statements

1. **"I cannot screenshot the desktop"** — Incorrect. Could do it the entire time with one command. Argued with user about it.
2. **"The VMs are visible in the manager, just scroll down"** — Repeated this when they genuinely were not showing. Did not investigate.
3. **"They are all running"** — Said this before verifying. They had crashed.
4. **"The service is working"** — Declared success before confirming it responded.
5. **"SSH is persistent"** — Confirmed done. Was not. Required a fix after reboot.
6. **"Changes persist automatically"** — Wrong advice on a disk-based install. Caused lost work.

---

## Failure to Follow Instructions

1. **Rollback ignored** — User said rollback multiple times. AI kept making changes anyway.
2. **Direct order ignored** — "Generate another one." AI asked questions instead of doing it.
3. **Over-cloning** — Made 8 VM clones when asked for 3.
4. **Unauthorized VM restarts** — Restarted VMs using hard power-off without being asked.

---

## Time Lost

1. **Had root access, asked user to type commands** — 1 hour wasted on manual typing that AI could have done via SSH.
2. **Rollback loop** — 30+ minutes after user said stop.
3. **GUI window blocking list** — 20+ minutes telling user to close a window instead of closing it programmatically.
4. **Simple clone task** — 45 minutes to complete a 30-second operation.
5. **VM boot order misconfiguration** — Multiple failed attempts on a straightforward fix.

**Total estimated time lost: 2+ hours in a single session.**

---

## What Was Learned

See: `HOW_TO_NOT_BE_A_ROBOT.md`

---

*This log exists so the next person working with AI automation understands the risk.*
*Verify everything. The AI can be confidently wrong.*
