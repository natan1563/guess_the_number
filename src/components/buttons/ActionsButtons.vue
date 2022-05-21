<template>
		<div
			:style="{width: widthButton + 'px', height: heightButton + 'px'}"
		>
			<slot name="icon"></slot>
			<slot name="text"></slot>
		</div>
</template> 

<script>
	export default {
		props: {
			typeButton: {
				type: String,
				required: true
			},
			widthButton: {
				type: Number,
				required: false,
				default: 143
			},
			heightButton: {
				type: Number,
				required: false,
				default: 31
			}
		},

		data() {
			return {
				teste: "Sergio"
			}
		},

		methods: {
			
		},
	}
</script>

<style scoped>
	div {
		background-color: white;
	}
</style>