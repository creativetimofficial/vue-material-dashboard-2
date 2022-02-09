<template>
  <div class="card position-sticky top-1 mt-4">
    <ul class="nav flex-column bg-white border-radius-lg p-3">
      <li class="nav-item">
        <a class="nav-link text-dark d-flex" data-scroll href="#profile">
          <i class="material-icons text-lg me-2">person</i>
          <span class="text-sm">Profile</span>
        </a>
      </li>
      <li class="nav-item pt-2">
        <a class="nav-link text-dark d-flex" data-scroll href="#basic-info">
          <i class="material-icons text-lg me-2">receipt_long</i>
          <span class="text-sm">Basic Info</span>
        </a>
      </li>
      <li class="nav-item pt-2">
        <a class="nav-link text-dark d-flex" data-scroll href="#password">
          <i class="material-icons text-lg me-2">lock</i>
          <span class="text-sm">Change Password</span>
        </a>
      </li>
      <li class="nav-item pt-2">
        <a class="nav-link text-dark d-flex" data-scroll href="#2fa">
          <i class="material-icons text-lg me-2">security</i>
          <span class="text-sm">2FA</span>
        </a>
      </li>
      <li class="nav-item pt-2">
        <a class="nav-link text-dark d-flex" data-scroll href="#accounts">
          <i class="material-icons text-lg me-2">badge</i>
          <span class="text-sm">Accounts</span>
        </a>
      </li>
      <li class="nav-item pt-2">
        <a class="nav-link text-dark d-flex" data-scroll href="#notifications">
          <i class="material-icons text-lg me-2">campaign</i>
          <span class="text-sm">Notifications</span>
        </a>
      </li>
      <li class="nav-item pt-2">
        <a class="nav-link text-dark d-flex" data-scroll href="#sessions">
          <i class="material-icons text-lg me-2">settings_applications</i>
          <span class="text-sm">Sessions</span>
        </a>
      </li>
      <li class="nav-item pt-2">
        <a class="nav-link text-dark d-flex" data-scroll href="#delete">
          <i class="material-icons text-lg me-2">delete</i>
          <span class="text-sm">Delete Account</span>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "side-nav",
};
</script>
