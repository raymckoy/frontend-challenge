<template>
  <div class="relative px py-2 mt-2 ml-2 mb-2 mr-6 mb-20">
    <input
      id="searchBar"
      v-model="search"
      class="border-grey text-grey w-full pl-10 pt-3 pb-3 shadow"
      type="text"
      name="search"
      placeholder="Search"
    />
    <div class="absolute pin-t py-5 px-2 text-grey-light">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        width="16pt"
        height="16pt"
        viewBox="0 0 16 16"
        version="1.1"
      >
        <g id="surface1">
          <path
            style=" stroke:none;fill-rule:nonzero;fill:rgb(158,157,175);fill-opacity:1;"
            d="M 10.855469 7.429688 C 10.855469 6.328125 10.464844 5.386719 9.683594 4.601562 C 8.898438 3.820312 7.957031 3.429688 6.855469 3.429688 C 5.757812 3.429688 4.8125 3.820312 4.03125 4.601562 C 3.25 5.386719 2.855469 6.328125 2.855469 7.429688 C 2.855469 8.53125 3.25 9.472656 4.03125 10.253906 C 4.8125 11.039062 5.757812 11.429688 6.855469 11.429688 C 7.957031 11.429688 8.898438 11.039062 9.683594 10.253906 C 10.464844 9.472656 10.855469 8.53125 10.855469 7.429688 Z M 15.429688 14.855469 C 15.429688 15.167969 15.316406 15.433594 15.089844 15.660156 C 14.863281 15.886719 14.59375 16 14.285156 16 C 13.964844 16 13.695312 15.886719 13.480469 15.660156 L 10.417969 12.605469 C 9.355469 13.34375 8.167969 13.714844 6.855469 13.714844 C 6.007812 13.714844 5.191406 13.550781 4.414062 13.21875 C 3.636719 12.886719 2.96875 12.441406 2.40625 11.878906 C 1.84375 11.316406 1.398438 10.648438 1.066406 9.871094 C 0.738281 9.09375 0.570312 8.28125 0.570312 7.429688 C 0.570312 6.578125 0.738281 5.761719 1.066406 4.988281 C 1.398438 4.210938 1.84375 3.539062 2.40625 2.976562 C 2.96875 2.414062 3.636719 1.96875 4.414062 1.636719 C 5.191406 1.308594 6.007812 1.144531 6.855469 1.144531 C 7.707031 1.144531 8.523438 1.308594 9.300781 1.636719 C 10.074219 1.96875 10.746094 2.414062 11.308594 2.976562 C 11.871094 3.539062 12.316406 4.210938 12.648438 4.988281 C 12.976562 5.761719 13.144531 6.578125 13.144531 7.429688 C 13.144531 8.738281 12.773438 9.925781 12.035156 10.992188 L 15.097656 14.054688 C 15.320312 14.273438 15.429688 14.542969 15.429688 14.855469 Z M 15.429688 14.855469 "
          />
        </g>
      </svg>
    </div>
    <div class="absolute pin-t pin-r py-5 px-2 text-grey-light">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        width="16pt"
        height="16pt"
        viewBox="0 0 16 16"
        version="1.1"
      >
        <g id="surface1">
          <path
            style=" stroke:none;fill-rule:nonzero;fill:rgb(158,157,175);fill-opacity:1;"
            d="M 0.5 4 L 13.5 4 C 13.777344 4 14 3.777344 14 3.5 L 14 1.5 C 14 1.222656 13.777344 1 13.5 1 L 0.5 1 C 0.222656 1 0 1.222656 0 1.5 L 0 3.5 C 0 3.777344 0.222656 4 0.5 4 Z M 15.5 6.5 L 2.5 6.5 C 2.222656 6.5 2 6.722656 2 7 L 2 9 C 2 9.277344 2.222656 9.5 2.5 9.5 L 15.5 9.5 C 15.777344 9.5 16 9.277344 16 9 L 16 7 C 16 6.722656 15.777344 6.5 15.5 6.5 Z M 13.5 12 L 0.5 12 C 0.222656 12 0 12.222656 0 12.5 L 0 14.5 C 0 14.777344 0.222656 15 0.5 15 L 13.5 15 C 13.777344 15 14 14.777344 14 14.5 L 14 12.5 C 14 12.222656 13.777344 12 13.5 12 Z M 13.5 12 "
          />
        </g>
      </svg>
    </div>
  </div>
</template>

<script>
import { mapActions, mapGetters } from 'vuex';

export default {
  name: 'ExpensesExpense',

  data() {
    return {
      search: '',
    };
  },

  computed: {
    ...mapGetters(['page']),
  },

  watch: {
    search: {
      handler: function() {
        this.searchExpenses(this.search);
      },
    },
  },

  methods: {
    ...mapActions(['searchExpenses']),
  },
};
</script>
