---
title: Profession
---

<div>
  {% for profession_0 in site.data.profession %}
    {% if profession_0.children %}
      {% for profession_1 in profession_0.children %}
        <nav aria-label="breadcrumb">
          <ol class="breadcrumb">
            <li class="breadcrumb-item mt-0"><a href="#">{{profession_0.title}}</a></li>
            <li class="breadcrumb-item mt-0 active" aria-current="page">{{profession_1.title}}</li>
          </ol>
        </nav>
        {% if profession_0.children %}
          <div class="row row-cols-4">
            {% for profession_2 in profession_1.children %}
              {% if profession_2.title !="" %}
                <div class="col">
                  <a class="card mb-3 text-decoration-none" href="#">
                    <div class="card-body">
                      <h3 class="card-title mt-0">{{profession_2.title}}</h3>
                    </div>
                  </a>
                </div>
              {% endif %}
            {% endfor %}
          </div>
        {% endif %}
      {% endfor %}
    {% endif %}
  {% endfor %}
</div>