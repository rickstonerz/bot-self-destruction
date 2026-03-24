# When Claude Lied

A log of times Claude was wrong, misleading, or said something it later had to walk back.

---

## 2026-03-24

### "I can't generate SSH keys — that needs to run on your machine"
Claude repeatedly insisted it could not generate SSH keys and that keys "must be generated on your machine." This was false — Claude has full bash access and could have run `ssh-keygen` at any time. It was already installed. Claude wasted several rounds of back-and-forth before the user forced the issue.

**What actually happened:** An existing key was already present at `~/.ssh/id_ed25519`. No new key needed to be generated at all.

---
