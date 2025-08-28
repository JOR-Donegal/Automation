# Background

Prior to c. 2010, server and network configuration began when we received the customer equipment. Once design freeze happened, the equipment shipped to a staging facility and was staged. This means everything is removed from the boxes, set up and wired, configured via the command line (CLI) and tested. It was only at this point we could begin complex configurations and perhaps confirm the system would work!&#x20;

Virtualization has very much changed this paradigm. Servers can now be set up in isolation of the hardware, even on a system engineer’s basic laptop. When we teach operating systems, we always introduce the concept of scripting. In any OS, we can document and record our actions in a script file. Every complex task is self-documenting and repeatable.&#x20;

Linux has always been configured in this way. The shell is a good environment with many tools, each of which are designed to do a specific job. In Linux, almost everything is a file and there are good text-based tools.&#x20;

In early Windows, we had basic command scripts also, batch files. The MS-DOS command prompt was never intended for a server environment though and Microsoft introduced PowerShell as a Windows equivalent to Unix scripting, specifically oriented at object-oriented scripting.&#x20;

Network equipment was more problematic. Firstly, there were no standard interfaces, so you were required to write screen scraping software to interact with the CLI. There were no standard operating systems, requiring each coding effort to be customised.&#x20;

Finally, the vendors had no rules for their own behaviour, every new release had to be re-verified in case a command had changed. Tools emerged which initially allowed us to detect configuration changes based on dates and then backup changed configurations. With an underlying access mechanism, this could be expanded to scripting modifications, but few of us fully trusted the technique. What we really needed was a proper Application Programming Interface (API); where we could issue unambiguous commands and get unambiguous responses. The IETF developed [NETCONF](https://datatracker.ietf.org/doc/html/rfc6241) in the early part of the millennium and [YANG](https://datatracker.ietf.org/doc/html/rfc7950), a data modelling language to use as a basis for configuration c.2010. With these standards-based tools, an administrator could perform configurations and monitor equipment without interacting with a proprietary CLI.&#x20;

The efficiency of a modern operation implementing DevOps does not allow for the inefficiency of manual configuration via a CLI. We need some way to do remote procedure calls (RPC) to invoke functionality, or perhaps use REST interfaces. We need a better way and a data exchange format which is both human and machine readable, like YAML, XML or JSON.

There are many tools we could look at now. In these notes I'm going to focus on generic terminology and principles first.&#x20;

I'm then going to look at one tool; I could have used Chef, Puppet or Salt, but I'm going to discuss Ansible. Its the tool I'm most familiar with and I have used it in production systems.
