---
title: Migrating to 1Password
date: 2020-04-19
---

One of my 2020 resolution was to start using secure passwords and 2FA (Two Factor Authentication) on every site where I had an account. I had been meaning to do this for a while, the final push came when I received a free 1Password family account.

Essentially, this meant
- Find all there sites where I had an account
- Change the password
- Enable 2FA

### Finding all the accounts
I have been active on the internet for 15 years now and that meant - _a lot of accounts!_ 

I broke this problem down into 3 steps
- Compile the list frequently visited sites that were on the top of my mind (Netflix, Amazon, Flipkart, Swiggy, banking portals, etc.)
- Look for mails tagged as "Updates" or "Promotional" in my Gmail, check browser history
- Change as I go for the sites/apps not in the first 2

The shortlist came to ~25 accounts.

### Changing the password
As a matter of shame, changing the passwords was a breeze since I had re-used 3-4 passwords (with some variations in casing or numbers).

I used 1Password's "Suggested Password" feature to do this. The only hiccups where when few sites insisted on a restricted character set or a "strong password policy" that required a few iteration of suggestions.

### Enabling 2FA
I chose to enable 2FA only for sites
- that could somehow debit me (banking websites, had saved card details, etc.)
- had PII that I cared about (FB, Twitter, etc.)

I chose to use 1Password's 2FA helper on sites where TOTP was available as a mode of authentication. This is probably not very wise to couple both factors behind a single source.

I made sure to take a physical print of the backup codes.

### Bonus 
For good measure, I deactivated more 40 accounts that I no longer used. Some made it easy by enabling deactivation was a self-serve process while others required to... _cringe_... write a support ticket.

### The good and the bad and the ugly
I have 60ish accounts enabled in my 1Password. Not having to type out my credentials is an usability win for me apart from the obvious security improvement. I've the 1Password companion app my phone that makes the process easier on mobile.

The biggest "bang my head" moment was in signing into Netflix on my Android TV & Fire stick. Netflix doesn't provide a login via device option and typing a long password via arrow keys was sufficiently frustrating for me to go back to a manual, smaller length password.

Though, HDFC NetBanking & Income Tax Portal took the cake for the ugly. Both of them trying a fancy client side hash of password on an `onchange` trigger of the password field. This did not play well with the password manager and I switched to bespoke passwords for them.

### Recommendations
How do you decide it's for you? You should use a password manager
- If you see breaches on (https://haveibeenpwned.com/)[https://haveibeenpwned.com/].
- If you reuse the same/similar password across websites, especially ones that can make you lose money.
- If you frequently forget your password.
- If you are paranoid.  