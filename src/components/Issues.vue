<template>
	<div class="issues">
		<template v-for="(issue, key) in issues">
			<span class="issues__date"> {{key}} </span>
			<template v-for="singleIssue in issue">
				<SingleIssue @star="updateIssue(key, singleIssue.id)"
										 :issue="singleIssue">
				</SingleIssue>
			</template>
		</template>
	</div>
</template>

<script>
  import SingleIssue from "./SingleIssue";

  export default {
    name: "GithubIssues",
    components: {SingleIssue},
    data: function () {
      return {
        issues: {
          "19-07-2016": [
            {
              id: 1,
              title: "Page changes",
              star: true,
            }, {
            id: 2,
              title: "Review of last issues",
              star: true,
            }],
          "18-07-2016": [{
            id: 1,
            title: "Visual UI Update Review",
            star: false,
          }, {
            id: 2,
            title: "Sidebar Changes",
            star: false,

          }],
          "15-07-2016": [{
            id: 1,
            title: "Crash update",
            star: false,
          }, {
            id: 2,
            title: "Page visual UI Update Review",
            star: true,
          }, {
            id: 3,
            title: "Sidebar Update",
            star: false,
          }],
          "14-07-2016": [{
            id: 1,
            title: "Crash issue",
            star: true,
          }, {
            id: 2,
            title: "Visual Update & Crash resolve",
            star: true
          }]
        }
      }
    },
    methods: {
      updateIssue: function (key, id) {
        console.error('update', key, id);
        const issues = [...this.issues[key].map(result => {
          if (result.id === id) {
            result.star = !result.star
          }
        })];
        console.log(issues);
      }
    }
  }
</script>

<style lang="scss"
			 scoped>
	.issues {
		padding: 0.5rem;
		&__date {
			font-size: 12px;
			color: darkgray;
		}

	}

</style>