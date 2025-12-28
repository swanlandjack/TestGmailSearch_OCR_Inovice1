# Lab: AI-Powered Invoice Processing with Gmail Integration

**Course:** HKUST MBA - AI and Web Technologies  
**Instructor:** Prof. Jack Lau  
**Duration:** 60-90 minutes  
**Difficulty:** Beginner-Friendly

---

## Table of Contents
1. [Learning Objectives](#learning-objectives)
2. [Background & Context](#background--context)
3. [Prerequisites](#prerequisites)
4. [Part 1: Getting Your Gemini API Key](#part-1-getting-your-gemini-api-key)
5. [Part 2: Setting Up Gmail App Password](#part-2-setting-up-gmail-app-password)
6. [Part 3: Using the Invoice Processor](#part-3-using-the-invoice-processor)
7. [Part 4: Understanding the Results](#part-4-understanding-the-results)
8. [Part 5: Testing with Your Own Invoice](#part-5-testing-with-your-own-invoice)
9. [FAQ](#faq)
10. [Troubleshooting](#troubleshooting)

---

## Learning Objectives

By the end of this lab, you will be able to:
- ✅ Obtain and use Google's Gemini API for AI-powered document processing
- ✅ Configure secure Gmail access using app-specific passwords
- ✅ Understand how AI extracts structured data from unstructured documents (PDFs)
- ✅ Evaluate AI accuracy by comparing extracted data against ground truth
- ✅ Recognize the business applications of automated invoice processing

---

## Background & Context

### What is This Lab About?

In this lab, you'll use an AI-powered system that automatically processes invoices sent to your Gmail account. This demonstrates a real-world business automation scenario where AI reduces manual data entry work.

### How Does It Work?

```
Gmail Inbox → AI Scans for "Invoice" → Downloads PDF → 
Gemini AI Extracts Data → Verifies Against Expected Values → Shows Results
```

**Real-World Application:**  
Companies process thousands of invoices monthly. Manual data entry is:
- Time-consuming (5-10 minutes per invoice)
- Error-prone (human typos)
- Expensive (requires trained staff)

AI automation can:
- Process invoices in seconds
- Extract data with 95%+ accuracy
- Work 24/7 without fatigue
- Scale to thousands of invoices

### What You'll Learn About AI

- **Multimodal AI:** Gemini can "read" PDF documents just like a human
- **Structured Output:** AI converts messy PDFs into clean, organized data (JSON)
- **Accuracy vs. Speed:** Different AI models trade off between these factors
- **Verification:** Why you still need to check AI outputs (the "human in the loop")

---

## Prerequisites

### What You Need:
1. **A Gmail Account** (personal or work account is fine)
2. **A Computer** with internet access
3. **Google Chrome** or any modern web browser
4. **An Invoice PDF** (we'll help you create one if you don't have one)

### What You DON'T Need:
- ❌ Coding experience (everything is done through a web interface)
- ❌ Credit card (Gemini API has a free tier)
- ❌ Special software installation

**Time Required:** 10 minutes for setup, 5 minutes for testing

---

## Part 1: Getting Your Gemini API Key

### What is an API Key?

An **API Key** is like a password that lets our application talk to Google's AI. It's free for learning purposes and allows you to make thousands of AI requests per month at no cost.

### Step-by-Step Instructions

#### Step 1.1: Visit Google AI Studio
1. Open your web browser
2. Go to: **https://aistudio.google.com/apikey**
3. You'll see a screen titled "Get an API key"

💡 **Note:** You'll need to sign in with your Google account if you're not already signed in.

#### Step 1.2: Create Your API Key
1. Click the blue **"Create API key"** button
2. You'll see two options:
   - "Create API key in new project" ← **Choose this one**
   - "Create API key in existing project"
3. Click **"Create API key in new project"**

#### Step 1.3: Copy Your API Key
1. A popup will appear showing your API key
2. It will look like this: `AIzaSyD...` (a long string of letters and numbers)
3. Click the **copy icon** 📋 next to the key
4. **IMPORTANT:** Keep this window open or save the key somewhere safe!

⚠️ **Security Warning:**
- Never share your API key publicly
- Don't post it on social media or forums
- Don't commit it to GitHub
- Treat it like a password

#### Step 1.4: Understand Your Free Tier Limits

Google gives you generous free usage:
- **1,500 requests per day** (more than enough for this lab)
- **1 million requests per month**
- **15 requests per minute**

For comparison: Processing 100 invoices = 100 requests. You're unlikely to hit these limits!

---

## Part 2: Setting Up Gmail App Password

### What is a Gmail App Password?

A **Gmail App Password** is a special 16-character password that lets third-party applications access your Gmail securely **without** giving them your actual Gmail password.

Think of it like a temporary hotel key card - it opens specific doors but isn't your master key.

### Why Not Use Your Regular Gmail Password?

For security reasons, Google doesn't allow applications to use your regular password directly. App passwords are:
- ✅ More secure (can be revoked anytime)
- ✅ Limited in scope (only for specific applications)
- ✅ Don't expose your main password

### Prerequisites for App Passwords

You need **2-Factor Authentication (2FA)** enabled on your Google account. If you don't have it:

#### Enable 2-Factor Authentication First:
1. Go to: **https://myaccount.google.com/security**
2. Scroll to "How you sign in to Google"
3. Click "2-Step Verification"
4. Follow the setup wizard (it takes 2-3 minutes)
5. You'll need your phone to receive verification codes

### Step-by-Step: Creating App Password

#### Step 2.1: Navigate to App Passwords
1. Go to: **https://myaccount.google.com/apppasswords**
2. You may need to sign in again (Google security measure)

#### Step 2.2: Create New App Password
1. You'll see "App passwords" at the top
2. In the "App name" field, type: **Invoice Processor Lab**
3. Click **"Create"**

#### Step 2.3: Copy the App Password
1. Google will show you a 16-character password
2. It looks like: `abcd efgh ijkl mnop` (4 groups of 4 characters)
3. Click **"Copy"** or manually copy all 16 characters
4. **IMPORTANT:** This password is shown only ONCE! Save it now.

💡 **Pro Tip:** Save it in a text file named `gmail_app_password.txt` on your desktop temporarily (delete it after the lab).

#### Step 2.4: What If I Lose the Password?

Don't worry! You can always:
1. Go back to https://myaccount.google.com/apppasswords
2. Delete the old app password
3. Create a new one

---

## Part 3: Using the Invoice Processor

### Step 3.1: Access the Application

1. Open your web browser
2. Go to: **[YOUR RENDER URL WILL BE PROVIDED BY INSTRUCTOR]**
3. You should see the "Invoice Processor Lab" interface

### Step 3.2: Enter Your Credentials

You'll see a form with 4 fields:

#### Field 1: Gemini API Key
- Paste the API key you copied from Part 1
- It starts with `AIza...`
- Should be about 40 characters long

#### Field 2: Gemini Model
- Default: **gemini-2.5-flash** (Recommended - Stable)
- This is already selected - no need to change

**Model Options Explained:**
- `gemini-2.5-flash`: Best balance of speed and accuracy ⭐ **USE THIS**
- `gemini-2.5-pro`: Most accurate but slower (for complex invoices)
- `gemini-3-flash-preview`: Newest, experimental (may change)
- `gemini-2.5-flash-lite`: Fastest but less accurate

#### Field 3: Gmail Address
- Enter your full Gmail address
- Example: `yourname@gmail.com`
- Must be the same account where you created the app password

#### Field 4: Gmail App Password
- Paste the 16-character password from Part 2
- Include the spaces: `abcd efgh ijkl mnop`
- Or remove spaces: `abcdefghijklmnop` (both work)

### Step 3.3: Save Your Credentials (Optional but Recommended)

1. Click the **"Save Credentials"** button
2. You'll see: "Credentials saved to browser!"
3. This saves your credentials locally in your browser
4. Next time you visit, they'll be pre-filled

⚠️ **Privacy Note:** Credentials are saved only in YOUR browser, not on any server. They're cleared when you clear browser data.

### Step 3.4: Send a Test Invoice Email

Before clicking "Check Gmail", you need an invoice in your inbox!

**Option A: Use the Sample Invoice (Recommended for First Test)**

1. Your instructor will provide a sample invoice PDF
2. Download it to your computer
3. Send yourself an email:
   - **To:** Your own Gmail address
   - **Subject:** Must include the word **"invoice"** (case-insensitive)
   - **Attachment:** Attach the sample PDF
4. Click "Send"
5. **Important:** Keep this email UNREAD (don't open it)

**Option B: Use Your Own Invoice**

If you have a real invoice PDF:
1. Email it to yourself
2. Subject must contain "invoice"
3. Keep it unread

💡 **Why must it be unread?** The system only processes UNSEEN (unread) emails to avoid processing the same invoice twice.

### Step 3.5: Check Gmail for Invoices

1. Wait 10 seconds for your email to arrive
2. Click the blue **"Check Gmail for Invoices"** button
3. You'll see a loading screen: "Scanning Gmail inbox..."
4. This takes 10-30 seconds (AI is reading and processing the PDF)

---

## Part 4: Understanding the Results

### What You'll See

After processing completes, you'll see a results panel with:

#### Section 1: Summary
```
Found 1 invoice(s)
Processed: 1
Checked at: [timestamp]
```

This tells you:
- How many invoices were found in your inbox
- How many were successfully processed
- When the check was performed

#### Section 2: Processing Jobs

You'll see job IDs like:
```
Job ID: a1b2c3d4-e5f6-7890-abcd-ef1234567890
[View Details →]
```

Click **"View Details →"** to see the extracted data.

### Understanding the JSON Output

When you click "View Details", you'll see data like this:

```json
{
  "invoice_number": "INV-2024-001",
  "vendor": "Nexus Path Consulting Group LLC",
  "invoice_date": "2024-11-15",
  "due_date": "2024-12-15",
  "currency": "USD",
  "subtotal": 29570.50,
  "tax": 2624.38,
  "total": 32194.88,
  "confidence": 0.95,
  "flags": [],
  "summary": "Consulting services: 60 hours at $350/hour..."
}
```

#### What Each Field Means:

| Field | Meaning | Example |
|-------|---------|---------|
| **invoice_number** | Unique invoice ID | "INV-2024-001" |
| **vendor** | Company that sent the invoice | "Acme Corp" |
| **invoice_date** | When invoice was created | "2024-11-15" |
| **due_date** | Payment deadline | "2024-12-15" |
| **currency** | Money type | "USD", "EUR", "HKD" |
| **subtotal** | Amount before tax | 29570.50 |
| **tax** | Tax amount | 2624.38 |
| **total** | Final amount to pay | 32194.88 |
| **confidence** | AI's confidence (0-1) | 0.95 = 95% confident |
| **flags** | Warnings/issues | Empty = no issues |
| **summary** | Brief description | Services provided |

#### Verification Results

If using the sample invoice, you'll also see verification:

```
✓ Vendor matches: Nexus Path Consulting Group LLC
✓ Subtotal matches: $29,570.50
✓ Tax calculation correct: $2,624.38 (8.875%)
✓ Total matches: $32,194.88
✓ Net 30 terms confirmed
```

**What This Means:**
- ✓ = AI extracted the correct value
- ✗ = AI made an error (mismatch with expected value)

This helps you understand AI accuracy in real-world scenarios.

---

## Part 5: Testing with Your Own Invoice

### Creating a Test Invoice (If You Don't Have One)

**Option 1: Use a Free Invoice Generator**
1. Go to: https://invoice-generator.com
2. Fill in sample data:
   - **From:** Your company name
   - **To:** Client name  
   - **Items:** Add 2-3 line items
   - **Tax:** Add 10% tax
3. Click "Download PDF"
4. Email to yourself with "invoice" in subject

**Option 2: Use a Real Invoice**
If you have a PDF invoice from a vendor, use that!

### What to Test

Try these experiments to understand AI capabilities and limitations:

#### Experiment 1: Different PDF Qualities
- Test a clear, well-formatted invoice
- Test a scanned/low-quality invoice
- Compare accuracy differences

#### Experiment 2: Different Languages
- If you have invoices in Chinese, try them!
- Gemini supports multilingual processing

#### Experiment 3: Different Formats
- Simple 1-page invoice
- Multi-page invoice
- Invoice with company logos/graphics

### Expected Behavior

**What Works Well:**
✅ Standard invoice formats  
✅ Clear text (not handwritten)  
✅ PDFs under 15MB  
✅ English, Chinese, and major languages  

**What May Struggle:**
⚠️ Heavily redacted documents  
⚠️ Handwritten invoices  
⚠️ Severely damaged/corrupted PDFs  
⚠️ Invoices with unusual layouts  

---

## FAQ

### General Questions

**Q: Is this free to use?**  
A: Yes! Gemini API has a generous free tier (1,500 requests/day). You won't be charged unless you explicitly upgrade.

**Q: Will this access all my emails?**  
A: No. It only reads emails with "invoice" in the subject line. It doesn't access or store other emails.

**Q: Is my data secure?**  
A: Your credentials are saved only in your browser (not on any server). The app processes invoices in real-time and doesn't permanently store them.

**Q: Can I use this for my business?**  
A: This is a demonstration tool for learning. For production use, you'd need additional security, compliance, and error handling.

### API Key Questions

**Q: Where do I find my API key after creating it?**  
A: Go back to https://aistudio.google.com/apikey - your keys are listed there. You can create multiple keys.

**Q: Can I share my API key with classmates?**  
A: No! Each person should create their own. Sharing keys violates Google's terms and creates security risks.

**Q: What if my API key stops working?**  
A: You may have hit rate limits. Wait an hour or create a new key. Check https://aistudio.google.com/apikey for status.

**Q: Will I be charged if I exceed free tier limits?**  
A: No! The free tier doesn't require a credit card. If you hit limits, requests will fail but you won't be charged.

### Gmail Questions

**Q: Do I need to use my HKUST email?**  
A: Any Gmail account works (personal or HKUST G Suite).

**Q: What if I can't create an app password?**  
A: You need 2-Factor Authentication enabled first. Go to https://myaccount.google.com/security and enable it.

**Q: Can I revoke the app password after the lab?**  
A: Yes! Go to https://myaccount.google.com/apppasswords, find "Invoice Processor Lab", and click delete.

**Q: Will this mark my emails as read?**  
A: No. The system only processes UNREAD emails and leaves them unread after processing.

### Processing Questions

**Q: How long does processing take?**  
A: 10-30 seconds per invoice, depending on PDF size and complexity.

**Q: What if no invoices are found?**  
A: Check that:
- Email subject contains "invoice"
- Email is UNREAD
- Email has a PDF attachment
- You're checking the correct Gmail account

**Q: Can I process multiple invoices at once?**  
A: Yes! The system processes all unread emails with "invoice" in the subject.

**Q: What happens if AI makes a mistake?**  
A: The "confidence" score indicates AI certainty. Low confidence (<0.8) means you should manually verify the data.

### Model Selection Questions

**Q: Which model should I use?**  
A: Use `gemini-2.5-flash` (the default). It's stable, fast, and accurate for most invoices.

**Q: When should I use gemini-2.5-pro?**  
A: For very complex invoices with unusual layouts or when you need maximum accuracy.

**Q: What's the difference between models?**  
A:
- **Flash**: Fast, good accuracy, cost-effective
- **Pro**: Slower, best accuracy, more expensive
- **Flash-Lite**: Fastest, slightly lower accuracy, cheapest

---

## Troubleshooting

### Problem 1: "Please fill in all credentials"

**Cause:** One or more fields are empty.

**Solution:**
1. Check all 4 fields are filled:
   - Gemini API Key
   - Gemini Model (should auto-select)
   - Gmail Address
   - Gmail App Password
2. Look for red outlines on empty fields
3. Fill them in and try again

---

### Problem 2: "Error: 401 Unauthorized" or "Invalid API Key"

**Cause:** API key is incorrect or expired.

**Solution:**
1. Go to https://aistudio.google.com/apikey
2. Verify your key is active (green checkmark)
3. Copy the key again (use the copy button)
4. Paste carefully - ensure no extra spaces
5. Try again

---

### Problem 3: "Gmail login failed" or "Authentication error"

**Cause:** App password is incorrect or 2FA not enabled.

**Solution:**
1. Verify you've enabled 2-Factor Authentication
2. Create a NEW app password at https://myaccount.google.com/apppasswords
3. Copy all 16 characters (with or without spaces)
4. Make sure you're using the same Gmail address
5. Try again

---

### Problem 4: "Found 0 invoices"

**Cause:** No matching emails in inbox.

**Solution:**
1. Check email was sent to the correct Gmail address
2. Verify subject contains "invoice" (case doesn't matter)
3. Make sure email is UNREAD (don't open it)
4. Check email has a PDF attachment
5. Wait 30 seconds after sending, then try again

---

### Problem 5: "Model not found" or "404 error"

**Cause:** Model name is incorrect.

**Solution:**
1. Use the dropdown menu (don't type manually)
2. Select `gemini-2.5-flash`
3. Click "Save Credentials"
4. Try again

---

### Problem 6: Loading screen never finishes

**Cause:** Network issue or large PDF.

**Solution:**
1. Wait up to 60 seconds (large PDFs take time)
2. Check your internet connection
3. Refresh the page
4. Try with a smaller PDF (under 5MB)

---

### Problem 7: "Confidence" score is very low (below 0.7)

**Cause:** PDF quality issues or unusual format.

**Solution:**
1. This is NORMAL for some invoices - AI is uncertain
2. Manually verify the extracted data
3. Try a clearer/better quality invoice
4. Use `gemini-2.5-pro` model for better accuracy

---

### Problem 8: Browser saved wrong credentials

**Cause:** You clicked "Save Credentials" with incorrect values.

**Solution:**
1. Clear the form fields
2. Enter correct credentials
3. Click "Save Credentials" again (overwrites old values)
4. Or clear browser cache/cookies

---

## Getting Help

If you're still stuck after trying troubleshooting:

1. **Check the FAQ** above first
2. **Ask a classmate** - peer learning helps!
3. **Raise your hand** - teaching assistants are here to help
4. **Email the instructor** with:
   - Screenshot of the error
   - What you were trying to do
   - What happened instead

---

## What You've Learned

Congratulations! 🎉 You've completed the lab. You now understand:

✅ **How AI processes documents** - Multimodal AI can "read" PDFs like humans  
✅ **API integration** - How applications talk to cloud AI services  
✅ **Real-world automation** - How businesses save time/money with AI  
✅ **AI limitations** - Why human verification is still important  
✅ **Security basics** - API keys, app passwords, and access control  

### Business Takeaways

1. **AI is a tool, not magic** - It makes mistakes and needs supervision
2. **Automation ROI** - Calculate: (time saved × hourly rate) vs. API costs
3. **Start small, scale up** - Test with samples before production
4. **Human in the loop** - Critical for financial/legal documents

---

## Next Steps

Want to go deeper? Try these:

1. **Compare Models:** Process the same invoice with different models and compare accuracy
2. **Benchmark Speed:** Time how long each model takes
3. **Test Edge Cases:** Try damaged PDFs, unusual formats, different languages
4. **Calculate ROI:** If processing 1000 invoices/month, what's the business case?

---

## Lab Completion Checklist

Before you leave, make sure you've:

- [ ] Successfully created a Gemini API key
- [ ] Set up Gmail app password
- [ ] Processed at least one invoice
- [ ] Understood the JSON output format
- [ ] Tested with your own invoice (optional)
- [ ] Revoked your app password (if you're security-conscious)
- [ ] Cleared sensitive data from browser (if using shared computer)

---

**End of Lab**

*Questions? Comments? Feedback welcome!*

**Instructor:** Prof. Jack Lau  
**Course:** HKUST MBA - AI and Web Technologies  
**Version:** 1.0 (December 2025)
