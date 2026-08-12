# Log Collection Evidence

## Overview

This section documents the collection and centralization of security telemetry from the monitored endpoints.

## Objective

The objective was to demonstrate how endpoint security logs can be collected and made available within a centralized SIEM for analysis.

## Log Sources

The lab generated and collected security telemetry from sources including:

- Windows Security events
- Linux system and authentication events
- Linux journald
- Linux audit events
- SSH authentication activity
- Wazuh agent telemetry

## Windows Log Collection

Windows Server security events were collected through the Wazuh agent.

Relevant security events included authentication activity, privileged logons, account changes, and security-group modifications.

## Linux Log Collection

Linux security telemetry was collected from the Debian endpoint.

This included authentication information, sudo activity, system events, and audit-related telemetry used during controlled testing.

## Centralized Monitoring

Collected endpoint events were forwarded to Wazuh where they could be normalized, searched, filtered, correlated, and analyzed.

The resulting workflow was:

Endpoint Activity → Operating System Logs → Wazuh Agent → Wazuh Manager → Wazuh Dashboard

## Validation

Log collection was validated by generating controlled endpoint activity and confirming that corresponding events appeared within Wazuh.

## Evidence

The accompanying evidence PDF contains screenshots demonstrating endpoint connectivity, log ingestion, and security events available for centralized monitoring.

## Outcome

Windows and Linux security telemetry was successfully centralized within Wazuh for subsequent detection, threat hunting, and incident investigation.
