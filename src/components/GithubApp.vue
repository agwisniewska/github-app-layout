<template>
	<div class="github-app">

		<aside>
			<ActionButtons/>
			<Menu/>
		</aside>
		<main>
			<GithubIssues/>
		</main>
	</div>
</template>

<script>
  import GithubIssues from "./Issues";
  import ActionButtons from "./ActionButtons";
  import Menu from "./Menu";
  import IconBase from "./icons/IconBase";
  import IconGithub from "./icons/IconGithub";

  export default {
    name: "GithubApp",
    components: {IconBase, IconGithub, ActionButtons, GithubIssues, Menu}
  }
</script>

<style scoped
			 lang="scss">
	.github-app {
		background-color: #f5f5f5;
		width: 50%;
		height: 50%;
		border-radius: 15px;
		display: flex;

		aside {
			background-color: #29243D;
			border-top-left-radius: 15px;
			border-bottom-left-radius: 15px;
			color: #fff;
			width: 25%;
		}
		main {
			width: 75%;
			overflow: auto;
		}
	}

</style>