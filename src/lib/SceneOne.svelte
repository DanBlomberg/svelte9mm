<script>
  import { OrbitControls, Text3DGeometry, Sky } from '@threlte/extras'
  import { T } from '@threlte/core'
</script>

<T.PerspectiveCamera
  makeDefault
  position={[8, -1, 2]}
  zoom={3}
  fov={120}
>
  <OrbitControls  autoRotate enableDampening/>

</T.PerspectiveCamera>

<Sky /> 

<T.Mesh position={[0, 0, 0]} >
  <T.SphereGeometry />
  <!-- <T.GridHelper /> -->
  <T.MeshStandardMaterial roughness={0} color={'gray'} metalness={1.0}/>
</T.Mesh>

<T.Mesh position={[-2, -3, 0]}>
  <Text3DGeometry 
    text={'DJBIV'}
    size={1}
    depth={1}/>
  <T.MeshStandardMaterial 
    roughness={0} 
    color={'purple'} 
    metalness={1.0}/>
</T.Mesh>
