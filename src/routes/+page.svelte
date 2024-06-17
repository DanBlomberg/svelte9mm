<script lang = "ts">
	/*
	 * Watch the video that corresponds to this code on YouTube!
	 * https://youtu.be/dnclxsoRO_E
	*/

	import {
		Canvas
	} from '@threlte/core';

	import SceneOne from '$lib/SceneOne.svelte';
	import SceneTwo from '$lib/SceneTwo.svelte';
	import SceneThree from '$lib/SceneThree.svelte';

</script>

<section>
	<h2>Scene One</h2>

	<div class="canvas-wrapper-sphere">
		<Canvas>
			<SceneOne />
		</Canvas>
	</div>


</section>

<!--
<section>
	<h2>Scene Two</h2>

	<div class="canvas-wrapper-text">
		<Canvas>
			<SceneTwo />
		</Canvas>
	</div>
</section>
-->

<section>
	<h2>Langdon Arms 9mm</h2>

	<div class="canvas-wrapper-gltf">
		<Canvas>
			<SceneThree />
		</Canvas>
	</div>
</section>

<style>
	.canvas-wrapper-sphere {
		position: relative;
		height: 300px;
		width: 1000px;
	}
	.canvas-wrapper-text {
		position: relative;
		height: 300px;
		width: 1000px;
	}
	.canvas-wrapper-gltf {
		position: relative;
		height: 1000px;
		width: 1000px;
    border: 2px;
	}
</style>
