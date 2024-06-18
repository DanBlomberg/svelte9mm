<script lang = "ts">
	/*
	 * My first project learning the basics of threlte
	*/

	import SceneOne from '$lib/SceneOne.svelte';
	import SceneTwo from '$lib/SceneTwo.svelte';
	import SceneThree from '$lib/SceneThree.svelte';
	import SceneFour from '$lib/SceneFour.svelte';

  import { Canvas, T } from '@threlte/core'
  import { Grid, Gizmo } from '@threlte/extras'
  import { PlaneGeometry } from 'three'

</script>

<section>
	<h2>Scene One</h2>

	<div class="canvas-wrapper-sphere">
		<Canvas>
			<SceneOne />
		</Canvas>
	</div>


</section>

<section>
	<h2>Scene Two</h2>

	<div class="canvas-wrapper-text">
		<Canvas>
			<SceneTwo />
		</Canvas>
	</div>
</section>

<section>
	<h2>Scene 3 Langdon Arms 9mm</h2>

	<div class="canvas-wrapper-gltf">
		<Canvas>
			<SceneThree />
		</Canvas>
	</div>
</section>

<section>
	<h2>Scene 4 Grid</h2>

	<div class="canvas-wrapper-grid">
		<Canvas>
			<SceneFour />
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
		height: 400px;
		width: 1200px;
    border: 2px;
	}
	.canvas-wrapper-grid {
		position: relative;
		height: 1000px;
		width: 1000px;
    border: 2px;
	}
</style>
