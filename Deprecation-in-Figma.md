# Deprecating components in Figma

## The Challenge

**To update components or building new ones from scratch?**

<!-- Deprecating components is not the same as removing components but replacing them by new ones.
We have a system that ensures nothinhg breaks, and will never remove the original. -->

## Naming

Add `[deprecated]` to the original name

{% hint style="danger" %}
Don't add it to the begining of the original name, because...

`❌ [Deprecated] Button`
{% endhint %}

**Don't move to a new "Deprecated Components" page**


## Visual hint

## Communication

- Comprehensive commit/publish messages

## Version names

We don't version components with semantic numbers in Figma (`1.2` `2.0` `2.1`) because we don't want different versions of a single component in production. 

What you see in Figma will always be the latest component, that's why it's important that you always keep your libraries updated.