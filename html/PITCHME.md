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

- [DITA-OT website](#dita-ot-website)
- [DITA-OT site plug-in](#dita-ot-site-plug-in)
- [Adding CSS & metadata](#adding-css--metadata)
- [Adding menu & classes](#adding-menu--classes)
- [Styling navigation](#styling-navigation)

<!-- /MarkdownTOC -->

---

## DITA-OT website

* Published via [GitHub pages][1] to [dita-ot.org][3]. 

* The website is maintained in DITA, [Markdown][6] and HTML, versioned in Git and updated by pushing commits to [github.com/dita-ot/dita-ot.github.io][4].

* GitHub pages is powered by [Jekyll][5], an open source tool like DITA-OT that   transforms files in one format with variables and templates, and generates output.

[1]:  https://pages.github.com
[2]:  http://dita-ot.github.io
[3]:  http://www.dita-ot.org
[4]:  https://github.com/dita-ot/dita-ot.github.io
[5]:  http://jekyllrb.com "Jekyll • Simple, blog-aware, static sites"
[6]:  http://daringfireball.net/projects/markdown/

---

## DITA-OT site plug-in

The DITA-OT site plug-in is available on GitHub:

<https://github.com/dita-ot/org.dita-ot.html>

### Why not just use this? <!-- .element: class="fragment" -->

* Contains code specific to the DITA-OT project <!-- .element: class="fragment" -->
* It requires Jekyll <!-- .element: class="fragment" -->
* Based on older HTML5 code <!-- .element: class="fragment" -->

---

## Adding CSS & metadata

Customizing the `chapterHead` template mode:

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
    <!-- Continue with DITA-OT defaults -->
  </head>
</xsl:template>
```
@[5-7](Add meta elements)
@[10-11](Add Bootstrap CSS)

---

## Adding menu & classes

Customizing the `chapterBody` template mode:

```xml
  <xsl:template match="*" mode="chapterBody">
    <body>
      <!-- Here there be defaults… -->
      <div class="navbar navbar-default navbar-static-top" role="navigation">
        <div class="container">
          <div class="navbar-header">
            <!-- Your menu here… -->
          </div>
        </div>
      </div>
      <main id="content" class="col-md-9 container" role="main">
        <xsl:apply-templates select="." mode="addContentToHtmlBodyElement"/>
      </main>
      <xsl:apply-templates select="." mode="addFooterToHtmlBodyElement"/>
    </body>
  </xsl:template>
```
@[4-5](Add class attributes & additional containers)
@[6-8](Add menu to header)

---

## Styling navigation

Customizing the `gen-user-sidetoc` template mode:

```xml
  <xsl:template match="*" mode="gen-user-sidetoc">
    <xsl:if test="$nav-toc = ('partial', 'full')">
      <nav class="col-md-3" role="toc">
        <div class="well well-sm">
          <ul class="bs-docs-sidenav">
            <xsl:choose>
              <!-- Here there be defaults… -->
            </xsl:choose>
          </ul>
        </div>
      </nav>
    </xsl:if>
  </xsl:template>
```
@[3-5](Add nav classes)
@[6-8](Selection logic for full/partial ToC unchanged)

