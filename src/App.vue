<script setup lang="ts">
import { TresCanvas } from '@tresjs/core';
import { OrbitControls } from '@tresjs/cientos';
import Astronaut from './components/Astronaut.vue';
</script>

<template>
  <TresCanvas clear-color="#82DBC5" window-size>
    <TresPerspectiveCamera
      :position="[3, 3, 3]"
      :fov="100"
      :look-at="[0, 0, 0]"
    />
    <OrbitControls />
    <Suspense>
      <Astronaut />
    </Suspense>
    <TresAmbientLight :intensity="2" />
    <TresDirectionalLight cast-shadow :position="[0, 2, 0]" :intensity="1" />
  </TresCanvas>
</template>

<style>
html,
body {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
}
#app {
  height: 100%;
  width: 100%;
}
</style>