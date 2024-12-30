---
description: Work out where we are and perform initial domain enumeration
---

# Domain Enumeration

### Find DNS Servers

{% tabs %}
{% tab title="Linux" %}
```bash
// Some code
dig ---
```
{% endtab %}

{% tab title="Windows" %}
```powershell
// Some code
Get-ChildItem ---
```
{% endtab %}
{% endtabs %}

### Get Current Domain

{% tabs %}
{% tab title="Linux" %}

{% endtab %}

{% tab title="Windows" %}
PowerView

```
Get-Domain
```

AD Module

```
Get-ADDomain
```
{% endtab %}
{% endtabs %}



