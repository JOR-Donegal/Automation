# Describing Ansible

When working with servers, one of the principles is to keep a minimal footprint of applications. Many automation tools use local agents installed on servers; Ansible is agentless and uses a push model, no extra software is running when Ansible is not in use.&#x20;

It has been kept as minimalist as possible, requiring only OpenSSH and Python to operate and using the credentials of the user. It uses su or sudo when privilege escalation is required. Ideally, password-less logins are used, using SSH credentials.&#x20;

Remote machines are all independent of each other.&#x20;

One advantage of this simple model is that we could also use Ansible to deploy software or updates. We can also use it to deploy or provision servers in a virtual environment. In datacentre slang this is sometimes called standing up a server.&#x20;

Sometimes things need to happen in sequence, this is referred to as orchestration. For example, on large-scale application, we bring up the database servers first, then the business logic layer, then the presentation layer, then the load balancing and security.&#x20;

Ansible can also be used for deployments. I can take software, generate executable files, move these files to a production server and start any required services.&#x20;

Ansible is idempotent; that is, if you run it multiple times, you get the same result. Ansible sets the state of a server but checks first to see if an action needs to be taken.&#x20;

Ansible uses modules, this defines what Ansible has pre-programmed capabilities for and they are OS specific. It is worthwhile looking through the list of available modules. Modules are declarative, you describe the state you want a server to be in, not how to get to that state. For example, the YUM module gives a simple example for doing updates.

```
name: upgrade all packages
 yum: name=* state=latest
```

Ansible can also use dynamic scripts to pull information from another system such as Amazon.
