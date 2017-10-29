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
- [Adding CSS & metadata](#adding-css--metadata)
- [Adding menu & classes to page body](#adding-menu--classes-to-page-body)
- [Styling navigation](#styling-navigation)

<!-- /MarkdownTOC -->

---

## Default HTML5 output


---

## DITA-OT project website


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

## Adding menu & classes to page body

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

