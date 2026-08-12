# Threat Detection Evidence

## Overview

This section documents the security threat-detection activities performed using Wazuh.

## Objective

The objective was to determine whether security-relevant activities generated within the controlled lab could be identified through endpoint telemetry and Wazuh detection rules.

## Detection Scenarios

Detection activities included:

- Authentication failures
- Repeated login attempts
- SSH-related activity
- Privileged Windows logons
- Linux sudo-to-root activity
- Account creation and modification
- Administrative group changes
- Controlled data-transfer indicators

## Authentication Detection

Authentication events were monitored to identify repeated failed logon attempts and other suspicious login behavior.

Repeated authentication failures can indicate password guessing or brute-force activity and therefore require SOC investigation.

## Privilege Escalation Detection

Linux privileged activity generated Wazuh alerts.

One observed rule was:

Rule ID: 5402

Description:
Successful sudo to ROOT executed.

MITRE ATT&CK:
T1548.003 - Sudo and Sudo Caching

This provided visibility into privileged activity occurring on the Linux endpoint.

## Windows Security Detection

Windows security telemetry provided visibility into privileged logons and account-related activity.

Relevant events included privileged authentication and account/security-group modifications.

## Account Manipulation

Controlled account activity was monitored to demonstrate detection of changes that could represent unauthorized account creation or privilege modification.

## MITRE ATT&CK

Where available, Wazuh MITRE ATT&CK mappings were reviewed to provide additional context regarding detected tactics and techniques.

## Evidence

The accompanying evidence PDF contains screenshots demonstrating authentication detection, privileged activity, account manipulation, and controlled data-transfer detection.

## Outcome

The detection phase demonstrated how centralized endpoint telemetry and SIEM rules can transform raw security events into actionable alerts for SOC investigation.
