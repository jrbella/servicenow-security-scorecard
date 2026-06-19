# ServiceNow Instance Security Scorecard

A self-assessment that measures the part of ServiceNow instance security nobody else measures.

ServiceNow already grades your technical hardening settings. Security Center gives you a compliance score and it usually sits in the high 80s out of the box. What nothing measures is the governance layer: whether every service account has a named owner, whether credentials rotate, whether anyone reviews who holds admin, whether your security events reach a SIEM. None of that is a setting, so nothing scores it, and that is exactly where the real risk in a mature instance lives. This scorecard makes that layer visible.

## Download

Grab the latest version from the [Releases page](RELEASE_LINK_HERE). Download the `.xlsx`, open it, and you have a picture of your posture in a few minutes. No instance access, no install.

## What it is

A spreadsheet covering 51 controls across 9 categories: Access Control, Authentication, Session Management, Instance Hardening, Service Account Governance, Data Protection, Integration and API Security, Logging and Monitoring, and Email Security. You rate each control on a maturity scale, and the summary does the math.

## What's inside

- Start Here: how to use it and how scoring works.
- Scorecard: the 51 controls. You fill the maturity column. Each row tells you where to check the setting in your instance.
- Summary: your overall score, maturity tier, a category breakdown, and a chart, all calculated automatically.

## How to use it

1. Download and open the file.
2. On the Scorecard tab, set Maturity from 0 to 3 for each control, in the yellow column. Mark anything that does not apply to your instance as N/A and it drops out of the math.
3. The Summary tab updates as you go.
4. Re-run it quarterly and watch the trend. Movement matters more than any single number.

The fastest way to assess the technical settings is Security Center > Hardening, which scores many of them for you. The governance rows, especially Service Account Governance, are manual, and they are where the score actually separates a strong instance from a weak one.

## How scoring works

Each control is weighted by criticality: Critical counts for more than High, which counts for more than Medium. Your score is the percent of the maximum possible, which rolls up to a maturity tier from At Risk to Optimized. Controls marked N/A are excluded entirely, so you are never penalized for something you do not run.

## Honest framing

This is a self-assessment, not an audit. It measures what you believe your posture is, which is a useful and underrated thing to make explicit, but it is the start of a conversation, not a certificate. Adapt the controls to your release, plugins, and risk profile.

## Read the full write-up

The thinking behind the scorecard, and a control-by-control walkthrough series, lives here: [Read the full write-up](ARTICLE_LINK_HERE). Each category gets its own deep dive on a live instance, showing what passing and failing actually look like.

## Use and adapt

Free to use, share, and adapt for your own environment. Attribution is appreciated. 

## Versions

Releases are tagged and the release notes serve as the changelog. Current: v1.0.

## About

Built by Jeffrey Bella II, focused on ServiceNow instance security governance. Connect: https://www.linkedin.com/in/jeffrey-bella-965873112
