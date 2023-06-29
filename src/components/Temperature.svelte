<script lang="ts">
	export let height: number;
	export let topDegrees: number;
	export let bottomDegrees: number;
</script>

<div class="temperature" style="height: {height}px;">
	<div class="inner">
		<p class="top">{topDegrees}° F</p>
		<p class="bottom">{bottomDegrees}° F</p>
	</div>
</div>

<style lang="scss">
	.temperature {
		display: flex;
		justify-content: center;
		align-items: center;

		transition: height 0.5s ease-in-out;

		height: 200px;
		width: 60px;
		border-radius: 30px;
		background: linear-gradient(
			180deg,
			#ff0000 -24.77%,
			#f16211 -12.15%,
			#9747ff 48.57%,
			#2776e6 87.21%,
			#25d7fe 112.44%,
			#ffffff 126.64%
		);
	}

	.inner {
		height: calc(100% - 7.5px);
		width: calc(100% - 7.5px);

		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;

		border-radius: 30px;
		background-color: #1e1f22;

		& p {
			text-transform: uppercase;
			color: white;
		}
	}
</style>
