

# Chargeback Alert System

> AI-powered chargeback risk detection for merchants - Prevent false chargebacks before they happen

![Demo](https://img.shields.io/badge/demo-live-brightgreen) ![React](https://img.shields.io/badge/react-18.3.1-blue) ![License](https://img.shields.io/badge/license-MIT-green)

## The Problem

**Chargebacks cost merchants $31 billion annually.** By the time a chargeback happens, merchants have already:
- Lost the product/service  
- Paid processing fees ($15-100 per dispute)  
- Damaged their merchant account standing  
- Spent hours fighting the dispute  

**Small businesses can't absorb these losses.** Prevention is better than fighting disputes after the fact.

---

## The Solution

This system analyzes transactions **before processing** to identify patterns that typically lead to chargebacks:

 Mismatched billing/shipping addresses  
 High-value orders from new customers  
 Customer chargeback history  
 Card-not-present vs in-person transactions  
 Suspicious transaction velocity    

**Result:** Merchants can flag risky transactions for additional verification, preventing chargebacks before they occur.

---

## Why This Matters for Block/Square

Merchants face chargeback risk daily:

 **Protecting small businesses** from fraud losses  
 **Reducing chargeback rates** (keeps merchant accounts healthy)  
 **Improving payment security** without adding friction  
 **Empowering merchants** with AI-powered risk intelligence previously only available to large enterprises  

---

## How It Works

### 1. Rule-Based Scoring (Transparent & Explainable)
```
High amount (>$800) → +30 points
Card-not-present → +20 points
Mismatched addresses → +15 points
Prior chargebacks → +30 points
New customer → +10 points
```

### 2. Risk Assessment
- **Score 0-29:** LOW risk → Approve automatically
- **Score 30-59:** MEDIUM risk → Standard processing
- **Score 60-100:** HIGH risk → Flag for manual review

### 3. Actionable Recommendations
- Specific factors that raised the score
- Clear merchant guidance (approve/review/verify)
- Transparent reasoning for every decision

---

## Key Features

 **Real-Time Risk Scoring** (0-100 scale with color-coded alerts)  
 **Explainable AI** (shows exactly why a transaction is risky)  
 **Risk Factor Detection** (identifies specific red flags)  
 **Merchant Recommendations** (approve/review/decline guidance)  
 **Square-Style Demo** (pre-loaded scenarios: coffee shop, electronics, gift cards)  
 **Zero Dependencies** (no API keys required - runs 100% client-side)  
 **Mobile Responsive** (works on any device)  

---

## Demo Scenarios

### 🟢 Low Risk (Score: 3)
**Scenario:** In-person coffee purchase, $8, loyal customer  
- Channel: POS (in-person)
- Customer: Returning with 24 transactions in 30 days
- History: Zero chargebacks
- **Recommendation:** Approve

### 🟡 Medium Risk (Score: 55)
**Scenario:** Large online electronics order, $950, new customer  
- Channel: Online (card-not-present)
- Customer: First-time buyer
- Addresses: Billing (Austin) ≠ Shipping (Dallas)
- **Recommendation:** Flag for review

### 🔴 High Risk (Score: 70)
**Scenario:** Online gift card, $300, prior chargebacks  
- Channel: Online
- Customer: 2 previous chargebacks
- History: 5 transactions in 30 days (velocity concern)
- **Recommendation:** Flag for manual review or additional verification

---

## Screenshots

### Transaction Analysis
*Coming soon - add after deployment*

### Risk Score Display
*Coming soon - add after deployment*

---

## Tech Stack

- **Frontend:** React 18.3.1
- **Risk Engine:** Rule-based algorithm (100% transparent)
- **Styling:** Custom CSS 
- **Deployment:** Netlify 
- **Version Control:** Git + GitHub

---

## Local Setup

```bash
# Clone repository
git clone https://github.com/AnyoBell/chargeback-alert-system.git
cd chargeback-alert-system

# Install dependencies
npm install

# Run development server
npm start
```

Visit `http://localhost:3000`

**Note:** No API keys required! The system uses rule-based logic that runs entirely in your browser.

---

**For this demo:**
 **Transparent** - Merchants can see exactly why a transaction is flagged  
 **Fast** - No API latency or rate limits  
 **Reliable** - No dependency on external services   
 **Configurable** - Easy to tune for specific merchant needs  

**Production Evolution:**
This rule-based foundation can be enhanced with:
- Integration with Square's historical chargeback data
- Real-time device fingerprinting
- Email/phone verification APIs
- AI-powered pattern recognition 

---

## What I Learned

**Challenge:** Balancing false positives vs false negatives  
**Solution:** Tiered risk levels - not every flag requires decline, just review

**Challenge:** Making risk assessment transparent for merchants  
**Solution:** Show exact factors and point values 

**Challenge:** Designing for real merchant workflows  
**Solution:** P

---

## Future Improvements

- [ ] **Dashboard view:** Track risk scores over time
- [ ] **Batch processing:** Analyze multiple transactions at once
- [ ] **Historical analysis:** Learn from merchant's actual chargeback history
- [ ] **Integration APIs:** Connect with Square/Stripe webhooks
- [ ] **Email verification:** Check if email domain matches billing region
- [ ] **Device fingerprinting:** Track device IDs for repeat fraud patterns
- [ ] **ML enhancement:** Add machine learning layer for pattern detection
- [ ] **SMS alerts:** Notify merchants of critical risks in real-time

---

## Why I Built This

As someone passionate about fintech and accessibility, I wanted to explore how intelligent systems can protect small businesses—not just banks and large enterprises. 

Chargebacks disproportionately hurt small merchants who can't absorb fraud losses. A coffee shop losing $1,000 to a false chargeback might be their entire day's profit.

This aligns perfectly with Block's mission of economic empowerment: **giving small merchants access to tools that were previously only available to big players.**




