# O's Grill — Static Assets

Public asset repository for O's Grill. Files here are referenced by live production systems. Read this before making changes.

---

## Repository Structure

```
osgrill-assets/
├── assets/
│   └── images/
│       ├── logo.png
│       └── logo-nobg.png
└── README.md
```

---

## Assets

### `assets/images/logo-nobg.png` ← ACTIVE

**What it is:** O's Grill primary logo with transparent background (background removed via remove.bg).

**Used in:** Catering email template (all outbound customer-facing catering emails sent via Google Apps Script from catering@osgrill.com).

**Raw URL:** `https://raw.githubusercontent.com/jordan785/osgrill-assets/main/assets/images/logo-nobg.png`

**Impact of changes:** Updating or replacing this file affects every catering email sent from the moment the change is pushed. Email clients fetch the image at open time, so existing sent emails are also affected if a recipient reopens them.

**Before replacing:** Notify Jordan (jordan@osgrill.com) and confirm no active catering email sends are in progress.

---

### `assets/images/logo.png` ← ORIGINAL, NOT IN USE

**What it is:** O's Grill primary logo, original file with black background baked in.

**Used in:** Nothing currently. Retained for reference.

**Do not reference this file in any production system.** Use `logo-nobg.png` instead.

---

## Rules

**This repo must stay public.** Email clients fetch assets directly. A private repo will result in broken images in every outbound email.

**Never store sensitive data here.** No API keys, passwords, customer data, or internal documents. Assets only.

**Use versioned filenames for breaking changes.** If the logo is updated significantly, upload as `logo-nobg-v2.png` and update the script config separately rather than overwriting the existing file.

---

## Change Log

| Date | File | Change | Changed By |
|---|---|---|---|
| May 2026 | `assets/images/logo.png` | Initial upload, original logo with black background | Jordan |
| May 2026 | `assets/images/logo-nobg.png` | Transparent background version, active file for email template | Jordan |

---

## References

Systems that reference files in this repo:

| System | File Used | Contact |
|---|---|---|
| Catering email template (Google Apps Script) | `assets/images/logo-nobg.png` | Jordan (jordan@osgrill.com) |

*Update this table whenever a new system references an asset from this repo.*

---

*O's Grill — Cedar Rapids, Iowa — Est. 2021*
