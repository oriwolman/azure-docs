---
title: Microsoft Security Code Analysis releases
description: This article describes upcoming releases for the Microsoft Security Code Analysis extension
author: TerryLanfear
manager: sukhans
ms.author: terrylan
ms.date: 01/09/2023
ms.topic: article
ms.service: security
services: azure

ms.assetid: 521180dc-2cc9-43f1-ae87-2701de7ca6b8
ms.tgt_pltfrm: na
ms.workload: na
---

# Microsoft Security Code Analysis releases and roadmap

> [!Note]
> Effective December 31, 2022, the Microsoft Security Code Analysis (MSCA) extension is retired. MSCA is replaced by the [Microsoft Security DevOps Azure DevOps extension](/azure/defender-for-cloud/azure-devops-extension). Follow the instructions in [Configure](/azure/defender-for-cloud/azure-devops-extension) to install and configure the extension.

Microsoft Security Code Analysis team in partnership with Developer Support is proud to announce recent and upcoming enhancements to our MSCA extension.


## Credential Scanner v2.0: Released in April 2020

### Innovations & Improvements

- **Core Engine**

   - Average performance upgrade of 25% with near linear run times
   - Context/evidence based searching and ranking for increased accuracy
   - Improvements to general password detections and matching logic for obvious placeholders (for example, fakePassword)

- **Coverage** - Support for 25+ secret types including the following top requested:

   - Fabric account certificate Passphrase
   - Client Secret/API Key
   - HTTP authorization header
   - Amazon S3 Client Secret Access Key
   - Azure Active Directory Client Access Token
   - Azure Function Master/API Key
   - Power BI Access Key
   - Azure Resource Manager template password pattern

- **Outputs**

   - Support for SARIF 2.1 and CSV file output file formats

## BinSkim v1.6.0: Released in April 2020

### Improvements

- FEATURE: Update to final SARIF v2 (version 2.1.16). This update enables results caching when passing --hashes on the command-line, a significant performance improvement when recursively analyzing directories with multiple copies of scan targets.
- BUG FIX: Fix typo in BA2021.DoNotMarkWritableSectionsAsExecutable output.
- PERFORMANCE: Eliminate PDB loading for all non-mixed-mode for managed assemblies, including IL Library (ahead of time compiled) binaries.
- FALSE NEGATIVE FIX: Verify that a PDB placed alongside a binary actually matches the binary under analysis
- FEATURE: Provide --local-symbol-directories argument to specify additional (local, non-symbol-server) PDB look-up locations
- FALSE POSITIVE FIX: Skip PDB-driven analysis for the generated .NET core native bootstrap exe (which is not user-controllable code).

## What's next in Q3 CY20?

- Java Security Analysis tool
- Python Security Analysis tool
- ES Lint to replace TS Lint for TypeScript and JavaScript
- Resource Manager Templates Analysis tool

## Tool Deprecation Notification

### Microsoft Security Risk Detection (MSRD) is deprecated on June 26 2020.

The deprecated MSRD fuzzing service will be replaced with an open source self-hosted developer fuzzing platform for Azure. This platform is currently being developed and tested in partnership with many of Microsoft’s core product teams. This fuzzing platform will integrate sanitizers and allow for adaptive, learning fuzz tests built into CI/CD pipelines that grow over time with software projects. The Open Source release of this platform is scheduled for the latter half of 2020.

## Next steps

For instructions on how to onboard and install Microsoft Security Code Analysis, refer to our [Onboarding and installation guide](security-code-analysis-onboard.md).

If you have more questions about the extension and the tools offered, check out our [FAQ page](security-code-analysis-faq.yml).
