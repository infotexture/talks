# Marking Down DITA

### _Lightweight authoring & publishing w/ Markdown & DITA Open Toolkit_

#### Roger Fienhold Sheen [@infotexture](https://twitter.com/infotexture)

---

<i class="fa fa-sitemap fa-4x pull-right muted"></i>

# Agenda

<!-- 
This talk introduces Jarno Elovirta’s DITA-OT Markdown plugins, which extend the DITA Open Toolkit so you can use Markdown files directly in topic references and export existing DITA content in Markdown format for use in other publishing systems.

This makes it easier for people to contribute content to DITA publications, enables mobile authoring workflows, facilitates review processes with less technical audiences and expands the range of publishing options to workflows based on Markdown.
-->

<!-- MarkdownTOC autolink="true" bracket="round" depth="1" -->

- [Markdown – Web Writing Simplified](#markdown-%E2%80%93-web-writing-simplified)
- [Using Markdown with DITA Open Toolkit](#using-markdown-with-dita-open-toolkit)
- [What aboutLightweight DITA?](#what-aboutlightweight-dita)
- [Benefits & Use Cases](#benefits--use-cases)

<!-- /MarkdownTOC -->

---

## Markdown – <br/>Web Writing Simplified

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
* Authors want to take their writing _(and tools)_ on the go.
  - Capture notes with a smartphone on the go
  - Flush out the draft back at the desk
  - Proofread the final result on a tablet later 
* Since writing in Markdown encourages focus on structure rather than presentation, it’s a good match for authoring scenarios where  minimal markup suffices. 

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
      _(tables, footnotes, and citations)_
  - [Github Flavored Markdown][16], or _GFM_, 
      _(strikethrough, fenced code blocks and syntax highlighting)_
  - [CommonMark][17] provides least-common-denominator syntax that should work well everywhere

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
* Pandoc’s [header attributes][21] can be used to define `id` or `outputclass` attributes

So `# Topic title { #carrot .juice}` becomes:

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

## What about<br/>Lightweight DITA?

___

_(coming soon to a toolkit near you…)_

---

## Benefits & Use Cases

<i class="fa fa-lightbulb fa-4x pull-right muted"></i>

* Markdown becomes a first-class citizen 
* Makes it easier to contribute to DITA publications
* Facilitates review processes with less technical audiences 
* Feed DITA into Markdown-based publishing systems 

___

### Publishing via GitBook

    .
    ├── index.md
    ├── SUMMARY.md
    ├── dev_ref
    ├── getting-started
    ├── parameters
    ├── release-notes
    └── user-guide

---

### Workflow Considerations

1. **Avoid roundtripping.**
2. **Simpler content stays Markdown.**  
    Simple content authored collaboratively over multiple versions is kept in Markdown, extended with _Markdown DITA_ conventions and combined as necessary with more complex content maintained in DITA XML.
3. **Convert complex content to DITA & keep it there.**  
    One-off contributions use Markdown as raw material and enriched with conditional processing attributes, conkeyrefs or other more complex semantics.

---

### Resources

* <http://daringfireball.net/projects/markdown/>
* <https://github.com/jelovirt/dita-ot-markdown/>
* <http://infotexture.net/2015/04/dita-ot-markdown-plugin/>

⁂

<!-- 
![][image-1]

[image-1]:  file:///Users/rofish/Documents/Work/Websites/graphics/markdown-dita_800.png
 -->
