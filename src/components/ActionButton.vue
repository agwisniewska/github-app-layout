<template>
	<div class="action-button"
				:class="button.color"></div>
</template>

<script>
  export default {
    name: "ActionButton",
    props: {
      button: {
        type: Object
      }
    }
  }
</script>

<style lang="scss"
			 scoped>
	.action-button {
		width: 10px;
		height: 10px;
		border-radius: 50%;
		margin: 0 0.2rem;
	}
	.green {
		background-color: green;
	}
	.red {
		background-color: red;
	}

	.yellow {
		background-color: yellow;

	}

</style>