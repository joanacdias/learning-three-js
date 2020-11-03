<template lang="pug">
    .playground(ref="playground-container")
</template>

<script>
import * as Three from 'three'

export default {
    name: 'Playground',
    components: {
    },
    data() {
        return {
            camera: null,
            scene: null,
            renderer: null,
            mesh: null
        }
    },
    methods: {
        init() {
            let container = this.$refs["playground-container"];
            
            // Create the scene
            this.scene = new Three.Scene();
            this.scene.background = new Three.Color('skyblue');

            // Create and locate the camera
            this.camera = new Three.PerspectiveCamera(30, window.innerWidth / window.innerHeight, 1, 1000);
            this.camera.position.z = 5;

            // Create the renderer
            this.renderer = new Three.WebGLRenderer();
            this.renderer.setSize(window.innerWidth, window.innerHeight);
            this.renderer.render( this.scene, this.camera );

            container.appendChild(this.renderer.domElement);
        },
        animate() {

        },
    },
    mounted() {
        this.init();
        this.animate();
    }
}
</script>

<style lang="scss" scoped>

</style>