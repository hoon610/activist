<template>
  <div class="flex flex-col">
    <div
      class="opacity-0 -my-4 w-full"
      :class="{
        '!opacity-100 flex items-center justify-center my-0 text-light-text dark:text-dark-cta-orange transition bg-light-cta-orange/80 dark:bg-dark-cta-orange/20 rounded-md border border-light-text dark:border-dark-cta-orange':
          sidebar.collapsed == true && sidebar.collapsedSwitch == true,
      }"
    >
      <Icon class="mt-[0.125em]" name="bi:filter" size="2em" />
    </div>
    <div
      class="opacity-0 text-light-text dark:text-dark-text transition"
      :class="{
        '!opacity-100':
          sidebar.collapsed == false || sidebar.collapsedSwitch == false,
      }"
    >
      <template v-for="(filter, key) in filters">
        <div
          @click="filter.reveal = !filter.reveal"
          class="flex items-center cursor-pointer w-fit"
        >
          <h3 v-if="filter.title" class="mb-2 font-bold font-display text-lg">
            {{ filter.title }}
          </h3>
          <div v-if="filter.expandable">
            <Icon
              class="flex-shrink-0 my-1 mb-3 ml-4"
              :class="{ 'rotate-180': filter.reveal }"
              name="bi:chevron-down"
              size="1.25em"
            />
          </div>
        </div>
        <div class="mb-4">
          <FormRadioGroup
            v-if="filter.type === 'radio'"
            :key="key"
            :options="filter.items"
            :name="filter.name"
            :title="filter.title"
            :style="filter.style"
            :allowCustomValue="filter.allowCustomValue"
            v-model="selectedValues[filter.name]"
          />
          <keep-alive>
            <FormCheckboxGroup
              v-if="
                (filter.type === 'checkbox' && !filter.reveal) ||
                filter.reveal === false
              "
              class="mb-1"
              :key="key"
              :options="filter.items"
              :name="filter.name"
              :title="filter.title"
              :style="filter.style"
              v-model="selectedValues[filter.name]"
            />
          </keep-alive>
          <FormSearch
            v-if="filter.type === 'search'"
            :key="key"
            :name="filter.name"
            v-model="selectedValues[filter.name]"
            :placeholder="filter.placeholder"
          />
        </div>
      </template>
    </div>
  </div>
</template>

<script setup lang="ts">
const sidebar = useSidebar();

interface FilterOption {
  label: string;
  value: string;
}

interface Filter {
  title: string;
  name: string;
  type: "radio" | "checkbox" | "search";
  items: FilterOption[];
  style?: string;
  allowCustomValue?: boolean;
  pageType?: string[];
  searchInput?: boolean;
  placeholder?: string;
  expandable?: boolean;
  reveal?: boolean;
}

interface Filters {
  [key: string]: Filter;
}

interface SelectedValues {
  [key: string]: string | string[];
}

const props = defineProps({
  filters: {
    type: Object as () => Filters,
    required: true,
  },
});

const filters = ref(props.filters);

const selectedValues: Ref<SelectedValues> = ref({});

watch(selectedValues.value, (newVal) => {
  console.log("selectedValues changed");
  console.log(newVal);

  // TODO: Filter items based on selected filters.
});
</script>
