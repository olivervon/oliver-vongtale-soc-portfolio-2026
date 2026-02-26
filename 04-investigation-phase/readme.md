# SOC Investigation Phase

## Objective

The purpose of this phase is to investigate attacker activity generated during the SOC lab attack simulation.

The investigation focuses on identifying authentication attacks, validating credential compromise, and confirming lateral movement using Windows Security logs.

Environment investigated:
- DC01 (Domain Controller)
- SRV01 (Member Server)

The investigation follows a SOC analyst workflow using native Windows event logging.

# Failed Logon Investigation - Event ID 4625

## Investigation Objective
Identify suspicious authentication failures within the Active Directory environment and determine whether activity indicates malicious behavior.

## Data Source
Domain Controller Security Logs (DC01)

Log Source:
Windows Security Event Log

Event Investigated:
4625 - An account failed to log on

## Investigation Process

The Security log on DC01 was filtered to display Event ID 4625 events. Multiple authentication failures were identified occurring within a short time period.

Analysis focused on identifying patterns commonly associated with brute force or password attack activity.

Key investigation fields reviewed:
- Account Name
- Logon Type
- Source Network Address
- Failure Reason
- Timestamp correlation

## Findings

Multiple failed authentication attempts were observed targeting privileged accounts.

The events shared the following characteristics:
- Repeated authentication failures
- Logon Type 3 (Network Logon)
- Common originating IP address
- Rapid authentication attempts

The Source Network Address matched the Kali Linux attacker machine operating inside the SOC lab network.

## Analyst Assessment

The authentication pattern is consistent with brute force password attempts originating from an internal host.

This activity represents the initial access phase of an attack prior to successful authentication and lateral movement.

## Evidence



## Conclusion

Event ID 4625 monitoring provides early detection capability for credential-based attacks within Active Directory environments.
