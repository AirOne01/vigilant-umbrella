<script lang="ts">
  import * as T from "three";

  let camera: T.PerspectiveCamera, scene: T.Scene, renderer: T.WebGLRenderer;
  let geometry: T.BoxGeometry, material: T.MeshNormalMaterial, mesh: T.Mesh;

  init();

  function init() {
    camera = new T.PerspectiveCamera(
      70,
      window.innerWidth / window.innerHeight,
      0.01,
      10
    );
    camera.position.z = 1;

    scene = new T.Scene();

    geometry = new T.BoxGeometry(0.2, 0.2, 0.2);
    material = new T.MeshNormalMaterial();

    mesh = new T.Mesh(geometry, material);
    scene.add(mesh);

    renderer = new T.WebGLRenderer({ antialias: true });
    renderer.setSize(window.innerWidth, window.innerHeight);
    renderer.setAnimationLoop(animate);
    document.body.appendChild(renderer.domElement);
  }

  function animate(time) {
    mesh.rotation.x = time / 2000;
    mesh.rotation.y = time / 1000;

    renderer.render(scene, camera);
  }
</script>

<main class="canvas">
</main>

<style>
  @import "colors.css";

  main {
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    margin: 0;
    padding: 0;
    color: #7fdbff;
    overflow: hidden;
  }
</style>
