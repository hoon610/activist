<template>
  <div
    class="text-light-text dark:text-dark-text bg-light-content dark:bg-dark-content"
  >
    <Head>
      <Title>{{ $t("pages.about.index.title") }}</Title>
    </Head>
    <div
      class="flex flex-col items-center w-full responsive-py-4 responsive-px-5"
    >
      <!-- Note: image on top of content. -->
      <img
        v-if="$colorMode.value == 'light'"
        class="h-40 mb-4 md:hidden sm:h-52"
        src="/images/content_pages/icons/activist_icon_light.png"
        alt="The activist icon: a lower case letter a with a half circle pointing down and to the left in the center."
      />
      <img
        v-else-if="$colorMode.value == 'dark'"
        class="h-40 mb-4 md:hidden sm:h-52"
        src="/images/content_pages/icons/activist_icon_dark.png"
        alt="The activist icon: a lower case letter a with a half circle pointing down and to the left in the center."
      />
      <div class="grid w-10/12 grid-cols-1 md:w-full 2xl:grid-cols-2">
        <div class="items-center space-y-4 text-left md:items-start">
          <!-- Note: image floating right of content. -->
          <img
            v-if="$colorMode.value == 'light'"
            class="hidden float-right p-4 h-52 md:block 2xl:hidden lg:h-64"
            src="/images/content_pages/icons/activist_icon_light.png"
            alt="The activist icon: a lower case letter a with a half circle pointing down and to the left in the center."
          />
          <img
            v-else-if="$colorMode.value == 'dark'"
            class="hidden float-right p-4 h-52 md:block 2xl:hidden lg:h-64"
            src="/images/content_pages/icons/activist_icon_dark.png"
            alt="The activist icon: a lower case letter a with a half circle pointing down and to the left in the center."
          />
          <h1 class="pb-2 font-bold responsive-h1">
            {{ $t("pages.about.index.header") }}
          </h1>
          <div class="flex flex-row py-2 space-x-3">
            <Icon
              class="text-light-link-text dark:text-dark-link-text mt-[0.125rem]"
              name="bi:info-circle-fill"
              size="1.25em"
            />
            <p>
              {{ $t("pages.about.index.subheader-1") }}
              <a
                class="items-center focus-brand link-text"
                href="https://www.figma.com/file/I9McFfaLu1RiiWp5IP3YjE/activist_public_designs?node-id=805%3A231&t=vNWHCPdiq5EbPaO9-1"
                target="_blank"
              >
                {{ $t("pages.about.index.subheader-2") }}
                <Icon
                  name="bi:box-arrow-up-right"
                  size="1em"
                  style="vertical-align: baseline"
                />
              </a>
              {{ $t("pages.about.index.subheader-3") }}
            </p>
          </div>
          <p>
            {{ $t("pages.about.index.section-1-paragraph-1") }}
          </p>
          <p>
            {{ $t("pages.about.index.section-1-paragraph-2") }}
          </p>
          <p>
            {{ $t("pages.about.index.section-1-paragraph-3") }}
          </p>
          <p>
            {{ $t("pages.about.index.section-1-paragraph-4") }}
          </p>
          <p class="pb-2 lg:pb-4">
            {{ $t("pages.about.index.section-1-paragraph-5-1") }}
            <a
              class="items-center focus-brand link-text"
              href="https://github.com/orgs/activist-org"
              target="_blank"
            >
              {{ $t("pages.about.index.section-1-paragraph-5-2") }}
              <Icon
                name="bi:box-arrow-up-right"
                size="1em"
                style="vertical-align: baseline"
              />
            </a>
            {{ $t("pages.about.index.section-1-paragraph-5-3") }}
            <a
              class="items-center focus-brand link-text"
              href="https://matrix.to/#/#activist_community:matrix.org"
              target="_blank"
            >
              {{ $t("pages.about.index.section-1-paragraph-5-4") }}
              <Icon
                name="bi:box-arrow-up-right"
                size="1em"
                style="vertical-align: baseline"
              />
            </a>
            {{ $t("pages.about.index.section-1-paragraph-5-5") }}
          </p>
          <div
            class="grid grid-cols-1 max-w-[70%] sm:max-w-[90%] md:max-w-[70%] lg:max-w-[60%] xl:max-w-[50%] 2xl:max-w-[80%] grid-rows-2 gap-y-4 sm:gap-y-0 sm:gap-x-4 md:gap-x-6 xl:gap-x-8 mx-auto sm:mx-0 sm:grid-cols-2 sm:grid-rows-1"
          >
            <BtnLabeled
              class="w-full"
              :cta="true"
              label="components.btn-labeled.request-access"
              linkTo="https://tally.so/r/nprxbq"
              fontSize="lg"
              ariaLabel="
                components.btn-labeled.request-access-aria-label
              "
            />
            <BtnLabeled
              class="w-full"
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
            src="/images/content_pages/icons/activist_icon_light.png"
            alt="The activist icon: a lower case letter a with a half circle pointing down and to the left in the center."
          />
          <img
            v-else-if="$colorMode.value == 'dark'"
            class="hidden 2xl:block h-72"
            src="/images/content_pages/icons/activist_icon_dark.png"
            alt="The activist icon: a lower case letter a with a half circle pointing down and to the left in the center."
          />
        </div>
      </div>
    </div>
  </div>
</template>
