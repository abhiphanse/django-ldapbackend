# Known Issues with this code #

## Mercurial Version ##
The Mercurial version is generally developmental and may have broken components.  At the time of authoring this page the development version does not have a functional password changing mechanism and the support files (views and forms) do not function as intended.  However, it will generally be pushed somewhere in the direction we are headed.

## Some known server issues ##
Debian stable's version of slapd (openldap) as of the 4th of September, 2009, cannot search for custom attributes.  So if you have a custom field (via your own OID or otherwise), or otherwise wish to use something other than **dn** or **uid** to search for your user, forget it.  The version in Debian unstable works, but requires a bunch of libraries from unstable to work.  This is OpenLDAP 2.4.11.  This may have been a one off from the repository, or something weird, but the problem was replicated in twelve VMs (which were used for testing slurpd).

## Kerberos ##
Kerberos is not being updated.  This may or may not happen in the future.  Yes, it's annoying for those of us using Kerberos to store posix passwords, but it's not a priority as it would require additional overhead for Django sites and many servers just do not have the grunt.