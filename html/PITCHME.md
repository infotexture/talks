## Bootstrapping DITA

### _Customizing HTML output for modern web frameworks_

#### Roger Sheen [@infotexture](https://twitter.com/infotexture)

---

<i class="fa fa-sitemap fa-5x pull-right muted"></i>

# Agenda

<!-- 
Web developers often use CSS frameworks, HTML5 boilerplate or component libraries like Bootstrap or Foundation to quickly build robust, responsive sites. With custom HTML plug-ins, DITA-OT can be extended to produce HTML5 output that makes use of these common templates so that generated documents can build on existing front-end solutions.

This talk will outline the process, using the DITA-OT project website at dita-ot.org as an example.
-->

<!-- MarkdownTOC autolink="true" bracket="round" depth="1" -->

- [Default HTML5 output](#default-html5-output)
- [DITA-OT project website](#dita-ot-project-website)
- [Bundling CSS & adding metadata](#bundling-css--adding-metadata)
- [Adding classes to generated HTML](#adding-classes-to-generated-html)

<!-- /MarkdownTOC -->

---

## Default HTML5 output

## DITA-OT project website

## Bundling CSS & adding metadata

Adding CSS & `<meta>` elements to the `<head>` of each HTML page

```xml
<xsl:template match="*" mode="chapterHead">
  <head>
    <!-- initial meta information -->
    <xsl:call-template name="generateCharset"/>   <!-- Set the character set to UTF-8 -->
    <!-- Add <meta> elements from basic Bootstrap template -->
    <meta http-equiv="X-UA-Compatible" content="IE=edge"/>
    <meta name="viewport" content="width=device-width, initial-scale=1"/>
    <!-- Continue with DITA-OT defaults -->
    <!-- […] -->
    <!-- Bootstrap core CSS -->
    <link href="/css/bootstrap.min.css" rel="stylesheet"/>
    <xsl:call-template name="gen-user-styles" />  <!-- include user's XSL style element and content here -->
    <xsl:call-template name="processHDF"/>        <!-- Add user HDF file, if specified -->
  </head>
</xsl:template>
```
@[5-7](Add meta elements)
@[10-11](Add Bootstrap CSS)

## Adding classes to generated HTML


