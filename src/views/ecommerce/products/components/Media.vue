<template>
  <div
    class="pt-3 bg-white multisteps-form__panel border-radius-xl"
    data-animation="FadeIn"
  >
    <h5 class="font-weight-bolder">Media</h5>
    <div class="multisteps-form__content">
      <div class="mt-3 row">
        <div class="col-12">
          <label class="form-control mb-0">Product images</label>
          <div
            action="/file-upload"
            class="form-control border dropzone"
            id="productImg"
          ></div>
        </div>
      </div>
      <div class="mt-4 button-row d-flex col-12">
        <vmd-button
          color="secondary"
          variant="gradient"
          class="mb-0 js-btn-prev"
          title="Prev"
          @click="this.$parent.prevStep"
          >Prev</vmd-button
        >
        <vmd-button
          type="button"
          color="dark"
          variant="gradient"
          class="mb-0 ms-auto js-btn-next"
          title="Next"
          @click="this.$parent.nextStep"
          >Next</vmd-button
        >
      </div>
    </div>
  </div>
</template>

<script>
import Dropzone from "dropzone";
import VmdButton from "@/components/VmdButton.vue";

export default {
  name: "media",
  components: {
    VmdButton,
  },
  mounted() {
    let myDropzone = new Dropzone("#productImg");
    myDropzone.on("addedfile", (file) => {
      console.log(`File added: ${file.name}`);
    });
  },
};
</script>
