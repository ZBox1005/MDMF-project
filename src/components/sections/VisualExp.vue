<script setup>
import FigureSection from './FigureSection.vue'
</script>

<template>
  <FigureSection
    title="Where MDMF Looks"
    src="resources/visual_exp.png"
    alt="Grad-CAM visualization of localized forensic evidence"
  >
    <template #caption>
      <b>Grad-CAM overlays on real / generated pairs (warmer = fake).</b><br>
      The global baseline lights up the same semantically salient regions for both.<br>
      MDMF concentrates on localized artifact regions in fakes and stays diffuse on reals.
    </template>
  </FigureSection>
</template>
