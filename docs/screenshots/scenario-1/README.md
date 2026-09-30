## Scenario 1: Suspicious Local User/Group Creation

### Objective

Detect and investigate the creation of a new local user/group on the Linux endpoint using Wazuh.

### Activity

A test account named `soc-test` was created on the Ubuntu endpoint.

### Detection

Wazuh detected the account creation activity and displayed the event in the Wazuh dashboard.

![Wazuh user creation alert](screenshots/scenario-1/01-wazuh-user-creation-alert.png)

### Investigation

The `soc-test` account was then investigated directly on the Linux endpoint.

#### User and Group Verification

The `id` and `getent group` commands were used to verify the account and group.

![User and group verification](../screenshots/scenario-1/02-soc-test-user-group-verification.png)

#### Sudo Group Check

The sudo group was checked to determine the relevant group membership.

![Sudo group check](../screenshots/scenario-1/03-sudo-group-membership-check.png)

#### Account Details

The account details were checked using `chage` and `getent passwd`.

![Account details](../screenshots/scenario-1/04-soc-test-account-details.png)

#### Last Login Check

The `lastlog` command was used to check the login history of the account.

![Last login check](../screenshots/scenario-1/05-soc-test-last-login-check.png)

### Investigation Summary

The `soc-test` account was confirmed to exist on the endpoint. Its group membership, account configuration, and login history were checked as part of the investigation.
