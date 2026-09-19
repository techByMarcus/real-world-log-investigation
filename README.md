# Authentication Log Investigation

A simulated SOC case involving repeated failed login attempts followed by a successful login from an unfamiliar IP address.

This repository documents how I worked through the alert, what evidence was available, why the sequence was suspicious, and what I would verify next in a production environment.

## Alert Summary

The alert involved three important observations:

1. Multiple failed authentication attempts
2. Repeated activity from the same source IP
3. A successful login after the failed attempts from an IP address not previously associated with the user

The investigation question was whether the sequence could be explained by normal user behavior or whether it was more consistent with credential compromise.

## Evidence Reviewed

| Evidence | Why it mattered |
| --- | --- |
| Repeated failed logins | Established that the activity was not a single mistyped password |
| Same source IP across attempts | Showed concentration of activity from one source |
| Short time window | Made automated or repeated guessing more plausible |
| Successful login after failures | Increased the risk that valid credentials had eventually been used |
| Unfamiliar source IP | Made the successful authentication less consistent with known user behavior |
| Prior login pattern | Provided a baseline for deciding whether the source was unusual |

## Investigation

I started with the failed authentication events and looked for repetition: whether the failures came from one source or several, how closely they occurred together, and whether the same account was involved.

The failed attempts were concentrated around the same source and occurred in a short period. I then reviewed the later successful authentication. Because the success followed the failures and came from an unfamiliar IP address, I treated the event as more serious than a routine password mistake.

At that point, the evidence supported escalation, but it still did not prove who was behind the login. In a real SOC, I would need additional context before calling the account definitively compromised.

## Analyst Assessment

**Disposition:** Likely true positive — potential account compromise.

The strongest indicator was the sequence itself: repeated failures followed by a successful authentication from an unfamiliar source.

I would escalate the alert for additional validation rather than close it as benign.

## Recommended Response

Immediate actions would depend on the environment and the account involved, but the next steps I would recommend are:

- Validate the login with the account owner
- Review successful and failed authentication activity before and after the event
- Reset credentials if the login cannot be verified
- Require or confirm multi-factor authentication
- Review whether the source IP appears against other users or systems
- Restrict or block the source if it is confirmed malicious
- Monitor the account for follow-on activity

## What I Would Verify in Production

Before finalizing the incident, I would want additional telemetry and business context:

- VPN or remote-access logs
- Device identity and endpoint telemetry
- Whether the source belongs to approved corporate infrastructure
- Whether the account is privileged
- Geolocation and impossible-travel indicators
- Any privilege changes, mailbox activity, file access, or lateral movement after the successful login
- Threat-intelligence context for the source IP

That distinction matters: the lab evidence was enough to justify escalation, but not enough to claim complete attribution or prove every stage of an account compromise.

## Scope

This is a **simulated training investigation**, not production SOC casework.

The repository is intended to show the decision process behind the alert review: identify the pattern, compare it with expected behavior, determine what the evidence supports, and document what additional information is still needed.

## Video Walkthrough

A walkthrough of the investigation is included in this repository:

[View the repository video](./finalsimpresentation.mp4)

An external copy is also available here:

[Watch the walkthrough on OneDrive](https://1drv.ms/v/c/6300dd9e66455bb4/IQBN5gGwLOtSRY9s3RrkyAuFAXWsjNEHSijdlywmsVKI5bc?e=OQwwft)

## Related Work

- [SOC Analyst Portfolio](https://github.com/techByMarcus/soc-analyst-portfolio)
- [Security Audit Tool](https://github.com/techByMarcus/security-audit-tool)
- [Portfolio](https://techbymarcus.github.io/aboutMarcus/)
