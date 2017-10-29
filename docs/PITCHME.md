# DITA-OT<br/>Docs

## Developments

#### Roger Sheen [@infotexture](https://twitter.com/infotexture)

---

<i class="fa fa-sitemap fa-5x pull-right muted"></i>

# Agenda

<!-- 
This talk provides an overview of DITA-OT documentation usage metrics and highlights recent changes to the docs and ideas for future improvements. We’ll close with room for suggestions from the community and a call for contributions with information on the browser-based workflow for suggesting changes.
-->

<!-- MarkdownTOC autolink="true" bracket="round" depth="1" -->

- [Doing the Numbers](#doing-the-numbers)
- [What's New?](#whats-new)
- [Suggestions](#suggestions)
- [How to Help](#how-to-help)

<!-- /MarkdownTOC -->

---

## Doing the Numbers

___

### Recent usage metrics

Active users since DITA-OT Day last year:

* ~ 3000 Monthly <!-- .element: class="fragment" -->
* ~ 846 Weekly   <!-- .element: class="fragment" -->
* ~ 54 Daily     <!-- .element: class="fragment" -->

___

### Content version demand

1. **1.8** ~ 19%    <!-- .element: class="fragment" -->
2. **dev** ~ 12%    <!-- .element: class="fragment" -->
3. **2.0** ~ 11%    <!-- .element: class="fragment" -->
4. **2.4** ~ 6%     <!-- .element: class="fragment" -->
5. **2.2** ~ 6%     <!-- .element: class="fragment" -->
6. **2.5** ~ 4%     <!-- .element: class="fragment" -->
7. **2.3** ~ 3%     <!-- .element: class="fragment" -->
8. **2.1** ~ 2%     <!-- .element: class="fragment" -->

___

### Platform distribution

#### By device

1. 88% on desktop  <!-- .element: class="fragment" -->
2. 10% on mobile   <!-- .element: class="fragment" -->
3. 2% on tablets   <!-- .element: class="fragment" -->

#### Operating systems

1. 71% on Windows  <!-- .element: class="fragment" -->
2. 12% on macOS    <!-- .element: class="fragment" -->
3. 7% on iOS       <!-- .element: class="fragment" -->
4. 5% on Linux     <!-- .element: class="fragment" -->
5. 3% on Android   <!-- .element: class="fragment" -->

---

## What's New?

___

### Recent Enhancements

<!-- Create Vizzlo fishbone timeline of OT releases -->
<!-- https://vizzlo.com/create/fishbone-timeline-chart -->

* Travis CI publishes the latest docs to [dita-ot.org/dev][1] whenever changes are pushed to the `develop` branch of the [dita-ot/docs][2] repository on GitHub.
* **Edit this page** — open DITA source in oXygen XML Web Author
* Keyboard shortcuts:
    * Topic finder — press <kbd>t</kbd> to filter topics by title
    * Search — press <kbd>s</kbd> to focus the search field
    * Help – press <kbd>?</kbd> to show shortcuts

[1]: http://www.dita-ot.org/dev/
[2]: https://github.com/dita-ot/docs/ 

___

<i class="fa fa-book fa-5x pull-right muted"></i>

### Docs Changes in 2.5

New _Developer Reference_ topics:

* [New Java API](http://www.dita-ot.org/dev/dev_ref/java-api.html)
* [Experimental map-first preprocessing](http://www.dita-ot.org/dev/dev_ref/map-first-preprocessing.html)
* [Migrating to release 2.5](http://www.dita-ot.org/dev/dev_ref/migrating-to-2.5.html)

___

<i class="fa fa-book fa-5x pull-right muted"></i>

### Three? Oh!

* New top-level structure             <!-- .element: class="fragment" -->
    - _Installing, Building, Customizing_  <!-- .element: class="fragment" -->
* New topics on Markdown plug-in      <!-- .element: class="fragment" -->
    - Using Markdown topics as input  <!-- .element: class="fragment" -->
    - Generating Markdown output      <!-- .element: class="fragment" -->
* New topic on Lightweight DITA       <!-- .element: class="fragment" -->
* New topic on normalized DITA output <!-- .element: class="fragment" -->

---

<i class="fa fa-comments fa-5x pull-right muted"></i>

## Suggestions

We welcome contributions to the DITA-OT documentation.  

1. Visit <http://www.dita-ot.org/dev/> for the latest docs.
2. If you'd like to help, review the [Contribution Guidelines][16].

[16]: https://github.com/dita-ot/docs/blob/develop/CONTRIBUTING.md

___

<i class="fa fa-flag fa-5x pull-right muted"></i>

## How to Help

### Create an Issue

If you find a bug — _and you don’t know how to fix it_:

1. [Review the open issues][18] to make sure it hasn't already been reported.
2. [Create an issue][17] to request changes.

_or — even better…_

[18]: https://github.com/dita-ot/docs/issues
[17]: https://github.com/dita-ot/docs/issues/new

---

<i class="fa fa-code fa-5x pull-right muted"></i>

### Create a Pull Request

If you know how to fix the issue yourself, here's what to do:

1. [Fork the repository][19],
2. [Create a new branch][20],
3. Make your changes on the new branch, and
4. [Send a pull request][21].

[19]: https://help.github.com/articles/fork-a-repo/
[20]: https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/
[21]: https://help.github.com/articles/using-pull-requests/

___

### Or…

![](assets/edit-this-page-button.png)

[3]: http://www.dita-ot.org/dev/user-guide/build-using-dita-properties-file.html
[4]: http://www.dita-ot.org/dev/user-guide/build-migrating-ant-to-dita.html
[5]: http://www.dita-ot.org/dev/dev_ref/pdf-customization.html
[6]: http://www.dita-ot.org/dev/dev_ref/pdf-transformation-history.html
[7]: http://www.dita-ot.org/dev/dev_ref/pdf-customization-approaches.html
[8]: http://www.dita-ot.org/dev/dev_ref/pdf-customization-plugin-types.html
[9]: http://www.dita-ot.org/dev/dev_ref/pdf-plugin-structure.html
[10]: http://www.dita-ot.org/dev/dev_ref/pdf-customization-best-practices.html
[11]: http://www.dita-ot.org/dev/dev_ref/pdf-customization-resources.html
[12]: http://www.dita-ot.org/dev/dev_ref/migration.html
[13]: http://www.dita-ot.org/dev/extension-points/extension-points-by-plugin.html
[14]: http://www.dita-ot.org/dev/user-guide/DITA-features-in-docs.html
[15]: dev_ref/migrating-to-2.4.html
