# Sample Invoice Template for Lab Testing

This template can be used to create test invoices for students. Use invoice-generator.com or any invoice creation tool.

---

## Sample Invoice #1: Standard Consulting Invoice

**Recommended for:** First test, baseline accuracy check

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                      INVOICE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

FROM:
Nexus Path Consulting Group LLC
123 Innovation Drive, Suite 400
San Francisco, CA 94105
USA
Tax ID: 12-3456789

BILL TO:
HKUST Business School
Clear Water Bay
Kowloon, Hong Kong

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Invoice Number:    INV-2024-001
Invoice Date:      November 15, 2024
Due Date:          December 15, 2024
Payment Terms:     Net 30

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

DESCRIPTION                           QTY    RATE        AMOUNT
─────────────────────────────────────────────────────────────
Strategy Consulting Hours              60    $350.00    $21,000.00
Workshop Facilitation                   1  $8,500.00     $8,500.00
Travel & Accommodation Expenses         1     $70.50        $70.50

                                              SUBTOTAL:  $29,570.50
                                   Tax (8.875% NY):       $2,624.38
                                              ─────────────────────
                                         TOTAL DUE:      $32,194.88

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PAYMENT INSTRUCTIONS:
Wire Transfer to:
Bank of America
Account: 123456789
Routing: 987654321
SWIFT: BOFAUS3N

NOTES:
Thank you for your business. Payment is due within 30 days.
For questions, contact: billing@nexuspath.com

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Expected AI Output:**
- Invoice Number: INV-2024-001
- Vendor: Nexus Path Consulting Group LLC
- Invoice Date: 2024-11-15
- Due Date: 2024-12-15
- Subtotal: 29570.50
- Tax: 2624.38
- Total: 32194.88
- Confidence: >0.95

---

## Sample Invoice #2: Simple Product Invoice

**Recommended for:** Testing product-based invoices

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TechGear Solutions Ltd.
456 Commerce Street
Austin, TX 78701
www.techgear.com

                         SALES INVOICE

Invoice #: TG-2024-0542
Date: December 1, 2024
Customer PO: PO-9876

SOLD TO:
Hong Kong University of Science and Technology
Procurement Department
Clear Water Bay, Kowloon
Hong Kong

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ITEM                    QTY    UNIT PRICE    TOTAL
─────────────────────────────────────────────────────
Laptop Computer - Pro    25      $1,299.00   $32,475.00
Wireless Mouse           25        $45.00    $1,125.00
USB-C Adapter            25        $29.99      $749.75
Laptop Bag               25        $79.00    $1,975.00

                                   Subtotal:  $36,324.75
                              Shipping (5%):   $1,816.24
                             Sales Tax (7%):   $2,543.73
                                   ─────────────────────
                              AMOUNT DUE:     $40,684.72

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Payment Due: December 31, 2024 (Net 30)
Payment Method: Credit Card / Bank Transfer

Questions? Contact: accounts@techgear.com | (512) 555-0199
```

**Expected AI Output:**
- Invoice Number: TG-2024-0542
- Vendor: TechGear Solutions Ltd.
- Date: 2024-12-01
- Due Date: 2024-12-31
- Subtotal: 36324.75
- Tax: 2543.73 (note: may combine shipping into tax)
- Total: 40684.72
- Confidence: >0.90

---

## Sample Invoice #3: Service Invoice (Monthly Recurring)

**Recommended for:** Testing subscription/recurring service invoices

```
CloudServe Technologies Inc.
789 Digital Avenue
Seattle, WA 98101
EIN: 98-7654321

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                   MONTHLY SERVICE INVOICE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Invoice #: CS-2024-NOV-8821
Billing Period: November 1-30, 2024
Invoice Date: November 30, 2024
Payment Terms: Due on Receipt

CUSTOMER:
HKUST IT Department
Clear Water Bay
Hong Kong

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

SERVICE DESCRIPTION                                    AMOUNT
─────────────────────────────────────────────────────────────
Cloud Storage (500GB @ $0.10/GB)                      $50.00
API Calls (250,000 @ $0.0001/call)                    $25.00
Database Hosting (Premium Tier)                      $199.00
Technical Support (10 hours @ $95/hr)                $950.00
SSL Certificates (5 domains)                          $75.00

                                         Subtotal:  $1,299.00
                                      Discount (10%):  -$129.90
                                   Tax (WA 10.5%):     $122.81
                                         ───────────────────
                                    TOTAL DUE:      $1,291.91

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Auto-Pay: This invoice will be charged to credit card ending in 4567
Next billing date: December 30, 2024

