
# Phishing Email Analysis Report

## 📧 1. Sample Phishing Email

**Subject:** Urgent! Your Account Will Be Suspended  
**From:** service@paypaI.com  

Dear Customer,

We detected unusual activity in your PayPal account.  
To secure your account, please confirm your details immediately by clicking the link below.  
If you do not act within 24 hours, your account will be permanently locked.

Click here to verify: http://secure-paypaI.com/verify  

Sincerely,  
PayPal Security Team

---

## 🔍 2. Phishing Indicators Found

### 2.1 Sender's Email Address (Spoofing)
- The email comes from `service@paypaI.com` which uses a capital **"i"** instead of a lowercase **"L"** in "PayPal".  
- This is a common spoofing technique used to deceive recipients.

### 2.2 Email Header Analysis (Using Online Tool)
**Tool Used:** [Google Admin Toolbox – Messageheader](https://toolbox.googleapps.com/apps/messageheader/)  

**Sample Header:**
```
Return-Path: <service@paypaI.com>
Received: from unknownhost.fakeisp.com (unknownhost.fakeisp.com [192.168.0.123])
Subject: Urgent! Your Account Will Be Suspended
From: "PayPal" <service@paypaI.com>
Reply-To: scammer@maliciousdomain.com
```

**Header Analysis Summary:**
- Return-Path mismatch indicates spoofing.
- IP address from untrusted host, not PayPal’s official servers.
- “Reply-To” points to a different domain (malicious).
- No SPF/DKIM authentication → Unverified sender.

### 2.3 Suspicious Link or Attachment
- The link `http://secure-paypaI.com/verify` is **not** a legitimate PayPal domain.
- It uses HTTP instead of HTTPS and a fake domain spelling.

### 2.4 Urgent or Threatening Language
- Words like "Urgent", "immediately", and "account will be permanently locked" are used to pressure the user.

### 2.5 Mismatched URLs
- Hovering over the link shows it points to a fake site not related to PayPal.
- Visual text and actual URL don’t match.

### 2.6 Spelling or Grammar Errors
- Slight unnatural grammar: "confirm your details immediately".
- Missing punctuation and slightly awkward wording.

---

## ✅ 3. Summary of Phishing Traits

- Spoofed sender address with deceptive domain name.
- Suspicious link not matching official brand website.
- Fear-inducing language to prompt immediate action.
- Generic greeting ("Dear Customer") instead of personalization.
- Header shows mismatched "From" and "Reply-To" fields.
- Slight grammar issues indicating low-quality, rushed message.

This email should be flagged as a phishing attempt and reported to the email provider or organization impersonated (PayPal in this case).
