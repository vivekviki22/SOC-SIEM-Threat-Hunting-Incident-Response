# Incident Response Evidence

## Overview

This section documents the incident-response process applied to security events generated and investigated during the SOC and SIEM project.

## Objective

The objective was to demonstrate how detected security events can progress from SIEM alerts into structured investigation and response activities.

## Incident Response Lifecycle

The project followed the following lifecycle:

1. Identification
2. Analysis
3. Containment
4. Eradication
5. Recovery
6. Lessons Learned

## Identification

Wazuh alerts were reviewed to identify security-relevant activity including:

- Repeated authentication failures
- Privileged logons
- Linux sudo-to-root activity
- Account creation and modification
- Administrative group changes
- Controlled data-transfer activity

## Analysis

Relevant security events were correlated using:

- Wazuh rule IDs
- Windows Security Event IDs
- Linux journal and audit records
- User information
- Agent information
- Timestamps
- Authentication activity
- Privilege-related events

## Containment

Potential containment actions for a confirmed incident include:

- Isolating affected endpoints
- Disabling suspicious accounts
- Terminating unauthorized sessions
- Restricting malicious network activity
- Preserving security evidence

During the controlled lab exercise, test activity was stopped after detection and validation.

## Eradication

Potential eradication actions include:

- Removing unauthorized accounts
- Removing unauthorized administrative privileges
- Removing malicious processes or persistence
- Correcting insecure configurations
- Resetting compromised credentials

## Recovery

Recovery activities include:

- Validating endpoint security
- Restoring required services
- Confirming legitimate account access
- Verifying secure configurations
- Continuing enhanced Wazuh monitoring

## Lessons Learned

The exercise demonstrated the importance of:

- Centralized security logging
- SIEM alert filtering
- Authentication-event correlation
- Privileged-access monitoring
- Rapid investigation of administrative changes
- Endpoint validation of SIEM alerts
- Continuous improvement of detection rules

## Incident Response Workflow

Alert → Triage → Investigation → Correlation → Containment → Eradication → Recovery → Lessons Learned

## Evidence

The accompanying evidence PDF contains screenshots supporting the identification, investigation, correlation, and validation stages of the incident-response workflow.

Containment, eradication, recovery, and lessons-learned procedures are documented as response actions based on the controlled lab scenarios.

## Outcome

The incident-response phase demonstrated how Wazuh alerts and endpoint telemetry can be transformed into a structured SOC investigation and response process.
