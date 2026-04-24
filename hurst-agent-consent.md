# Messaging Opt-In and Consent — hurst-agent

## Service Description

`hurst-agent` is a private, single-recipient Python application that generates automated trading-system notifications from Hurst cyclic-analysis state transitions. Messages are sent via Twilio SMS (and optional email) only to the account owner's verified mobile number.

## Consent Model

There is one recipient: the account owner, David Alcindor.

- **Recipient number:** verified by the account owner at registration time with Twilio.
- **Sender number:** the account owner's own Twilio subaccount toll-free number.
- **Opt-in event:** the account owner configures the recipient number directly in GitHub Actions Secrets (a web form) as part of running the private agent on their own infrastructure. This configuration is the opt-in.
- **Distribution:** no third parties. No marketing. No resale. No user signups. No customer data.

## Opt-Out

The account owner can opt out at any time by:

- Replying `STOP` to any message from the sender number (Twilio honors `STOP` / `STOPALL` / `UNSUBSCRIBE` / `CANCEL` / `END` / `QUIT` keywords and halts delivery automatically), or
- Removing the recipient number from GitHub Actions Secrets, which stops dispatch at source.

## Help

Replying `HELP` to the sender number returns:

> Hurst signal alerts - personal-use single-recipient service. Reply STOP to unsubscribe.

## Contact

marketpredictiveanalysis@gmail.com

---

This document exists solely to describe the consent model for Twilio toll-free verification. No public claims are made; this service is not offered to the public.
