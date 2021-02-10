# OPA Gatekeeper - Helm Charts


- We have created a helm chart to manage all your kubernetes security policies in a centralised manner.
- Some of the policies are taken from the official [OPA GATEKEEPER](https://github.com/open-policy-agent/gatekeeper) repo. You can check the library provided by them.

[OPA GATEKEEPER POLICY LIBRARY](https://github.com/open-policy-agent/gatekeeper-library/tree/master/library) 

We at CloudSecOps have created blogs to understand the basics of Rego policies as well as some implementation of our own custom policies in the cluster. To check out the blog posts on various policies you can visit the [CloudSecOps](https://www.cloudsecops.com) blog. 

<em>(Note:- Some of the custom policy implementations are very simple and basic compared to the ones present in the Gatekeeper library. You can customize them or write your own to suit your needs.) </em>

## 
## Auditing 

There are various ways in which auditing and logging can be done for OPA Gatekeeper. You can refer the official documentation for more information.

We at cloudsecops used the default auditing provided by kubernetes to mainly focus on gathering violation logs and forward the logs to EFK. You can read the detailed blog post [here](https://cloudsecops.com).
##
## Usecases
<details>
<summary>NetworkPolicy Guard Rails</summary>
<br>
    <ul>
        <li>Enforce Namespace Restrictions for Robust NetworkPolicy Enforcement.</li>
        <li>Restrict Namespace and Pod Selectors in NetworkPolicies.</li>
        <li>Restrict Ingress Traffic Label Selectors in NetworkPolicies.</li>
        <li>Restrict Ingress Ports in NetworkPolicies.</li>
        <li>Restrict Ingress IP CIDR Ranges in NetworkPolicies.</li>
        <li>Restrict Egress Label Selectors in NetworkPolicies.</li>
        <li>Restrict Egress Ports in NetworkPolicies.</li>
        <li>Restrict Egress IP CIDR Ranges in NetworkPolicies.</li>
    </ul>
<br>
</details>
<details>
<summary>RBAC Guard Rails</summary>
<br>
    <ul>
        <li>Service Accounts: Prohibit Namespaces.</li>
        <li>Restrict Users who can Manage Roles and Cluster Roles.</li>
        <li>Prohibit Wildcard Verbs in Roles and ClusterRoles.</li>
        <li>Prohibit Wildcard Subjects in RoleBindings and ClusterRoleBindings.</li>
    </ul>
    <br>
    </details> 
<details>
<summary>Volume Controls</summary>
<br>
    <ul>
        <li>Storage Classes: Prohibit Retain Reclaim Policy.</li>
        <li>Storage Classes: Require Strong Encryption.</li>
        <li>Deny Privileged Containers.</li>
    </ul>
    <br>
 </details>
<details>
<summary>CI/CD and Secure Configuration</summary>
<br>
    <ul>
        <li>CI/CD: Require Trusted Image Repository and Hardened Images.</li>
        <li>CI/CD: Block Latest Image Tag.</li>
        <li>Pods: Prohibit Unauthorized Host Paths.</li>
        <li>Pods: Prohibit Host Network.</li>
        <li>Pods: Prohibit Unauthorized Config Map Volumes.</li>
        <li>Prohibit Pod Exec Resource.</li>
    </ul> 
<br>
</details>
<details>
<summary>POD Security Policies</summary>
<br>
    <ul>
        <li>Restrict escalation to root privileges.</li>
        <li>Control Linux capabilites.</li>
        <li>Control usage of Host file system/network-ports/namespaces</li>
        <li>Control container sysctl profiles.</li>
        <li>Control AppArmor profile used by containers.</li>
        <li>Control secComp profile used by containers.</li>
        <li>Control the seLinux context of containers.</li>
    </ul> 
<br><br>
</details>

##
## Installation
Can be installed from the current directory. <br>
` helm install foo . ` 

##
## Learning Gatekeeper with katacoda.
You can learn to use OPA Gatekeeper and write custom REGO policies with the following [Katacoda scenarios.](https://www.katacoda.com/cloudsecops)


