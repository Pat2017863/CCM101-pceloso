# Security Audit Report

## 1. Principle of Least Privilege (PoLP)

The Principle of Least Privilege means that users and applications should only receive the permissions they need to perform their tasks. It is important in cloud computing because unnecessary permissions can allow attackers to access sensitive information or make unwanted changes if an account is compromised.

## 2. Attack Surface

The attack surface is the collection of entry points that an attacker could use to access or affect a virtual machine. These include open network ports, running services, exposed applications, and accounts with weak security. Reducing unnecessary entry points helps make a server more secure.

## 3. Default Deny Policy

A Default Deny policy blocks incoming network traffic unless a firewall rule specifically allows it. This is safer than trying to block individual attackers because unknown or unwanted connections are denied automatically, while only approved services can receive traffic.

## 4. Initial Security Audit

The initial audit checks the server's running services, exposed ports, and web application before the firewall is activated. The Nginx application is deployed on TCP port 8080 so its accessibility can be tested before and after applying firewall rules.

## 5. Audit Evidence

- `vulnerable-app-running.png` — evidence that the web application responds before firewall configuration.
- `firewall-activated.png` — evidence of the active UFW firewall and its default policies.
- `firewall-port-allowed.png` — evidence of the numbered firewall rules and the web application's response after configuration.

## 6. Security Conclusion

A host-based firewall adds another layer of protection to a server. Allowing only necessary services, such as SSH for administration and TCP port 8080 for the web application, helps reduce the attack surface. Firewall configuration should be combined with regular updates, strong authentication, and continuous monitoring.
