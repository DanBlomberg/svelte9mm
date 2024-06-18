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
  position={[10, 0, 0]} 
  zoom={15} 
  fov{100}  
  target={[0, 0, 0]}>

  <OrbitControls 
    autoRotate 
    enableDampening 
    autoRotateSpeed={6} 
  />


</T.PerspectiveCamera >


  <T.Group position = {[0, 1, 0]} scale={2}>
     <Gun>
      <GLTF></GLTF>
     </Gun>
  </T.Group>

