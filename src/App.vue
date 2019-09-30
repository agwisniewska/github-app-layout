<template>
			<GithubApp/>
</template>

<script>
  import GithubApp from './components/GithubApp.vue'

  export default {
    name: 'app',
    components: {
      GithubApp
    }
  }
</script>

<style lang="scss">
	@import url('https://fonts.googleapis.com/css?family=Open+Sans&display=swap');

	body {
		font-family: "Open Sans", sans-serif;
		height: 100vh;
		background: url("./assets/background.jpg") no-repeat center center fixed;
		background-size: cover;
		display: flex;
		justify-content: center;
		align-items: center;


	}
</style>
