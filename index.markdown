---
layout: default
title: Home
structured_data: structured-data/home.html
---

{% include header.html %}

<main>
  <!-- Hero section -->
  <div class="relative isolate pt-14">
    <div class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80" aria-hidden="true">
      <div class="hero-gradient-shape relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#4F46E5] to-[#312E81] opacity-30 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]"></div>
    </div>
    <div class="mx-auto max-w-7xl px-6 py-24 sm:py-32 lg:flex lg:items-center lg:gap-x-10 lg:px-8 lg:py-40">
      <div class="mx-auto max-w-2xl lg:mx-0 lg:flex-auto">
        {% if site.data.landing.hero.announcement.text %}
        <div class="flex">
          <p class="relative rounded-full px-4 py-1 text-sm leading-6 text-gray-500 ring-1 ring-gray-900/10 hover:ring-gray-900/20">
            {{ site.data.landing.hero.announcement.text }}
            <a href="{{ site.data.landing.hero.announcement.link | relative_url }}" class="whitespace-nowrap font-semibold text-indigo-600">
              <span class="absolute inset-0" aria-hidden="true"></span> {{ site.data.landing.hero.announcement.link_text }} <span aria-hidden="true">&rarr;</span>
            </a>
          </p>
        </div>
        {% endif %}
        <h1 class="mt-10 text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl">{{ site.data.landing.hero.title }}</h1>
        <p class="mt-6 text-lg leading-8 text-gray-600">{{ site.data.landing.hero.description }}</p>
        <div class="mt-10 flex items-center gap-x-6">
          <a href="{{ site.data.landing.hero.cta_primary.link | relative_url }}" class="rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">{{ site.data.landing.hero.cta_primary.text }}</a>
          <a href="{{ site.data.landing.hero.cta_secondary.link | relative_url }}" class="text-sm font-semibold leading-6 text-gray-900">{{ site.data.landing.hero.cta_secondary.text }} <span aria-hidden="true">→</span></a>
        </div>
      </div>
      <div class="mt-16 sm:mt-24 lg:mt-0 lg:w-1/2 lg:flex-shrink-0">
        <img src="{{ '/assets/reviato-mobile-dashboard.webp' | relative_url }}" alt="Reviato Mobile Dashboard" class="block lg:hidden mx-auto w-full max-w-sm rounded-xl shadow-xl">
        <img src="{{ '/assets/business-overview.webp' | relative_url }}" alt="Business Overview" class="hidden lg:block w-full rounded-xl shadow-xl">
      </div>
    </div>
  </div>

  <!-- Logo cloud -->
  <div class="mx-auto max-w-7xl px-6 lg:px-8">
    <div class="mx-auto grid max-w-lg grid-cols-4 items-center gap-x-8 gap-y-12 sm:max-w-xl sm:grid-cols-6 sm:gap-x-10 sm:gap-y-14 lg:mx-0 lg:max-w-none lg:grid-cols-5">
      {% for logo in site.data.landing.logos %}
      <img class="col-span-2 max-h-12 w-full object-contain lg:col-span-1" src="{{ logo.url | relative_url }}" alt="{{ logo.name }}" width="158" height="48">
      {% endfor %}
    </div>
  </div>

  <!-- Feature section (Dark) -->
  <div class="mx-auto mt-32 max-w-7xl sm:mt-56 sm:px-6 lg:px-8">
    <div class="relative isolate overflow-hidden bg-gray-900 px-6 py-20 sm:rounded-3xl sm:px-10 sm:py-24 lg:py-24 xl:px-24">
      <div class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 sm:gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-2 lg:items-center lg:gap-y-0">
        <div class="lg:row-start-2 lg:max-w-md">
          <h2 class="text-3xl font-semibold tracking-tight text-balance text-white sm:text-4xl">{{ site.data.landing.dark_section.title }}</h2>
          <p class="mt-6 text-lg/8 text-gray-300">{{ site.data.landing.dark_section.description }}</p>
        </div>
        <img src="{{ '/assets/business-overview.webp' | relative_url }}" alt="EthosLink Dashboard Screenshot" class="relative -z-20 max-w-xl min-w-full rounded-xl shadow-xl ring-1 ring-white/10 lg:row-span-4 lg:w-5xl lg:max-w-none" width="800" height="500">
        <div class="max-w-xl lg:row-start-3 lg:mt-10 lg:max-w-md lg:border-t lg:border-white/10 lg:pt-10">
          <dl class="max-w-xl space-y-8 text-base/7 text-gray-300 lg:max-w-none">
            {% for feature in site.data.landing.dark_section.features %}
            <div class="relative pl-9">
              <dt class="inline font-semibold text-white">
                <svg class="absolute top-1 left-1 h-5 w-5 text-indigo-500" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
                  <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.719c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                </svg>
                {{ feature.title }}
              </dt>
              <dd class="inline">{{ feature.description }}</dd>
            </div>
            {% endfor %}
          </dl>
        </div>
      </div>
    </div>
  </div>

  <!-- Solutions section -->
  <div class="mx-auto mt-32 max-w-7xl px-6 sm:mt-56 lg:px-8" id="solutions">
    <div class="mx-auto max-w-2xl lg:text-center">
      <h2 class="text-base/7 font-semibold text-indigo-600">{{ site.data.landing.solutions.title }}</h2>
      <p class="mt-2 text-4xl font-semibold tracking-tight text-pretty text-gray-900 sm:text-5xl lg:text-balance">{{ site.data.landing.solutions.subtitle }}</p>
      <p class="mt-6 text-lg/8 text-gray-600">{{ site.data.landing.solutions.description }}</p>
    </div>
    <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-none">
      <dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-16 lg:max-w-none lg:grid-cols-3">
        {% for feature in site.data.landing.solutions.items %}
        <div class="flex flex-col">
          <dt class="flex items-center gap-x-3 text-base/7 font-semibold text-gray-900">
            {% case feature.icon %}
            {% when 'insight' %}
            <svg class="h-5 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
              <path d="M11.5 1.75a.75.75 0 0 0-1.5 0v1.128a5.752 5.752 0 0 0-4.33 3.656.75.75 0 0 0 1.414.53A4.252 4.252 0 0 1 10 4.25h.75v2.25H9.5a3.75 3.75 0 0 0-3.75 3.75v.25a.75.75 0 0 0 1.5 0v-.25A2.25 2.25 0 0 1 9.5 7.75h1.25v2.25a3.75 3.75 0 0 0 3.75 3.75.75.75 0 0 0 0-1.5 2.25 2.25 0 0 1-2.25-2.25V4.25h.75a4.25 4.25 0 0 1 4.25 4.25.75.75 0 0 0 1.5 0A5.75 5.75 0 0 0 11.5 2.878V1.75Z" />
            </svg>
            {% when 'globe' %}
            <svg class="h-5 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
              <path fill-rule="evenodd" d="M10 1.25a8.75 8.75 0 1 0 0 17.5 8.75 8.75 0 0 0 0-17.5Zm6.215 8a7.252 7.252 0 0 0-5.465-5.465 17.53 17.53 0 0 1 1.35 5.465h4.115Zm-5.615 1.5v3.872c.563.374 1.453.628 2.4.628 1.27 0 2.5-.455 3.265-1.22a7.233 7.233 0 0 0 .796-3.28h-6.461Zm-1.5 0H2.92a7.233 7.233 0 0 0 .796 3.28c.765.765 1.995 1.22 3.265 1.22.947 0 1.837-.254 2.4-.628V10.75Zm0-1.5V5.378c-.563-.374-1.453-.628-2.4-.628-1.27 0-2.5.455-3.265 1.22A7.233 7.233 0 0 0 2.92 9.25h6.18Zm1.5 0h6.46a7.233 7.233 0 0 0-.796-3.28c-.765-.765-1.995-1.22-3.265-1.22-.947 0-1.837.254-2.4.628V9.25Zm-1.5 5.372V10.75h-2.25v2.27c0 .648.125 1.81 2.25 1.856Zm1.5-4.622V5.378c2.125.046 2.25 1.208 2.25 1.856V9.25h-2.25Z" clip-rule="evenodd" />
            </svg>
            {% when 'automation' %}
            <svg class="h-5 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
              <path fill-rule="evenodd" d="M15.312 11.424a5.5 5.5 0 0 1-9.201 2.466l-.312-.311h2.433a.75.75 0 0 0 0-1.5H3.989a.75.75 0 0 0-.75.75v4.242a.75.75 0 0 0 1.5 0v-2.43l.31.31a7 7 0 0 0 11.712-3.138.75.75 0 0 0-1.449-.39Z" clip-rule="evenodd" />
              <path fill-rule="evenodd" d="M4.688 8.576a5.5 5.5 0 0 1 9.201-2.466l.312.311H11.77a.75.75 0 0 0 0 1.5h4.243a.75.75 0 0 0 .75-.75V2.929a.75.75 0 0 0-1.5 0V5.36l-.31-.31A7 7 0 0 0 3.239 8.188a.75.75 0 1 0 1.449.39Z" clip-rule="evenodd" />
            </svg>
            {% else %}
            <svg class="h-5 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.719c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
            </svg>
            {% endcase %}
            {{ feature.title }}
          </dt>
          <dd class="mt-4 flex flex-auto flex-col text-base/7 text-gray-600">
            <p class="flex-auto">{{ feature.description }}</p>
            <p class="mt-6">
              <a href="#" class="text-sm/6 font-semibold text-indigo-600">Learn more <span aria-hidden="true">→</span></a>
            </p>
          </dd>
        </div>
        {% endfor %}
      </dl>
    </div>
  </div>

  <!-- Portfolio section -->
  <div class="mx-auto mt-32 max-w-7xl px-6 sm:mt-56 lg:px-8" id="portfolio">
    <div class="mx-auto max-w-4xl text-center">
      <h2 class="text-base/7 font-semibold text-indigo-600">{{ site.data.landing.portfolio.title }}</h2>
      <p class="mt-2 text-5xl font-semibold tracking-tight text-pretty text-gray-900 sm:text-balance">{{ site.data.landing.portfolio.subtitle }}</p>
      <p class="mt-6 text-lg/8 text-gray-600">{{ site.data.landing.portfolio.description }}</p>
    </div>

    <!-- Portfolio features -->
    <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-none">
      <dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-16 lg:max-w-none lg:grid-cols-3">
        {% for feature in site.data.landing.portfolio.features %}
        <div class="flex flex-col">
          <dt class="flex items-center gap-x-3 text-base/7 font-semibold text-gray-900">
            <svg class="h-5 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.719c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
            </svg>
            {{ feature.title }}
          </dt>
          <dd class="mt-4 flex flex-auto flex-col text-base/7 text-gray-600">
            <p class="flex-auto">{{ feature.description }}</p>
          </dd>
        </div>
        {% endfor %}
      </dl>
    </div>

    <!-- CTA to visit Reviato -->
    <div class="mt-16 text-center">
      <a href="{{ site.data.landing.portfolio.link.url }}" class="rounded-md bg-indigo-600 px-6 py-3 text-lg font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">{{ site.data.landing.portfolio.link.text }}</a>
    </div>

    <!-- Portfolio stats -->
    <div class="mt-20">
      <dl class="grid grid-cols-1 gap-0.5 overflow-hidden rounded-2xl text-center sm:grid-cols-3">
        {% for stat in site.data.landing.portfolio.stats %}
        <div class="flex flex-col bg-gray-400/5 p-8">
          <dt class="text-sm/6 font-semibold text-gray-600">{{ stat.label }}</dt>
          <dd class="order-first text-3xl font-semibold tracking-tight text-gray-900">{{ stat.value }}</dd>
        </div>
        {% endfor %}
      </dl>
    </div>
  </div>

 {% include index/testimonials.html %}
</main>

{% include footer.html %}
