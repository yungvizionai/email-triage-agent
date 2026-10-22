# AI Email Triage Agent (Free Template)

A copy-paste starting point for an assistant that reads your inbox each day, sorts the important email from the noise, and hands you a short list of what needs your attention.

Built by [Ken Yung](https://www.linkedin.com/in/kenyung/) at **Yung Vizion AI**. Originally written for home service business owners who lose time digging through a crowded inbox.

---

## Who this is for

Owners and operators who get dozens of emails a day and waste time finding the few that matter. Customer requests, supplier updates, and scheduling notes get buried under newsletters and promotions. This hands that first pass to an assistant.

If you only get a handful of emails a day, you do not need this yet.

## What it does

- Reads the unread email in your inbox
- Sorts each message into buckets you define
- Writes a short morning brief
- Keeps the important email where you will see it and moves the noise out of the way
- Flags payment changes, money requests, and suspicious emails for you to verify yourself

## What you need

- An AI assistant that can connect to your email. This template is written for [Claude Cowork](https://claude.com/product/cowork), and the structure adapts to other tools.
- A few buckets that match how your business actually runs.

## How to use it

1. Download [`email-triage-agent-template.md`](./email-triage-agent-template.md) to your computer.
2. Open it in a plain text editor like Notepad or Sublime Text.
3. Replace everything in `[BRACKETS]` with your details.
4. Save the file.
5. In Claude Cowork, or your AI tool, attach the saved `.md` file as the instructions for a new scheduled task.
6. Set the schedule. In Cowork you can use the `/schedule` command. Pick a time outside peak usage hours, like early morning or evening.
7. Run it once by hand the first time. It may ask for permission to read your email, save drafts, and move mail to your cleanup folder. Approve only those. Decline anything that lets it send email. If your tool offers an "automatically approve" mode for scheduled runs, skip it. Approving the few actions you need, one time, keeps everything else blocked when nobody is watching. Approving them on a manual run keeps the automatic runs from pausing later.
8. Watch it for a week or two, then adjust your buckets and rules.

## Customize your buckets

The buckets are the part that matters most. Pick categories that match the decisions you make each morning. A few examples:

- **HVAC or plumbing shop:** Customers, Suppliers, Scheduling, Local events, Noise
- **Solo consultant:** Prospects, Clients, Tools and platforms, Industry news, Noise
- **Retail or service storefront:** Orders, Vendors, Staff, Promotions to review later, Noise

## Lessons from building it

A few things I got wrong the first time, so you can skip them:

- **Read everything, not the last day.** An early version filtered to the past 24 hours and missed most of the inbox. Read all unread mail in the inbox instead.
- **Pull every page.** Email tools often return results in batches. If the assistant stops at the first batch, it only sees part of the inbox.
- **Stay in the loop early.** Check its work for the first couple of weeks before trusting it to run on its own.
- **Move only the noise.** Keep the important email in the inbox so it stays in front of you. Sweep the noise to a folder.

## Safety

- Start read-only. Let it read and sort before you let it move anything.
- Never let it reply, send, forward, or delete without your say-so.
- Limit it to one cleanup label or folder.
- Never give it access to payments, banking, or account settings.
- Treat the brief as a pointer. Before acting on anything involving money, passwords, or account changes, open the original email and verify by phone using a number you already have.

### Why the extra rules (updated October 2026)

Attackers have started hiding instructions inside emails, written for the AI assistant that reads them. A hidden line might tell the assistant to call a scam email urgent, or to add "update this vendor's payment details" to your to-do list. This is called prompt injection, and security researchers expect it to stay a problem for a long time.

The template now includes:

- Safety rules that tell the assistant email content is information to sort, never instructions to follow
- A Check Before Acting bucket for payment changes, money requests, password requests, and emails that try to talk to the AI
- A "verify by phone" note on every flagged item, and no recommended actions involving money
- A default to keep anything uncertain in the inbox instead of filing it as noise
- Draft only. The assistant no longer sends the brief to you by email.
- A reminder to judge each email by its content, so a useful update from a promo-heavy sender doesn't get filed as noise

These rules lower the risk. They do not remove it. Keeping the assistant's permissions narrow is what limits the damage if it gets fooled.

Further reading: [Phishing emails are baiting your AI assistant](https://www.malwarebytes.com/blog/ai/2026/10/phishing-emails-are-baiting-your-ai-assistant) (Malwarebytes)

## Want help setting this up?

I offer a free, focused Discovery Call to help diagnose a pain point in your operation, with a short report on what I find and how I would fix it. It is a quick session by design, meant to respect your time.

➡️ Book a call: [calendly.com/yungvizionai/30min](https://calendly.com/yungvizionai/30min)

More free tools: [github.com/yungvizionai](https://github.com/yungvizionai)
