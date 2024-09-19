<script setup lang="ts">

import SiteContainer from "@/components/SiteContainer.vue";
import SiteList from "@/components/devTools/SiteList.vue";
import MusicPlatformsIconsList from "@/components/MusicPlatformsIconsList.vue";
import SiteLink from "@/components/devTools/SiteLink.vue";
import LogotypeIcon from "@/components/icons/LogotypeIcon.vue";
import {ref} from "vue";

const MENU_ITEMS = [
	[
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
	],
	[
		{
			link: '/styleGuide',
			name: 'Style Guide',
			isRouterLink: false,
		},
		{
			link: '/styleGuide',
			name: 'Instructions',
			isRouterLink: false,
		},
		{
			link: '/styleGuide',
			name: 'Changelog',
			isRouterLink: false,
		},
		{
			link: '/styleGuide',
			name: 'Credit',
			isRouterLink: false,
		},
		{
			link: '/styleGuide',
			name: 'Powered by Webflow',
			isRouterLink: false,
		},
		{
			link: '/styleGuide',
			name: 'Licenses',
			isRouterLink: false,
		},
	]
];

var isAlignContentColumn = ref(true);
</script>

<template>
	<footer class="base-footer">
		<SiteContainer class="base-footer_container">
			<div class="base-footer_container-logotype-block">
				<div>
					<LogotypeIcon/>
				</div>
				<div>

				</div>
			</div>
			<div class="base-footer__menu">
				<div
						v-for="menuColumn in MENU_ITEMS"
						class="base-footer__menu-lists"
				>
					<SiteList
							:isAlignContentColumn="isAlignContentColumn"
							class="base-footer__menu-list"
					>
						<li
								v-for="menuItem in menuColumn"
								class="base-footer__menu-list__item"
						>
							<SiteLink
									:path="menuItem.link"
									:isRouterLink="menuItem.isRouterLink"
							>
								{{ menuItem.name }}
							</SiteLink>
						</li>
					</SiteList>
				</div>
			</div>
			<MusicPlatformsIconsList/>
		</SiteContainer>
	</footer>
</template>

<style scoped lang="scss">
.base-footer {
	padding-top: 100px;
	padding-bottom: 127px;

	&_container {
		display: flex;
		gap: 16px;

		&-logotype-block {
			max-width: 447px;
			width: 100%;
		}
	}

	&__menu {
		display: flex;
		gap: 16px;

		&-lists {
			max-width: 222px;
			width: 100%;

			& li + li {
				margin-top: 10px;
			}
		}
	}
}
</style>