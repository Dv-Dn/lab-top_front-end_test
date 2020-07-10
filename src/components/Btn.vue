<template>
	<div class="button-block">
		<button class="button" v-on="$listeners" v-bind="$attrs">
			download
			<span class="button__inner">
				<span class="button__blobs">
					<span class="button__blob"></span>
					<span class="button__blob"></span>
					<span class="button__blob"></span>
					<span class="button__blob"></span>
				</span>
			</span>
		</button>
		<svg>
			<defs>
				<filter id="goo">
					<feGaussianBlur
						in="SourceGraphic"
						result="blur"
						stdDeviation="10"
					></feGaussianBlur>
					<feColorMatrix
						in="blur"
						mode="matrix"
						values="1 0 0 0 0 0 1 0 0 0 0 0 1 0 0 0 0 0 21 -7"
						result="goo"
					></feColorMatrix>
					<feBlend in2="goo" in="SourceGraphic" result="mix"></feBlend>
				</filter>
			</defs>
		</svg>
	</div>
</template>
