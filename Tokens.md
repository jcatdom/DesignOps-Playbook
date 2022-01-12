# Tokens

On it's most basic definition, tokens are a combination of a definition and it's value, a simple line of code that stores the decisions we make:

**Some examples**

`color primary = #2900D1`

`padding large = 16px`

`font-size large = 18px`

`etc`

### Formats

Depending on the tool you use, this definition will be in a specific format:

**SUI**

We use the naming standardised from [emmet](https://docs.emmet.io/cheat-sheet/) 

`c-primary: #2900D1 default!`

`p-l: 16px default!`

`fz-l: 18px default!`

And also, there are two types of tokens in SUI

Those stored in SUI Theme (tokens): `$c-success: #00A544 default!;`

and those stored in each Component (component tokens): `$bgc-notification-success: $c-success default!;`

{% hint style="info" %}
The `default!;` part means that it will have this value, unless is overriden anywhere else. 
{% endhint %}


**Figma**

In this tool, where code is not present, the same tokens look like this:

![](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/tokens-figma.png)

{% hint style="warning" %}
Figma still doesn't support tokens for spacing, paddings and margins 
{% endhint %}

**Tokens in Apps**

Soon