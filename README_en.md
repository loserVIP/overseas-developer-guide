# Overseas Developer & Cross-Border Business Guide

[中文](README.md) ｜ Knowledge base: [fatevia.cn/en](https://fatevia.cn/en/)

> A practical checklist for indie developers, app teams and cross-border marketers: developer account registration and review, overseas ad accounts, Telegram bot development and quant tooling. Issues and PRs are welcome.

---

## Contents

- [1. Google Play Developer](#1-google-play-developer)
- [2. Apple Developer](#2-apple-developer)
- [3. Overseas Advertising](#3-overseas-advertising)
- [4. Telegram Bot & Mini App](#4-telegram-bot--mini-app)
- [5. Account Security Basics](#5-account-security-basics)
- [6. Further Reading & Services](#6-further-reading--services)

---

## 1. Google Play Developer

### Personal vs Organization account

| Item | Personal | Organization |
| :--- | :--- | :--- |
| Fee | USD 25 (one-time) | USD 25 (one-time) |
| Documents | Government ID | Business license + D-U-N-S number |
| Pre-launch testing | Closed testing required | Usually not required |
| Best for | Side projects, utility apps | Company products, finance/health apps |

Read more: [Personal vs Organization](https://fatevia.cn/en/blog/articles/google-play-personal-vs-organization-account.html) ｜ [Sign-up checklist](https://fatevia.cn/en/blog/articles/google-play-console-signup-checklist.html)

### Payment failed / card declined

1. Make sure the card supports international online payments.
2. Prefer a physical Visa / Mastercard; many virtual and prepaid cards are rejected.
3. Keep the billing address and cardholder name identical to your Google payments profile.
4. Repeated failures trigger risk control; wait 24 hours before retrying.
5. Check the exact error code in the Google Payments center.

Full guide: [Payment failed](https://fatevia.cn/en/blog/articles/google-developer-account-payment-failed-how-to-fix.html) ｜ [Card declined](https://fatevia.cn/en/blog/articles/google-developer-credit-card-declined.html)

### Closed testing for new personal accounts

- Current rule: at least **12 testers opted in for 14 consecutive days** before applying for production.
- Testers must actually install and open the app; inactive opt-ins do not count.
- Ship updates during the test and answer the production access questionnaire carefully.

See: [App publishing process](https://fatevia.cn/en/blog/articles/google-play-app-publishing-process.html)

### Organization accounts and D-U-N-S

- Legal name and address must match the D-U-N-S record exactly, including punctuation.
- Updates to D-U-N-S data may take several business days to sync.

See: [Organization account & D-U-N-S](https://fatevia.cn/en/blog/articles/google-play-organization-account-and-duns.html)

---

## 2. Apple Developer

| Type | Annual fee | Notes |
| :--- | :--- | :--- |
| Individual | USD 99 | Your legal name is shown on the App Store |
| Organization | USD 99 | Requires a D-U-N-S number |
| Enterprise | USD 299 | Internal distribution only, strict review |

- **Name mismatch**: your Apple ID name must match your legal ID. [Legal name tips](https://fatevia.cn/en/blog/articles/apple-individual-developer-legal-name-tips.html)
- **D-U-N-S lookup**: check Apple's lookup tool before requesting a new number. [D-U-N-S basics](https://fatevia.cn/en/blog/articles/apple-developer-duns-number-basics.html)
- **Enrollment**: [Step-by-step guide](https://fatevia.cn/en/blog/articles/apple-developer-program-enrollment-guide.html) ｜ [Which platform first?](https://fatevia.cn/en/blog/articles/choose-google-or-apple-developer-account-first.html)

---

## 3. Overseas Advertising

- **Search-intent demand** (tools, services, specific problems): start with Google Ads Search.
- **Impulse products** (fashion, gadgets, content): start with Facebook feed ads.
- Run a small 14-day test on either channel before scaling.
- Verify your Business Manager, enable 2FA, keep landing pages consistent with ad creatives, and scale budgets gradually.

See: [Facebook vs Google Ads](https://fatevia.cn/en/blog/articles/facebook-vs-google-ads-crossborder.html) ｜ [Google Ads accounts](https://fatevia.cn/en/google-ads-account/) ｜ [Facebook ad accounts](https://fatevia.cn/en/facebook-ads-account/)

---

## 4. Telegram Bot & Mini App

| Error | Cause | Fix |
| :--- | :--- | :--- |
| `429 Too Many Requests` | Rate limit exceeded | Wait `retry_after` seconds, then retry |
| `403 Forbidden: bot was blocked by the user` | User blocked the bot | Mark the user unreachable and stop sending |
| `400 Bad Request: chat not found` | Bot not in the chat, or wrong chat_id | Add the bot to the group/channel as admin |

- Rate limits: about 1 msg/s per chat, 20 msg/min per group, ~30 msg/s overall for broadcasts.
- Always validate Mini App `initData` on the server (HMAC-SHA256 with a key derived from `WebAppData` and your bot token).
- Never expose the bot token to the frontend or commit it to a repository.

See: [Telegram bot development](https://fatevia.cn/en/telegram-bot-development/)

---

## 5. Account Security Basics

- Use a dedicated email and phone number per account, with 2FA enabled.
- Do not share payment methods or login devices across accounts.
- Keep copies of all documents submitted during registration for future re-verification.

See: [Developer account security basics](https://fatevia.cn/en/blog/articles/developer-account-security-basics.html)

---

## 6. Further Reading & Services

| Area | Scope | Link |
| :--- | :--- | :--- |
| Developer accounts | Google Play / Apple registration consulting | [Google Play](https://fatevia.cn/en/google-play-developer-account/) ｜ [Apple](https://fatevia.cn/en/apple-developer-account/) |
| Advertising | Google Ads / Facebook account consulting | [Google Ads](https://fatevia.cn/en/google-ads-account/) ｜ [Facebook](https://fatevia.cn/en/facebook-ads-account/) |
| Custom development | Telegram bots, Mini Apps | [View](https://fatevia.cn/en/telegram-bot-development/) |
| Quant tools | Exchange API automation, backtesting | [View](https://fatevia.cn/en/quant-software-custom/) |

- All articles: [fatevia.cn/en/blog](https://fatevia.cn/en/blog/)
- Contact: Telegram [@FaceLuck](https://t.me/FaceLuck)

---

## Contributing

Issues and PRs are welcome. Content is for reference only; always follow each platform's official policies.
