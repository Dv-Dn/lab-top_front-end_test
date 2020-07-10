<template>
	<div
		class="icon"
		v-html="require('!!html-loader!@/assets/icons/' + name + '.svg')"
	></div>
</template>

<script>
export default {
	props: ["name"],
	mounted() {
		this.$el.firstChild.removeAttribute("height");
		this.$el.firstChild.removeAttribute("width");
	},
};
</script>
