# Gedcom-Eventize

Copyright © 2017, Christopher Alan Mosher, Shelton, Connecticut, USA, <cmosher01@gmail.com>.

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=CVSSQ2BWDCKQ2)
[![License](https://img.shields.io/github/license/cmosher01/Gedcom-Eventize.svg)](https://www.gnu.org/licenses/gpl.html)

Turn GEDCOM tags into generic events (EVEN/TYPE/NOTE).

With this input

---
0 @I1@ INDI
1 _MILT Age: 23
---

the command

---
gedcom-eventize -w '.*._MILT' -t military
---

produces

---
0 @I1@ INDI
1 EVEN
2 TYPE military
2 NOTE Age: 23
---




With this input

---
0 @I1@ INDI
1 RESI Age: 23
---

the command

---
gedcom-eventize -w '.*.RESI'
---

produces

---
0 @I1@ INDI
1 RESI
2 NOTE Age: 23
---
