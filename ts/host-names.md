[title]: # (Host Names)
[tags]: # (faq,hostnames,conventions)
[priority]: # (703)
# Host Names

We follow these general naming conventions and constraints:

https://support.microsoft.com/en-us/help/909264/naming-conventions-in-active-directory-for-computers-domains-sites-and

An underscore "_" in the host name is not currently supported. The underscore has a special role, as it is permitted for the first character in SRV records by RFC definition, but newer DNS servers may also allow it anywhere in a name. For more details, see: http://technet.microsoft.com/en-us/library/cc959336.aspx