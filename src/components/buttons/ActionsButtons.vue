<!-- <template>
		<div
			:style="this.buttonCollor()"
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
			buttonCollor() {
				const collorsByType = {
					help: this.setCustomStyles({ "#39CC33", "#48A728" }),
					give: this.setCustomStyles({ "#FF4D54", "#D6151D" }),
					disabled: this.setCustomStyles({ "#E5E5E5", "#D9D9D9" }),
					help: this.setCustomStyles({ "#00B1F2", "#009AD3" }),
				}

				if (!this.typeButton in collorsByType) {
					return
				}

				return collorsByType[this.typeButton]
			},

			setCustomStyles({color, shadowColor}) {
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
	div {
		background-color: white;
	}
</style> -->