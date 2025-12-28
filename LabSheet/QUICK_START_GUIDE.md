# Invoice Processor Lab - Quick Start Guide

**⏱️ 15-Minute Setup | No Coding Required**

---

## What You'll Do

Use AI to automatically extract data from invoice PDFs in your Gmail inbox.

---

## Step 1: Get Gemini API Key (5 minutes)

1. Go to: **https://aistudio.google.com/apikey**
2. Click **"Create API key in new project"**
3. **Copy** the key (starts with `AIza...`)
4. Keep it safe - you'll need it in Step 3

---

## Step 2: Get Gmail App Password (5 minutes)

### Enable 2-Factor Authentication First (if not already enabled):
1. Go to: **https://myaccount.google.com/security**
2. Click **"2-Step Verification"**
3. Follow setup (takes 3 minutes)

### Create App Password:
1. Go to: **https://myaccount.google.com/apppasswords**
2. App name: **Invoice Processor**
3. Click **"Create"**
4. **Copy** the 16-character password
5. Save it somewhere safe

---

## Step 3: Send Test Email (1 minute)

1. Email yourself with:
   - **To:** Your Gmail address
   - **Subject:** Test invoice
   - **Attachment:** Any invoice PDF (or ask instructor for sample)
2. **Don't open the email** (keep it unread)

---

## Step 4: Process Invoice (2 minutes)

1. Open the lab application: **[URL from instructor]**
2. Fill in the form:
   - **Gemini API Key:** Paste from Step 1
   - **Gemini Model:** Leave as `gemini-2.5-flash`
   - **Gmail Address:** Your email
   - **Gmail App Password:** Paste from Step 2
3. Click **"Save Credentials"**
4. Click **"Check Gmail for Invoices"**
5. Wait 15 seconds

---

## Step 5: View Results

1. You'll see: "Found 1 invoice(s)"
2. Click **"View Details"** on the job ID
3. See the extracted data in JSON format:
   ```json
   {
     "invoice_number": "...",
     "vendor": "...",
     "total": 1234.56,
     ...
   }
   ```

---

## ✅ Done!

You've just used AI to automatically process an invoice!

**Need help?** See the full lab sheet for detailed troubleshooting.

---

## Common Issues

### "Please fill in all credentials"
→ All 4 fields must be filled

### "Invalid API key"
→ Go back to https://aistudio.google.com/apikey and copy again

### "Gmail login failed"  
→ Make sure you created an **app password**, not using your regular password

### "Found 0 invoices"
→ Make sure:
- Subject contains "invoice"
- Email is **unread**
- Has PDF attachment

---

## After the Lab

**Security Tip:** Revoke your app password when done:
1. Go to: https://myaccount.google.com/apppasswords
2. Find "Invoice Processor"
3. Click **Delete**

---

**Questions?** Ask your instructor or TA!
