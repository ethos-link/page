---
layout: default
title: Home
---

{% include header.html %}

<main>
  <!-- Hero section -->
  <div class="relative isolate pt-14">
    <div class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80" aria-hidden="true">
      <div class="relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)"></div>
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
                {% if feature.title contains 'Smart Review' %}
                <svg class="absolute top-1 left-1 h-5 w-5 text-indigo-500" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
                  <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.719c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                </svg>
                {% elsif feature.title contains 'AI-Powered' %}
                <svg class="absolute top-1 left-1 h-5 w-5 text-indigo-500" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
                  <path fill-rule="evenodd" d="M10 2c1.415 0 2.707.497 3.728 1.325a5.003 5.003 0 0 1 3.947 3.947A5.003 5.003 0 0 1 18.998 10a5.003 5.003 0 0 1-1.323 3.728A5.003 5.003 0 0 1 14 16a5.003 5.003 0 0 1-8 0 5.003 5.003 0 0 1-3.675-2.272A5.003 5.003 0 0 1 1.002 10a5.003 5.003 0 0 1 1.323-3.728A5.003 5.003 0 0 1 6 4a5.003 5.003 0 0 1 4-2Z" clip-rule="evenodd" />
                </svg>
                {% elsif feature.title contains 'Automated' %}
                <svg class="absolute top-1 left-1 h-5 w-5 text-indigo-500" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
                  <path fill-rule="evenodd" d="M15.312 11.424a5.5 5.5 0 0 1-9.201 2.466l-.312-.311h2.433a.75.75 0 0 0 0-1.5H3.989a.75.75 0 0 0-.75.75v4.242a.75.75 0 0 0 1.5 0v-2.43l.31.31a7 7 0 0 0 11.712-3.138.75.75 0 0 0-1.449-.39Z" clip-rule="evenodd" />
                  <path fill-rule="evenodd" d="M4.688 8.576a5.5 5.5 0 0 1 9.201-2.466l.312.311H11.77a.75.75 0 0 0 0 1.5h4.243a.75.75 0 0 0 .75-.75V2.929a.75.75 0 0 0-1.5 0V5.36l-.31-.31A7 7 0 0 0 3.239 8.188a.75.75 0 1 0 1.449.39Z" clip-rule="evenodd" />
                </svg>
                {% else %}
                <svg class="absolute top-1 left-1 h-5 w-5 text-indigo-500" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
                  <path d="M4.632 3.533A2 2 0 0 1 6.577 2h6.846a2 2 0 0 1 1.945 1.533l1.976 8.234A3.489 3.489 0 0 0 16 11.5H4c-.476 0-.93.095-1.344.267l1.976-8.234Z" />
                  <path fill-rule="evenodd" d="M4 13a2 2 0 1 0 0 4h12a2 2 0 1 0 0-4H4Zm11.24 2a.75.75 0 0 1 .75-.75H16a.75.75 0 0 1 .75.75v.01a.75.75 0 0 1-.75.75h-.01a.75.75 0 0 1-.75-.75V15Zm-2.25-.75a.75.75 0 0 0-.75.75v.01c0 .414.336.75.75.75H13a.75.75 0 0 0 .75-.75V15a.75.75 0 0 0-.75-.75h-.01Z" clip-rule="evenodd" />
                </svg>
                {% endif %}
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
            {% if feature.icon == 'users' %}
            <svg class="h-5 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
              <path d="M10 9a3 3 0 1 0 0-6 3 3 0 0 0 0 6ZM6 8a2 2 0 1 1-4 0 2 2 0 0 1 4 0ZM1.49 15.326a.78.78 0 0 1-.358-.442 3 3 0 0 1 4.308-3.516 6.484 6.484 0 0 0-1.905 3.959c-.023.222-.014.442.025.654a4.97 4.97 0 0 1-2.07-.655ZM16.44 15.98a4.97 4.97 0 0 0 2.07-.654.78.78 0 0 0 .357-.442 3 3 0 0 0-4.308-3.517 6.484 6.484 0 0 1 1.907 3.96 2.32 2.32 0 0 1-.026.654ZM18 8a2 2 0 1 1-4 0 2 2 0 0 1 4 0ZM5.304 16.19a.844.844 0 0 1-.277-.71 5 5 0 0 1 9.947 0 .843.843 0 0 1-.277.71A6.975 6.975 0 0 1 10 18a6.974 6.974 0 0 1-4.696-1.81Z" />
            </svg>
            {% elsif feature.icon == 'brain' %}
            <svg class="h-5 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
              <path fill-rule="evenodd" d="M10 2c1.415 0 2.707.497 3.728 1.325a5.003 5.003 0 0 1 3.947 3.947A5.003 5.003 0 0 1 18.998 10a5.003 5.003 0 0 1-1.323 3.728A5.003 5.003 0 0 1 14 16a5.003 5.003 0 0 1-8 0 5.003 5.003 0 0 1-3.675-2.272A5.003 5.003 0 0 1 1.002 10a5.003 5.003 0 0 1 1.323-3.728A5.003 5.003 0 0 1 6 4a5.003 5.003 0 0 1 4-2Z" clip-rule="evenodd" />
            </svg>
            {% elsif feature.icon == 'automation' %}
            <svg class="h-5 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
              <path fill-rule="evenodd" d="M15.312 11.424a5.5 5.5 0 0 1-9.201 2.466l-.312-.311h2.433a.75.75 0 0 0 0-1.5H3.989a.75.75 0 0 0-.75.75v4.242a.75.75 0 0 0 1.5 0v-2.43l.31.31a7 7 0 0 0 11.712-3.138.75.75 0 0 0-1.449-.39Z" clip-rule="evenodd" />
              <path fill-rule="evenodd" d="M4.688 8.576a5.5 5.5 0 0 1 9.201-2.466l.312.311H11.77a.75.75 0 0 0 0 1.5h4.243a.75.75 0 0 0 .75-.75V2.929a.75.75 0 0 0-1.5 0V5.36l-.31-.31A7 7 0 0 0 3.239 8.188a.75.75 0 1 0 1.449.39Z" clip-rule="evenodd" />
            </svg>
            {% else %}
            <svg class="h-5 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.719c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
            </svg>
            {% endif %}
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
      <a href="{{ site.data.landing.portfolio.link.url }}" target="_blank" class="rounded-md bg-indigo-600 px-6 py-3 text-lg font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">{{ site.data.landing.portfolio.link.text }}</a>
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

{% include index/contact.html %}
</main>

{% include footer.html %}