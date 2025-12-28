# Instructor Guide: Invoice Processing Lab

**Course:** HKUST MBA - AI and Web Technologies  
**Lab Duration:** 60-90 minutes  
**Class Size:** Suitable for 10-50 students

---

## Pre-Lab Preparation (1 week before)

### 1. Test the Application
- [ ] Verify Render deployment is working
- [ ] Test with sample invoice
- [ ] Check all models are accessible
- [ ] Confirm no API rate limits

### 2. Prepare Materials
- [ ] Print Quick Start Guide (1 per student)
- [ ] Have full Lab Sheet available digitally
- [ ] Prepare sample invoice PDF (provided below)
- [ ] Create backup API keys (in case students have issues)

### 3. Classroom Setup
- [ ] Test projector/screen
- [ ] Verify classroom WiFi
- [ ] Have application URL ready to share
- [ ] Prepare troubleshooting station

---

## Sample Invoice for Students

**Download/Create:**
Use the invoice-generator.com or provide this sample:

```
Company: Nexus Path Consulting Group LLC
Invoice Number: INV-2024-001
Date: November 15, 2024
Due Date: December 15, 2024

Services:
- Consulting Hours (60h @ $350/hr): $21,000.00
- Workshop Facilitation (1 @ $8,500): $8,500.00
- Travel Expenses: $70.50

Subtotal: $29,570.50
Tax (8.875%): $2,624.38
Total: $32,194.88

Payment Terms: Net 30
```

Save as PDF and make available for download.

---

## Lab Session Timeline (90 minutes)

### Introduction (10 minutes)
**Topics to Cover:**
- Lab objectives
- Real-world business context
- AI capabilities and limitations
- Safety/security reminders

**Key Points:**
- "Today you'll see how AI automates manual data entry"
- "This technology saves companies millions in labor costs"
- "You'll learn both what AI can do AND where it fails"

### Live Demo (10 minutes)
**Walk through the process:**
1. Show Gemini API Studio
2. Create an API key (use your own account)
3. Show Gmail app password creation
4. Process a sample invoice on the projector
5. Explain the JSON output

**Talking Points:**
- "Notice the confidence score - AI tells you when it's uncertain"
- "The verification shows where AI matched expected values"
- "This same process can handle thousands of invoices per day"

### Hands-On Work (45 minutes)

**Minute 0-15: Setup Phase**
- Students get API keys
- Students create app passwords
- TAs circulate to help

**Common Issues to Watch For:**
- Students typing API key incorrectly
- Students not enabling 2FA first
- Students using regular password instead of app password

**Minute 15-30: First Test**
- Students send themselves test email
- Students process first invoice
- Celebrate first successes!

**Minute 30-45: Experimentation**
- Students try different invoices
- Compare models
- Test edge cases

### Discussion & Debrief (20 minutes)

**Discussion Questions:**
1. "What surprised you about AI accuracy?"
2. "What types of errors did the AI make?"
3. "How would you use this in your company?"
4. "What safeguards would you add for production use?"

**Key Learning Points to Emphasize:**
- AI is probabilistic, not deterministic
- Confidence scores are important
- Human verification still needed
- Different models trade speed vs. accuracy
- Cost-benefit analysis matters

### Wrap-Up (5 minutes)
- Review learning objectives
- Preview next class
- Remind students to revoke app passwords
- Collect feedback

---

## Teaching Assistant Briefing

### TA Responsibilities
1. **Circulate during setup** - help with API keys and passwords
2. **Monitor chat/questions** - watch for common issues
3. **Document interesting findings** - note unique student discoveries
4. **Emergency API keys** - have backup keys if students hit rate limits

### Common Student Questions

**Q: "Is this safe?"**
A: "Yes, we're using read-only access via app passwords. You can revoke access anytime."

**Q: "Will this cost money?"**
A: "No, the free tier is generous. You'd need to process 1,500 invoices today to hit limits."

**Q: "Can I use this for my company?"**
A: "This is a learning tool. For production, you'd need additional security, compliance, and error handling."

**Q: "Why didn't it find my invoice?"**
A: "Check: (1) Subject has 'invoice', (2) Email is unread, (3) Has PDF attachment"

---

## Troubleshooting Decision Tree

### Student: "It's not working!"

**Step 1: Identify Error Type**
- "What error message do you see?"
- "At which step did it fail?"

**Step 2: Common Fixes**

