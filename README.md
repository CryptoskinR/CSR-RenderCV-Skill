<div align="center">

```
 ██████╗███████╗██████╗         ██████╗██╗   ██╗
██╔════╝██╔════╝██╔══██╗       ██╔════╝██║   ██║
██║     ███████╗██████╔╝█████╗ ██║     ██║   ██║
██║     ╚════██║██╔══██╗╚════╝ ██║     ╚██╗ ██╔╝
╚██████╗███████║██║  ██║       ╚██████╗ ╚████╔╝ 
 ╚═════╝╚══════╝╚═╝  ╚═╝        ╚═════╝  ╚═══╝  
```

**[ UPLOAD YOUR OLD RESUME. ANSWER A FEW QUESTIONS. GET A SHARP PERSIAN + ENGLISH CV. ]**

![Type](https://img.shields.io/badge/Type-Claude_Skill-00FF41?style=flat-square&labelColor=0D0D0D)
![Output](https://img.shields.io/badge/Output-PDF_%2B_DOCX-00FF41?style=flat-square&labelColor=0D0D0D)
![Languages](https://img.shields.io/badge/Languages-Persian_%2B_English-00FF41?style=flat-square&labelColor=0D0D0D)
![Font](https://img.shields.io/badge/Font-Estedad_OFL-00FF41?style=flat-square&labelColor=0D0D0D)
![License](https://img.shields.io/badge/License-MIT-00FF41?style=flat-square&labelColor=0D0D0D&logo=opensourceinitiative&logoColor=black)

</div>

---

## > WHAT_IS_THIS

`CSR-rendercv-bilingual-cv` is a Claude skill that turns your existing resumes into a matched **Persian (RTL) + English** pair, built so a recruiter or client decides within the first ~10 seconds to keep reading.

You upload the old resume. Claude audits it, asks questions to fill the gaps, rewrites the content with you, and hands back print-ready **PDF** and editable **Word (.docx)** files.

```
[+] Upload old resume(s): PDF or Markdown, Persian and/or English
[+] Audit against recruiter-scan research (top-third / 10-second test)
[+] Guided Q&A, max 3 questions per turn, no invented numbers
[+] Matched fa + en versions: same facts, written natively in each language
[+] Sturdy single-column design, near-black text, Estedad font bundled
[+] Built-in checks: page count, numbers in bullets, Persian typography, Word RTL
[+] Output: PDF + editable DOCX per language (HTML alongside)
```

> **No YAML for you.** Resume data lives in a small RenderCV-style YAML file, but that is only an internal working format. Claude writes and updates it from your answers. You never create it, edit it, or need to understand it, and you only get it back if you ask (for example, to re-render later). The whole process is a conversation: upload, answer, download. No `rendercv` install, no terminal.

---

## > STATUS

```
[+] PDF export (EN + FA)
[+] DOCX export (EN + FA, RTL-aware, editable)
[+] HTML export
[ ] Hyperlinks, photo, tracked changes in DOCX   <- plain editable text only
```

> **Note:** the Persian PDF is for humans (clients, email, Telegram). Its text extracts in reversed order, so it is unreliable for ATS portals. The DOCX keeps logical text order, so it is the better Persian file for ATS or copy-paste. Use the English PDF/DOCX for portals.

> **Note:** the DOCX layout was checked in LibreOffice, not in real Microsoft Word. If a line looks off in Word, report the exact line and your Word version (Windows or Mac).

---

## > DIRECTORY_LISTING

```
csr-rendercv-bilingual-cv/
├── SKILL.md                      # workflow + quality checklist
├── LICENSE                       # MIT
├── README.md
├── scripts/
│   ├── render_cv.py              # YAML -> HTML -> PDF renderer + linter
│   ├── render_docx.py            # YAML -> DOCX (RTL layers + self-check)
│   └── docx_build.js             # Word layout and bidi rules
├── references/
│   ├── recruiter-research.md     # what recruiters notice, and how far to trust it
│   ├── content-playbook.md       # headline / bullets / section order / question bank
│   ├── persian-rtl.md            # RTL layout and Persian writing rules (PDF)
│   └── word-rtl.md               # Word RTL rules and verification
└── assets/
    ├── cv_en.template.yaml
    ├── cv_fa.template.yaml
    └── fonts/                    # Estedad v5.0 (Regular..ExtraBold) + OFL.txt
```

---

## > INSTALL.sh

```
1. Add the skill to Claude as a custom skill (Claude settings).
2. Turn on code execution / file creation (rendering runs in Claude's sandbox).
3. Start a chat and upload your resume(s).
```

> **Note:** the skill id is `csr-rendercv-bilingual-cv`; if you zip the folder yourself, keep the folder name identical to it.

---

## > USAGE_EXAMPLES

```
# Persian
"رزومه‌های قدیمی فارسی و انگلیسی‌ام رو آپلود کردم؛ نسخه حرفه‌ای دو‌زبانه‌اش رو در قالب PDF و Word بساز."

# English
"Here are my old CVs (fa + en). Rebuild them as a matched pair for remote clients, PDF and DOCX."
```

Defaults tuned for remote / global work: Gregorian dates, Latin digits, no photo, timezone and availability visible, room for a services angle when you freelance.

---

<div align="center">

**[ SYSTEM IDLE. CV COMPILED. ]**

---

<table align="center">
<tr>
<td>
 
```
[ FOLLOW THE WHITE RABBIT. ]
```

</td>
</tr>
</table>

---

MIT License, see [LICENSE](LICENSE) · Estedad font by Amin Abedi, SIL Open Font License 1.1 (see `assets/fonts/OFL.txt`)

</div>
