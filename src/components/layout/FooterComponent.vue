<template>
	<v-footer
		app
		dark
		dense
		height="100"
		elevation="0"
		:absolute="true"
		class="foolter d-flex flex-row align-center"
		:style="{ 'background-color': color }"
	>
		<v-container>
			<v-row
				v-if="!breakpoints.includes(breakpoint)"
				class="px-xl-16 px-lg-16 px-md-10 px-sm-10"
			>
				<v-col class="d-flex flex-row align-center">
					<strong class="white--text">
						&#169; {{ new Date().getFullYear() }} WillFly. All rights reserved.
					</strong>
				</v-col>

				<v-col class="d-flex flex-row justify-end">
					<v-btn
						text
						color="#A9AFBB"
						@click="redirect(link.path)"
						:key="index"
						v-for="(link, index) in links"
					>
						{{ link.name }}
					</v-btn>
				</v-col>
			</v-row>

			<v-row v-else class="d-flex flex-row align-center">
				<v-col>
					<p class="text-center">
						<strong class="white--text">
							&#169; {{ new Date().getFullYear() }} WillFly.
						</strong>
					</p>
				</v-col>
			</v-row>
		</v-container>
	</v-footer>
</template>

<script>
	export default {
		name: 'SystemFoolter',

		props: {
			color: {
				type: String,
				default: 'rgba(26, 26, 44, 0.9)',
			},
		},

		data() {
			return {
				breakpoints: ['sm', 'xs'],
				links: [
					{
						name: 'Termos de uso',
						path: 'https://willfly.com.br/termos-de-uso',
					},
					{
						name: 'Política de privacidade',
						path: 'https://willfly.com.br/politica-de-privacidade',
					},
				],
			}
		},

		computed: {
			breakpoint: function () {
				return this.$vuetify.breakpoint.name
			},
		},

		methods: {
			redirect(path) {
				window.open(path, '_blank')
			},
		},
	}
</script>

<style scoped>
	.foolter {
		margin-bottom: 118px;
		background: rgba(26, 26, 44, 0.7) !important;
	}
</style>
