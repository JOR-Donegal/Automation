# Configuration Files

We can have a section in the playbooks with any variables required to keep things tidy.

```
vars:
  secret_key: /users/johnoraw/.ssh/secret.rsa
```

Playbooks can be long and complex, as can the inventory file. For this reason, we may have separate configuration files to hold things like defaults and security key information. We can then declare this grouped variable information file in the playbook.

```
vars_files:
  jor_keys.yml
```

When host configuration information gets too complex, we can dedicate an individual file to a host and save it in the directory host\_vars.&#x20;

When group configuration information gets too complex, we can dedicate an individual file to the group and save it in the directory group\_vars.
