<template>
  <div class="action-buttons">
		<div v-for="button in actionButtons" :key="button.color">
			<ActionButton :button="button"></ActionButton>
		</div>
  </div>
</template>

<script>
import ActionButton from "./ActionButton";
export default {
  name: "ActionButtons",
  components: {ActionButton},
  data: function() {
    return {
      actionButtons: [
        {
          color: "red",
          type: "CLOSE"
        },
        {
          color: "green",
          type: "MAXIMIZE"
        },
        {
          color: "yellow",
          type: "MINIMIZE"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
	.action-buttons {
		display: flex;
		align-items: center;
		padding: 1rem;
	}

</style>
