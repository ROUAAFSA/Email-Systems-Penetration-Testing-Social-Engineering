# Email Systems Penetration Testing & Social Engineering

**Academic cybersecurity project | 2025–2026**

A controlled penetration-testing lab assessing email security, web information exposure, and human susceptibility to phishing for a simulated organization, **NexaCorp Financial Services**.

The project combines reconnaissance, email-security assessment, phishing simulation, security findings, and remediation recommendations to demonstrate how technical weaknesses and social engineering can combine to create organizational risk.

## Objectives

- Assess email security and SPF, DKIM, and DMARC configuration.
- Explore web reconnaissance and information-disclosure risks.
- Simulate phishing campaigns and analyze campaign interactions.
- Evaluate social-engineering risks in a controlled environment.
- Document security findings and recommend appropriate countermeasures.

## Lab Architecture

The lab used three virtual machines:

- **Kali Linux 2024:** reconnaissance, web services, DNS, and phishing campaign management.
- **Windows 10:** simulated employee workstation.
- **Ubuntu 22.04:** simulated phishing proxy server.

The environment used an isolated lab network and fictional organizational data.

## Tools & Technologies

- **GoPhish** — phishing campaign management and interaction tracking.
- **Evilginx2** — simulated live-proxy phishing scenario.
- **Social-Engineer Toolkit (SET)** — website-cloning component.
- **theHarvester and Sherlock** — reconnaissance and OSINT.
- **MailHog** — test email delivery and inspection.
- **dnsmasq, Apache2, Nginx** — DNS and web infrastructure.
- **Kali Linux, Ubuntu, Windows 10** — lab environments.

## Methodology

1. **Reconnaissance & OSINT:** examined website metadata, DNS configuration, and publicly discoverable information.
2. **Enumeration:** identified simulated employee email conventions and prepared test profiles.
3. **Campaign setup:** configured phishing scenarios and test email delivery.
4. **Controlled simulation:** observed email interactions and documented the simulated credential-capture scenario.
5. **Analysis:** classified findings by severity and assessed their potential impact.
6. **Remediation:** proposed email-authentication hardening, web-server cleanup, phishing-awareness training, and phishing-resistant MFA.

## Key Results

The presentation documented the following results within the simulated lab:

- 25 phishing emails sent in one campaign.
- 1 tracked phishing-link click.
- 1 credential submission captured in the simulated scenario.
- Missing SPF, DMARC, and DKIM configurations identified in the test environment.
- Sensitive resource references exposed through `robots.txt`.

These results illustrate the importance of combining technical security controls with user-awareness measures.

## Findings & Recommendations

| Finding | Recommended mitigation |
|---|---|
| Missing SPF configuration | Publish and validate an appropriate SPF policy. |
| Missing DMARC policy | Configure DMARC and progressively enforce the policy. |
| Missing DKIM signing | Implement DKIM signing and publish the corresponding DNS record. |
| Sensitive resources exposed | Remove unnecessary files and restrict web-root access. |
| Phishing susceptibility | Provide targeted security-awareness training and recurring authorized simulations. |
| Live-proxy phishing risk | Deploy phishing-resistant MFA, such as FIDO2/WebAuthn. |

## Skills Demonstrated

- Email security assessment
- Phishing simulation and campaign analysis
- Web reconnaissance and OSINT
- Security findings documentation
- Risk analysis and remediation planning
- Security awareness and human-factor assessment
- Virtualized lab setup and networked security tooling

## Ethical Use

This project was conducted as an academic exercise using a simulated organization and lab environment. The tools and techniques demonstrated are intended for authorized security testing and education only. Do not target real users or systems without explicit authorization.
