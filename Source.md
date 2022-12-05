# Source of truth

Every style and component are present in Figma and Code, and we work hard to maintain them perfectly aligned.

## Do Figma and Code sync automatically?

No, we don't have an automatic process to sync Figma and Code. You need to update your side proactively to the changes made on the other side.

* If you find a defect in the code but the Figma file is OK: Adjust Code
* If you find a defect in the Figma file but the code is OK: Adjust Figma
* If you find a defect in Figma and also in Code: Adjust both

### Vale but, in case of difference, which one is "The Source of truth"?

We don't have a _single_ source of truth. Designers work primarelly in Figma, and must trust that everything is OK in Figma the same way Developers must asumme that the code is correct.

We've tried to force it for a while, but a really "single" source of truth is not feasible in a multi-disciplinary, multi-platform company. 

We encourage our designers and developers to ensure their tools and components are updated by fixing and reporting everything they find we need to fix.

This way Designers can work in Figma trusting that everything is correct the same way developers can asumme the code is correct and safe to be implemented.

### So, in case of difference, which one is "the right one"?

The documentation, the decisions defined and documented. If there's no documentation available, or it's deprected, you need to create it and attach it to the request.

## How do we ensure consistency with this fragmented no-source of truth?

We have [tokens](Tokens.md), probably the most powerful system to get every App in sync so far.

Learn how to update the Figma files or the code here:

{% content-ref url="Bugs.md" %}
[Bugs.md](Bugs.md)
{% endcontent-ref %}
