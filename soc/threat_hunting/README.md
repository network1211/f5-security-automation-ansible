# Automated Threat Hunting and Security Remediation

## Summary
Threat hunting and incident investigation is a time-consuming job. If automation process flags the suspicious activities with the combinations of 'weak-signals' on the network, and performs the remediation process, it can dramatically reduce the risks on the company.

## Prerequisites
- ELK(Elasticsearch, Logstash, Kibana) installed
- Ansible installed at same server with ELK
- F5 BIG-IP provisioned with AWAF/APM/LTM

## Use-Case Scenario
In this use-case, you will simulate the 'Red Team' operation first. After this 'Red Team' simulation, you can start the investigation using Elasticsearch and perform the automated remediation using Ansible. 

### *Red Team*
![Red Team - Attack Flow](red_team_flow.png)
