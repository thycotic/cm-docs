[title]: #	(Secret Server Requirements)
[tags]: #	(faq,ss,apis,connection)
[priority]: #	(604)
# Secret Server Requirements

**Question**: What are the quick, hard requirements for connecting to Secret Server?

**Answer**: 

- Must have SS 10.7:
  - Requires REST APIs

- Must have the "IsConnectionManager" flag set on SS license
- When we connect, we try to check what version of SS is being used:
  - If below 10.7 we will not connect
  - If we cannot detect the SS version, we return the message we receive from SS and it usually means the SS version # is hidden, and we receive an “Access Denied” message

- A SS Username