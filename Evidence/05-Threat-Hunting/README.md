# Threat Hunting Evidence

## Overview

This section documents threat hunting and security-event investigation performed using Wazuh.

## Objective

The objective was to move beyond individual alerts and investigate related activity across endpoints, accounts, timestamps, and security events.

## Threat Hunting Activities

Activities included:

- Reviewing Wazuh security alerts
- Filtering events by rule ID
- Filtering by endpoint and user
- Reviewing authentication failures
- Investigating privileged activity
- Reviewing account modifications
- Correlating related security events
- Establishing event timelines
- Validating alerts against endpoint evidence

## Rule-Based Investigation

Wazuh rule IDs were used to isolate relevant events.

For example:

Rule ID: 5402

Description:
Successful sudo to ROOT executed.

Filtering on specific rules allowed security-relevant events to be separated from unrelated telemetry.

## Authentication Investigation

Authentication activity was reviewed to identify:

- Failed authentication attempts
- Successful authentication
- Repeated login activity
- SSH-related events
- Associated users and endpoints

## Privilege Investigation

Privilege-related events from Windows and Linux systems were reviewed to identify elevated access and determine whether the activity was expected.

## Event Correlation

Related events were correlated using:

- Timestamp
- Agent
- IP address
- User
- Rule ID
- Windows Event ID
- Authentication information
- Privilege activity
- Account modifications

## Investigation Workflow

The threat-hunting workflow followed:

1. Identify the alert.
2. Review severity and affected endpoint.
3. Filter relevant Wazuh events.
4. Review normalized event information.
5. Validate against endpoint evidence.
6. Correlate related activity.
7. Establish a timeline.
8. Determine the significance of the activity.
9. Document the findings.

## Evidence

The accompanying evidence PDF contains screenshots demonstrating Wazuh Threat Hunting, filtering, authentication analysis, privilege investigation, and event correlation.

## Outcome

The exercise demonstrated how SIEM telemetry can be systematically investigated to determine the context and significance of security alerts.
