---
layout: default
title: Blog
pagination:
  enabled: true
---

<div class="space-y-12">
{% for post in paginator.posts %}
    <article>
        <div class="mb-4">
            <span class="text-sm text-slate-500">{{ post.date | date: "%Y년 %-m월 %-d일" }}</span>
        </div>
        <h3 class="font-display text-2xl font-bold text-slate-900 mb-4">
            <a href="{{ post.url | relative_url }}" class="hover:text-blue-700 transition-colors">
                {{ post.title }}
            </a>
        </h3>
        <div class="text-md text-slate-700 leading-relaxed space-y-3">
            <a href="{{ post.url | relative_url }}">{{ post.excerpt }}</a>
        </div>
    </article>
{% endfor %}
</div>

<!-- Pagination Links -->
{% if paginator.total_pages > 1 %}
<div class="mt-16 pt-8 flex items-center justify-center space-x-4 text-lg">

    <!-- Previous -->
    {% if paginator.previous_page %}
        <a href="{{ paginator.previous_page_path | relative_url }}" class="text-slate-700 hover:underline">&larr;</a>
    {% endif %}

    <!-- Numbered pages -->
    {% for trail in paginator.page_trail %}
        {% if trail.num == paginator.page %}
            <span class="font-bold text-slate-900">{{ trail.num }}</span>
        {% else %}
            <a href="{{ trail.path | relative_url }}" class="text-slate-700 hover:underline">{{ trail.num }}</a>
        {% endif %}
    {% endfor %}

    <!-- Next -->
    {% if paginator.next_page %}
        <a href="{{ paginator.next_page_path | relative_url }}" class="text-slate-700 hover:underline">&rarr;</a>
    {% endif %}

</div>
{% endif %}