<script setup lang="ts">
import SiteContainer from "@/components/SiteContainer.vue";
import MusicPlatformsIconsList from "@/components/MusicPlatformsIconsList.vue";
</script>

<template>
	<SiteContainer>
		<div class="home-view">
			<div class="home-view_wrapper">
				<div class="home-view_wrapper_image">
					<img src="@/assets/images/home/nigger.png" alt="nigger"/>
				</div>
				<div class="home-view_wrapper_content">
					<div class="wrapper_content_text">
						Take your podcast to the <span class="wrapper_content_text_line">next</span> level
					</div>
					<div class="wrapper_content_listen">
						<h4 class="wrapper_content_listen__title">Listen on</h4>
						<MusicPlatformsIconsList/>
					</div>
				</div>
			</div>
		</div>
	</SiteContainer>
</template>

<style scoped lang="scss">
.home-view {
	padding-top: 119px;

	&_wrapper {
		padding: 40px 0;
		display: flex;
		flex: 1 1;

		&_image {
			border-radius: 12px;
		}

		&_content {
			display: flex;
			justify-content: center;
			align-items: flex-start;
			padding: 194px 40px 153px 40px;
			flex-direction: column;
		}

		& > div {
			width: 100%;
		}
	}
}

.wrapper_content {
	&_text {
		font-size: 70px;
		color: #fff;
		max-width: 526px;
		margin-bottom: 74px;

		&_line {
			position: relative;

			&:after {
				content: "";
				background: url("@/assets/images/home/textLine.svg") no-repeat bottom left;
				position: absolute;
				bottom: 0;
				left: 0;
				height: 100%;
				width: 100%;
			}
		}
	}

	&_listen {
		padding-left: 22px;
		
		&__title {
			color: #fff;
			margin-bottom: 16px;

		}
	}
}
</style>