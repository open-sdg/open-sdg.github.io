---
title: How to implement the 2-column "goal-by-target" layout for your goal pages
excerpt: Open SDG has a 1-column layout for goal pages, but here is how you can override it to achieve a 2-column layout
author_profile: false
render_with_liquid: false
---
In versions of Open SDG prior to 2.0.0 there were multiple "layouts" for goal pages. Starting with 2.0.0, Open SDG will focus on a single layout for goal pages, allowing us to ensure that the entire platform lives up to our high standards for accessibility and usability. 

One of the goal layouts that is no longer available in 2.0.0 is the "goal-by-target" layout, which displayed the SDG targets in the left column, and the SDG indicators in the right column. Since this was a popular layout, this blog post is intended to show how you can override the latest goal layout to achieve this.

The file that controls the markup of the goal layout is [/_layouts/goal.html](https://github.com/open-sdg/open-sdg/blob/2.0.0-dev/_layouts/goal.html). As with any file in this folder, you can "override" it by placing your own version at the same location, and with the same filename, in your site repository. In other words, you would put a file called `goal.html` in your site repository's `_layouts` folder. 

As for the contents of this file, that is completely up to you. Here is a version that achieves the 2-column layout, which you can copy into your override:

```
{% raw %}
{% include head.html %}
{% include header.html %}

<div class="container">
  {% include components/goal/breadcrumbs.html %}
  {% if site.create_goals.previous_next_links %}
    {% include components/previous-next-links.html previous_label=page.t.goal.previous next_label=page.t.goal.next %}
  {% endif %}
</div>

{% include components/goal/header.html %}

<div id="main-content" class="container" role="main">

  {% include components/goal/goal-content.html content=content %}

  <div class="container g-0">
    <div class="row">
      <div class="col-md-6">
        <h2>{{ page.t.general.targets }}</h2>
      </div>
      <div class="col-md-6">
        <h2>{{ page.t.general.indicators }}</h2>
      </div>
    </div>

    {% assign goal_indicators = page.indicators | where: 'goal_number', page.goal.number | group_by: 'target_number' %}
    {% for group in goal_indicators %}
      {% assign target = group.name | sdg_lookup %}
      <div class="row">
        <div class="col-md-6">
            <h3>
              <span class="visually-hidden">{{ page.t.general.target }}</span> {{ target.number }}
            </h3>
            <div>{{ target.name }}</div>
        </div>
        <div class="col-md-6">
          {% for indicator in group.items %}

            {% assign tag_classes = "" | split: "," %}
            {% if indicator.tags %}
              {% for tag in indicator.tags %}
                {% assign tag_slug = "indicator-" | append: tag | slugify %}
                {% assign tag_classes = tag_classes | push: tag_slug %}
              {% endfor %}
            {% endif %}
            {% assign tag_classes = tag_classes | join: " " %}
            {% if indicator.progress_status and indicator.progress_status != '' %}
              {% assign indicator_has_progress = true %}
            {% endif %}

            <div class="row">
              <h4>
                <span class="visually-hidden">{{ page.t.general.indicator }}</span> {{ indicator.number }}
              </h4>
              <div class="col">
                {% if indicator.placeholder and indicator.placeholder != '' %}
                  {{ indicator.placeholder }}
                {% else %}
                  <a href="{{ indicator.url }}">{{ indicator.name }}</a>
                  {% include components/indicator/tags.html tags=indicator.tags reporting_status=true indicator=indicator %}
                {% endif %}
                {% if indicator_has_progress %}
                  <div class="col-lg-1 goal-page-indicator-progress">
                    <span class="visually-hidden">{{ site.progress_status.status_heading | t }}</span>
                    {% include components/progress/progress-status.html indicator=indicator %}
                  </div>
                {% endif %}
              </div>
            </div>
          {% endfor %}
        </div>
      </div>
    {% endfor %}
  </div>
  {% include back-to-top.html %}
</div>


{% include footer.html %}
{% endraw %}
```

By itself, though, this will be lacking. It also needs some style changes in order to work. You can copy the following into your `_sass/custom.scss` file:

```
.layout-goal {
    .container {
        h3, h4 {
            margin: 0;
            font-size: $fontSize;
            &:after {
                content: "";
                display: block;
                border-bottom: 1px solid $color-dark;
                margin-top: 5px;
                margin-bottom: 5px;
            }
        }
        .row {
            margin-bottom: 20px;
        }
        .goal-page-indicator-progress {
            margin-left: 0px;
        }
    }
}
```

With these two bits of code you should be able to achieve the 2-column goal layout. Please note that, by overriding a file, you are taking on some development responsibility to maintain the code and to tweak it (as needed) during version upgrades.

Please let us know how this goes in our [Github discussions section](https://github.com/open-sdg/open-sdg/discussions)!
