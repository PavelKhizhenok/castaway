<script lang="ts">
import {RouterLink} from "vue-router";

export default {
	name: 'SiteLink',
	components: {RouterLink},
	props: {
		path: {
			type: String,
			required: true,
		},
		isRouterLink: {
			type: Boolean,
			default: false
		}
	}
}
</script>

<template>
	<RouterLink
			:to="path"
			class="site-link"
			v-if="isRouterLink"
	>
		<slot></slot>
	</RouterLink>
	<a
			:href="path"
			class="site-link"
			v-else
	>
		<slot></slot>
	</a>
</template>

<style scoped lang="scss">
.site-link {
	text-decoration: none;
	color: #fff;
	font-size: 17px;
	font-weight: 400;
	line-height: 27px;
	font-family: 'DMSansFont', sans-serif;
	transition: color 0.3s ease;

	&:hover {
		color: #118DA8;
	}

	+ .site-link {
		margin-left: 40px;
	}
}

.active-site-link {
	color: #118DA8;
}
</style>