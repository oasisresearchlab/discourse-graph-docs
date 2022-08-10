# Sharing your discourse graph

You can export your discourse graph as a whole, or from queries of your graph, to archive your most important notes, or share them with others.

The extension exports to 1) markdown, 2) csv (neo4j-compatible [labeled property graph](https://neo4j.com/blog/rdf-triple-store-vs-labeled-property-graph-difference/)), and 3) `json`

Demo:

{% embed url="https://www.loom.com/share/ca222cb93efb4ed890b4c9e91f05db52" %}

### Markdown export options

Since markdown has different flavors, and different tools you might want to export/archive your notes to handle links differently (e.g., wikilinks vs. markdown links) and different operating systems have different filename limitations, we have a range of options for customizing the markdown export. These can be found on the `Export` tab of the discourse graph configuration in `roam/js/discourse-graph`.

![](<../.gitbook/assets/CleanShot 2022-08-10 at 10.03.33@2x.png>)

Here is a brief explanation of each option:

* `Max Filename Length` sets the maximum length of the filenames; this is important if you have page names that are quite long and may run afoul of, say, Windows' filename length limit of 250-260 characters.
* `Remove Special Characters` removes all "special characters" that may lead to trouble for filenames in different operating systems, such as `?` (not allowed on Windows) or `/` (denotes file/folder boundaries).
* `Simplified Filename` strips away all "template" characters (i.e., everything except the `{content}` in the node format: for example, if you define a Claim node as `[[CLM]] - {content}`, and have a Claim node `[[[[CLM]] - people are lazy]]`, the exported filename will be `people are lazy`
* `Frontmatter` specifies what properties to add to the YAML.&#x20;
  * By default, the properties are:
    * `title: {text}`
    * `url:` [`https://roamresearch.com/#/app/yourGraphName/page/{uid}`](https://roamresearch.com/#/app/roam-synthesis/page/{uid})``
    * `author: {author}`
    * `date: {date}`
  * You can add properties as key-value pairs in the same format:
    * <img src="../.gitbook/assets/CleanShot 2022-08-10 at 10.11.22.gif" alt="" data-size="original">
* `Resolve Block References` and `Resolve Block Embeds` control whether you want to resolve block references/embeds in your export. You can keep this turned off if you are unsure of the privacy implications of references/embeds.
* Link Type controls whether inline page references are wikilinks (`[[like this]]`) or alias (`[like this](pageName.md)`)

Here is an example of a discourse graph exported to Obsidian-compatible markdown: [https://publish.obsidian.md/joelchan-notes](https://publish.obsidian.md/joelchan-notes)