| Symptom | Quick Fix |
|---------|-----------|
| "Invalid API key" | Regenerate key at aistudio.google.com |
| "Gmail login failed" | Check 2FA enabled, create new app password |
| "Found 0 invoices" | Verify email is unread, has "invoice" in subject |
| "Loading forever" | Wait 60 sec, then refresh page |
| "Low confidence score" | This is normal! Explain it's AI being honest |

**Step 3: Nuclear Option**
If all else fails:
1. Clear browser cache/cookies
2. Use incognito window
3. Start fresh with new API key + app password

---

## Advanced Topics (Optional)

If students finish early or want to go deeper:

### Experiment 1: Model Comparison
- Process same invoice with all 4 models
- Compare accuracy, speed, confidence
- Discuss cost-benefit tradeoffs

### Experiment 2: Edge Cases
- Provide intentionally difficult invoices:
  - Low-quality scans
  - Unusual formats
  - Multi-page invoices
  - Non-English invoices

### Experiment 3: Business Case Analysis
Worksheet:
```
Scenario: Your company processes 500 invoices/month
Current process: 8 minutes per invoice @ $25/hour labor cost
AI process: 30 seconds per invoice @ $0.002 API cost

Calculate:
1. Current monthly labor cost: ___
2. AI monthly cost: ___
3. Monthly savings: ___
4. Annual ROI: ___
```

---

## Assessment Ideas

### Formative Assessment (During Lab)
- Monitor student progress
- Ask students to explain JSON output
- Check understanding of confidence scores

### Summative Assessment Options

**Option 1: Short Quiz**
1. What is an API key?
2. Why use app passwords instead of regular passwords?
3. What does a confidence score of 0.6 mean?
4. Name 2 limitations of AI invoice processing

**Option 2: Business Case Assignment**
"Write a 1-page memo to your CEO proposing AI invoice processing. Include: business problem, solution, ROI calculation, risks, and recommendation."

**Option 3: Technical Report**
"Test the invoice processor with 5 different invoices. Report accuracy, speed, and errors. Recommend which model to use for production."

---

## Safety & Ethics Discussion Points

### Privacy
- "What data does the AI see?"
- "How long is data stored?"
- "Who has access to your invoices?"

### Bias
- "Could AI discriminate against certain vendors?"
- "What if invoice is in a language AI doesn't know well?"

### Responsibility
- "Who's liable if AI makes an expensive mistake?"
- "Should humans always verify AI outputs?"

### Job Displacement
- "What happens to invoice processors when AI takes their jobs?"
- "How should companies handle workforce transition?"

---

## Post-Lab Follow-Up

### Within 24 Hours:
- [ ] Email lab materials to students
- [ ] Share application URL again
- [ ] Post FAQ updates based on common issues
- [ ] Collect student feedback

### Within 1 Week:
- [ ] Grade assignments (if applicable)
- [ ] Review student feedback
- [ ] Update lab materials for next semester
- [ ] Document lessons learned

---

## Backup Plans

### If Application Goes Down:
**Plan A:** Use screenshots/recorded demo  
**Plan B:** Reschedule lab for next class  
**Plan C:** Run application locally (if you have the setup)

### If WiFi Fails:
**Plan A:** Switch to mobile hotspot  
**Plan B:** Theory-only session with demo videos  
**Plan C:** Reschedule

### If Too Many Students Hit Rate Limits:
**Plan A:** Have students work in pairs  
**Plan B:** Use your backup API keys  
**Plan C:** Increase time between requests

---

## Learning Objectives Mapping

| Objective | Assessment Method |
|-----------|------------------|
| Obtain Gemini API key | Hands-on completion |
| Configure Gmail access | Hands-on completion |
| Understand AI extraction | Explain JSON output |
| Evaluate AI accuracy | Compare confidence scores |
| Recognize business value | Business case discussion |

---

## Resources for Further Learning

**For Students:**
- Google AI Studio: https://aistudio.google.com
- Gemini API Docs: https://ai.google.dev/docs
- Invoice Processing Best Practices: [provide link]

**For Instructors:**
- Prompt Engineering Guide: https://docs.anthropic.com/prompt-engineering
- AI Ethics Framework: [provide link]
- Industry Use Cases: [provide link]

---

## Contact & Support

**Technical Issues:**
- Email: [your email]
- Office Hours: [times]
- TA Support: [TA contact]

**Emergency Contact:**
- Phone: [your phone]
- Backup instructor: [name]

---

**Good luck with the lab!**

*This guide is a living document. Please share feedback and improvements.*

**Version:** 1.0 (December 2025)  
**Author:** Prof. Jack Lau  
**Course:** HKUST MBA - AI and Web Technologies
