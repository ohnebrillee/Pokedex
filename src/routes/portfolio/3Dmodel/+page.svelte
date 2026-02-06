<script >
	import { onMount } from 'svelte';
    import * as THREE from 'three';

    onMount(() =>{
        const scene = new THREE.Scene();
        const camera = new THREE.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 0.1, 1000 );

        const renderer = new THREE.WebGLRenderer();
        renderer.setSize( window.innerWidth, window.innerHeight );
        renderer.setAnimationLoop( animate );
        document.body.appendChild( renderer.domElement );

        const geometry = new THREE.BoxGeometry( 1, 1, 1 );
            const material = new THREE.MeshPhongMaterial({
      color: 0xFFFFFF,    // red (can also use a CSS color string here)
      flatShading: true,
    });
        const cube = new THREE.Mesh( geometry, material );
                const color = 0xAAAAAA;
    const intensity = 3;
    const light = new THREE.DirectionalLight(color, intensity);
    light.position.set(0, 10, 0);
    light.target.position.set(5, 0, 0);
    scene.add(light);
    scene.add(light.target);

    const light2 = new THREE.DirectionalLight(color, intensity);
    light2.position.set(0, -10, 5);
    light2.target.position.set(5, 0, 0);
    scene.add(light2);
    scene.add(light2.target);
        scene.add( cube );

        camera.position.z = 5;

        function animate() {

        cube.rotation.x += 0.01;
        cube.rotation.y += 0.01;

        renderer.render( scene, camera );

        }
    })

    
</script>