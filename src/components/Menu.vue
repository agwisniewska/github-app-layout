<template>
	<ul class="menu">
		<li v-for="item in menuItems"
				:key="item.id"
				:tabindex="item.id"
				class="menu__menu-element">
			<template v-if="item.title === 'All'">
				<IconBase
					icon-color="#fff">
					<IconStar></IconStar>
				</IconBase>
			</template>
			<template v-else-if="item.title === 'Open'">
				<IconBase
					icon-color="#fff">
					<IconStar></IconStar>
				</IconBase>
			</template>
			<template v-else>
				<IconBase
					icon-color="#fff">
					<IconStar></IconStar>
				</IconBase>
			</template>
			{{ item.title }}

			<span> {{ item.counter }} </span>
		</li>
	</ul>
</template>

<script>
  import IconBase from "./icons/IconBase";
  import IconGithub from "./icons/IconGithub";
  import IconOpenIssue from "./icons/IconOpenIssue";
  import IconClosedIssue from "./icons/IconClosedIssue";
  import IconStar from "./icons/IconStar";

  export default {
    name: "Menu",
    components: {IconBase, IconStar, IconGithub, IconOpenIssue, IconClosedIssue},
    data: function () {
      return {
        menuItems: [
          {
            id: 1,
            iconUrl: "../assets/icon-github.svg",
            title: "All",
            counter: 12
          },
          {
            id: 2,
            iconUrl: "../assets/icon-open-issue.svg",
            title: "Open",
            counter: 4
          },
          {
            id: 3,
            iconUrl: "../assets/icon-closed-issue.svg",
            title: "Close",
            counter: 8
          }
        ]
      };
    }
  };
</script>

<style lang="scss"
			 scoped>
	.menu {
		margin: 0;
		padding: 0;
		&__menu-element {
			display: flex;
			justify-content: space-between;
			align-items: center;
			list-style-type: none;
			padding: 1rem;
			font-size: 14px;
			cursor: pointer;
			i {
				background-size: 20px 30px;
			}
			&:hover, &:active, &:focus {
				background-color: #433E57;
				outline: none;
			}
			.menu-element {
				&__icon {
					margin-right: 5px;
				}
			}
		}
	}
</style>
