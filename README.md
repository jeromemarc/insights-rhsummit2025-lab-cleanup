# Example: Clean Hybrid Cloud Console account from all integrations and behavior groups

This repository contains an example Ansible playbook designed to clean up a Red Hat Hybrid Cloud Console account by deleting all integrations and behavior groups. It is intended for use cases such as Red Hat Summit lab teardown after sessions conclude.

Disclaimer: This playbook is provided as an example for educational purposes. It may require modifications to fit specific use cases or security policies. Use it at your own discretion.

## Features
- Authenticates with Red Hat API using **OAuth 2.0 Client Credentials**.
- Fetches **integrations** and **behavior groups** via Hybrid Cloud Console / Insights API.
- Deletes **integrations** and **behavior groups** based on specific criteria.

## Pre-requisites
Before running the playbook, ensure you have the following variables configured:

- **`hcc_client_id`**: Your Red Hat API Client ID.
- **`hcc_client_secret`**: Your Red Hat API Client Secret.

# Documentation & References
- [Red Hat Insights API Documentation](https://console.redhat.com/docs/api)
- [Red Hat Insights API Cheatsheet](https://developers.redhat.com/cheat-sheets/red-hat-insights-api-cheat-sheet)
- [Red Hat Insights Documentation](https://docs.redhat.com/en/documentation/red_hat_insights/1-latest)
