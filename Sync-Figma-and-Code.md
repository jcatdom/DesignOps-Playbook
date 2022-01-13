# Sync Figma and Code

We don't have an automatic sync process between Figma and Code

Every change you make in one part of the code or a Figma file need to be adjusted on the counterpart proactevely.

### In case of differences, which one is the source of truth?

**The right one:**

In most of the cases we know how a component or style should look like, as a matter of fact that's how we spot defects when we realise something is not as defined.

- If you find a defect in the code but your Figma file is OK, the code needs to be adjusted
- If you find a defect in your Figma file but the code is OK, the Figma file needs to be adjusted

### So, we don't have a single source of truth

That's correct, we don't have a single source of truth. Designers work in Figma and must assume that everything is OK in Figma the same way Developers should always asumme the code is correct.

### How to request a change:

**If you make a change in Figma that needs to be coded:**

- In SUI: [Open an issue in github](https://github.com/SUI-Components/sui-components/issues/new?template=report-a-bug---issue.md)
- In your brand: Open a ticket in your project

**If you make a change in Code that needs to be included in Figma:**

- Open a ticket for DesignOps in [Jira](https://jira.scmspain.com/secure/RapidBoard.jspa?projectKey=DO&rapidView=4329)