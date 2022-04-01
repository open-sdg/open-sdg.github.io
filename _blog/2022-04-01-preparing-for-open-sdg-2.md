---
title: Preparing for Open SDG 2.0.0 
excerpt: How to prepare for the upcoming major release of Open SDG 2.0.0 by upgrading Bootstrap and Chart.js
date: 2022-04-01
---

We are excited to be approaching the release of Open SDG 2.0.0, and we want to make the upgrade process as seamless as possible. To that end, in 1.8.0 we added some options to help you prepare. In this post we'll cover how to use these options, and also what to expect in Open SDG 2.0.0.

## Previewing 2.0.0

The two biggest changes in Open SDG 2.0.0 will be in the versions of two dependencies: [Bootstrap](https://getbootstrap.com/) and [Chart.js](https://www.chartjs.org/). Open SDG has always depended on Bootstrap 3 and Chart.js 2, but in Open SDG 2.0.0 we will switch to the latest versions of these dependencies: Bootstrap 5 and Chart.js 3.

To get a preview of what your site will look and behave like with these upgraded dependencies, we have added options to enable one or both of these. Here are the steps to use these new options:

1. Make sure you have [upgraded to Open SDG 1.8.0](https://open-sdg.readthedocs.io/en/latest/upgrades/upgrading-1-8-0/) or later
2. Enable the two options in your site configuration. For example:
    a. If you are using the site configuration form, tick the boxes for "Bootstrap 5" and "Chart.js 3".
    b. If you are maintaining your site configuration manually, add these lines:

        bootstrap_5: true
        chartjs_3: true

## What to expect

After enabling these options, you may notice a few changes to your platform. The changes may be obvious, or subtle, or nearly imperceptible, depending on your existing site configuration. Here is a list of the changes, along with some screenshots:

1. The header on large screens (desktops, etc.) may change slightly. Here is what it will look like:

    ![Screenshot of the new desktop header](/assets/images/2022-04-01-preparing-for-open-sdg-2/header-desktop.png)

2. The header on small screens (phones, etc.) will change noticably, to a "hamburger-menu" approach. Here is what that will look like:

    ![Screenshot of the new desktop header](/assets/images/2022-04-01-preparing-for-open-sdg-2/header-mobile.png)

3. If you were not already using the "frontpage-alt" layout, then the frontpage will gain some additional sections. Here is what it will look like:

    ![Screenshot of the new frontpage](/assets/images/2022-04-01-preparing-for-open-sdg-2/frontpage.png)

4. Depending on which layout you were using for goals, you may notice some changes to the goal pages. Here is what they will look like:

    ![Screenshot of the new goal page](/assets/images/2022-04-01-preparing-for-open-sdg-2/goal-page.png)

## Overriden files

**If you are not overriding any Open SDG files (in other words, if you have not added any files in the `_includes` or `_layouts` folders) then you need not read further.** We recommend that you leave these options enabled on your platform, so that when Open SDG 2.0.0 is released, it will be a seamless upgrade.

If you *are* overriding some Open SDG files, then read on for details on what to look out for. As with any release, if the files you are overriding have changed, then you may need to incorporate those changes into your versions, if you would like to be able to preview the Bootstrap 5 and Chart.js 3 support.

### Overridden files for Bootstrap 5 support

Upgrading to Bootstrap 5 required many changes to files in Open SDG. Here is a list of files that have been changed in-place to support Bootstrap 5:

1. _includes/assets/js/tabs.js
2. _includes/scripts.html
3. _layouts/goals.html
4. _layouts/post.html
5. assets/js/sdg.js

Note that there are many more, as well, that are in an alternate location. More on that in the next section.

### Alternate files for Bootstrap 5 support

A unique twist in the 1.8.0 release is that many files had to be changed so much that an alternate version was created and placed in a "boostrap5" subfolder. When the `bootstrap_5` setting is enabled, these files are replaced by an alternate version. If you are overriding any of these files and want to enable Bootstrap 5, you will need to do 2 things for each file:

1. Adjust your override according to the alternate Bootstrap 5 version
2. Move your override into the "bootstrap5" subfolder

Here is the list of files that have alternate version for Bootstrap 5 in Open SDG 1.8.0:

Original version | Alternate Bootstrap 5 version
--- | ---
_includes/assets/js/accessibility.js | _includes/assets/js/**bootstrap5**/accessibility.js
_includes/assets/js/accessibleTabs.js | _includes/assets/js/**bootstrap5**/accessibleTabs.js
_includes/components/card.html | _includes/**bootstrap5**/components/card.html
_includes/components/contrast-toggle.html | _includes/**bootstrap5**/components/contrast-toggle.html
_includes/components/goal/breadcrumbs.html | _includes/**bootstrap5**/components/goal/breadcrumbs.html
_includes/components/goal/header.html | _includes/**bootstrap5**/components/goal/header.html
_includes/components/indicator/breadcrumbs.html | _includes/**bootstrap5**/components/indicator/breadcrumbs.html
_includes/components/indicator/data-main.html | _includes/**bootstrap5**/components/indicator/data-main.html
_includes/components/indicator/data-panes.html | _includes/**bootstrap5**/components/indicator/data-panes.html
_includes/components/indicator/data-tabs.html | _includes/**bootstrap5**/components/indicator/data-tabs.html
_includes/components/indicator/header.html | _includes/**bootstrap5**/components/indicator/header.html
_includes/components/indicator/indicator-main.html | _includes/**bootstrap5**/components/indicator/indicator-main.html
_includes/components/indicator/indicator-progress.html | _includes/**bootstrap5**/components/indicator/indicator-progress.html
_includes/components/indicator/metadata-panes-default.html | _includes/**bootstrap5**/components/indicator/metadata-panes-default.html
_includes/components/indicator/metadata-panes.html | _includes/**bootstrap5**/components/indicator/metadata-panes.html
_includes/components/indicator/metadata-section.html | _includes/**bootstrap5**/components/indicator/metadata-section.html
_includes/components/indicator/metadata-tabs-default.html | _includes/**bootstrap5**/components/indicator/metadata-tabs-default.html
_includes/components/indicator/metadata-tabs.html | _includes/**bootstrap5**/components/indicator/metadata-tabs.html
_includes/components/indicator/tags.html | _includes/**bootstrap5**/components/indicator/tags.html
_includes/components/language-toggle-dropdown.html | _includes/**bootstrap5**/components/language-toggle-dropdown.html
_includes/components/language-toggle-links.html | _includes/**bootstrap5**/components/language-toggle-links.html
_includes/components/language-toggle.html | _includes/**bootstrap5**/components/language-toggle.html
_includes/components/previous-next-links.html | _includes/**bootstrap5**/components/previous-next-links.html
_includes/components/post/breadcrumbs.html | _includes/**bootstrap5**/components/post/breadcrumbs.html
_includes/footer.html | _includes/**bootstrap5**/footer.html
_includes/header.html | _includes/**bootstrap5**/header.html
_includes/navigation-link.html | _includes/**bootstrap5**/navigation-link.html
_includes/navigation.html | _includes/**bootstrap5**/navigation.html
_includes/search.html | _includes/**bootstrap5**/search.html

### Overridden files for Chart.js 3 support

Upgrading to Chart.js 3 required several changes as well. Here is a list of files that have been changed to support Chart.js 3:

1. _includes/assets/js/chartjs/accessibleCharts.js
2. _includes/assets/js/chartjs/noDataMessage.js
3. _includes/assets/js/chartjs/rescaler.js
4. _includes/components/charts/annotation_presets.js
5. _includes/components/charts/chart.html
6. _includes/components/charts/line.html
7. _includes/scripts.html
8. assets/js/sdg.js

Note that there are 2 more, as well, that have been renamed. More on that in the next section.

### Alternate files for Chart.js 3 support

Similarly, in the 1.8.0 release 2 files had to be changed so much that an alternate version was renamed to add "-chartjs3". When the `chartjs_3` is enabled, the following files are replaced by an alternate version. If you are overriding any of these files and want to enable Chart.js 3, you will need to do 2 things for each file:

1. Adjust your override according to the alternate Chart.js 3 version
2. Rename your override to add "-chartjs3"

Here is the list of files that have alternate version for Chart.js 3 in Open SDG 1.8.0:

Original version | Alternate Chart.js 3 version
--- | ---
_includes/assets/js/chartjs/accessibleCharts.js | _includes/assets/js/chartjs/accessibleCharts<strong>-chartjs3</strong>.js
_includes/assets/js/indicatorView.js | _includes/assets/js/indicatorView<strong>-chartjs3</strong>.js

## Bootstrap 5 layouts

When Bootstrap 5 is enabled, the "layout" used for 2 pages will change. If you have customised either of these pages' layouts, you will need to do 2 things in each case:

1. Adjust your override according to the Bootstrap 5 version
2. Move your override to the location of the Bootstrap 5 version

The pages and Bootstrap 5 layouts are listed below:

Page | Bootstrap 5 layout
--- | ---
Goal page | _layouts/goal-bootstrap5.html
Reporting Status page | _layouts/reportingstatus-bootstrap5.html
Indicator page | _layouts/indicator-bootstrap5.html

> Note about the goal page: Historically Open SDG has supported a few different goal pages. Going into Open SDG 2.0.0 there will be a single version of the goal page supported in the platform. But we will be posting tutorials and examples of how to customise the goal page to achieve the other versions.

## Custom chart types in Chart.js 3

If you have implemented any custom types, or you have overridden the behavior of the "line", "bar", or "binary" chart types, then here is a quick description of the new architecture for chart types.

Historically each chart type has been defined in the [_includes/components/charts folder](https://github.com/open-sdg/open-sdg/tree/1.8.0-dev/_includes/components/charts) using the `opensdg.chartConfigAlter` function.

By contrast, with Chart.js 3, the chart types are defined in the [_includes/assets/js/view folder](https://github.com/open-sdg/open-sdg/tree/2.0.0-dev/_includes/assets/js/view) by adding a function to the `opensdg.chartTypes` object.

So, to define your custom chart type, in your custom javascript you would add an object to `opensdg.chartTypes` in the same way. For example, [here is how the "bar" type is defined](https://github.com/open-sdg/open-sdg/blob/2.0.0-dev/_includes/assets/js/view/chartTypeBar.js).

To override the behavior of one of the core chart types ("line", "bar", and "binary") you can override that particular file (such as the chartTypeBar.js file linked above) in the usual way.

## Summary

In summary, in Open SDG 2.0.0 we will be upgrading to Bootstrap 5 and Chart.js 3. As of Open SDG 1.8.0, there are optional settings that can be used to preview your site with these upgraded versions. We recommend that you take advantage of these settings, to ensure that your upgrade to Open SDG 2.0.0 will be as seamless as possible. If you are not overriding any files, the process is quite easy. If you are overriding files, you might need to make some adjustments to your versions, as described above.

As always, if you have any questions or concerns about this upgrade path or any of the specifics discussed here, please do not hesitate to bring them up in [our discussion board](https://github.com/open-sdg/open-sdg/discussions).
