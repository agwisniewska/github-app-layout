<template>
	<div class="single-issue">
		{{issue.title}}
		<div @click="$emit('star', true)">
			<IconBase
				:icon-color="issue.star ? '#000' : '#fff'">
				<IconStar></IconStar>
			</IconBase>
		</div>

	</div>
</template>

<script>
  import IconBase from "./icons/IconBase";
  import IconStar from "./icons/IconStar";

  export default {
    components: {IconBase, IconStar},
    props: {
      issue: {
        type: Object
      }
    }

  }
</script>

<style lang="scss"
			 scoped>
	.single-issue {
		display: flex;
		justify-content: space-between;
		align-items: center;
		border-radius: 5px;
		background-color: white;
		padding: 0.5rem;
		margin: 0.5rem;
		font-size: 14px;
		svg {
			cursor: pointer;
		}
	}
</style>
