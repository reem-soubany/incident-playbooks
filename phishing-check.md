# Phishing Check

This playbook assumes a solo helpdesk with no email security portal. If MS365 Defender/AppRiver/Proofpoint is available, follow those instructions for immediate action.

**When to use:** User got a suspicious email or clicked a sketchy link.

**Pre-checks:**
1. Ask for the original email (.eml) or full headers
2. Confirm if the user replied or sent anything back
3. Check if the user entered their username/password or MFA thru linked page

**Steps:**
1.If user information was entered, reset password immediately & sign out of sessions
2. Review headers → look at Return-Path + SPF/DKIM/DMARC
3. Run anti-virus scan & review browser extensions
5. Block sender/domain if confirmed malicious
6. Report to security mailbox/provider

**Evidence:**
- Screenshot of header auth results.
- Ticket created: immediate steps & actions taken.

 _Last tested: April 2025_

