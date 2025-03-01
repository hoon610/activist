<template>
  <div
    class="text-light-text dark:text-dark-text bg-light-content dark:bg-dark-content"
  >
    <Head>
      <Title>{{ $t("pages.legal.trademark-policy.title") }}</Title>
    </Head>
    <div
      class="flex flex-col items-center w-full responsive-py-4 responsive-px-5"
    >
      <!-- Note: image on top of content. -->
      <img
        v-if="$colorMode.value == 'light'"
        class="h-40 mb-4 md:hidden sm:h-52"
        src="/images/content_pages/icons/bootstrap_trademark_light.png"
        alt="The trademark symbol - tm within a square.."
      />
      <img
        v-else-if="$colorMode.value == 'dark'"
        class="h-40 mb-4 md:hidden sm:h-52"
        src="/images/content_pages/icons/bootstrap_trademark_dark.png"
        alt="The trademark symbol - tm within a square.."
      />
      <div class="grid w-10/12 grid-cols-1 md:w-full 2xl:grid-cols-2">
        <div class="items-center space-y-4 text-left md:items-start">
          <!-- Note: image floating right of content. -->
          <img
            v-if="$colorMode.value == 'light'"
            class="hidden float-right p-4 h-52 md:block 2xl:hidden lg:h-64"
            src="/images/content_pages/icons/bootstrap_trademark_light.png"
            alt="The trademark symbol - tm within a square.."
          />
          <img
            v-else-if="$colorMode.value == 'dark'"
            class="hidden float-right p-4 h-52 md:block 2xl:hidden lg:h-64"
            src="/images/content_pages/icons/bootstrap_trademark_dark.png"
            alt="The trademark symbol - tm within a square.."
          />
          <h1 class="pb-2 font-bold responsive-h1">Trademark Policy</h1>
          <p
            class="responsive-h4 text-light-special-text dark:text-dark-special-text"
          >
            {{ $t("pages.legal.trademark-policy.last-updated") }}
          </p>
          <p>
            {{ $t("pages.legal.trademark-policy.section-1-paragraph-1") }}
          </p>
          <p>
            {{ $t("pages.legal.trademark-policy.section-1-paragraph-2") }}
          </p>
          <p>
            {{ $t("pages.legal.trademark-policy.section-1-paragraph-3") }}
          </p>
          <p>
            {{ $t("pages.legal.trademark-policy.section-1-paragraph-4") }}
          </p>
          <p>
            {{ $t("pages.legal.trademark-policy.section-1-paragraph-5-1") }}
            <a class="focus-brand link-text" href="mailto:team@activist.org">
              team@activist.org
            </a>
            .
            {{ $t("pages.legal.trademark-policy.section-1-paragraph-5-2") }}
          </p>
          <h2 class="font-bold responsive-h3">
            {{ $t("pages.legal.trademark-policy.section-2-subheader") }}
          </h2>
          <ul class="ml-6 list-disc">
            <li>
              {{ $t("pages.legal.trademark-policy.section-2-list-1-item-1") }}
            </li>
            <li>
              {{ $t("pages.legal.trademark-policy.section-2-list-1-item-2") }}
            </li>
            <li>
              {{ $t("pages.legal.trademark-policy.section-2-list-1-item-3") }}
            </li>
            <li>
              {{ $t("pages.legal.trademark-policy.section-2-list-1-item-4") }}
            </li>
            <li>
              {{ $t("pages.legal.trademark-policy.section-2-list-1-item-5") }}
            </li>
            <li>
              {{ $t("pages.legal.trademark-policy.section-2-list-1-item-6") }}
            </li>
            <li>
              {{ $t("pages.legal.trademark-policy.section-2-list-1-item-7") }}
            </li>
            <li>
              {{ $t("pages.legal.trademark-policy.section-2-list-1-item-8") }}
            </li>
          </ul>
          <h2 class="font-bold responsive-h3">
            {{ $t("pages.legal.trademark-policy.section-3-subheader") }}
          </h2>
          <p>
            {{ $t("pages.legal.trademark-policy.section-3-paragraph-1") }}
          </p>
          <ul class="ml-6 list-disc">
            <li>
              {{ $t("pages.legal.trademark-policy.section-3-list-1-item-1") }}
            </li>
            <li>
              {{ $t("pages.legal.trademark-policy.section-3-list-1-item-2") }}
            </li>
          </ul>
          <h2 class="font-bold responsive-h3">
            {{ $t("pages.legal.trademark-policy.section-4-subheader") }}
          </h2>
          <ul class="ml-6 list-disc">
            <li>
              {{ $t("pages.legal.trademark-policy.section-4-list-1-item-1") }}
            </li>
          </ul>
          <h2 class="font-bold responsive-h3">
            {{ $t("pages.legal.trademark-policy.section-5-subheader") }}
          </h2>
          <p>
            {{ $t("pages.legal.trademark-policy.section-5-paragraph-1") }}
          </p>
          <p class="pb-2 lg:pb-4">
            {{ $t("pages.legal.trademark-policy.section-5-paragraph-2-1") }}
            <a
              class="items-center focus-brand link-text"
              href="https://github.com/orgs/activist-org"
              target="_blank"
            >
              {{ $t("pages.legal.trademark-policy.section-5-paragraph-2-2") }}
              <Icon
                name="bi:box-arrow-up-right"
                size="1em"
                style="vertical-align: baseline"
              />
            </a>
            {{ $t("pages.legal.trademark-policy.section-5-paragraph-2-3") }}
            <a
              class="items-center focus-brand link-text"
              href="https://matrix.to/#/#activist_community:matrix.org"
              target="_blank"
            >
              {{ $t("pages.legal.trademark-policy.section-5-paragraph-2-4") }}
              <Icon
                name="bi:box-arrow-up-right"
                size="1em"
                style="vertical-align: baseline"
              />
            </a>
            {{ $t("pages.legal.trademark-policy.section-5-paragraph-2-5") }}
          </p>
          <div
            class="flex flex-col items-center space-y-2 md:items-left sm:space-x-4 sm:space-y-0 sm:flex-row"
          >
            <BtnLabeled
              :cta="false"
              label="components.btn-labeled.return-home"
              linkTo="/"
              fontSize="lg"
              ariaLabel="components.btn-labeled.return-home-aria-label"
            />
          </div>
        </div>
        <div class="flex justify-end pr-32">
          <!-- Note: image right of content. -->
          <img
            v-if="$colorMode.value == 'light'"
            class="hidden 2xl:block h-72"
            src="/images/content_pages/icons/bootstrap_trademark_light.png"
            alt="The trademark symbol - tm within a square.."
          />
          <img
            v-else-if="$colorMode.value == 'dark'"
            class="hidden 2xl:block h-72"
            src="/images/content_pages/icons/bootstrap_trademark_dark.png"
            alt="The trademark symbol - tm within a square.."
          />
        </div>
      </div>
    </div>
  </div>
</template>
