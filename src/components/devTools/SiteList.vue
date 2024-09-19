<script lang="ts">
	export default {
		name: 'SiteList',
		props: {
			isAlignContentColumn: {
				type: Boolean,
				default: false
			}
		}
	}
</script>

<template>
	<ul
			class="site-list"
			:class="{ 'site-list-column': isAlignContentColumn }"
	>
		<slot></slot>
	</ul>
</template>

<style scoped lang="scss">
.site-list {
	list-style: none;
	display: flex;
	justify-content: space-between;
	padding: 0;

	&-column {
		flex-direction: column;
	}
}
</style>