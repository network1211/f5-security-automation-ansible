# Automated Remediation of Unauthorized POD in OpenShift environment

## Summary
In a typical data center security design, advanced application security solutions are deployed at the edge of a Kubernetes or OpenShift environment. 
With F5 CIS integration, edge WAF could get a certain level of visibility for the specific pod inside Kubernetes or OpenShift cluster. 
But it is still can not stop the attack within the cluster.  To overcome this challenge, 'NAP(NGINX App Protect)' could be deployed as a POD or service proxy in Kubernetes or OpenShift cluster. 
The NAP(NGINX App Protect) delivers Layer 7 visibility and granular control for the applications while enabling the advanced level of the application security policies. 
With NAP deployment, DevSecOps can ensure only legitimate traffic allowed while all other unwanted traffics blocked. 
The NAP can monitor the traffic traversing namespace boundaries between pods and provide the advanced application protection at the layer-7 level for East-West traffic. 

## Prerequisites
- ELK(Elasticsearch, Logstash, Kibana) installed (required Platinum or Trial license)
- Ansible installed on the same server with ELK
- Evaluation license of NAP(NGINX App Protect)
- You can reqeust the evaluation license of NGINX App Protect in [here](https://www.nginx.com/free-trial-request/).
- Minimum 1 x OCP cluster installed.

## Use-Case Scenario
In this use-case, you will analyze F5 telemetry logs using ELK stack.  These sample logs include normal web-requests from users global, and you will be able to find malicious attacks from logs. Once you successfully import sample ELK logs to the ELK in your lab, you can perform your own 'Threat Hunting' and complete the automated remediation using Ansible. 

### *Red Team*
While we don't include the attack simulation process in this repo, this diagram could help you understand how the whole attack process is proceeding by the attacker.
