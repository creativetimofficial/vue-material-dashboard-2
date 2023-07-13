<template>
  <div class="container-fluid py-4">
    <div class="row">
      <div class="col-md-8 mx-auto">
        <div class="card mt-4">
          <div class="card-header p-3">
            <h5 class="mb-0">Alerts</h5>
          </div>
          <div class="card-body p-3 pb-0">
            <material-alert
              class="font-weight-light"
              color="primary"
              dismissible
            >
              <span class="text-sm"
                >A simple primary alert with
                <a href="javascript:;" class="alert-link text-white"
                  >an example link</a
                >. Give it a click if you like.</span
              >
            </material-alert>
            <material-alert
              class="font-weight-light"
              color="secondary"
              dismissible
            >
              <span class="text-sm"
                >A simple secondary alert with
                <a href="javascript:;" class="alert-link text-white"
                  >an example link</a
                >. Give it a click if you like.</span
              >
            </material-alert>
            <material-alert
              class="font-weight-light"
              color="success"
              dismissible
            >
              <span class="text-sm"
                >A simple success alert with
                <a href="javascript:;" class="alert-link text-white"
                  >an example link</a
                >. Give it a click if you like.</span
              >
            </material-alert>
            <material-alert
              class="font-weight-light"
              color="danger"
              dismissible
            >
              <span class="text-sm"
                >A simple danger alert with
                <a href="javascript:;" class="alert-link text-white"
                  >an example link</a
                >. Give it a click if you like.</span
              >
            </material-alert>
            <material-alert
              class="font-weight-light"
              color="warning"
              dismissible
            >
              <span class="text-sm"
                >A simple warning alert with
                <a href="javascript:;" class="alert-link text-white"
                  >an example link</a
                >. Give it a click if you like.</span
              >
            </material-alert>
            <material-alert class="font-weight-light" color="info" dismissible>
              <span class="text-sm"
                >A simple info alert with
                <a href="javascript:;" class="alert-link text-white"
                  >an example link</a
                >. Give it a click if you like.</span
              >
            </material-alert>
            <material-alert class="font-weight-light" color="light" dismissible>
              <span class="text-sm"
                >A simple light alert with
                <a href="javascript:;" class="alert-link text-white"
                  >an example link</a
                >. Give it a click if you like.</span
              >
            </material-alert>
            <material-alert color="dark" dismissible>
              <span class="text-sm"
                >A simple dark alert with
                <a href="javascript:;" class="alert-link text-white"
                  >an example link</a
                >. Give it a click if you like.</span
              >
            </material-alert>
          </div>
        </div>
        <div class="card mt-4">
          <div class="card-header p-3">
            <h5 class="mb-0">Notifications</h5>
            <p class="text-sm mb-0">
              Notifications on this page use Toasts from Bootstrap. Read more
              details
              <a
                href="https://getbootstrap.com/docs/5.0/components/toasts/"
                target="
          "
                >here</a
              >.
            </p>
          </div>
          <div class="card-body p-3">
            <div class="row">
              <div class="col-lg-3 col-sm-6 col-12">
                <button
                  class="btn bg-gradient-success w-100 mb-0 toast-btn"
                  type="button"
                  data-target="successToast"
                  @click="snackbar = 'success'"
                >
                  Success
                </button>
              </div>
              <div class="col-lg-3 col-sm-6 col-12 mt-sm-0 mt-2">
                <button
                  class="btn bg-gradient-info w-100 mb-0 toast-btn"
                  type="button"
                  data-target="infoToast"
                  @click="snackbar = 'info'"
                >
                  Info
                </button>
              </div>
              <div class="col-lg-3 col-sm-6 col-12 mt-lg-0 mt-2">
                <button
                  class="btn bg-gradient-warning w-100 mb-0 toast-btn"
                  type="button"
                  data-target="warningToast"
                  @click="snackbar = 'warning'"
                >
                  Warning
                </button>
              </div>
              <div class="col-lg-3 col-sm-6 col-12 mt-lg-0 mt-2">
                <button
                  class="btn bg-gradient-danger w-100 mb-0 toast-btn"
                  type="button"
                  data-target="dangerToast"
                  @click="snackbar = 'danger'"
                >
                  Danger
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="position-fixed bottom-1 end-1 z-index-2">
      <material-snackbar
        v-if="snackbar === 'success'"
        title="Material Dashboard"
        date="11 mins ago"
        description="Hello, world! This is a notification message."
        icon="done"
        color="white"
        iconColor="success"
        :closeHandler="closeSnackbar"
        iconName="close"
      />
      <material-snackbar
        v-if="snackbar === 'info'"
        title="Material Dashboard"
        date="11 mins ago"
        description="Hello, world! This is a notification message."
        icon="notifications"
        color="info"
        iconColor="white"
        :closeHandler="closeSnackbar"
        iconName="close"
      />
      <material-snackbar
        v-if="snackbar === 'warning'"
        title="Material Dashboard"
        date="11 mins ago"
        description="Hello, world! This is a notification message."
        icon="travel_explore"
        color="white"
        iconColor="warning"
        :closeHandler="closeSnackbar"
        iconName="close"
      />
      <material-snackbar
        v-if="snackbar === 'danger'"
        title="Material Dashboard"
        date="11 mins ago"
        description="Hello, world! This is a notification message."
        icon="campaign"
        color="white"
        iconColor="danger"
        :closeHandler="closeSnackbar"
        iconName="close"
      />
    </div>
  </div>
</template>

<script>
import MaterialSnackbar from "@/components/MaterialSnackbar.vue";
import MaterialAlert from "@/components/MaterialAlert.vue";

export default {
  name: "Notifications",
  components: {
    MaterialSnackbar,
    MaterialAlert,
  },
  data() {
    return {
      snackbar: null,
    };
  },
  methods: {
    closeSnackbar() {
      this.snackbar = null;
    },
  },
};
</script>
