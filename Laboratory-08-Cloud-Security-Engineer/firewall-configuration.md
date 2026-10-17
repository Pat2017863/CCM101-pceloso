# Firewall Configuration

## 1. Overview

This activity uses UFW (Uncomplicated Firewall) to protect an Ubuntu server running an Nginx web application in a Docker container. The firewall is configured to deny incoming connections by default while allowing the services required for administration and web access.

## 2. Commands Executed

### Step 1: Inspect Listening Ports

```bash
sudo ss -tuln
sudo ufw status verbose
```

The first command displays listening network sockets, while the second checks the firewall's current status and policies.

### Step 2: Allow SSH

```bash
sudo ufw allow ssh
```

This permits incoming SSH connections so administrators can remotely manage the server.

### Step 3: Configure Default Policies

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

The first command blocks incoming traffic by default, while the second permits outgoing traffic by default.

### Step 4: Enable the Firewall

```bash
sudo ufw enable
```

This activates UFW and applies the configured firewall rules.

### Step 5: Allow the Web Application

```bash
sudo ufw allow 8080/tcp
```

This allows incoming TCP connections to port 8080, which is published for the Nginx web application.

### Step 6: Verify the Rules and Application

```bash
sudo ufw status verbose
sudo ufw status numbered
curl -I http://localhost:8080
```

These commands verify the firewall policies, display numbered rules, and test the web application from the local machine.

## 3. Why SSH Must Be Allowed First

If I run `sudo ufw enable` before `sudo ufw allow ssh`, the default deny incoming policy may block new SSH connections and prevent remote administration until access is restored through an authorized console.

## 4. Security Best Practices

- Allow only the network ports required by the application.
- Restrict SSH access to trusted administrative addresses when possible.
- Use strong authentication and keep the operating system and containers updated.
- Avoid exposing database services directly to the public internet.
- Review firewall rules regularly and remove unnecessary permissions.
- Verify both host firewall rules and cloud network security rules.
- Remember that Docker-published ports may require additional firewall controls.

## 5. Verification Results

Record the actual results from the playground before submission.

- Firewall status: [Write the result shown by UFW.]
- Default incoming policy: [Write the displayed policy.]
- Default outgoing policy: [Write the displayed policy.]
- SSH rule: [Confirm whether the rule appears.]
- TCP port 8080 rule: [Confirm whether the rule appears.]
- Nginx response: [Record the actual HTTP response.]

## 6. Conclusion

UFW provides a simple way to manage incoming and outgoing network traffic on a Linux server. By applying a default deny policy and allowing only the required services, the administrator can reduce unnecessary exposure and improve the server's security.
