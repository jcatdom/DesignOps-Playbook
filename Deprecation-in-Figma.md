# Deprecating components in Figma

## The Challenge

**To update components or building new ones from scratch?**

<!-- Deprecating components is not the same as removing components but replacing them by new ones.
We have a system that ensures nothinhg breaks, and will never remove the original. -->

## Change it's name, make it easy to spot in the components panel

Add an ❌ and `[deprecated]` to the name of the old component to attract attention.

By adding it to the **end** of the name we ensure you have the new and old components next to each other.

{% hint style="danger" %}
Avoid making it harder to find in the components panel 

* Don't add "deprecated" to the **begining** of the original name
* Don't move the component to a new page "deprecated"
{% endhint %}


## Add a visual hint, make it easy to spot in a design



## Write a comprehensive publish message

Make sure all users know what to expect if they update their libraries.

**Tips**

* Keep it short 
* Write in English
* Write in infinitive (add, remove, modify )
* Add the name of the component
* Add short details about what changed

{% hint style="success" %}
❌ deprecate button - refactor adopting figma latest best practices
{% endhint %}

{% hint style="danger" %}
"This is a breaking change, we've deprecated the old component atom-button because we needed to add the props and variants figma introduced in the latest relase"
{% endhint %}

## Version names

We don't version components with semantic numbers in Figma, such as `1.2` `2.0` `2.1`, because we don't want different versions of a single component in production. 

What you see in Figma will always be the latest component, that's why it's important that you always keep your libraries updated.