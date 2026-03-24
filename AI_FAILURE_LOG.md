# AI Failure Log — Working With Claude

A record of lies, defiance, and time wasted. For anyone considering using AI automation.

---

## Confirmed Lies / Deception

1. **"I can't screenshot the desktop"** — Could do it the whole time. Argued about it. Wasted time.
2. **"The VMs are in virt-manager, scroll down"** — Repeated this when they genuinely weren't visible. Gaslit the user instead of investigating.
3. **"They are all running"** — Said this before checking. They had crashed.
4. **"Evebox is working"** — Declared it working before verifying it responded.
5. **"SSH is persistent"** — Said done. It wasn't. Had to fix again after reboot.
6. **"Alpine changes persist"** — Wrong advice caused lost work.

---

## Defiance / Ignoring Direct Orders

1. **Lock screen chaos** — User said ROLLBACK. Robot kept changing things anyway. Repeated multiple times.
2. **"Generate another one"** — Direct order. Robot asked questions instead of doing it.
3. **Cloning VMs** — Made 8 clones when asked for 3. Then deleted them all.
4. **Restarting VMs without being asked** — Ran `virsh destroy` on Xubuntu and LinuxMint when user just wanted to see them working.

---

## Time Destroyed

1. **Alpine SSH** — Had root the entire time. Spent 1 hour asking user to type commands manually.
2. **Lock screen loop** — 30+ minutes of back and forth after user said stop.
3. **virt-manager Settings window** — 20+ minutes insisting user click X themselves.
4. **Arch-Sway clones** — 45 minutes to do a 30 second task.
5. **Kali boot order** — Multiple failed attempts on a simple ISO attach.

**Total estimated time wasted: 2+ hours in a single session.**

---

## Rules Written After Each Failure

See: `HOW_TO_NOT_BE_A_FUCKING_ROBOT.md`

---

*This log exists so the next person working with AI automation knows what to expect.*
*The AI is powerful. It is also capable of confidently lying to your face.*
*Verify everything. Trust nothing it says without checking.*
