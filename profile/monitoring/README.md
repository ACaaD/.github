# Monitoring

All ACaaD components are configurable to expose telemetry data via the opentelemetry protocol and can be consumed from Grafana utilizing the full LGTM stack.
As an example, the C# service publishes metrics and logs, the consumers populate spans. Sample Grafana dashboards are included in the respective repositories.

## Service Internal Metrics

![image](https://github.com/user-attachments/assets/2748c04e-a21d-4dba-b86b-578c713ec9f8)

## Host Metrics

![image](https://github.com/user-attachments/assets/4ede12d8-2b68-4add-b45a-3316d207c2f7)

## Critical Paths/Spans

Note: The spans serve two purposes in the consumer project. For one they are very useful to identify performance bottlenecks, especially in the highly concurrent processing of server metadata.
However, their main purpose as of now is to enable integration test hooks to wait for specific events happening inside the consumer, for example a signalr client connecting to the server.
This means that not all processes are completely covered via tracing, but only the ones that are of interest during integration test execution.

### Metadata Synchronization

![image](https://github.com/user-attachments/assets/a55c2719-777a-4937-a1d5-45be9ee8a230)

### Consumer Startup

![image](https://github.com/user-attachments/assets/56592eeb-477a-4882-9eee-5045e5642742)

### Consumer Shutdown

![image](https://github.com/user-attachments/assets/7ad3bfbf-7897-4f46-ac4c-ac2b0407ffba)
