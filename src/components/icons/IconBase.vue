<template>
	<svg xmlns="http://www.w3.org/2000/svg"
			 class="base-icon"
			 :width="width"
			 :height="height"
			 viewBox="0 0 18 18"
			 :aria-labelledby="iconName"
			 role="presentation">
		<g :fill="iconColor">
			<slot/>
		</g>
	</svg>
</template>




<script>
  export default {
    props: {
      iconName: {
        type: String,
        default: 'box'
      },
      width: {
        type: [Number, String],
        default: 18
      },
      height: {
        type: [Number, String],
        default: 18
      },
      iconColor: {
        type: String,
        default: '#fff'
      }
    }
  }
</script>
<style lang="scss" scoped>
	path {
		stroke: #e0e0e0;
		stroke-width: 1px;
		stroke-linejoin: round;
	}

	svg {
		overflow: visible !important;
	}

</style>
