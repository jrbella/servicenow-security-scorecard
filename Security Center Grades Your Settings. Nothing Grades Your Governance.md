# Your ServiceNow Instance Has a Security Posture. Most Teams Have Never Put a Number on It.

Most ServiceNow security conversations happen one layer up from where I want to focus today. We talk about the apps: an ACL on a custom table, a flow that should never have emailed production, a script running as the wrong user. That work matters. But underneath every app sits the instance itself, and the instance has a security posture of its own. Access control, authentication, session handling, hardening properties, service accounts, integrations, logging. Most teams know all of it matters. Very few can tell you, in a single number, how they are actually doing.

Ask "how secure is our instance" and you usually get a feeling instead of a measure. "Pretty solid." "We turned on the high security plugin." "We should probably clean up our service accounts." We know what's there, but it lives in scattered heads and never rolls up into one picture a team, or a leader, can point at.

ServiceNow does give you part of the answer. Security Center has a Hardening compliance score that grades your instance against recommended settings. It recalculates on a schedule you control, monthly by default, with a manual refresh available anytime. If you have never opened it, do that this week. It is the fastest read on your technical hardening you will get and probably one of the most undervalued products ServiceNow has to offer.

But a compliance score on settings is not the same as a view of your security posture. The hardening score is very good at the things it can check automatically. It says much less about the things that are organizational rather than technical: whether every service account has a named owner, whether credentials actually rotate, whether your security events reach a SIEM, whether anyone reviews who holds admin. Those are exactly the gaps I keep running into, and they are not a properties problem. They are a governance problem, and at a higher level, an organizational one.

So I built a scorecard to capture the whole picture, and I am sharing it.

It is a simple spreadsheet. 51 controls across 9 categories:

- Access Control
- Authentication
- Session Management
- Instance Hardening
- Service Account Governance
- Data Protection
- Integration and API Security
- Logging and Monitoring
- Email Security

You rate each control on a maturity scale from 0 to 3. The summary tab does the math and gives you an overall score, a maturity tier, and a breakdown by category. Open it, fill one column, and you have a picture in a few minutes.

A few choices in it are worth explaining, because the reasoning is the part you can reuse even if you never touch my version.

### Maturity, not pass or fail

Security is rarely binary. "Partially implemented" is a real and common state, and a 0 to 3 scale captures progress that a checkbox hides. It also makes the score move as you improve, which is the whole point of measuring.

### Weighted by criticality

Not every control carries the same risk. A missing default-deny model is not the same size problem as an unconfigured spam filter. Controls move the score in proportion to their criticality tier, Critical moves it more than High, and High more than Medium, so the number reflects risk rather than just counting boxes.

### Score only what applies

If a control does not apply to your instance, you mark it N/A and it drops out of the math entirely. You never get punished for something you do not run. This sounds small. It is the difference between a score people trust and a score people argue with.

### Service accounts get their own category

This is the area I care most about, and the one I see neglected most. Integration accounts with standing admin, no named owner, and credentials that have not changed in years are one of the quietest and largest risks in a mature instance. If your scorecard treats them as a footnote, your real posture is worse than your number says.

---

This is meant to be a self-assessment, not an audit. It measures what you believe your posture is, which is a useful and underrated thing to make explicit, but it is the start of a conversation, not a certificate. Run it once to get a baseline. Run it again next quarter and watch the trend. Movement is the real signal.

You can download it here: **[link]**. It is free. Use it, adapt it to your release and your risk profile, and tell me what you would change. I am especially interested in the controls you think I am missing.

## About this series

This scorecard is the hub of a series. Each category gets its own deep dive, where I walk through the controls on a demo instance and show what passing and failing actually look like. For categories a fresh instance starts empty on, like service accounts, I build the governed version from scratch on that same demo instance so you can see the before and after.

**Planned deep dives:**

- Access Control and Authorization
- Authentication and Identity
- Session Management
- Instance Hardening
- Service Account Governance
- Data Protection
- Integration and API Security
- Logging and Monitoring
- Email Security

I am also working on the next step, which is letting this run itself instead of asking you to fill it in by hand. More on that soon.

If instance security is part of your world, connect with me here: [linkedin.com/in/jeffrey-bella-965873112](https://www.linkedin.com/in/jeffrey-bella-965873112)