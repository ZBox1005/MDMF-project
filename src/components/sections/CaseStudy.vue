<script setup>
import FigureSection from './FigureSection.vue'
</script>

<template>
  <FigureSection
    title="Generalizes to Unseen Video Generators"
    src="resources/opensora-case.png"
    alt="OpenSora case study"
  >
    <template #caption>
      <b>Stress-test on OpenSora frames (unseen at training).</b><br>
      32,750 frames from 3,275 generated videos vs. matched MSR-VTT real frames.<br>
      Competitive baselines collapse under the distribution shift; MDMF holds.
    </template>
  </FigureSection>
</template>
