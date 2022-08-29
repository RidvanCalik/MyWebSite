<template>

  <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" :v-if="{ theme== 'light' }">
    <path
      d="M15 4a1 1 0 1 0 0 2V4zm0 11v-1a1 1 0 0 0-1 1h1zm0 4l-.707.707A1 1 0 0 0 16 19h-1zm-4-4l.707-.707A1 1 0 0 0 11 14v1zm-4.707-1.293a1 1 0 0 0-1.414 1.414l1.414-1.414zm-.707.707l-.707-.707.707.707zM9 11v-1a1 1 0 0 0-.707.293L9 11zm-4 0h1a1 1 0 0 0-1-1v1zm0 4H4a1 1 0 0 0 1.707.707L5 15zm10-9h2V4h-2v2zm2 0a1 1 0 0 1 1 1h2a3 3 0 0 0-3-3v2zm1 1v6h2V7h-2zm0 6a1 1 0 0 1-1 1v2a3 3 0 0 0 3-3h-2zm-1 1h-2v2h2v-2zm-3 1v4h2v-4h-2zm1.707 3.293l-4-4-1.414 1.414 4 4 1.414-1.414zM11 14H7v2h4v-2zm-4 0c-.276 0-.525-.111-.707-.293l-1.414 1.414C5.42 15.663 6.172 16 7 16v-2zm-.707 1.121l3.414-3.414-1.414-1.414-3.414 3.414 1.414 1.414zM9 12h4v-2H9v2zm4 0a3 3 0 0 0 3-3h-2a1 1 0 0 1-1 1v2zm3-3V3h-2v6h2zm0-6a3 3 0 0 0-3-3v2a1 1 0 0 1 1 1h2zm-3-3H3v2h10V0zM3 0a3 3 0 0 0-3 3h2a1 1 0 0 1 1-1V0zM0 3v6h2V3H0zm0 6a3 3 0 0 0 3 3v-2a1 1 0 0 1-1-1H0zm3 3h2v-2H3v2zm1-1v4h2v-4H4zm1.707 4.707l.586-.586-1.414-1.414-.586.586 1.414 1.414z" />
  </svg>
  <svg id="Layer_1" data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 96.19 41.68">
    <defs>
      <style>
        .cls-1 {
          fill: #1d2b3f;
          stroke: #1d1d1b;
        }

        .cls-1,
        .cls-2,
        .cls-3,
        .cls-4,
        .cls-5 {
          stroke-miterlimit: 10;
        }

        .cls-1,
        .cls-2,
        .cls-3,
        .cls-4 {
          stroke-width: 3px;
        }

        .cls-2 {
          fill: #c6c6c6;
          stroke: #c6c6c6;
        }

        .cls-3 {
          fill: #9d9d9c;
          stroke: #9d9d9c;
        }

        .cls-4,
        .cls-5 {
          fill: #fff;
          stroke: #fff;
        }

        .cls-5 {
          stroke-width: 2px;
        }
      </style>
    </defs>
    <rect class="cls-1" x="1.5" y="1.5" width="93.19" height="38.68" rx="19.34" />
    <circle class="cls-2" cx="21.22" cy="20.84" r="15.57" />
    <circle class="cls-3" cx="14.8" cy="22.35" r="3.49" />
    <circle class="cls-3" cx="27.65" cy="26.1" r="1.15" />
    <circle class="cls-3" cx="29.63" cy="16.14" r="0.49" />
    <polygon class="cls-4"
      points="58.12 28.9 57.13 27.09 55.31 26.1 57.13 25.1 58.12 23.29 59.11 25.1 60.93 26.1 59.11 27.09 58.12 28.9" />
    <polygon class="cls-4"
      points="74.27 19.2 74.03 18.78 73.61 18.54 74.03 18.31 74.27 17.89 74.5 18.31 74.92 18.54 74.5 18.78 74.27 19.2" />
    <polygon class="cls-5"
      points="64.79 13.78 64.74 13.68 64.64 13.63 64.74 13.57 64.79 13.47 64.85 13.57 64.95 13.63 64.85 13.68 64.79 13.78" />
  </svg>

</template>

<script>
const theme = defineProps(['theme'])
</script>
