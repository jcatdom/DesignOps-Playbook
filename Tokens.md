# Tokens

On it's most basic definition, tokens are a combination of a definition and it's value, a simple line of code that stores the decisions we make:

Some examples:

`color primary = #2900D1`
`padding large = 16px`
`font-size large = 18px`
`etc`

Depending on the tool you use, this definition will be in a specific format:

The same example looks like this in SUI, because we use the naming standardised from [emmet](https://docs.emmet.io/cheat-sheet/) 

`c-primary: #2900D1 default!`
`p-l: 16px default!`
`fz-l: 18px default!`

In Figma (where code is not present) the same tokens look like this:

![](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/tokens-figma.png)

{% hint style="warning" %}
Figma still doesn't support tokens for spacing, paddings and margins 
{% endhint %}


**Tokens in SUI**

There are two types if tokens in SUI:

Tokens (stored in SUI Theme)

`$c-success: #00A544 default!;`

Component Tokens (stored in each Component)

`$bgc-notification-success: $c-success default!;`

{% hint style="info" %}
The `default!;` part means that it will have this value, unless is overriden anywhere else. 
{% endhint %}

**Tokens in Apps**

Soon