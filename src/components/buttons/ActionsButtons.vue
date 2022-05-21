<template>
		<div
			class="button-default"
			:style="this.buttonStyles()"
		>
			<slot name="icon" class="icon-default"></slot>
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
				default: 130
			},
			heightButton: {
				type: Number,
				required: false,
				default: 40
			}
		},

		data() {
			return {
				teste: "Sergio"
			}
		},

		methods: {
			buttonStyles() {
				const collorsByType = {
					help: this.setCustomStyles("#39CC33", "#48A728"),
					give: this.setCustomStyles("#FF4D54", "#D6151D"),
					disabled: this.setCustomStyles("#E5E5E5", "#D9D9D9"),
					again: this.setCustomStyles("#00B1F2", "#009AD3"),
				}
				
				console.log(collorsByType[this.typeButton])

				if (this.typeButton in collorsByType) {
					return collorsByType[this.typeButton]
				}

				return
			},

			setCustomStyles(color, shadowColor) {
				return {
					backgroundColor: color,
					border: `2px solid ${color}`,
					boxShadow: `0px 3px 0px ${shadowColor}`,
					borderRadius: "12px",
					width: `${this.widthButton}px`,
					height: `${this.heightButton}px`
				}
			}
		},
	}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@700&display=swap');

.button-default {
	display: flex;
	justify-content: space-around;
	align-items: center;
	font-family: Inter;
	font-weight: 700;
	font-size: 18px;
	padding: 0px 5px;
	color: #FFFFFF;
}
</style>
