# Password Reset Playbook

**When to use:** User can’t sign in / forgot password / account locked.

**Pre-checks:**
1. Confirm user identity
2. Check if account is locked or disabled
3. Confirm MFA method available

**Steps:**
1. Open: Azure AD → find user
2. Reset password. Require change at next sign-in
3. If locked: unlock account
4. Ask user to sign out everywhere, then retry

**Edge cases I’ve seen:**
- Time skew on laptop breaks sign-in → sync time, retry.
- VPN cached creds → disconnect VPN, sign in, reconnect.

**Rollback:**
- Reset password again in AD and require change at next sign-in
- Make sure the account isn't locked/disabled

**Evidence to capture:**
- Screenshot of successful sign-in timestamp
- Ticket created: cause (forgot/lockout), fix steps

_Last tested: April 2025_
