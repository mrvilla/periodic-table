<template>
  <div class="chemical-elements">
    <div
      :class="[
        'chemical-element__wrapper',
        'prd' + chemical.row + 'gp' + chemical.column
      ]"
      v-for="(chemical, index) in periodicList"
      :key="index"
    >
      <i class="chemical-element__atomic-number">{{ chemical.atomicNumber }}</i>
      <span class="chemical-element__symbol">{{ chemical.symbol }}</span>
      <span class="chemical-element__name">{{ chemical.name }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "chemical-elements",
  props: ["periodicList"]
};
</script>
