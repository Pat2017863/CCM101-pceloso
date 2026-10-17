# Laboratory 08: The Cloud Security Engineer

**Course:** CCM101 – Cloud Computing  
**Mission:** Mission 8 – The Cloud Security Engineer  
**Platform:** KillerCoda Ubuntu Playground

## 1. Mission Overview

This mission focuses on protecting a Linux server using a host-based firewall. An Nginx web application is deployed in a Docker container on port 8080. UFW is then configured to deny incoming traffic by default while allowing SSH for remote administration and TCP port 8080 for the web application.

## 2. Objectives

- Understand the Principle of Least Privilege.
- Explain the concept of an attack surface.
- Inspect active listening ports on an Ubuntu server.
- Configure UFW with a Default Deny incoming policy.
- Allow SSH and the required web application port.
- Verify firewall rules and test the web application.
- Document the configuration and reflect on cloud security.

## 3. Commands Executed

### Inspect the Server

```bash
sudo ss -tuln
sudo ufw status verbose
```

### Deploy the Web Application

```bash
docker run -d --name secure-web-app -p 8080:80 nginx:latest
curl -I http://localhost:8080
```

### Configure the Firewall

```bash
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw allow 8080/tcp
```

### Verify the Configuration

```bash
sudo ufw status verbose
sudo ufw status numbered
curl -I http://localhost:8080
docker ps
```

## 4. Skills Learned

- Deploying a web application using Docker.
- Inspecting network ports on Linux.
- Configuring UFW firewall rules.
- Applying the Principle of Least Privilege.
- Reducing a server's attack surface.
- Testing a web application using curl.
- Documenting cloud security procedures using Markdown.
- Managing laboratory files using Git and GitHub.

## 5. Screenshots

The following screenshots provide evidence of the laboratory tasks:

1. `screenshots/vulnerable-app-running.png` — successful initial Nginx response.
2. `screenshots/firewall-activated.png` — active firewall and default policies.
3. `screenshots/firewall-port-allowed.png` — numbered firewall rules and successful web request.

## 6. Conclusion

This mission demonstrates how a host-based firewall can reduce unnecessary network exposure. By allowing only required services and verifying the configuration, an administrator can improve a server's security and reduce the risk of unauthorized access.
