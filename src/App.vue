<script setup lang="ts">
import DataSetup from './components/DataSetup.vue';
import DataSetupFallack from './components/DataSetupFallack.vue';
</script>

<template>
  <Suspense>
    <template #default>
      <DataSetup />
    </template>
    <template #fallback>  <DataSetupFallack /></template>
  </Suspense>
</template>
