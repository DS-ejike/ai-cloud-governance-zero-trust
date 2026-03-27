# AI-Driven Cloud Governance and Zero Trust Enforcement in Azure

This repository demonstrates a practical implementation of Zero Trust enforcement in Azure using Policy-as-Code, identity-driven segmentation, and AI-based anomaly detection.

## Objectives
- Deny insecure cloud configurations before deployment
- Enforce identity-first access controls
- Detect anomalous activity using a lightweight ML model
- Automate policy deployment and compliance reporting

## Key capabilities
- Azure Policy definitions and initiative
- Bicep deployment templates
- Azure DevOps pipeline for policy deployment
- Python anomaly detection and risk scoring
- PowerShell scripts for deployment and reporting

## Use cases
- Prevent public exposure of storage accounts and web apps
- Enforce managed identity usage for Azure App Service
- Encourage private endpoint adoption
- Score suspicious activity from telemetry logs

## Repo layout
- `policies/` Azure Policy definitions and initiative
- `bicep/` deployment templates
- `ml-model/` Python ML logic
- `scripts/` PowerShell automation
- `pipeline/` Azure DevOps YAML
- `docs/` supporting research and EB2-NIW evidence summaries

## Quick start
1. Clone the repo.
2. Install Python dependencies:
   ```bash
   pip install -r requirements.txt

3. Update bicep/parameters.dev.json with your management group or subscription scope.
4. Deploy policies:
   ```bash
   ./scripts/deploy-policies.ps1 -Location eastus -ManagementGroupId <mg-id>
6. Run anomaly scoring:
   ```bash
   python ml-model/train_and_score.py --input data/sample_telemetry.csv
  
