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

  ---

## Scenario 1 Evidence

![Wazuh user creation alert](../screenshots/scenario-1/01-wazuh-user-creation-alert.png)

![User and group verification](../screenshots/scenario-1/02-soc-test-user-group-verification.png)

![Sudo group check](../screenshots/scenario-1/03-sudo-group-membership-check.png)

![Account details](../screenshots/scenario-1/04-soc-test-account-details.png)

![Last login check](../screenshots/scenario-1/05-soc-test-last-login-check.png)

---

## Scenario 2 Evidence

![Wazuh SSH attack detection](../screenshots/scenario-2/01-wazuh-ssh-attack-detection.png)

![SSH failed login and authentication log](../screenshots/scenario-2/02-ssh-failed-login-auth-log.png)

![soc-attacker account verification](../screenshots/scenario-2/03-soc-attacker-account-verification.png)

![No successful SSH login](../screenshots/scenario-2/04-no-successful-ssh-login-confirmed.png)
