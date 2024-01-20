<template>
  <nav
    class="border-t border-gray-200 px-4 flex items-center justify-between sm:px-0 my-3"
  >
    <div class="-mt-px w-0 flex-1 flex">
      <a
        @click.prevent="goToPreviousPage"
        href="#"
        class="pt-4 pr-1 inline-flex items-center text-sm font-medium text-gray-500 hover:text-gray-700 hover:border-gray-300"
      >
        <ArrowLeftIcon
          class="mr-3 h-5 w-5 text-gray-400"
          aria-hidden="true"
        />
        Previous
      </a>
    </div>
    <div class="-mt-px w-0 flex-1 flex justify-end">
      <a
        @click.prevent="goToNextPage"
        href="#"
        class="border-t-2 border-transparent pt-4 pl-1 inline-flex items-center text-sm font-medium text-gray-500 hover:text-gray-700 hover:border-gray-300"
      >
        Next
        <ArrowRightIcon
          class="ml-3 h-5 w-5 text-gray-400"
          aria-hidden="true"
        />
      </a>
    </div>
  </nav>
</template>

<script>
import {
  ArrowLeftIcon,
  ArrowRightIcon,
} from "@heroicons/vue/24/solid";

export default {
  components: {
    ArrowLeftIcon,
    ArrowRightIcon,
  },
  props: {
    goToNextPage: {
      type: Function,
      required: true,
    },
    goToPreviousPage: {
      type: Function,
      required: true,
    },
  },

  setup(props) {
    return {
      goToNextPage: props.goToNextPage,
      goToPreviousPage: props.goToPreviousPage,
    };
  },
};
</script>
