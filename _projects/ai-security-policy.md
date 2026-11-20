---
layout: page
title: AI Security Policy
caption: AI security assessment and acceptable use policy for a multi-brand restaurant group
description: >
  Researched and drafted an AI acceptable use policy for a multi-brand restaurant
  group, and presented it to the IT director.
date: 2026-11-20
permalink: /projects/ai-security-policy/
sitemap: false
---

<div class="term" style="margin-top:2rem">
<p class="t-bar"><span>Menu  Utilities  Options  Help</span><span>PRJ003</span></p>
<p class="t-cmd">Command ===&gt; <span class="t-wht">OPEN SECURITY.GOVERNANCE</span></p>
<p class="t-title" style="font-size:1.2rem;margin:.6rem 0 .4rem">AI Security Assessment and Acceptable Use Policy</p>
<p class="t-desc">Researched and drafted an AI acceptable use policy for a multi-brand restaurant group, and presented it to the IT director.</p>
<div class="t-who" style="margin-top:.9rem">
<span class="t-dim">ROLE</span><span>IT Intern</span>
<span class="t-dim">TIMELINE</span><span>July 2026</span>
<span class="t-dim">AUDIENCE</span><span>IT Director</span>
<span class="t-dim">SKILLS</span><span class="t-yel">Security governance, risk assessment, data classification, Microsoft 365 / Entra ID, AI security, policy writing</span>
</div>
<p class="t-pf"><span>F3=<a href="{{ '/' | relative_url }}">Back</a></span><span>F5=<a href="{{ '/assets/docs/cg-ai-acceptable-use-policy.pdf' | relative_url }}">Read the policy (PDF)</a></span></p>
</div>

## The problem

Leadership was exploring Claude, an AI assistant, for company-wide use and had open questions:

- How do we keep guest and employee data out of AI tools?
- What happens to data we upload?
- Can it safely connect to Microsoft 365 and our project management platform?
- How would we know if someone misused it?

Restaurants carry extra risk here. Card payment data, guest reservation and allergy details, and employee payroll records all move through a workforce spread across many locations, most of whom aren't office staff.

## My approach

1. **Answered leadership's questions one by one,** researching each against the vendor's published documentation for its business plans.
2. **Assessed the security controls available on each plan tier,** including SSO, MFA, provisioning, retention, audit logs, and data export.
3. **Evaluated the risks of each integration:** what the AI could read, what it could change, and who would have to approve it.
4. **Identified governance gaps** leadership hadn't raised yet: incident response, connector approval, contractor access, and legal liability.
5. **Drafted policy recommendations** and presented the research and draft to the IT director.

## Key decisions and why

### Managed accounts only, no personal AI accounts for work

Business plans fall under commercial terms that keep company chats out of model training. Personal accounts don't carry those protections, and IT can't see or control them.

### Connectors start read-only

Once an AI can read email and files, a malicious email can carry hidden instructions, a risk called *prompt injection*. Pairing that with write access (sending email, editing files) creates a path to data loss. Write actions are limited to approved roles, and auto-approve stays off.

### Fix permissions before connecting Microsoft 365

The connector uses delegated permissions: the AI sees whatever the signed-in user can see. Overshared SharePoint folders become AI exposure overnight, so permission cleanup has to come first.

### Plan around the controls you don't have

Audit logs and custom data retention are only available on the vendor's top tier. Instead of ignoring the gap, the policy adds **compensating controls**: monthly access reviews, same-day offboarding, and periodic review of exported conversation data.

### Training before access

A written policy tells people what not to do, but most data leaks come from honest mistakes. Requiring training and a short quiz before access, with re-acknowledgment every two months, targets the biggest real risk: the user.

## What I changed after presenting

After presenting, I revisited the draft and strengthened it:

- **Verified every product claim against official documentation.** One correction: only the organization's *Primary Owner* can export full conversation data, not all owners. And exports leave out deleted messages and AI-generated files, so they aren't complete monitoring on their own.
- **Removed advice to "ask the AI whether data is safe to share."** By the time the AI answers, the data has already been shared.
- **Added what the first draft missed:** payment card data (PCI DSS), prompt injection, shadow AI, offboarding, vendor certifications, and a step-by-step incident response process.
- **Found a Conditional Access gap:** Microsoft 365 location and network restrictions don't apply to the connector, because requests come from the vendor's IP addresses.
- **Restructured it into a standard policy format,** with scope, roles, data classification, enforcement, and a signature block.

## Outcome

The research and draft policy were presented to the IT director as input for the company's AI rollout planning. The policy was not formally adopted.

**What I learned:** security policy is mostly about people and defaults, not settings. The strongest controls were the simple ones: read-only by default, training before access, and a clear list of what never goes into an AI tool.

## The document

<div class="t-grid" style="margin:1rem 0">
  <a href="{{ '/assets/docs/cg-ai-acceptable-use-policy.pdf' | relative_url }}"><img src="{{ '/assets/img/projects/ai-policy/policy-page-1.png' | relative_url }}" alt="Page 1 of the CG AI Acceptable Use Policy: title, policy details table, purpose, scope, and definitions" loading="lazy" style="border:1px solid var(--term-frame-edge);border-radius:4px"></a>
  <a href="{{ '/assets/docs/cg-ai-acceptable-use-policy.pdf' | relative_url }}"><img src="{{ '/assets/img/projects/ai-policy/policy-page-2.png' | relative_url }}" alt="Page 2 of the CG AI Acceptable Use Policy: roles, approved tools, and acceptable use" loading="lazy" style="border:1px solid var(--term-frame-edge);border-radius:4px"></a>
</div>

**[Read the full policy (PDF, 7 pages)]({{ '/assets/docs/cg-ai-acceptable-use-policy.pdf' | relative_url }})**

*Company details have been replaced with a fictional organization, Camilotes Group, for public sharing.*
