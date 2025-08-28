# Data Models

Behind any configuration initiative, we need a data model. Some questions arise when we are modelling a system&#x20;

* What is its configuration?&#x20;
* If we can retrieve data from the system, what is its state?&#x20;
* Can the equipment notify us of events which occur?&#x20;

## XML&#x20;

Where data must be human and machine readable, most modern systems will use Extensible Markup Language (XML).

```
<?xml version="1.0"?>
 <note> 
    <to>Class</to>
    <from>JOR</from>
    <duedate>18MAR23</duedate>
    <heading>Assignment</heading>
    <body>Assignment 1 has now been posted to the web. </body>
</note>

```

An XML document consists of

1. A declaration of XML version
2. A root element within which all other elements must be nested
3. Child elements (to, from, duedate, heading, body)
4. End of root element&#x20;

All elements must have a closing tag, normally marked as /

Every element can be nested, and this nesting provides unique paths to elements, some of which may otherwise have the same name. This gives each element namespace isolation.

Attributes can be contained in the start tag of an element and must be contained in quotation marks, for example&#x20;

```
<note date=”18MAR23”>. 
```

Generally, I prefer to use elements rather than attributes.

## JSON&#x20;

JavaScript Object Notation or JSON is a good alternative as an underlying data standard. XML is a bit verbose, but well structured. JSON is more economical and easier for a human to read.

```
{ 
"name":"John", 
“job”: “Lecturer
"age":”Too old”, 
“pay":"Too little" 
}';
```

You should review the basics of [JSON](https://www.w3schools.com/js/js_json_intro.asp).

## YAML&#x20;

YAML (YAML Ain't Markup Language) is minimalist compared to XML and is used by some automation tools, notably Ansible.

```
# Lecturers

JOR:
	FirstName: John
	Surname: ORaw
	Job: Lecturer
	        Brain Surgeon
	        Rocket Scientist
```

You should also review the basics of [YAML](http://docs.ansible.com/ansible/devel/reference_appendices/YAMLSyntax.html)
