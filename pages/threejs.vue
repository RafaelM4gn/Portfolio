<template>
  <div>
    <div id="canvas" />
  </div>
</template>

<script>
import * as THREE from 'three'
import { OrbitControls } from 'three/examples/jsm/controls/OrbitControls'
export default {
  name: 'HelloWorld',
  data () {
    return {
      background: 0x0080FF,
      alpha: 0,
      canvas: 'canvas',
      width: '25rem',
      height: '25rem'
    }
  },
  mounted () {
    this.init()
  },
  methods: {
    init: function () {
      const container = document.getElementById(this.canvas)
      container.style.width = this.width
      container.style.height = this.height

      this.renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true })
      this.renderer.setClearColor(this.background, this.alpha)
      this.renderer.setSize(container.clientWidth, container.clientHeight)
      container.appendChild(this.renderer.domElement)
      this.scene = new THREE.Scene()
      // console.log(container.clientWidth / container.clientHeight);
      this.camera = new THREE.PerspectiveCamera(
        75,
        container.clientWidth / container.clientHeight,
        0.01,
        10
      )

      this.camera.position.z = 0.29
      this.controls = new OrbitControls(this.camera, this.renderer.domElement)
      this.controls.enableZoom = false
      this.controls.enablePan = false
      this.controls.update()
      this.scene = new THREE.Scene()

      const geometry = new THREE.BoxGeometry(0.2, 0.2, 0.2)
      const material = new THREE.MeshNormalMaterial()

      this.mesh = new THREE.Mesh(geometry, material)
      this.scene.add(this.mesh)

      this.ani()
    },
    ani: function () {
      // console.log("estoy ejecutandome");
      requestAnimationFrame(this.ani)
      this.mesh.rotation.y += 0.01
      this.mesh.rotation.x += 0.02
      this.mesh.rotation.z += 0.03
      this.renderer.render(this.scene, this.camera)
    }
  }
}
</script>
