# UFW Firewall Configuration and Port Blocking

## Objective
To configure and test firewall rules using UFW (Uncomplicated Firewall) in Kali Linux.

## Tools Used
- Kali Linux
- UFW (Uncomplicated Firewall)
- Telnet

## Steps Performed

### 1. Block Telnet Port (23)

The following command was used to deny incoming connections on port 23:

```bash
sudo ufw deny 23/tcp
```

Output:

```text
Rule added
Rule added (v6)
```

### 2. Verify Firewall Status

The firewall status was checked using:

```bash
sudo ufw status verbose
```

Output showed:

```text
Status: active
Default: deny (incoming), allow (outgoing)

22/tcp      ALLOW IN    Anywhere
23/tcp      DENY IN     Anywhere
22/tcp(v6)  ALLOW IN    Anywhere (v6)
23/tcp(v6)  DENY IN     Anywhere (v6)
```

### 3. Test the Blocked Port

A Telnet connection attempt was made:

```bash
telnet localhost 23
```

Result:

```text
Connection failed: Connection refused
Unable to connect to remote host
```

## Screenshot

![Firewall Configuration](images/firewall-screenshot.jpeg)

## Results

- Successfully enabled and configured UFW firewall.
- Allowed SSH traffic on port 22.
- Blocked Telnet traffic on port 23.
- Verified firewall rules using UFW status.
- Confirmed port blocking through Telnet connection testing.

## Conclusion

The UFW firewall was successfully configured to block Telnet (port 23) connections. The firewall rules were verified and the denied connection demonstrated that the security policy was correctly enforced.# CyberSecurity-Task4
