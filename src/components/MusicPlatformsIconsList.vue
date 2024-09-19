<script setup lang="ts">

import SiteList from "@/components/devTools/SiteList.vue";
import PinterestIcon from "@/components/icons/PinterestIcon.vue";
import TowerIcon from "@/components/icons/TowerIcon.vue";
import PerplePeopleIcon from "@/components/icons/PerplePeopleIcon.vue";
import SpotifyIcon from "@/components/icons/SpotifyIcon.vue";
import CloudIcon from "@/components/icons/CloudIcon.vue";
import SiteLink from "@/components/devTools/SiteLink.vue";

const iconsArray = [
	{
		icon: SpotifyIcon,
		link: "https://spotifyjs.com",
	},
	{
		icon: PinterestIcon,
		link: "https://PinterestIcon.com",
	},
	{
		icon: CloudIcon,
		link: "https://CloudIcon.com",
	},
	{
		icon: PerplePeopleIcon,
		link: "https://PerplePeopleIcon.com",
	},
	{
		icon: TowerIcon,
		link: "https://.com",
	},
];
</script>

<template>
	<div>
		<SiteList>
			<li v-for="iconName in iconsArray" class="listen__icons-list__item">
				<SiteLink :path="iconName.link">
					<component :key="String(iconName)" :is="iconName.icon"/>
				</SiteLink>
			</li>
		</SiteList>
	</div>
</template>

<style scoped>
.listen__icons-list__item + .listen__icons-list__item {
	margin-left: 17px;
}
</style>