<template>
  <div class="card" :class="darkMode ? 'bg-gradient-dark' : ''">
    <div class="pb-0 card-header" :class="darkMode ? 'bg-transparent' : ''">
      <h6 :class="darkMode ? 'text-white' : ''">{{ title }}</h6>
    </div>
    <div class="p-3 card-body">
      <div
        class="timeline timeline-one-side"
        :data-timeline-axis-style="darkMode ? 'dashed' : 'dotted'"
      >
        <div class="mb-3 timeline-block">
          <span class="timeline-step p-3 bg-dark">
            <i class="material-icons text-white text-sm opacity-10"
              >notifications</i
            >
          </span>
          <div class="timeline-content pt-1">
            <h6
              class="mb-0 text-sm font-weight-bold"
              :class="darkMode ? 'text-white' : ''"
            >
              $2400, Design changes
            </h6>
            <p class="mt-1 mb-0 text-xs text-secondary">22 DEC 7:20 PM</p>
            <p class="mt-3 mb-2 text-sm" :class="darkMode ? 'text-white' : ''">
              People care about how you see the world, how you think, what
              motivates you, what you’re struggling with or afraid of.
            </p>
          </div>
        </div>
        <div class="mb-3 timeline-block">
          <span class="timeline-step bg-primary p-3">
            <i class="material-icons text-white text-sm opacity-10">code</i>
          </span>
          <div class="timeline-content pt-1">
            <h6
              class="text-sm font-weight-bold mb-0"
              :class="darkMode ? 'text-white' : ''"
            >
              New order #1832412
            </h6>
            <p class="text-secondary text-xs mt-1 mb-0">21 DEC 11 PM</p>

            <p class="mt-3 mb-2 text-sm" :class="darkMode ? 'text-white' : ''">
              People care about how you see the world, how you think, what
              motivates you, what you’re struggling with or afraid of.
            </p>
          </div>
        </div>
        <div class="mb-3 timeline-block">
          <span class="timeline-step bg-success p-3">
            <i class="material-icons text-white text-sm opacity-10"
              >shopping_cart</i
            >
          </span>
          <div class="timeline-content pt-1">
            <h6
              class="mb-0 text-sm font-weight-bold"
              :class="darkMode ? 'text-white' : ''"
            >
              Server payments for April
            </h6>
            <p class="mt-1 mb-0 text-xs text-secondary">21 DEC 9:34 PM</p>
            <p class="mt-3 mb-2 text-sm" :class="darkMode ? 'text-white' : ''">
              People care about how you see the world, how you think, what
              motivates you, what you’re struggling with or afraid of.
            </p>
          </div>
        </div>
        <div class="mb-3 timeline-block">
          <span class="timeline-step bg-info p-3">
            <i class="material-icons text-white text-sm opacity-10"
              >credit_card</i
            >
          </span>
          <div class="timeline-content pt-1">
            <h6
              class="mb-0 text-sm text-dark font-weight-bold"
              :class="darkMode ? 'text-white' : ''"
            >
              New card added for order #4395133
            </h6>
            <p class="mt-1 mb-0 text-xs text-secondary">20 DEC 2:20 AM</p>
            <p class="mt-3 mb-2 text-sm" :class="darkMode ? 'text-white' : ''">
              People care about how you see the world, how you think, what
              motivates you, what you’re struggling with or afraid of.
            </p>
          </div>
        </div>
        <div class="mb-3 timeline-block">
          <span class="timeline-step bg-dark p-3">
            <i class="material-icons text-white text-sm opacity-10">vpn_key</i>
          </span>
          <div class="timeline-content pt-1">
            <h6
              class="mb-0 text-sm text-dark font-weight-bold"
              :class="darkMode ? 'text-white' : ''"
            >
              Unlock packages for development
            </h6>
            <p class="mt-1 mb-0 text-xs text-secondary">18 DEC 4:54 AM</p>
            <p class="mt-3 mb-2 text-sm" :class="darkMode ? 'text-white' : ''">
              People care about how you see the world, how you think, what
              motivates you, what you’re struggling with or afraid of.
            </p>
          </div>
        </div>
        <div class="timeline-block">
          <span class="timeline-step bg-primary p-3">
            <i class="material-icons text-white text-sm opacity-10"
              >inventory_2</i
            >
          </span>
          <div class="timeline-content pt-1">
            <h6
              class="mb-0 text-sm text-dark font-weight-bold"
              :class="darkMode ? 'text-white' : ''"
            >
              New message unread
            </h6>
            <p class="mt-1 mb-0 text-xs text-secondary">16 DEC</p>
            <p class="mt-3 mb-2 text-sm" :class="darkMode ? 'text-white' : ''">
              People care about how you see the world, how you think, what
              motivates you, what you’re struggling with or afraid of.
            </p>
          </div>
        </div>
        <div class="timeline-block">
          <span class="timeline-step bg-success p-3">
            <i class="material-icons text-white text-sm opacity-10">done</i>
          </span>
          <div class="timeline-content pt-1">
            <h6
              class="mb-0 text-sm text-dark font-weight-bold"
              :class="darkMode ? 'text-white' : ''"
            >
              Notifications unread
            </h6>
            <p class="mt-1 mb-0 text-xs text-secondary">15 DEC</p>
            <p class="mt-3 mb-2 text-sm" :class="darkMode ? 'text-white' : ''">
              People care about how you see the world, how you think, what
              motivates you, what you’re struggling with or afraid of.
            </p>
          </div>
        </div>
        <div class="timeline-block">
          <span class="timeline-step bg-info p-3">
            <i class="material-icons text-white text-sm opacity-10">mail</i>
          </span>
          <div class="timeline-content pt-1">
            <h6
              class="mb-0 text-sm text-dark font-weight-bold"
              :class="darkMode ? 'text-white' : ''"
            >
              New request
            </h6>
            <p class="mt-1 mb-0 text-xs text-secondary">14 DEC</p>
            <p class="mt-3 mb-2 text-sm" :class="darkMode ? 'text-white' : ''">
              People care about how you see the world, how you think, what
              motivates you, what you’re struggling with or afraid of.
            </p>
          </div>
        </div>
        <div class="timeline-block">
          <span class="timeline-step bg-dark p-3">
            <i class="material-icons text-white text-sm opacity-10"
              >sports_esports</i
            >
          </span>
          <div class="timeline-content pt-1">
            <h6
              class="mb-0 text-sm text-dark font-weight-bold"
              :class="darkMode ? 'text-white' : ''"
            >
              Controller issues
            </h6>
            <p class="mt-1 mb-0 text-xs text-secondary">13 DEC</p>
            <p class="mt-3 mb-2 text-sm" :class="darkMode ? 'text-white' : ''">
              People care about how you see the world, how you think, what
              motivates you, what you’re struggling with or afraid of.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "timeline-card",
  props: { darkMode: Boolean, title: String },
};
</script>
