# Gedcom-Eventize

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
