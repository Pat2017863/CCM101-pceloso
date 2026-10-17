# Mission 8 Reflection: The Cloud Security Engineer

Completing this laboratory helped me understand why server security is important in cloud computing. A server may run an application correctly, but it can still be vulnerable if its network ports and services are not properly secured.

A host-based firewall protects a server by controlling the traffic entering and leaving the machine. Even if the physical network perimeter is breached, the firewall provides another layer of protection on the server itself. It can block unauthorized incoming connections while allowing the services needed by legitimate users. However, a firewall is not enough on its own, so regular updates, strong authentication, and monitoring are also necessary.

Managing open network ports is important because every exposed service can become a possible entry point for attackers. Closing unnecessary ports reduces the attack surface and limits the number of services that need protection. In this activity, SSH was allowed for administration, while TCP port 8080 was allowed for the web application.

Leaving a database port such as MySQL port 3306 open to the public internet is dangerous. Attackers may attempt to guess passwords, exploit software vulnerabilities, or access sensitive records. Database access should normally be restricted to trusted application servers or authorized networks rather than being available to everyone online.

This mission changed my perspective because I realized that deploying a working application is only one part of operating a secure server. A small mistake in firewall configuration can expose services that should remain private. I also learned why administrators must check their firewall rules carefully and allow SSH before enabling a default deny policy on a remotely managed machine.

My GitHub portfolio now has a dedicated folder for Mission 8, adding to the previous seven missions. It helps organize my laboratory reports, commands, reflections, and screenshots in one place. Having these activities in a repository also allows me to review my progress and demonstrate the cloud computing skills I have practiced.

Overall, this activity taught me that cloud security requires careful configuration, regular verification, and continuous improvement rather than a one-time setup.
