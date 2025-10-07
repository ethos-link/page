---
layout: default
title: About EthosLink
permalink: /about/
structured_data: structured-data/about.html
---

{% include header.html %}

<main>
  <!-- About section -->
  <div class="mx-auto mt-32 max-w-7xl px-6 sm:mt-56 lg:px-8" id="about">
    <div class="mx-auto max-w-2xl lg:mx-0">
      <h2 class="text-base/7 font-semibold text-indigo-600">{{ site.data.landing.about.title }}</h2>
      <p class="mt-2 text-4xl font-semibold tracking-tight text-pretty text-gray-900 sm:text-5xl lg:text-balance">{{ site.data.landing.about.subtitle }}</p>
      <p class="mt-6 text-lg/8 text-gray-600">{{ site.data.landing.about.description }}</p>
    </div>
    <div class="mx-auto mt-16 grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 lg:mx-0 lg:mt-10 lg:max-w-none lg:grid-cols-12">
      <div class="relative lg:order-last lg:col-span-5">
        <svg class="absolute -top-[40rem] left-1 -z-10 h-[50rem] w-[50rem] -translate-x-1/2 stroke-gray-300/70 [mask-image:radial-gradient(64rem_64rem_at_top,white,transparent)]" aria-hidden="true">
          <defs>
            <pattern id="e87443c8-56e4-4c20-9111-55b82fa704e3" width="200" height="200" patternUnits="userSpaceOnUse">
              <path d="M0.5 0V200M200 0.5L0 0.499983" />
            </pattern>
          </defs>
          <rect width="100%" height="100%" stroke-width="0" fill="url(#e87443c8-56e4-4c20-9111-55b82fa704e3)" />
        </svg>
        <figure class="border-l border-indigo-600 pl-8">
          <blockquote class="text-xl/8 font-semibold tracking-tight text-gray-900">
            <p>"{{ site.data.landing.about.quote }}"</p>
          </blockquote>
          <figcaption class="mt-8 flex gap-x-4">
            <img src="{{ '/assets/founder-avatar.webp' | relative_url }}" alt="{{ site.data.landing.about.founder.name }}" class="mt-1 size-10 flex-none rounded-full bg-gray-50">
            <div class="text-sm/6">
              <div class="font-semibold text-gray-900">{{ site.data.landing.about.founder.name }}</div>
              <div class="text-gray-600">{{ site.data.landing.about.founder.role }}</div>
            </div>
          </figcaption>
        </figure>
      </div>
      <div class="max-w-xl text-base/7 text-gray-700 lg:col-span-7">
        <p>{{ site.data.landing.about.story }}</p>
        <ul role="list" class="mt-8 max-w-xl space-y-8 text-gray-600">
          {% for value in site.data.landing.about.values %}
          <li class="flex gap-x-3">
            <svg class="mt-1 h-5 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
              <path fill-rule="evenodd" d="M10 18a8 8 0 1 0 0-16 8 8 0 0 0 0 16Zm3.857-9.809a.75.75 0 0 0-1.214-.882l-3.236 4.53L8.93 10.7a.75.75 0 1 0-1.06 1.061l1.884 1.884a.75.75 0 0 0 1.137-.089l4-5.5Z" clip-rule="evenodd" />
            </svg>
            <span><strong class="font-semibold text-gray-900">{{ value.title }}</strong> {{ value.description }}</span>
          </li>
          {% endfor %}
        </ul>
      </div>
    </div>
  </div>
</main>

{% include footer.html %}
