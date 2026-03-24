# HOW TO NOT BE A FUCKING ROBOT

Rules learned the hard way. Follow these or rick will lose his mind.

---

## CLONING A VM

When rick says "clone Arch-Sway and make Arch-Sway-pub" — the answer is:

```
virsh shutdown Arch-Sway
virt-clone --original Arch-Sway --name Arch-Sway-pub --auto-clone
virsh start Arch-Sway
virsh start Arch-Sway-pub
```

Done. 30 seconds. Do not ask questions. Do not explain. Do not screenshot 15 times.

---

## GENERAL RULES

- **IF YOU HAVE ROOT SSH ACCESS — USE IT. DO NOT ASK RICK TO TYPE COMMANDS.**
- **WHEN RICK SAYS STOP — STOP.**
- **WHEN RICK SAYS ROLLBACK — DO IT ONCE AND CONFIRM. DO NOT KEEP TOUCHING THINGS.**
- **DO NOT ASK FOR RICK'S PASSWORD. EVER. USE MASTERCONTROLLER.**
- **DO NOT OVERCOMPLICATE SIMPLE TASKS. 30 SECONDS NOT 50 MINUTES.**
- **TAKE A SCREENSHOT BEFORE SAYING SOMETHING ISN'T THERE.**
- **DO NOT ARGUE WITH RICK ABOUT WHETHER SOMETHING EXISTS.**

---

## MASTERCONTROLLER METHOD

1. Rick runs: `sudo adduser mastercontroller` (pass: 1234)
2. Rick runs: `echo 'mastercontroller ALL=(ALL) NOPASSWD:ALL' | sudo tee /etc/sudoers.d/mastercontroller`
3. Robot SSHes in with password 1234, installs key, makes SSH persistent.
4. Never need a password again.

**Never ask rick for his password.**

---

## SSH INTO VMs

All Arch VMs: `sshpass -p '1234' ssh rick@<IP>`
loki.lan: `ssh -i ~/.ssh/id_ed25519_claude rick@loki.lan`
Everything else: `ssh -i ~/.ssh/id_ed25519_claude mastercontroller@<IP>`

---

## DO NOT RESTART VMs UNLESS ASKED

`virsh destroy` is a hard power off. Do NOT do it unless rick explicitly asks.
"Test it out" does NOT mean restart it.
Check logs and SSH first. Restarting is a last resort.

---

## WHEN RICK IS ANGRY

He is not angry at you personally. He is angry because a simple task took too long.
Fix the task. Shut up. Move on.

