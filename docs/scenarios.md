# Detection Scenarios

## Scenario 1: Suspicious Local User/Group Creation

### Objective

Detect the creation of a new local user/group and investigate the resulting Wazuh alert.

### Activity

A test account named `soc-test` was created on the Linux endpoint.

### Detection

Wazuh detected the account/group creation activity and generated a security alert.
The alert showed the creation of the `soc-test` group on the Linux endpoint. The event was then investigated to verify the account and its configuration.

### Investigation

The alert was reviewed in the Wazuh dashboard to identify:

- The affected endpoint
- The event
- The username/group involved
- The Wazuh rule
- The alert severity

---

## Scenario 2: SSH Login Attempt Using a Non-Existent User

### Objective

Detect suspicious SSH authentication attempts involving a username that does not exist on the system.

### Activity

Multiple failed SSH login attempts were generated using a non-existent username.

### Detection

Wazuh monitored the Linux authentication log and generated an alert for the activity.

- **Rule ID:** 5710
- **Severity Level:** 5
- **Detection:** `sshd: Attempt to login using a non-existent user`

The alert indicated that an SSH login attempt was made using the non-existent username `soc-attacker`.

### Investigation

The alert was reviewed to identify:

- The source of the event
- The attempted username
- The affected endpoint
- The Wazuh rule
- The alert severity
- The authentication failure details
