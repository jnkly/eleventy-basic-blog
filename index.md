---
layout: base.njk
---

# Hello, world!

This is an [11ty](https://www.11ty.dev/) starter. It includes a basic blog, a few pages.

## Blog posts

{% if postListItems.length %}
  <section>
    <div>
      <h2{{ postListHeading }}</h2>
      <ol>
        {% for item in postListItems %}
          {% if item.date.getTime() <= global.now %}
            <li class="post-list__item">
              <h3>
                <a href="{{ item.url }}" rel="bookmark">{{ item.data.title }}</a>
              </h3>
              <p>
                <time datetime="{{ item.date | w3DateFilter }}">{{ item.date | dateFilter }}</time>
              </p>
            </li>
          {% endif %}
        {% endfor %}
      </ol>
    </div>
  </section>
{% endif %}
