<script>
  import { Canvas } from '@threlte/core'
  import { T } from '@threlte/core'
  import { Mesh } from 'three'
  import { Grid, GLTF, OrbitControls, Sky} from '@threlte/extras'
  import Gun from '$lib/models/9MM.svelte'

</script>

<GLTF
  url='3DModel/9MM.gltf'
  interactive
  on:click={() => {
    console.log('User clicked!')
  }}
/>

<T.PerspectiveCamera 
  makeDefault 
  position={[.25, .25, .25]} 
  zoom={1} 
  fov{10}  
  target={[.25, .25, .25]}>

  <OrbitControls 
    enableDampening 
  />

</T.PerspectiveCamera >

<Sky />
<Grid />

<T.DirectionalLight />
<T.AmbientLight
  intensity={0.5}
/>

  <T.Group position = {[0, 0, 0]} scale={2}>
     <Gun>
      castShadow
      <GLTF></GLTF>
     </Gun>
  </T.Group>