Support: support@cloudserve.com | 1-800-CLOUD-99
```

**Expected AI Output:**
- Invoice Number: CS-2024-NOV-8821
- Vendor: CloudServe Technologies Inc.
- Date: 2024-11-30
- Subtotal: 1299.00 (may vary due to discount handling)
- Tax: 122.81
- Total: 1291.91
- Confidence: 0.85-0.95 (monthly recurring format may reduce confidence)

---

## Sample Invoice #4: Multi-Currency International Invoice

**Recommended for:** Testing currency handling and international formats

```
╔════════════════════════════════════════════════════════════╗
║              HONG KONG CONSULTING LIMITED                  ║
║         香港諮詢有限公司                                     ║
╚════════════════════════════════════════════════════════════╝

Unit 2501, 25/F, Central Plaza
18 Harbour Road, Wan Chai
Hong Kong SAR
Company Registration: 12345678

────────────────────────────────────────────────────────────

                         TAX INVOICE

Invoice Number:    HK-INV-2024-1205
Date of Issue:     5 December 2024
Due Date:          4 January 2025 (Net 30)

BILL TO:
Massachusetts Institute of Technology
77 Massachusetts Avenue
Cambridge, MA 02139, USA

────────────────────────────────────────────────────────────

DESCRIPTION                         QTY    RATE         TOTAL
═══════════════════════════════════════════════════════════
Research Collaboration Fee            1   HKD 50,000   50,000.00
Translation Services (Eng-Chi)       40    HKD 800     32,000.00
Project Management                   20    HKD 1,200   24,000.00

                                           SUBTOTAL:   106,000.00 HKD
                                                  ═══════════════════
                                        TOTAL DUE:   106,000.00 HKD

────────────────────────────────────────────────────────────

Exchange Rate Reference: 1 USD = 7.8 HKD (Approx. USD 13,589.74)

PAYMENT DETAILS:
Bank: HSBC Hong Kong
Account Name: Hong Kong Consulting Limited
Account Number: 123-456789-001
SWIFT: HSBCHKHHHKH

No tax applicable (Hong Kong has no sales tax/VAT)

For inquiries: admin@hkconsulting.hk | +852 2234 5678
```

**Expected AI Output:**
- Invoice Number: HK-INV-2024-1205
- Vendor: Hong Kong Consulting Limited
- Date: 2024-12-05
- Due Date: 2025-01-04
- Currency: HKD
- Subtotal: 106000.00
- Tax: 0.00
- Total: 106000.00
- Confidence: 0.80-0.90 (international format may reduce confidence)

---

## Sample Invoice #5: Edge Case - Complex Multi-Page Invoice

**Recommended for:** Advanced testing, understanding AI limitations

**Characteristics:**
- Multi-page (2-3 pages)
- Detailed line items (20+ items)
- Multiple tax rates
- Itemized discounts
- Complex payment terms

**Notes for Instructors:**
This should be created as a real PDF with:
- Page 1: Header, customer info, first 10 line items
- Page 2: Remaining line items, subtotals
- Page 3: Tax breakdown, payment terms, footer

**Expected Behavior:**
- Confidence: 0.70-0.85 (complexity reduces confidence)
- May miss some line items
- May struggle with multi-page totals
- Good teaching moment about AI limitations!

---

## How to Use These Templates

### Option 1: Use Invoice Generator Website
1. Go to: https://invoice-generator.com
2. Copy the template details
3. Fill in the form
4. Download PDF

### Option 2: Create in Word/Google Docs
1. Copy template text
2. Format as needed
3. Save/Export as PDF

### Option 3: Use Professional Tools
- QuickBooks
- FreshBooks
- Wave
- Zoho Invoice

---

## Email Template for Sending to Students

**Subject:** Test Invoice for AI Lab

**Body:**
```
Hi [Student Name],

Here is a sample invoice for testing the Invoice Processor Lab.

Instructions:
1. Download the attached PDF
2. Forward this email to yourself (or attach PDF to new email)
3. Make sure subject line contains "invoice"
4. Keep the email UNREAD
5. Use the lab application to process it

Expected results are documented in the lab materials.

Good luck!

Prof. Lau
```

---

## Testing Checklist for Instructors

Before the lab, test each invoice:

- [ ] Sample #1: Standard consulting (baseline test)
- [ ] Sample #2: Product invoice (different format)
- [ ] Sample #3: Recurring service (subscription format)
- [ ] Sample #4: Multi-currency (international handling)
- [ ] Sample #5: Complex multi-page (edge case)

Verify:
- [ ] All invoices parse successfully
- [ ] Confidence scores are reasonable (>0.7)
- [ ] Key fields extracted correctly
- [ ] Edge cases demonstrate AI limitations appropriately

---

**Recommendation:** Start students with Sample #1, then let them explore #2-#4. Use #5 for advanced students or discussion of limitations.

**Version:** 1.0 (December 2025)
