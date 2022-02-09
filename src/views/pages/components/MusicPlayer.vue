<template>
  <div
    class="card card-background card-background-mask-dark align-items-start mt-4"
  >
    <div
      class="full-background cursor-pointer"
      style="
        background-image: url('https://images.unsplash.com/photo-1604213410393-89f141bb96b8?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTA5fHxuYXR1cmV8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=60');
      "
    ></div>

    <div class="card-body">
      <h5 class="text-white mb-0">{{ title }}</h5>
      <p class="text-white text-sm">{{ desc }}</p>
      <div class="d-flex mt-4 pt-2">
        <vmd-button
          color="white"
          variant="outline"
          class="rounded-circle p-2 mb-0"
          type="button"
        >
          <i
            class="p-2 material-icons"
            :class="this.$store.state.isRTL ? 'skip_next' : 'skip_previous'"
            >skip_next</i
          >
        </vmd-button>
        <vmd-button
          color="white"
          variant="outline"
          class="rounded-circle p-2 mx-2 mb-0"
          type="button"
        >
          <i class="material-icons p-2">play_arrow</i>
        </vmd-button>
        <vmd-button
          color="white"
          variant="outline"
          class="rounded-circle p-2 mb-0"
          type="button"
        >
          <i
            class="material-icons p-2"
            :class="this.$store.state.isRTL ? 'skip_previous' : 'skip_next'"
            >skip_previous</i
          >
        </vmd-button>
      </div>
    </div>
  </div>
</template>

<script>
import VmdButton from "@/components/VmdButton.vue";

export default {
  name: "music-player",
  props: {
    title: {
      type: String,
      default: "Some Kind Of Blues",
    },
    desc: {
      type: String,
      default: "Deftones",
    },
  },
  components: {
    VmdButton,
  },
};
</script>
