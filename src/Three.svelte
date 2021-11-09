<script>
  import {
    AmbientLight,
    BoxBufferGeometry,
    Canvas,
    DirectionalLight,
    Mesh,
    MeshStandardMaterial,
    PerspectiveCamera,
    Scene,
    WebGLRenderer
  } from "svelthree";

  let cubeGeometry = new BoxBufferGeometry(1, 1, 1);
  let cubeMaterial = new MeshStandardMaterial();
</script>

<main>
  <Canvas let:sti w={100} h={100}>
    <Scene {sti} let:scene id="scene1" props={{ background: 0xedf2f7 }}>
      <PerspectiveCamera {scene} id="cam1" pos={[0, 0, 3]} lookAt={[0, 0, 0]} />
      <AmbientLight {scene} intensity={1.25} />
      <DirectionalLight {scene} pos={[3, 3, 3]} />
      <Mesh
        {scene}
        geometry={cubeGeometry}
        material={cubeMaterial}
        mat={{ roughness: 0.5, metalness: 0.5, color: 0xff3e00 }}
        pos={[0, 0, 0]}
        rot={[0.5, 0.6, 0]}
        scale={[1, 1, 1]} />
    </Scene>
    <WebGLRenderer
      {sti}
      sceneId="scene1"
      camId="cam1"
      config={{ antialias: true, alpha: false }} />
  </Canvas>
</main>

<style>
  main {
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    margin: 0;
    background-color: red;
  }
</style>
