## General Vision for the Core Services of Canary.io

At its heart, the core of canary.io is meant to evolve into a networked collection of ephemeral processes that are capable of delivering availability and performance info for a large set of URLs. Ideally it is dial-tone like in nature, sacrificing just about everything to be up, always serving events to interested parties and services.

Events can be dropped on the floor - the system does not require strong consistency, but does require availability and partition tolerence. When responding to an incident, I would rather have some events instead of no events - the monitoring / visbility system should have better availabiity than the components being monitored.

This core services should be able to provide the outside world access to a small sliding window of measurements and also provide some level of data streaming via chunked http and websockets.

Secondary services such as dashboards, data retention, alerting, web hooks, etc would be built off of the core.
