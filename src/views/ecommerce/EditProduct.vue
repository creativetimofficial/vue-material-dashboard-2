<template>
  <div class="py-4 container-fluid">
    <div class="row">
      <div class="col-lg-6">
        <h4>Make the changes below</h4>
        <p>
          We’re constantly trying to express ourselves and actualize our dreams.
          If you have the opportunity to play.
        </p>
      </div>
      <div
        class="text-right col-lg-6 d-flex flex-column justify-content-center"
      >
        <button
          type="button"
          class="mt-2 mb-0 btn bg-gradient-success ms-lg-auto me-lg-0 me-auto mt-lg-0"
        >
          Save
        </button>
      </div>
    </div>
    <div class="mt-4 row">
      <div class="col-lg-4">
        <div class="card mt-4" data-animation="true">
          <div class="card-header p-0 position-relative mt-n4 mx-3 z-index-2">
            <a class="d-block blur-shadow-image">
              <img
                src="../../assets/img/products/product-11.jpg"
                alt="img-blur-shadow"
                class="img-fluid shadow border-radius-lg"
              />
            </a>
            <div
              class="colored-shadow"
              style="
                background-image: url('../../assets/img/products/product-11.jpg');
              "
            ></div>
          </div>
          <div class="card-body text-center">
            <div class="mt-n6 mx-auto">
              <button
                class="btn bg-gradient-success btn-sm mb-0 me-2"
                type="button"
                name="button"
              >
                Edit
              </button>
              <button
                class="btn btn-outline-dark btn-sm mb-0"
                type="button"
                name="button"
              >
                Remove
              </button>
            </div>
            <h5 class="font-weight-normal mt-4">Product Image</h5>
            <p class="mb-0">
              The place is close to Barceloneta Beach and bus stop just 2 min by
              walk and near to "Naviglio" where you can enjoy the main night
              life in Barcelona.
            </p>
          </div>
        </div>
      </div>
      <div class="mt-4 col-lg-8 mt-lg-0">
        <div class="card">
          <div class="card-body">
            <h5 class="font-weight-bolder">Product Information</h5>
            <div class="row mt-4">
              <div class="col-12 col-sm-6">
                <VmdInput variant="dynamic" label="Name" />
              </div>
              <div class="mt-3 col-12 col-sm-6 mt-sm-0">
                <VmdInput variant="dynamic" label="Weight" />
              </div>
            </div>
            <div class="row mt-4">
              <div class="col-3">
                <VmdInput variant="dynamic" label="Collection" />
              </div>
              <div class="col-3">
                <VmdInput variant="dynamic" label="Price" />
              </div>
              <div class="col-3">
                <VmdInput variant="dynamic" label="Quantity" />
              </div>
            </div>
            <div class="row">
              <div class="col-sm-6">
                <label class="mt-4 ms-0">Description</label>
                <p class="text-xs form-text text-muted ms-1 d-inline">
                  (optional)
                </p>
                <div id="edit-description-edit" class="h-50">
                  Long sleeves black denim jacket with a twisted design.
                  Contrast stitching. Button up closure. White arrow prints on
                  the back.
                </div>
              </div>
              <div class="col-sm-6">
                <label class="mt-4 ms-0">Category</label>
                <select
                  class="form-control"
                  name="choices-category"
                  id="choices-category-edit"
                >
                  <option value="Choice 1" selected>Furniture</option>
                  <option value="Choice 2">Real Estate</option>
                  <option value="Choice 3">Electronics</option>
                  <option value="Choice 4">Clothing</option>
                  <option value="Choice 5">Others</option>
                </select>
                <label class="mt-3 ms-0">Color</label>
                <select
                  class="form-control"
                  name="choices-color"
                  id="choices-color-edit"
                >
                  <option value="Choice 1" selected>Black</option>
                  <option value="Choice 2">White</option>
                  <option value="Choice 3">Blue</option>
                  <option value="Choice 4">Orange</option>
                  <option value="Choice 5">Green</option>
                </select>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="mt-4 row">
      <div class="col-sm-4">
        <div class="card">
          <div class="card-body">
            <h5 class="font-weight-bolder mb-4">Socials</h5>
            <div class="col-12">
              <vmd-input label="Shopify Handle" variant="dynamic" />
            </div>
            <div class="col-12 mt-3">
              <vmd-input label="Facebook Handle" variant="dynamic" />
            </div>
            <div class="col-12 mt-3">
              <vmd-input label="Instagram Handle" variant="dynamic" />
            </div>
          </div>
        </div>
      </div>
      <div class="mt-4 col-sm-8 mt-sm-0">
        <div class="card">
          <div class="card-body">
            <div class="row">
              <h5 class="font-weight-bolder mb-4">Pricing</h5>
              <div class="col-3">
                <vmd-input label="Price" variant="dynamic" />
              </div>
              <div class="col-4">
                <select
                  class="form-control"
                  name="choices-sizes"
                  id="choices-currency-edit"
                >
                  <option value="Choice 1" selected>USD</option>
                  <option value="Choice 2">EUR</option>
                  <option value="Choice 3">GBP</option>
                  <option value="Choice 4">CNY</option>
                  <option value="Choice 5">INR</option>
                  <option value="Choice 6">BTC</option>
                </select>
              </div>
              <div class="col-5">
                <vmd-input label="SKU" variant="dynamic" />
              </div>
            </div>
            <div class="row">
              <div class="col-12">
                <label class="mt-4 ms-0">Tags</label>
                <select
                  class="form-control"
                  name="choices-tags"
                  id="choices-tags-edit"
                  multiple
                >
                  <option value="Choice 1" selected>In Stock</option>
                  <option value="Choice 2">Out of Stock</option>
                  <option value="Choice 3">Sale</option>
                  <option value="Choice 4">Black Friday</option>
                </select>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
/* eslint-disable prettier/prettier */
import Quill from "quill";
import Choices from "choices.js";
import VmdInput from "@/components/VmdInput.vue";

export default {
  name: "edit-product",

  components: { VmdInput },
  mounted() {
    if (document.getElementById("edit-description-edit")) {
      new Quill("#edit-description-edit", {
        theme: "snow", // Specify theme in configuration
      });
    }
    this.getChoices("choices-category-edit");
    this.getChoices("choices-color-edit");
    this.getChoices("choices-currency-edit");

    if (document.getElementById("choices-tags-edit")) {
      var tags = document.getElementById("choices-tags-edit");
      const examples = new Choices(tags, {
        removeItemButton: true,
      });

      examples.setChoices(
        [
          {
            value: "One",
            label: "Expired",
            disabled: true,
          },
          {
            value: "Two",
            label: "Out of Stock",
            selected: true,
          },
        ],
        "value",
        "label",
        false,
      );
    }
  },
  methods: {
    getChoices(id) {
      if (document.getElementById(id)) {
        var element = document.getElementById(id);
        return new Choices(element, {
          searchEnabled: false,
        });
      }
    },
  },
};
</script>
