<script setup>
import FigureSection from './FigureSection.vue'
</script>

<template>
  <FigureSection
    title="Further Analysis"
    src="resources/further_analysis.png"
    alt="Ablation studies"
  >
    <template #caption>
      <div style="text-align: left;">
        <b>(a)</b> Patch size <i>W</i>: detection peaks at intermediate granularity.<br>
        <b>(b)</b> Backbone scaling: MDMF improves from ViT-S/14 to ViT-G/14, while F-ConV degrades on the largest.<br>
        <b>(c)</b> Post-processing (JPEG / blur / noise): MDMF degrades far more gently than F-ConV.<br>
        <b>(d)</b> Hard voting needs two coupled thresholds and swings widely; distributional MMD over PFS stays consistently higher.
      </div>
    </template>
  </FigureSection>
</template>
