<template>
  <project-base :src="src"
    :demos="demos" />
</template>

<script>
  // The primary stuff
  import ProjectBase from '~/components/project/ProjectBase';
  import fileSrc from '~/assets/talks/dynamic-css/jsconfus18.slides';

  // Inline-Demo Components as needed
  import cssAwesome from '~/components/demos/cssAwesome';
  import cssChart from '~/components/demos/cssChart';
  import layoutFlow from '~/components/demos/layoutFlow';
  import hslTheme from '~/components/demos/hslTheme';

  export default {
    components: {
      ProjectBase,
    },
    data() {
      return {
        src: fileSrc,
        demos: {
          cssAwesome,
          cssChart,
          layoutFlow,
          hslTheme,
        }
      }
    },
  }
</script>

<style lang="scss">
@import '~/assets/scss/_vuefinder.scss';
</style>
