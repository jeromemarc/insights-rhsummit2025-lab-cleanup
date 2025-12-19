## Clean Hybrid Cloud Console Account (Integrations, Behavior Groups, Vulnerability & Compliance Artifacts)

This repository contains example Ansible playbooks designed to clean up a **Red Hat Hybrid Cloud Console (HCC)** account by removing artifacts created during lab or demo environments, such as **Red Hat Summit labs**.

The cleanup includes:
- Integrations
- Behavior groups
- Compliance policies
- Vulnerability and compliance remediations created during the lab

These playbooks are intended for **lab teardown and account reset** after sessions conclude.


### ⚠️ Disclaimer

These playbooks are provided as **examples for educational purposes**.  
They may require modification to fit your specific environment, organizational policies, or security requirements.

**Use at your own discretion.**


### Features

- Authenticates with Red Hat APIs using **OAuth 2.0 Client Credentials**
- Interacts with **Hybrid Cloud Console / Lightspeed APIs**
- Deletes:
  - Integrations
  - Behavior groups
  - Compliance policies
  - Vulnerability & compliance remediations created during labs
- Supports cleanup scoped by a **GUID** used during the lab


### Prerequisites

Before running any playbook, ensure the following variables are configured:

- `hcc_client_id` – Your Red Hat API Client ID  
- `hcc_client_secret` – Your Red Hat API Client Secret  

These credentials must have sufficient permissions to manage Insights, Compliance, and Vulnerability resources.


### Usage

Run the following command and provide the **GUID** associated with the lab environment:

```bash
ansible-playbook clean_lab.yml -e "guid=GUID"
ansible-playbook clean_vuln_comp.yml -e "guid=GUID"
```


### Documentation & References
- [Red Hat Lightspeed API Documentation](https://console.redhat.com/docs/api)
- [Red Hat Lightspeed API Cheatsheet](https://developers.redhat.com/cheat-sheets/red-hat-insights-api-cheat-sheet)
- [Red Hat Lightspeed Documentation](https://docs.redhat.com/en/documentation/red_hat_insights/1-latest)
