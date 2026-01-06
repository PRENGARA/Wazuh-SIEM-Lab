# Lessons Learned: Building SIEM Visibility with Wazuh & Palo Alto

## Why Centralized Logging Matters
Configuring a Syslog server profile, log forwarding, and policy-based logging on every device creates consistent, centralized visibility. This enables faster detection and response, better compliance reporting, and more effective threat hunting.

## Practical Insights from the Lab
- **Syslog Profiles & Transport**: Keep transport simple (UDP) initially, but consider TCP/TLS for reliability and confidentiality in production.
- **Forwarding Scope**: Map all relevant log types (threat, traffic, system, config) to ensure complete coverage and avoid blind spots.
- **Policy Integration**: Tie forwarding to **Security Policies** so actionable events are captured. Validate after commit.
- **Event Generation**: Use safe test malware to confirm end-to-end ingestion and parsing (e.g., `data.type: THREAT`).
- **Endpoint Onboarding**: Installing the Wazuh agent on key systems (like IAMLAB-VDC) enriches telemetry beyond network events.

## Troubleshooting & Tuning
- **Alert Fatigue**: Start with broad forwarding, then tune match lists and rules to reduce noise.
- **Performance & Storage**: Plan for log volume growth; implement indexing/retention policies.
- **Integrity & Trust**: Protect syslog traffic; encrypt when crossing untrusted networks; verify cert chains if using TLS.
- **Clock Skew**: Ensure consistent NTP across devices; mismatched timestamps hinder investigations.

## Best Practices
- Version control SIEM configurations and document change history.
- Validate ingestion with dashboards and searches (e.g., saved searches for THREAT events).
- Create runbooks for common incidents leveraging the SIEM.

## Outcome
The lab demonstrates a complete pipeline from firewall event generation to SIEM ingestion and alerting, establishing a foundation for blue-team operations and continuous monitoring.
