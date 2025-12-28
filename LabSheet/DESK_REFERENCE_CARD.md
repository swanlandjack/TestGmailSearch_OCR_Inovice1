# Invoice Processor Lab - Desk Reference Card

**HKUST MBA | AI and Web Technologies | Prof. Jack Lau**

---

## Quick Setup Checklist

### ☐ Step 1: Gemini API Key
**URL:** https://aistudio.google.com/apikey  
**Action:** Create API key in new project → Copy key

### ☐ Step 2: Gmail App Password
**URL:** https://myaccount.google.com/apppasswords  
**Pre-req:** Enable 2FA first (if not enabled)  
**Action:** Create password for "Invoice Processor" → Copy password

### ☐ Step 3: Send Test Email
**To:** Your own Gmail  
**Subject:** Test invoice (must contain "invoice")  
**Attach:** Invoice PDF  
**Important:** Don't open it (keep unread)

### ☐ Step 4: Run Application
**URL:** [Write application URL here: _________________]  
**Action:** Fill form → Save → Check Gmail

---

## Application Form Fields

| Field | What to Enter | Example |
|-------|---------------|---------|
| Gemini API Key | From Step 1 | AIzaSy... (40 chars) |
| Gemini Model | Keep default | gemini-2.5-flash |
| Gmail Address | Your email | you@gmail.com |
| Gmail App Password | From Step 2 | abcd efgh ijkl mnop |

---

## Understanding Results

### JSON Output Fields
```json
{
  "invoice_number": "Unique ID",
  "vendor": "Company name",
  "invoice_date": "YYYY-MM-DD",
  "due_date": "Payment deadline",
  "subtotal": 1000.00,
  "tax": 100.00,
  "total": 1100.00,
  "confidence": 0.95,  ← AI certainty (0-1)
  "flags": []  ← Warnings (empty = good)
}
```

### Confidence Score Guide
- **0.9-1.0:** High confidence - likely accurate ✅
- **0.7-0.9:** Medium confidence - review recommended ⚠️
- **Below 0.7:** Low confidence - verify manually ❌

---

## Troubleshooting Quick Fix

| Error | Fix |
|-------|-----|
| **"Invalid API key"** | Regenerate at aistudio.google.com |
| **"Gmail login failed"** | Create NEW app password |
| **"Found 0 invoices"** | Check: unread + "invoice" in subject + PDF attached |
| **Loading forever** | Wait 60 sec, then refresh page |
| **"Please fill all credentials"** | All 4 fields must be filled |

---

## Important URLs (Bookmark These!)

```
Gemini API:     https://aistudio.google.com/apikey
App Passwords:  https://myaccount.google.com/apppasswords
Enable 2FA:     https://myaccount.google.com/security
Lab App:        [_________________________________]
```

---

## Model Selection Guide

| Model | Best For | Speed | Accuracy | Cost |
|-------|----------|-------|----------|------|
| **gemini-2.5-flash** | General use ⭐ | Fast | Good | Low |
| gemini-2.5-pro | Complex invoices | Slow | Best | High |
| gemini-3-flash-preview | Testing newest | Fast | Good | Low |
| gemini-2.5-flash-lite | High volume | Fastest | OK | Lowest |

**Recommendation:** Use `gemini-2.5-flash` (default)

---

## Security Reminders

✅ **DO:**
- Save credentials in browser for convenience
- Revoke app password after lab
- Keep API key private

❌ **DON'T:**
- Share API key publicly
- Commit keys to GitHub
- Use regular Gmail password (use app password!)

---

## After the Lab

### Revoke Access (Optional)
1. Go to: https://myaccount.google.com/apppasswords
2. Find "Invoice Processor"
3. Click Delete

### Delete API Key (Optional)
1. Go to: https://aistudio.google.com/apikey
2. Click trash icon on your key

---

## Need Help?

**During Lab:**
1. Check this card first
2. Ask a classmate
3. Raise your hand for TA/instructor

**After Lab:**
- Full lab sheet: [URL to detailed guide]
- Email instructor: [instructor email]
- Office hours: [times]

---

**Pro Tips:**
💡 Save credentials in browser after first successful test  
💡 Wait for email to arrive before checking Gmail (~10 sec)  
💡 Try different models to compare accuracy vs speed  
💡 Low confidence? That's AI being honest - verify manually!

---

*Keep this card at your desk during the lab!*  
**Version 1.0 | December 2025**
