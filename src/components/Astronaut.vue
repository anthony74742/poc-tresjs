<script setup lang="ts">
import { ref } from 'vue'
import { useAnimations, useGLTF } from '@tresjs/cientos'

// const { scene: model, animations } = await useGLTF(
//   '../assets/Car.glb',
// )
const { scene: model, animations } = await useGLTF(
  '/assets/astronaut/scene.gltf',
)

const { actions } = useAnimations(animations, model)

console.log(actions)

const currentAction = ref(actions.wave)

currentAction.value.play()

</script>

<template>
  <primitive :object="model" />
</template>