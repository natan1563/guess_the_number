<template class="pointer">
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
			}
		},

		methods: {
			buttonStyles() {
				const collorsByType = {
					default : this.setCustomStyles("#FFFFFF", "#BFBFBF", "#48A728"),
					defaultDisabled: this.setCustomStyles("#EFEFEF", "#BFBFBF", "#C4C4C4"),
					defaultHover: this.setCustomStyles("#FFFFFF", "#FFFFFF"),
					active: this.setCustomStyles("#DBF4FE", "#78D9FC", "#78D9FC"),
					activeDisabled: this.setCustomStyles("#DBF4FE", "#78D9FC", "#78D9FC"),
					activeHover: this.setCustomStyles("#DBF4FE", "#DBF4FE"),
					help: this.setCustomStyles("#39CC33", "#39CC33", "#48A728"),
					helpDisabled: this.setCustomStyles("#14BE0D", "#14BE0D", "#48A728"),
					helpHover: this.setCustomStyles("#39CC33", "#39CC33"),
					give: this.setCustomStyles("#FF4D54", "#FF4D54", "#D6151D"),
					giveDisabled: this.setCustomStyles("#E62D34", "#E52D34", "#D6151D"),
					giveHover: this.setCustomStyles("#FF4D54", "#FF4D54"),
					disabled: this.setCustomStyles("#E5E5E5", "#E5E5E5", "#D9D9D9"),
					again: this.setCustomStyles("#00B1F2", "#00B1F2", "#009AD3"),
					againDisabled: this.setCustomStyles("#03ABE9", "#03ABE9", "#009AD3"),
					againHover: this.setCustomStyles("#00B1F2", "#00B1F2"),
				}
				if (this.typeButton in collorsByType) {
					return collorsByType[this.typeButton]
				}

				return
			},

			setCustomStyles(color, borderColor, shadowColor = "") {
				return {
					backgroundColor: color,
					border: `2px solid ${borderColor}`,
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
	cursor: pointer;
}
</style>
