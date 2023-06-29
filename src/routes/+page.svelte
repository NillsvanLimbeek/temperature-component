<script lang="ts">
	import Temperature from '../components/Temperature.svelte';

	let height: number = 200;
	let topDegrees: number = 90;
	let bottomDegrees: number = 45;
</script>

<div class="wrapper">
	<Temperature {height} {topDegrees} {bottomDegrees} />

	<div class="inputs">
		<div class="input">
			<label for="height">Height</label>
			<input type="number" name="height" bind:value={height} />
		</div>

		<div class="input">
			<label for="top-degrees">Top Degrees</label>
			<input type="number" name="top-degrees" bind:value={topDegrees} />
		</div>

		<div class="input">
			<label for="bottom-degrees">Bottom Degrees</label>
			<input type="number" name="bottom-degrees" bind:value={bottomDegrees} />
		</div>
	</div>
</div>

<style lang="scss">
	.wrapper {
		height: 100vh;
		width: 100vw;
		background-color: #1e1f22;

		display: flex;
		justify-content: center;
		align-items: center;
	}

	.inputs {
		margin-left: 50px;
	}

	.input {
		display: flex;
		flex-direction: column;
		margin-bottom: 15px;

		& label {
			color: white;
		}
	}
</style>
