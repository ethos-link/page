---
layout: default
title: Privacy Policy
permalink: /privacy/
noindex: true
---

{% include header.html %}

<main class="mx-auto max-w-4xl px-6 py-16 sm:py-24 lg:px-8">
  <div class="mx-auto max-w-3xl">
    <h1 class="text-4xl font-bold tracking-tight text-gray-900 sm:text-5xl mb-4">Privacy Policy</h1>
    <p class="text-sm text-gray-600 mb-8">Effective date: {{ site.data.privacy.date }}</p>

    {% for clause in site.data.privacy.clauses %}
    <section class="mb-8">
      <h2 class="text-2xl font-semibold text-gray-900 mb-4">{{ clause.title }}</h2>
      <div class="prose prose-gray max-w-none text-gray-700 leading-relaxed">
        {{ clause.content | markdownify }}
      </div>
    </section>
    {% endfor %}
  </div>
</main>

{% include footer.html %}
