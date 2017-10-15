# DITA-OT<br/>Docs 

## Developments

#### Roger W. Fienhold Sheen

---  

<i class="fa fa-sitemap fa-5x pull-right muted"></i>

# Agenda

<!-- 
This talk provides an overview of DITA-OT documentation usage metrics and highlights recent changes to the docs and ideas for future improvements. We’ll close with room for suggestions from the community and a call for contributions with information on the browser-based workflow for suggesting changes.
-->

<!-- MarkdownTOC autolink="true" bracket="round" depth="1" -->

- [What's New?](#whats-new)
- [Suggestions](#suggestions)
- [How to Help](#how-to-help)

<!-- /MarkdownTOC -->

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

<figure><img src="images/dita-ot-website-keyboard-shortcuts.png" border="1" /></figure>

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

* New topics on Markdown plug-in      <!-- .element: class="fragment" -->
    - Using Markdown topics as input  <!-- .element: class="fragment" -->
    - Generating Markdown output      <!-- .element: class="fragment" -->
    - Publishing via GitBook          <!-- .element: class="fragment" -->
* New topic on generating normalized DITA output <!-- .element: class="fragment" -->
* New top-level structure             <!-- .element: class="fragment" -->
    * _Installing_                    <!-- .element: class="fragment" -->
    * _Building/Publishing_           <!-- .element: class="fragment" -->
    * _Customizing/Extending/Plugins_ <!-- .element: class="fragment" -->
    * _Troubleshooting_               <!-- .element: class="fragment" -->

---  

<i class="fa fa-check fa-5x pull-right muted"></i>


---  

<i class="fa fa-comments fa-5x pull-right muted"></i>

## Suggestions

We welcome contributions to the DITA-OT documentation.  

1. Visit <http://www.dita-ot.org/dev/> for the latest docs.
2. If you'd like to help, review the [Contribution Guidelines][16].

[16]: https://github.com/dita-ot/docs/blob/develop/CONTRIBUTING.md
___  

### Create an Issue

If you find a bug — _and you don’t know how to fix it_:

1. [Review the open issues][18] to make sure it hasn't already been reported.
2. [Create an issue][17] to request changes.

_or — even better…_

[18]: https://github.com/dita-ot/docs/issues
[17]: https://github.com/dita-ot/docs/issues/new

---  

<i class="fa fa-code fa-5x pull-right muted"></i>

## How to Help

### Create a Pull Request

If you know how to fix the issue yourself, that's great!  

Here's what to do:

1. [Fork the repository][19],
2. [Create a new branch][20], 
3. Make your changes on the new branch, and 
4. [Send a pull request][21].

> Or — if that all sounds too complicated — just click the **Edit this page** link.

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
[19]: https://help.github.com/articles/fork-a-repo/
[20]: https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/
[21]: https://help.github.com/articles/using-pull-requests/