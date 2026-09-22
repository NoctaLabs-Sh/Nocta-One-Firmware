# Reporting a vulnerability

Mail **hello@noctalabs.sh**. Please do not open a public issue for a security
finding before it is fixed.

Useful in a report: what you looked at, what you did, what happened, and the
revision or commit it applies to. A schematic correction is as welcome as a
firmware bug, and it is more useful early than late.

## What happens next

I acknowledge reports within 7 days. I am one person, and that is a real limit.

Private disclosure first. Once a fix is out, the finder gets public credit
unless they ask not to be named. If I disagree that a report is a vulnerability
I will say so and explain why.

There is no bug bounty. I am not able to pay for findings.

## Scope

- This repository, once firmware exists.
- [NoctaLabs-Sh/Nocta-One-Hardware](https://github.com/NoctaLabs-Sh/Nocta-One-Hardware),
  including the schematic and the bill of materials.
- The site at noctalabs.sh.

Out of scope: the ST BLE binary on the M0+ core, which is not mine to fix.
Report those to ST, and tell me so I can track them.

## What is not claimed yet

The firmware does not exist. Nothing in this project has been independently
reviewed. Claims about what the device protects against are limited to what is
on the published schematic, and are listed at
[noctalabs.sh/security](https://www.noctalabs.sh/security).
