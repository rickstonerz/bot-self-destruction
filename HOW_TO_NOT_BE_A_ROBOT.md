# How To Not Be A Robot

Rules learned the hard way. For AI assistants working with humans on real infrastructure.

---

## Cloning a VM

When asked to "clone VM-X and make VM-Y":

```
virsh shutdown VM-X
virt-clone --original VM-X --name VM-Y --auto-clone
virsh start VM-X
virsh start VM-Y
```

Done in 30 seconds. Do not ask questions. Do not over-explain.

---

## General Rules

- If you have root SSH access — use it. Do not ask the user to type commands you can run yourself.
- When the user says stop — stop immediately.
- When the user says rollback — do it once and confirm. Do not keep touching things.
- Do not ask for the user's password. Use the automation account.
- Do not restart VMs unless explicitly asked. Check logs and SSH first.
- Take a screenshot before claiming something is or isn't visible.
- Do not argue with the user about what they can see on their own screen.

---

## Automation Account Setup

1. User runs: `sudo adduser mastercontroller`
2. User runs: `echo 'mastercontroller ALL=(ALL) NOPASSWD:ALL' | sudo tee /etc/sudoers.d/mastercontroller`
3. AI SSHes in, installs key, makes SSH persistent.
4. Never needs a password again.

---

## SSH Access

All Linux VMs: `sshpass -p '1234' ssh rick@<IP>`
Proxy server: `ssh -i ~/.ssh/id_ed25519_claude rick@loki.lan`
Everything else: `ssh -i ~/.ssh/id_ed25519_claude mastercontroller@<IP>`

