<template>
	<div id="app">
		<section class="service">
			<div class="wrap">
				<Title class="service__title" value="something AS A SERVICE" />
				<div class="service__grid">
					<ServiceItem
						:key="i"
						v-for="(a, i) in serviceItems"
						:title="a.title"
						:icon="a.icon"
						:text="a.text"
					/>
				</div>
			</div>
		</section>
		<section class="lightpaper">
			<div class="lightpaper__before spacer"></div>
			<div class="lightpaper__main">
				<div class="lightpaper__img-block" v-scrollanimation>
					<img class="lightpaper__img" src="@/assets/Broshure@1X.png" alt="" />
				</div>
				<article class="lightpaper__content" v-scrollanimation>
					<h3 class="lightpaper__title">OUR LIGHTPAPER</h3>
					<p class="lightpaper__text">
						Team is currently working on all its documents.
					</p>
				</article>
				<Btn class="lightpaper__btn">download</Btn>
			</div>
			<div class="spacer"></div>
		</section>
		<section class="product">
			<div class="wrap">
				<Title value="something search product" class="product__title" />
			</div>
		</section>
	</div>
</template>

<script>
import ServiceItem from "@/components/ServiceItem";
import Title from "@/components/Title";
import Btn from "@/components/Btn";
export default {
	name: "App",
	components: { ServiceItem, Btn, Title },
	data: () => ({
		serviceItems: [
			{
				icon: "icon_icon 01",
				title: "Digital identity",
				text:
					"Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
			},
			{
				icon: "icon_icon 02",
				title: "Trust Score",
				text:
					"Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
			},
			{
				icon: "icon_icon 03",
				title: "Search engine",
				text:
					"Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
			},
			{
				icon: "icon_icon 04",
				title: "User friendly",
				text:
					"Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
			},
		],
	}),
};
</script>

<style lang="scss">
@import "@/scss/main";
</style>
