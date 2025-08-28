# Ansible

There is a classic Sci-Fi book by Orson Scott Card called Ender’s Game (the movie was less good but did have Harrison Ford!). In the book the Ansible is used to control many remote spaceships at the same time. Setting up infrastructure is a long and complex job. The configuration tool Ansible is one of the ways we can configure many nodes simultaneously using automation, in an agentless manner; that is without installing dedicated software on the target hardware. Ansible is maintained on [GitHub](https://github.com/ansible/ansible) and the design principles include “…have a dead simple setup process and a minimal learning curve”. One of the better books on the subject is by O’Reilly; Hochstein, L. and Moser, R., 2017. Ansible: Up and Running: Automating Configuration Management and Deployment the Easy Way. " O'Reilly Media, Inc.".

Before beginning you would normally be familiar with the environment you are trying to configure. I would prefer to be familiar with network equipment or an operating system before using Ansible to configure it. If I can’t configure and script the environment, I have work to do before attempting to automate its configuration.&#x20;

Ideally configuration should be stateless. I should be able to say a server has a particular configuration and then (in the words of Jean-Luc Picard) “make it so”.&#x20;

If a service is already installed it should not be duplicated no matter how many times I run the configuration tool. And I should be able to run tasks in parallel across multiple servers.&#x20;

The descriptions in this document are very simple and as you can imagine, a real-world deployment will have some complexity and formality. The main thing I needed to leave out for simplicity was version control. In real deployments, will keep a track of changes to any configuration files and these days, I use git exclusively for this.&#x20;

Our starting point: we need a domain specific language (DSL) to describe the state of servers or devices and we will need tools and a protocol to enforce this state.
