# Marking Down DITA

### _Lightweight authoring & publishing <small>with</small> Markdown & DITA Open Toolkit_

#### Roger Fienhold Sheen [@infotexture](https://twitter.com/infotexture)

___

<i class="fa fa-sitemap fa-4x pull-right muted"></i>

# Agenda

<!-- 
This talk introduces Jarno Elovirta’s DITA-OT Markdown plugins, which extend the DITA Open Toolkit so you can use Markdown files directly in topic references and export existing DITA content in Markdown format for use in other publishing systems.

This makes it easier for people to contribute content to DITA publications, enables mobile authoring workflows, facilitates review processes with less technical audiences and expands the range of publishing options to workflows based on Markdown.
-->

<!-- MarkdownTOC autolink="true" bracket="round" depth="1" -->

- [Markdown – Web Writing Simplified](#markdown-%E2%80%93-web-writing-simplified)
- [Using Markdown with DITA Open Toolkit](#using-markdown-with-dita-open-toolkit)
- [What about Lightweight DITA?](#what-about-lightweight-dita)
- [Benefits & Use Cases](#benefits--use-cases)

<!-- /MarkdownTOC -->

---

## Markdown – <br>Web Writing Simplified

1. a plain text formatting syntax; _and_ 
2. software … that converts the plain text … to HTML

> The overriding design goal for Markdown’s formatting syntax is to make it as readable as possible. The idea is that a Markdown-formatted document should be publishable as-is, as plain text, without looking like it’s been marked up with tags or formatting instructions. 

Note:
Created in 2004 by John Gruber & Aaron Swartz, [Markdown][4] is: 

So while Markdown was originally designed to make it easier to write for the web without worrying about angle brackets and tags, it’s proving useful for more than just websites…

[4]:    http://daringfireball.net/projects/markdown/

___

<i class="fa fa-mobile-phone fa-4x pull-right muted"></i>

### Mobile Authoring & Lightweight Content

* Mobile devices drive interest in lightweight content
* Authors want to take their writing _(and tools)_ on the go
  - _Capture notes with a smartphone on the go_
  - _Flesh out the draft back at the desk_
  - _Proofread the final result on a tablet later_ 
* Markdown helps focus on structure over presentation 
* Good for scenarios where minimal markup suffices

___

### Markdown Meets DITA

* The DITA learning curve presents a barrier to adoption.

* But why ask people to struggle with XML or learn a new tool before they can provide input to our publications?

_Shouldn’t we just let people write ‽_

_ — Let the tools figure out what to do._

___

### Plaintext panacea?

Several proposals rely on Markdown to simplifly authoring:

* **DITA Glass** — _oXygen's URL-based on-the-fly conversion_
* **Lightweight DITA** — _more on that in a moment…_

Some use `h2d` to convert to HTML as an interim format. 

This limits vocabulary to the original Markdown syntax — _but now there’s another way…_

---

## Using Markdown with DITA Open Toolkit

<i class="fa fa-puzzle-piece fa-4x pull-left muted"></i>

Jarno Elovirta’s [DITA-OT Markdown][11] plugin extends the toolkit so you can use Markdown files as topics and convert DITA to Markdown. 

Install it in DITA-OT 2.2 – 2.5 with the `dita` command:

    dita --install https://github.com/jelovirt/dita-ot-markdown/releases/ ↩
      download/1.3.0/com.elovirta.dita.markdown_1.3.0.zip

[11]:   https://github.com/jelovirt/dita-ot-markdown

___

### Adding Markdown topics

To add a Markdown topic, set the `@format` attribute to `markdown` so the plugin will recognize the source file as Markdown and convert it to DITA:

    <map>
      <topicref href="markdown-dita-topic.md" format="markdown"/>
    </map>

___

### Publishing to Markdown

The plugin not only _reads_ Markdown, it also provides new output formats to convert DITA content to Markdown.

    dita --input=userguide.ditamap --format=markdown

* Use `markdown` to publish Markdown DITA files.

* For [GitHub Flavored Markdown](https://help.github.com/categories/writing-on-github/): `markdown_github`.

* To publish via [GitBook](https://www.gitbook.com), use `markdown_gitbook`.

---

### A Myriad of Markdowns

* The original Markdown syntax supports basic HTML
* A variety of extensions support additional applications
  - [MultiMarkdown][15], or _MMD_  
      _(tables, footnotes & citations)_
  - [Github Flavored Markdown][16], or _GFM_  
      _(strikethrough, fenced code blocks & syntax highlighting)_
  - [CommonMark][17] provides reliable shared syntax that should work well everywhere
  - _and many more…_

[15]: http://fletcherpenney.net/multimarkdown/
[16]: https://help.github.com/articles/github-flavored-markdown/
[17]: http://commonmark.org/

___

### The “Markdown DITA” Format

The **DITA-OT Markdown** plugin introduced a new Markdown flavor called _“Markdown DITA”_, a representation of DITA content in Markdown.

_Markdown DITA_ builds on CommonMark, using standard Markdown constructs or those from other established Markdown flavors to represent DITA content. 

___

### Keys As Reference Links

<i class="fa fa-key fa-4x pull-right muted"></i>

The shortcut reference link syntax is used to represent DITA key references, so you can just write `[key]` to create a cross-reference like `<xref keyref="key"/>`.

___

### Definition lists

Definition lists use the [PHP Markdown Extra][19] format, so 

    Term
    :   Definition.

becomes a DITA definition list:

    <dl>
      <delentry>
        <dt>Term</dt>
        <dd>Definition.</dd>
      </delentry>
    </dl>

[19]:   http://michelf.com/projects/php-markdown/extra/#def-list

___

### Syntax Extensions

<i class="fa fa-plus-sign-alt icon-4x pull-left muted"></i>

* Tables use the [MultiMarkdown][20] table extension format
* Pandoc’s [header attributes][21] can be used to define `@id` or `@outputclass` attributes

So `# Topic title {#carrot .juice}` becomes:

    <topic id="carrot" outputclass="juice">
      <title>Topic title</title>

[20]:   http://fletcherpenney.net/multimarkdown/
[21]:   http://johnmacfarlane.net/pandoc/demo/example9/pandocs-markdown.html#extension-header_attributes

___

### DITA-Specific Extensions

Where necessary, _Markdown DITA_ establishes new conventions to support additional DITA features:

* Specify the information type of the generated DITA topic with a header attribute like `{.task}`
* Generate `<section>` and `<example>` elements with the `{.section}` and `{.example}` attributes.

The plugin’s [syntax reference][24] provides an overview of the supported constructs  and illustrates how DITA’s XML structures are represented in _Markdown DITA_. 

[24]:   https://github.com/jelovirt/dita-ot-markdown/wiki/Syntax-reference

---

### _But that was all available<br/>two years ago…_

___

### _… so what’s new?_

___

### It’s built in.

### DITA Open Toolkit 3.0 <!-- .element: class="fragment" -->

---

## What about <br>Lightweight DITA?

___

### New Authoring Formats

<i class="fa fa-binoculars fa-4x pull-right muted"></i>

**DITA Open Toolkit** Release 3.0 provides preview support for the _MDITA_ and _HDITA_ authoring formats planned for LwDITA.

These new formats have been proposed<sup>*</sup> as alternative representations of DITA content in Markdown or HTML.

> <sup>*</sup> [Lightweight DITA Committee Note](http://docs.oasis-open.org/dita/LwDITA/v1.0/cn01/LwDITA-v1.0-cn01.pdf) _(coming soon…)_

___

### MDITA

**Lightweight DITA authoring format based on Markdown.**

Recent proposals include two profiles for MDITA:

* _“Core profile”_ — based on GitHub Flavored Markdown and includes elements that are common to many other Markdown implementations.
* _“Extended profile”_ — borrows features from other flavors of Markdown to represent a broader range of DITA content with existing plain-text syntax conventions.

___

### So what’s the difference? 

The Markdown DITA parser included in the `org.lwdita` plug-in provides preliminary support for LwDITA profiles — _**and** additional Markdown constructs_.

Set `@format` to `mdita` for LwDITA-specific processing:

    <map>
      <topicref href="mdita-topic.md" format="mdita"/>
    </map>

Note: MDITA parsing is stricter than the more lenient document parsing approach that is applied to markdown documents.

---

## Benefits & Use Cases

<i class="fa fa-lightbulb fa-4x pull-right muted"></i>

* Markdown becomes a first-class citizen
* Makes it easier to contribute to DITA publications
* Facilitates review processes with less technical audiences
* Feed DITA into Markdown-based publishing systems

___

### Workflow Considerations

___

### №1

#### Avoid roundtripping. <!-- .element: class="fragment" -->

#### Seriously. <!-- .element: class="fragment" -->

#### _unless you like data loss…_ <!-- .element: class="fragment" -->

---

### №2

#### Simpler content stays in Markdown. <!-- .element: class="fragment" -->

Simple content authored collaboratively over multiple versions is kept in Markdown, extended with Markdown DITA conventions and combined as necessary with more complex content maintained in DITA XML. <!-- .element: class="fragment" -->

___

### Maintain simple content in Markdown & publish with DITA

1. Create topic content in Markdown
2. Add topic reference to ditamap: `@format="markdown"`
3. Include DITA XML topics with complex content
3. Publish DITA map to multiple output formats

---

### №3

#### Convert complex content to DITA & keep it there. <!-- .element: class="fragment" -->

One-off contributions use Markdown as raw material and are subsequently enriched with conditional processing attributes, conkeyrefs or other more complex semantics. <!-- .element: class="fragment" -->

___

### Draft topics in Markdown for conversion to DITA

1. Draft topic content in Markdown
2. Add topic reference to ditamap: `@format="markdown"`
3. Publish normalized DITA output: `--format=dita`
4. Save generated DITA topic
5. Enrich topic with DITA constructs
6. Maintain & publish subsequent revisions in DITA

---

### Publishing DITA content with Markdown-based toolchains

1. Create simple topics in Markdown
2. Combine with complex DITA content in maps
3. Publish DITA map to Markdown-based formats:
    + `--format=markdown`
    + `--format=markdown_github`
    + `--format=markdown_gitbook`
4. Mix in additional Markdown content
5. Publish via GitBook, Leanpub, etc.

___

### Sample [GitBook][9] output

[<img src="https://raw.githubusercontent.com/infotexture/talks/dita-europe/assets/ot-docs-markdown-gitbook_800.png" width="666" title="infotexture.github.io/ot-docs-markdown"/>](http://infotexture.github.io/ot-docs-markdown)

[9]: https://www.gitbook.com

___

### GitBook Output Structure

Sample output: [github.com/infotexture/ot-docs-markdown](https://github.com/infotexture/ot-docs-markdown)

    .
    ├── index.md
    ├── SUMMARY.md
    ├── dev_ref
    ├── getting-started
    ├── parameters
    ├── release-notes
    └── user-guide

Rendered result: [infotexture.github.io/ot-docs-markdown](http://infotexture.github.io/ot-docs-markdown)

---

![][image-2]
[image-2]:  https://raw.githubusercontent.com/infotexture/talks/dita-europe/assets/markdown-dita_800.png

---

### Resources

* [github.com/jelovirt/org.lwdita](https://github.com/jelovirt/org.lwdita) _(new in DITA-OT 3.0)_
* [infotexture.net/2015/04/dita-ot-markdown-plugin](http://infotexture.net/2015/04/dita-ot-markdown-plugin/)
* [github.com/jelovirt/dita-ot-markdown](https://github.com/jelovirt/dita-ot-markdown/) _(deprecated)_
* [daringfireball.net/projects/markdown](https://daringfireball.net/projects/markdown/)
* [commonmark.org](http://commonmark.org/)

⁂
