<template>
	<div class="title" v-scrollanimation>
		<div class="title__symbol-block">
			<span class="title__symbol"></span>
		</div>
		<h2 class="title__h2">{{ value }}</h2>
	</div></template
>
<script>
export default {
	props: {
		value: String,
	},
};
</script>
