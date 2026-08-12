# Attack Simulation Evidence

## Overview

This section documents controlled security simulations performed within the isolated SOC lab environment.

## Objective

The purpose of the simulations was to generate realistic security telemetry and determine whether the monitoring and detection environment could identify the resulting activity.

## Lab Safety

All security testing was performed within systems specifically configured for the cybersecurity lab.

No production systems or unauthorized external systems were targeted.

## Simulated Activities

Controlled testing included:

- SSH authentication activity
- Repeated authentication attempts
- Privileged-access activity
- Test account creation and modification
- Administrative group modification
- Controlled data-transfer activity

## Authentication Testing

Authentication activity was generated to produce security events that could be collected and investigated through Wazuh.

The workflow demonstrated:

Controlled Test → Authentication Events → Endpoint Logs → Wazuh → Alert / Investigation

## Privilege Testing

Controlled privilege-related activity was performed to validate monitoring of elevated access.

This generated Windows and Linux security telemetry that could subsequently be investigated through the SIEM.

## Account Manipulation Testing

Controlled account creation and modification activities were performed to validate monitoring of security-sensitive account changes.

## Data-Transfer Testing

Controlled file-transfer activity was used to generate telemetry for the data-exfiltration monitoring scenario.

The activity was performed only with test data inside the isolated lab environment.

## Validation

After each controlled simulation, endpoint telemetry and Wazuh events were reviewed to determine whether the activity was successfully captured.

## Evidence

The accompanying evidence PDF contains screenshots from the controlled attack-simulation and validation workflow.

## Outcome

The simulations demonstrated how controlled security testing can be used to validate SIEM visibility and detection capabilities before security controls are relied upon in operational environments.
