<template>
	<article class="service-item" v-scrollanimation>
		<Icon :name="icon"></Icon>
		<h3 class="service-item__title">{{ title }}</h3>
		<p class="service-item__text">
			{{ text }}
		</p>
	</article>
</template>
<script>
import Icon from "@/components/Icon";
export default {
	components: {
		Icon,
	},
	props: {
		text: String,
		title: String,
		icon: String,
	},
};
</script>
