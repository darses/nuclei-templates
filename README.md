# My Nuclei Templates

A curated collection of custom ProjectDiscovery [Nuclei](https://github.com/projectdiscovery/nuclei) templates maintained for vulnerability research, asset discovery, technology fingerprinting, and security assessments.

---

## Repository Structure

The repository is organized by template purpose and validation lifecycle:

| Directory | Description |
| :--- | :--- |
| [`drafts/`](./drafts/) | In-development, untested, or unverified templates (`verified: false`). All new templates begin here. |
| [`cve/`](./cve/) | Confirmed vulnerability checks and exploits mapped to CVE IDs. |
| [`panel/`](./panel/) | Detection signatures for administrative consoles, login interfaces, and device web portals. |
| [`tech/`](./tech/) | Technology fingerprinting, frameworks, software components, and centralized favicon hashes (`tech/custom-favicon-detect.yaml`). |
| [`network/`](./network/) | Protocol and service signatures across non-HTTP protocols (SSH, SMTP, raw TCP, IKE, etc.). |
| [`saas/`](./saas/) | Fingerprints for hosted cloud platforms, tenant environments, and SaaS logins. |
| [`other/`](./other/) | Specialized vendor-focused suites (e.g. Citrix, Ivanti, Microsoft, Palo Alto Networks) and auxiliary tools. |
| [`private/`](./private/) | Proprietary detection logic, internal scripts, and research notes. |

---

## License

This repository is licensed under the terms of the [GNU General Public License v3.0 (GPLv3)](./LICENSE).
