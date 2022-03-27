# Creating discourse relationships

**You can create formal discourse relations between nodes by writing and outlining!**

The extension has an in-built [grammar](../fundamentals/the-discourse-graph-extension-grammar/) that enables it to recognize when certain patterns of writing and outlining are meant to express particular discourse relations (e.g., support, oppose, inform) between discourse nodes. When it recognizes these patterns, it "writes" them to a formal discourse graph data structure, that you can then use to explore or query your discourse graph.

## Basic "stock" patterns

The extension ships with the ability to recognize three such writing/outlining patterns. Give them a try!

### Question informed by Evidence

Go into a question page.&#x20;

Create a block, and reference an evidence page.

Like this:

![](<../.gitbook/assets/CleanShot 2022-03-26 at 21.57.06.png>)

The system now formally recognizes that this piece of evidence **informs** the question (and equivalently, the question is **informed by** that evidence)!

You can verify this by checking the [discourse context](exploring-your-discourse-graph/discourse-context.md) of the question or the evidence page.

Or by running a [query](querying-your-discourse-graph.md) for evidence that informs that question.

### Claim supported by Evidence

Create a block anywhere, and reference a claim page. We'll call this the claim block.

Indent a block underneath the claim block. And reference the page `[[SupportedBy]]`. We'll call this the connecting block.

Indent a block underneath the connecting block. And reference an evidence page.

Like this:

![](<../.gitbook/assets/CleanShot 2022-03-26 at 21.57.25.png>)

The system now formally recognizes that this piece of evidence **supports** that claim (and equivalently, the claim is **supported by** that evidence)!

You can verify this by checking the [discourse context](exploring-your-discourse-graph/discourse-context.md) of the claim or the evidence page.

Or by running a [query](querying-your-discourse-graph.md) for evidence that supports that claim.

### Claim opposed by Evidence

Create a block anywhere, and reference a claim page. We'll call this the claim block.

Indent a block underneath the claim block. And reference the page `[[OpposedBy]]`. We'll call this the connecting block.

Indent a block underneath the connecting block. And reference an evidence page.

Like this:

![](<../.gitbook/assets/CleanShot 2022-03-26 at 21.57.49.png>)

The system now formally recognizes that this piece of evidence **opposes** that claim (and equivalently, the claim is **opposed by** that evidence)!

You can verify this by checking the [discourse context](exploring-your-discourse-graph/discourse-context.md) of the claim or the evidence page.

Or by running a [query](querying-your-discourse-graph.md) for evidence that supports that claim

## Digging deeper

Want to recognize other patterns that aren't listed here? Or don't like these? You can [change them](extending-and-personalizing-your-discourse-graph.md)! But you might first want to [understand how the grammar works](../fundamentals/the-discourse-graph-extension-grammar/).
