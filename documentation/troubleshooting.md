# 🛠️ Troubleshooting

This document records problems encountered while building and using the home lab.

## Troubleshooting Template

### Issue: [Short description]

**Date:** YYYY-MM-DD

**Environment:**

- VM:
- OS:
- VirtualBox:
- Network mode:

**Objective:**

What were you trying to accomplish?

**Problem:**

What happened?

**Error Message:**

```text
Paste the exact error here.
```

**Investigation:**

Document commands, logs, settings, and tests used.

**Root Cause:**

Explain what caused the issue.

**Solution:**

Document the steps that fixed it.

**Verification:**

Explain how you confirmed the issue was resolved.

**Lessons Learned:**

- Lesson 1
- Lesson 2

## Useful Linux Commands

### OS information

```bash
cat /etc/os-release
hostnamectl
```

### Network information

```bash
ip addr
ip route
```

### Connectivity

```bash
ping <IP>
```

### Disk

```bash
df -h
```

### Memory

```bash
free -h
```

### Processes

```bash
ps aux
```

### Logs

```bash
journalctl
```

## Documentation Principle

Keep the original error message and document failed troubleshooting attempts as well as the final solution.

A strong entry should answer:

> What happened → Why it happened → How it was fixed → What I learned
