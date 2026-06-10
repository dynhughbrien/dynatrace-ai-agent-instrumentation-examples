# Copilot Studio 

This is how you monitor:
👉 https://copilotstudio.microsoft.com/ (the actual URL experience)
This requires synthetic monitoring / uptime monitoring.


1) Start with built-in Copilot Studio analytics
Use Copilot Studio’s built-in analytics to track:

conversation volume
success/failure trends
action usage
agent effectiveness
operational patterns over time (microsoft.com)
2) Enable telemetry export / Application Insights
Microsoft materials indicate Copilot Studio can send telemetry to Application Insights, which is the easiest way to get operational telemetry, debugging signals, and custom monitoring hooks. (adoption.microsoft.com)

3) Monitor capacity and quotas in Power Platform admin center
For production agents, watch:

message consumption
capacity
dependency usage
throttling risk / overages (learn.microsoft.com)
4) Add security/compliance monitoring
If governance matters, Microsoft recommends using analytics plus Microsoft Sentinel detection/monitoring for Copilot Studio-related events. (learn.microsoft.com)

5) For Dynatrace: ingest telemetry through OpenTelemetry
Dynatrace’s current AI Observability guidance says it supports OpenTelemetry and direct OTLP ingestion for AI observability, with an AI Observability app for tracing agents, models, providers, services, and evaluations. (docs.dynatrace.com)

Important caveat
I did not find evidence that Dynatrace currently has a native, first-class “Copilot Studio” integration comparable to some explicitly listed AI platforms. Dynatrace documents broad AI integrations and OpenTelemetry-based custom instrumentation, but Copilot Studio was not clearly listed as a dedicated native integration in the sources I found. So for Copilot Studio, the safe recommendation is custom telemetry/export + Dynatrace ingestion, not “turn on a built-in Dynatrace Copilot Studio connector.” (docs.dynatrace.com)
