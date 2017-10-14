# DITA-OT Docs Developments

#### Roger W. Fienhold Sheen

---  

<i class="fa fa-sitemap fa-5x pull-right muted"></i>

# Agenda

<!-- TOC max1 -->

<!-- 
This talk provides an overview of DITA-OT documentation usage metrics and highlights recent changes to the docs and ideas for future improvements. We’ll close with room for suggestions from the community and a call for contributions with information on the browser-based workflow for suggesting changes.
-->

---  

## What's New? — dita-ot.org!

<figure><img src="images/dita-ot-website-2-4.png" border="1" /></figure>

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

---  

## Docs Changes in 2.3

<i class="fa fa-book fa-5x pull-right muted"></i>

* New _User Guide_ topics on publishing via the `dita` command:
    + [Using a properties file][3]
    + [Migrating Ant builds][4]
* New _Developer Reference_ sections on customization:
    + [Customizing PDF output][5]
        - [History of the PDF transformation][6]
        - [PDF customization approaches][7]
        - [Types of custom PDF plug-ins][8]
        - [PDF plug-in structure][9]
        - [Best practices for custom PDF plug-ins][10]
        - [Resources for custom PDF plug-ins][11]
    + [Migrating customizations][12]

---  

<i class="fa fa-book fa-5x pull-right muted"></i>

## What's More in 2.4

* New [Extension points by plug-in][13] generated from installed plug-ins
* New [DITA features in the documentation][14] topic
* A new topic on [Migrating to release 2.4][15]

<figure><img src="images/dita-ot-generated-extension-points.png" border="1" /></figure>

---  

<i class="fa fa-check fa-5x pull-right muted"></i>

## Progress Report — Last Year's Ideas

___  

### Additional Content

* ~~Migration topics — Migrating customizations to 2.0, 2.1, 2.2~~
* ~~Setting DITA-OT parameters with `.properties` files~~

___  

### Enhancements

* ~~Generate documentation for all supported extension points~~
* ~~Apply DITA 1.3 XML mention domain tags~~
* ~~Automated dev docs builds~~

---  

<i class="fa fa-lightbulb fa-5x pull-right muted"></i>

## Still To Do — What's Next?

* Update sample build scripts — Add examples on building docs
* Modularize CSS & extend coverage
* Flag new content based on version?
* Dedicated _Tutorials_ section?
* Enhanced HTML5 output?
* Revise top-level structure
    * _Installing_
    * _Building/Publishing_
    * _Customizing/Extending/Plugins_
    * _Troubleshooting_
* Automated testing

---  

<i class="fa fa-comments fa-5x pull-right muted"></i>

## Suggestions

Visit <http://www.dita-ot.org/dev/> for the latest docs.

We welcome contributions to the DITA-OT documentation.  
If you'd like to help, review the [Contribution Guidelines][16].

___  

### Create an Issue

If you find a bug — _and you don’t know how to fix it_, [create an issue][17] to request changes.

Before you do that, [review the open issues][18] to make sure it hasn't already been reported.

_or — even better…_

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

[2]: https://github.com/dita-ot/docs/ 
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
[16]: https://github.com/dita-ot/docs/blob/develop/CONTRIBUTING.md
[17]: https://github.com/dita-ot/docs/issues/new
[18]: https://github.com/dita-ot/docs/issues
[19]: https://help.github.com/articles/fork-a-repo/
[20]: https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/
[21]: https://help.github.com/articles/using-pull-requests/
