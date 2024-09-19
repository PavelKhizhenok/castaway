<script setup lang="ts">

import LogotypeIcon from "@/components/icons/LogotypeIcon.vue";
import SiteLink from "@/components/devTools/SiteLink.vue";

const SITE_ROUTES = [
	{
		link: '/',
		name: 'Home',
		isRouterLink: true,
	},
	{
		link: '/episodes',
		name: 'Episodes',
		isRouterLink: true,
	},
	{
		link: '/about',
		name: 'About',
		isRouterLink: true,
	},
	{
		link: '/contact',
		name: 'Contact',
		isRouterLink: true,
	},
];
</script>

<template>
	<header class="base-header">
		<div class="base-header_wrapper">
			<div class="base-header_wrapper__item">
				<LogotypeIcon/>
			</div>
			<nav class="base-header_wrapper__item">
				<SiteLink
						v-for="route in SITE_ROUTES"
						:path='route.link'
						:isRouterLink="route.isRouterLink"
				>
					{{ route.name }}
				</SiteLink>
			</nav>
		</div>
	</header>
</template>

<style scoped lang="scss">
.base-header {
	position: fixed;
	top: 0;
	left: 0;
	right: 0;
	max-height: 119px;
	z-index: 25;
	background-color: #191919;
	border-bottom: 1px #f2f2f2 solid;
	width: 100%;
	display: flex;
	justify-content: center;

	&_wrapper {
		margin: 24px 0;
		max-width: 1440px;
		width: 100%;
		display: flex;
		justify-content: space-between;
		padding: 20px 50px;

		&_item {
			display: flex;
			align-items: center;
		}
	}
}
</style>