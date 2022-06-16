# Tokens

On it's most basic definition, tokens are a combination of `name` and `value`. A simple way to store decisions.

```
color primary = #2900D1
padding large = 16px
font-size large = 18px
```

### Format / Language

We don't have a single format for Tokens, depending on the tool you use they will be in a specific format

#### SUI

We use SCSS (hence the $ sign) and a naming convention standardised from [emmet](https://docs.emmet.io/cheat-sheet/) 

```
$c-primary: #2900D1 default!;
$p-l: 16px default!;
$fz-l: 18px default!;
```
{% hint style="info" %}
`default!;` means that the value will be this one until it's overriden anywhere else. 
{% endhint %}

**There are two types of tokens in SUI**

Tokens stored in SUI Theme (tokens):

`$c-success: #00A544 default!;`

Tokens stored in each Component (component tokens)

`$bgc-notification-success: $c-success default!;`

#### Figma

{% hint style="warning" %}
Figma still doesn't support tokens for spacing, paddings and margins 
{% endhint %}

In this tool, where code is not present, colour and text tokens look like this:

![](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/tokens-figma.png)


**Tokens in Apps**

Soon