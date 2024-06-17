<script>
  import { OrbitControls, Text3DGeometry, Sky,  } from '@threlte/extras'
  import { T } from '@threlte/core'
</script>

<T.PerspectiveCamera
  makeDefault
  position={[20, 2, 15]}
  zoom={8}
  fov={120}
  lookat={20, 0, 0}
>
  <OrbitControls />

</T.PerspectiveCamera>

<Sky /> 

<T.Mesh >
  <Text3DGeometry 
    text={'Aafedt'}
    size={4}
    depth={1}/>

  <T.GridHelper />

  <T.MeshStandardMaterial 
    roughness={0} 
    color={'brown'} 
    metalness={1.0}/>
</T.Mesh>
