# Communicating with Devices

## RPC&#x20;

A Remote Procedure Call (RPC) occurs when a programme invokes a procedure to run on another computer; the procedure runs as if it were local. A client makes an RPC to a server to execute a specific piece of code. When we look at the NETCONF RFC {1} section 4 we get an overview of the RPC model and the example of a NETCONF call with no parameters is shown;

Parameters are passed in a standard XML format; 1234567

After a the server will respond with ether a or an **\<rpc-reply>** or an **\<rpc-error>**

```
<rpc-reply message-id="101" xmlns="urn:ietf:params:xml:ns:netconf:base:1.0"
 xmlns:ex="http://example.net/content/1.0"
    <data>
        <!-- contents here... -->
    </data>
</rpc-reply>
```

## REST&#x20;

The Internet was designed with a very simple underlying protocol set; Hyper Text Transfer Protocol (HTTP) is the protocol which allows us to transfer hypertext between devices \[7]. Hyper Text Markup Language (HTML) is the standard language for human usable web applications. Extensible Markup Language (XML) is human or machine readable and lets us format what appear to be documents with data structures.

Although these Internet technologies were designed to allow people to interact with servers, machine-to-machine communications are equally possible. REpresentational State Transfer (REST) web services have become popular due to their simplicity and ubiquity. A stateless interface can be manipulated by simple HTTP operations like GET, PUT, POST, etc. REST gives us something like a programmable web \[8]. The IETF are currently developing an alternative standard to NETCONF using REST, this is called RESTCONF.
