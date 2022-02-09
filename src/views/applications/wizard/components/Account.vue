<template>
  <div
    class="pt-3 bg-white multisteps-form__panel border-radius-xl"
    data-animation="FadeIn"
  >
    <div class="text-center row">
      <div class="mx-auto col-10">
        <h5 class="font-weight-normal">What are you doing? (checkboxes)</h5>
        <p>
          Give us more details about you. What do you enjoy doing in your spare
          time?
        </p>
      </div>
    </div>
    <div class="multisteps-form__content">
      <div class="mt-4 row">
        <div class="col-sm-3 ms-auto">
          <input type="checkbox" class="btn-check" id="btncheck1" />
          <label
            class="btn btn-lg btn-outline-success border-2 px-6 py-5"
            for="btncheck1"
          >
            <i class="material-icons">brush</i>
          </label>
          <h6>Design</h6>
        </div>
        <div class="col-sm-3">
          <input type="checkbox" class="btn-check" id="btncheck2" />
          <label
            class="btn btn-lg btn-outline-success border-2 px-6 py-5"
            for="btncheck2"
          >
            <i class="material-icons">integration_instructions</i>
          </label>
          <h6>Code</h6>
        </div>
        <div class="col-sm-3 me-auto">
          <input type="checkbox" class="btn-check" id="btncheck3" />
          <label
            class="btn btn-lg btn-outline-success border-2 px-6 py-5"
            for="btncheck3"
          >
            <i class="material-icons">developer_mode</i>
          </label>
          <h6>Develop</h6>
        </div>
      </div>
      <div class="mt-4 button-row d-flex">
        <button
          class="mb-0 btn bg-gradient-light js-btn-prev"
          type="button"
          title="Prev"
          @click="this.$parent.prevStep"
        >
          Prev
        </button>
        <button
          class="mb-0 btn bg-gradient-dark ms-auto js-btn-next"
          type="button"
          title="Next"
          @click="this.$parent.nextStep"
        >
          Next
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "account",
};
</script>
