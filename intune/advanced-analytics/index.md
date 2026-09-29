---
title: "Advanced Analytics overview"
description: Discover what Microsoft Intune Advanced Analytics is, how it extends endpoint analytics with advanced device insights, proactive troubleshooting, and enhanced reporting.
ms.date: "2026-03-24T00:00:00Z"
ms.topic: concept-article
---

# Advanced Analytics overview

Microsoft Intune Advanced Analytics delivers deep, actionable insights into the health and performance of your organization's endpoints. Built on the foundation of [endpoint analytics](../endpoint-analytics/index.md), it helps IT teams proactively manage user experience and optimize productivity through data-driven intelligence. By turning raw telemetry into meaningful insights, Advanced Analytics reduces support costs, accelerates problem resolution, and ensures a more reliable technology experience for every user.

## Available reports and capabilities

Advanced Analytics enhances endpoint analytics with the following reports and capabilities:

[Resource performance report](resource-performance.md)

> Identifies CPU and RAM performance issues by device, model, and manufacturer to guide purchasing decisions.

[Battery health report](battery-health.md)

> Monitors battery health for Windows devices to ensure long battery life and a better user experience.

[Anomalies report](anomalies.md)

> Tracks device health for regressions in user experience and productivity after configuration changes.

[Device timeline report](device-timeline.md)

> Shows detailed events with low latency to help troubleshoot device issues quickly.

[Device query](device-query.md)

> Provides near real-time data about the state and configuration of Windows devices.

[Device query for multiple devices](device-query-multiple-devices.md)

> Allows you to run queries directly in Intune to retrieve inventory data across multiple devices and platforms.

[Device scopes](device-scopes.md)

> Allows you to use scope tags to filter reports for a subset of devices. See scores, insights, and recommendations specific to those devices.

## Prerequisites

To use Advanced Analytics features, devices must meet the [endpoint analytics prerequisites](../endpoint-analytics/index.md#prerequisites) and you must [configure endpoint analytics](../endpoint-analytics/configure.md) in your tenant.

This section details **additional prerequisites** specific to Advanced Analytics. Certain features may have their own additional prerequisites; see the individual feature articles for more information.

![](../media/icons/16/cloud.svg) **Cloud requirements**

> - Public cloud
> - Sovereign cloud environments:
>   - U.S. Government Community Cloud (GCC) High
>   - U.S. Department of Defense (DoD)
>
>   > [!NOTE]
>   >
>   > Support for Advanced Analytics in DoD environments doesn't include the [*Device query*](device-query.md) functionality or the [*Resource performance*](resource-performance.md) report. For more information, see [Microsoft Intune for US Government GCC service description](../fundamentals/government-service.md).

![](../media/icons/16/configuration.svg) **Device configuration requirements**

> Advanced Analytics features support Windows devices that are:
>
> - Managed by Intune
> - Co-managed (Intune + Configuration Manager)
> - Microsoft Entra joined
> - Microsoft Entra hybrid joined

![](../media/icons/16/licensing.svg) **Licensing requirements**

> This feature requires a subscription in addition to Microsoft Intune Plan 1 or Plan 2. For licensing options, see [Microsoft Intune plans and pricing](https://aka.ms/MicrosoftIntunePricing) and [Microsoft 365 Security Enterprise Plans](https://www.microsoft.com/security/pricing/enterprise-plans).

## Get started with Advanced Analytics

Before deploying Advanced Analytics, complete these foundational tasks:

- Assess your organization's privacy and compliance requirements for device data. Review the Intune [data platform schema](ref-data-platform-schema.md) to understand which data is captured.
- Define escalation and support procedures for handling analytics findings.
- Train staff on IT processes you plan to optimize, such as help desk triage, hardware refresh cycles, and app updates. Treat this as a continuous improvement cycle for faster and more proactive issue resolution.

### Enable Advanced Analytics

When license requirements are met, then Advanced Analytics capabilities are automatically enabled in your tenant.

> [!NOTE]
>
> It might take up to 48 hours after you buy licenses or start a trial to see Advanced Analytics features in your tenant.

For the extra reports and capabilities on Windows devices:

- Devices must be enrolled in Intune and onboarded to endpoint analytics.
- [Device query for multiple devices](device-query-multiple-devices.md) requires a properties catalog policy to be configured and deployed.

### Advanced Analytics in the Intune admin center

Advanced Analytics is built into Microsoft Intune and appears in the **Reports** &gt; **Endpoint analytics** section, as well as other areas of the Intune admin center. When enabled, it adds the following enhancements:

- Endpoint analytics reports are extended with:
  - [Resource performance report](resource-performance.md)
  - [Battery health report](battery-health.md)
  - [Anomalies report](anomalies.md)
  - [Device scopes](device-scopes.md)
- Single device views are extended with:
  - [Battery health report](battery-health.md)
  - [Device timeline report](device-timeline.md), which replaces the [application reliability report](../endpoint-analytics/app-reliability.md)
  - [Resource performance report](resource-performance.md)
  - [Device query](device-query.md)
- Additional capabilities:
  - [Device query for multiple devices](device-query-multiple-devices.md) under the **Devices** node in the Intune admin center
  - [STIG audit baseline](../device-security/security-baselines/stig-audit-baseline.md) to assess Windows device compliance against Department of Defense (DoD) Security Technical Implementation Guide requirements

### Integrate Advanced Analytics into business processes

After completing the setup tasks, follow these steps to embed Advanced Analytics into daily operations:

1. **Update support processes** to:
   - Use the [device timeline report](device-timeline.md) to identify patterns, such as restarts or updates linked to anomalies.
   - Use [device query](device-query.md) to retrieve live device data for troubleshooting.
   - Use [device query for multiple devices](device-query-multiple-devices.md) to gain insights across your entire device fleet.
2. **Schedule regular reviews** of:
   - [Anomalies reports](anomalies.md) after OS or app updates to catch issues early.
   - [Battery health reports](battery-health.md) to identify devices needing attention for better performance and user experience.
   - [Resource performance reports](resource-performance.md) to track performance by device, model, and manufacturer—helpful for future purchasing decisions.
