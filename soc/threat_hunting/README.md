# Automated Threat Hunting and Security Remediation

## Summary
Threat hunting and incident investigation is a time-consuming job. Suppose the automation process flags the suspicious activities with the combinations of 'weak-signals' on the network and performs the remediation process. In that case, it can dramatically reduce the risks of the company. Below is the network diagram for this use-case.


## Prerequisites
- ELK(Elasticsearch, Logstash, Kibana) installed (required Platinum or Trial license)
- Ansible installed on the same server with ELK
- F5 BIG-IP provisioned with AWAF/APM/LTM

## Use-Case Scenario
In this use-case, you will analyze F5 telemetry logs using ELK stack.  These sample logs include normal web-requests from users global, and you will be able to find malicious attacks from logs. Once you successfully import sample ELK logs to the ELK in your lab, you can perform your own 'Threat Hunting' and complete the automated remediation using Ansible. 

### *Red Team*
While we don't include the attack simulation process in this repo, this diagram could help you understand how the whole attack process is proceeding by the attacker.
![Red Team - Attack Flow](red_team_flow.png)

## Setup and Configuration
Follow the links below in order to begin setup and configuration.
1. [Importing sample CSV files to your Kibana](https://github.com/network1211/f5-security-automation-ansible/blob/master/soc/threat_hunting/import_elk/import_elk.md)
2. [Creating Kibana Dashboard for SOC analysts](https://github.com/network1211/f5-security-automation-ansible/blob/master/soc/threat_hunting/kibana_dashboard/dashboard-main.md)
3. [Simulating 'Threat Hunting'](https://github.com/network1211/f5-security-automation-ansible/blob/master/soc/threat_hunting/hunting/hunting.md)
4. [Automated Remediation using Ansible](https://github.com/network1211/f5-security-automation-ansible/blob/master/soc/threat_hunting/automation/README.md)
