# Motion

Our Motion system improves the narrative of our products.
The movement, in addition to attracting attention, guides users with a more dynamic, fluid and intuitive experience, helping them to progress and interact with our platforms to be more productive.

We differentiate between two types of Motion:

**Transitions:**  They are CSS properties that help to more smoothly render any movement or change of state associated with our components or between UI elements that have a spatial or navigational relationship.

**Custom animations:** When it is not possible to generate your animation with a combination of transitions/animations by CSS, we will use animated .json with the export to Lottie.

You can see the differences with [visual examples here](https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=66%3A179&node-id=101%3A722&viewport=653%2C412%2C0.07&scaling=contain&starting-point-node-id=101%3A722)


## Transitions
Our components/screens can have associated transitions, generating interactions/microinteractions. You can use several types, customize the duration, its acceleration, its direction, delay or loop.

Together, they choreograph our products. By correctly combining its properties, you can generate an experience that represents your brand and make users identify with it.

### Transitions Presets:  The basics
We contemplate the most common transitions for SUi, we can expand the catalog in the future if necessary.

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1428&viewport=-2455%2C364%2C0.4&scaling=contain&starting-point-node-id=335%3A1428&hotspot-hints=0&hide-ui=1" %}

### Transitions Presets: Combos examples
You can combine the above presets according to your needs.

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1444&viewport=-2455%2C364%2C0.4&scaling=scale-down&starting-point-node-id=335%3A1444&hotspot-hints=0&hide-ui=1" %}

### How it works?
Transitions are Presets defined with customizable properties according to your vertical. Below you will see the customization properties that you can modify.

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1448&viewport=-5438%2C-81%2C0.77&scaling=scale-down&starting-point-node-id=335%3A1448&hotspot-hints=0&hide-ui=1" %}

You can also set various properties for your transitions/animations depending on your needs.

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1470&viewport=-5438%2C-81%2C0.77&scaling=scale-down&starting-point-node-id=335%3A1470&hotspot-hints=0&hide-ui=1" %}

## Properties

### Duration
We tokenize the durations so you have more freedom when applying them. We generate 9 standard durations but
Figma by default associates 300ms to any transition (except for the new Spring Animations Timing functions).

You can associate a different speed token in your vertical to adapt them to your brand, both in the components and between the elements of your vertical that have a spatial or navigation relationship. By default, SUi contemplates pre-established times. Even so, keep in mind the Do's & Don'ts that you will find below for your customization.

{% embed url="{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1496&viewport=-5438%2C-81%2C0.77&scaling=scale-down&starting-point-node-id=335%3A1496&hotspot-hints=0&hide-ui=1" %}" %}

### Timing function
We advise applying Ease timings whenever possible to make your animations shine. You can also adjust its properties according to your brand, although by default there are the beziers that Figma will provide when you apply these properties, so it will make your job easier to keep them the same but... up to you!

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1545&viewport=-5438%2C-81%2C0.77&scaling=scale-down&starting-point-node-id=335%3A1545&hotspot-hints=0&hide-ui=1" %}

### Timing function Easing Back (from Figma)
Figma provides these Timing options and UX can make use of them.. Easing back, creates a bounce in the animation that serves as anticipatory action. The animation exceeds the initial keyframe value and then speeds up when it reaches the end.

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1566&viewport=-5438%2C-81%2C0.77&scaling=scale-down&starting-point-node-id=335%3A1566&hotspot-hints=0&hide-ui=1" %}

### Timing function: Figma Spring Animations
Figma allows you to create these other Timing properties (linked to Transitions Presets like the rest of Time functions) where their configuration is different: Stiffness, Damping & Mass that are generated through Keyframes from FE.

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1582&viewport=-5438%2C-81%2C0.77&scaling=scale-down&starting-point-node-id=335%3A1582&hotspot-hints=0&hide-ui=1" %}

Application examples of Figma Spring Animations as transitions

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1615&viewport=-5438%2C-81%2C0.77&scaling=scale-down&starting-point-node-id=335%3A1615&hotspot-hints=0&hide-ui=1" %}

Examples of use that Figma recommends on Spring Animations such as transitions or animations.

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1621&viewport=-5438%2C-81%2C0.77&scaling=scale-down&starting-point-node-id=335%3A1621&hotspot-hints=0&hide-ui=1" %}

### Direction
Up/Down/Left/Right direction props.

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1636&viewport=-5438%2C-81%2C0.77&scaling=scale-down&starting-point-node-id=335%3A1636&hotspot-hints=0&hide-ui=1" %}

### Delay
If you need to delay the playback of the transition/animation, you can apply a delay as long as you think necessary without limitations.

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1642&viewport=-5438%2C-81%2C0.77&scaling=scale-down&starting-point-node-id=335%3A1642&hotspot-hints=0&hide-ui=1" %}

### Loop
You can create loops on your animations. For example, a Spinner we don't know how long it will be on the screen, so it must have the Loop prop active.

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1651&viewport=-5438%2C-81%2C0.77&scaling=scale-down&starting-point-node-id=335%3A1651&hotspot-hints=0&hide-ui=1" %}

## Does & Dont’s

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1661&viewport=-5438%2C-81%2C0.77&scaling=scale-down&starting-point-node-id=335%3A1661&hotspot-hints=0&hide-ui=1" %}

{% embed url="https://www.figma.com/proto/B2rY1jzzrP0uDdRE6GPdWQ/Motion?page-id=335%3A571&node-id=335%3A1672&viewport=-5438%2C-81%2C0.77&scaling=scale-down&starting-point-node-id=335%3A1672&hotspot-hints=0&hide-ui=1" %}
