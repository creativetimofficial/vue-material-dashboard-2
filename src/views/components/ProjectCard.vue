<template>
  <div class="card">
    <div class="card-header pb-0">
      <div class="row">
        <div class="col-lg-6 col-7">
          <h6>{{ title }}</h6>
          <p class="text-sm mb-0" v-html="description"></p>
        </div>
        <div class="col-lg-6 col-5 my-auto text-end">
          <div class="dropdown float-lg-end pe-4">
            <a
              class="cursor-pointer"
              id="dropdownTable"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              <i class="fa fa-ellipsis-v text-secondary" aria-hidden="true"></i>
            </a>
            <ul
              class="dropdown-menu px-2 py-3 ms-sm-n4 ms-n5"
              aria-labelledby="dropdownTable"
              style=""
            >
              <li>
                <a class="dropdown-item border-radius-md" href="javascript:;">
                  Action
                </a>
              </li>
              <li>
                <a class="dropdown-item border-radius-md" href="javascript:;">
                  AnotherAction
                </a>
              </li>
              <li>
                <a class="dropdown-item border-radius-md" href="javascript:;">
                  SomethingElse
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div class="card-body px-0 pb-2">
      <div class="table-responsive">
        <table class="table align-items-center mb-0">
          <thead>
            <tr>
              <th
                v-for="(heading, index) of headers"
                :key="index"
                :class="[
                  index === 1 ? 'ps-2' : '',
                  index >= 2 ? 'text-center' : '',
                ]"
                class="text-uppercase text-secondary text-xxs font-weight-bolder opacity-7"
              >
                {{ heading }}
              </th>
            </tr>
          </thead>
          <tbody>
            <tr
              v-for="(
                {
                  logo,
                  title,
                  members,
                  budget,
                  progress: { percentage, color },
                },
                index
              ) of projects"
              :key="index"
            >
              <td>
                <div class="d-flex px-2 py-1">
                  <div>
                    <img :src="logo" class="avatar avatar-sm me-3" alt="Logo" />
                  </div>
                  <div class="d-flex flex-column justify-content-center">
                    <h6 class="mb-0 text-sm">{{ title }}</h6>
                  </div>
                </div>
              </td>
              <td>
                <div class="avatar-group mt-2">
                  <a
                    v-for="(member, index) of members"
                    :key="index"
                    href="javascript:;"
                    class="avatar avatar-xs rounded-circle"
                    data-bs-toggle="tooltip"
                    data-bs-placement="bottom"
                    title=""
                    data-bs-original-title=""
                  >
                    <img :src="member" alt="Team member" />
                  </a>
                </div>
              </td>
              <td class="align-middle text-center text-sm">
                <span class="text-xs font-weight-bold"> {{ budget }} </span>
              </td>
              <td class="align-middle d-flex justify-content-end">
                <div class="progress-wrapper w-75 mx-auto">
                  <div class="progress-info">
                    <div class="progress-percentage">
                      <span class="text-xs font-weight-bold"
                        >{{ percentage }}%
                      </span>
                    </div>
                  </div>
                  <div class="progress">
                    <div
                      class="progress-bar"
                      :class="`w-${percentage}  bg-gradient-${color}`"
                      role="progressbar"
                      :aria-valuenow="percentage"
                      aria-valuemin="0"
                      aria-valuemax="100"
                    ></div>
                  </div>
                </div>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "projectCard",
  props: {
    title: {
      type: String,
      default: "",
    },
    description: {
      type: String,
      default: "",
    },
    headers: {
      type: Array,
      required: true,
    },
    projects: {
      type: Array,
      required: true,
      logo: String,
      title: String,
      members: Array,
      budget: String,
      progress: {
        type: Object,
        percentage: Number,
        color: String,
      },
    },
  },
};
</script>
