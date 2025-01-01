---
description: Work out where we are and perform initial domain enumeration
---

# Domain Enumeration

### Check DHCP Information

```bash
nmap --script broadcast-dhcp-discover
```

### Check DNS Information

```bash
nmap --script dns-srv-enum --script-args dns-srv-enum.domain=$FQDN_DOMAIN
```

### Discover DCs

And potentially other interesting servers

{% tabs %}
{% tab title="dnsutils" %}
Find the principal DC

```bash
nslookup -type=srv _ldap._tcp.pdc._msdcs.$FQDN_DOMAIN
```

Find other DCs

```bash
nslookup -type=srv _ldap._tcp.dc._msdcs.$FQDN_DOMAIN
```

Find the Global Catalog

```bash
nslookup -type=srv gc._msdcs.$FQDN_DOMAIN
```

Find other possible DCs

```bash
nslookup -type=srv _kerberos._tcp.$FQDN_DOMAIN
nslookup -type=srv _kpasswd._tcp.$FQDN_DOMAIN
nslookup -type=srv _ldap._tcp.$FQDN_DOMAIN
```
{% endtab %}

{% tab title="netexec" %}
Get the DC List

```bash
nxc ldap <ip> -u user -p pass --dc-list
```
{% endtab %}
{% endtabs %}









