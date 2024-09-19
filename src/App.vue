<script setup lang="ts">
import { RouterView } from 'vue-router'
import BaseHeader from "@/components/headers/BaseHeader.vue";
import BaseFooter from "@/components/footers/BaseFooter.vue";
</script>

<template>
	<BaseHeader/>
	<main>
		<RouterView/>
	</main>
	<BaseFooter/>
</template>

<style scoped>

</style>
