# Monitoring

All ACaaD components are configurable to expose telemetry data via the opentelemetry protocol and can be consumed from Grafana utilizing the full LGTM stack.
As an example, the C# service publishes metrics and logs, the consumers populate spans. Sample Grafana dashboards are included in the respective repositories.

## Service Internal Metrics

![image](https://github.com/user-attachments/assets/2748c04e-a21d-4dba-b86b-578c713ec9f8)

## Host Metrics

![image](https://github.com/user-attachments/assets/3e79aa0b-31c4-4998-a132-0a883d68d921)

