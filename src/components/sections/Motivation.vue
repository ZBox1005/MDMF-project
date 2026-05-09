<script setup>
import FigureSection from './FigureSection.vue'
</script>

<template>
  <FigureSection
    title="Motivation"
    src="resources/motivation.png"
    alt="Intuition behind Patch Forensic Signature"
  >
    <template #caption>
      <div style="text-align: center;">
        <b>Intuition behind Patch Forensic Signature (PFS)</b>
      </div>
      <div style="text-align: left; margin-top: 6px;">
        <b>Left:</b> a real cat and a generated dog with plausible localized irregularities (highlighted).<br>
        <b>Middle:</b> global image-level detection aggregates a <b>semantic-dominant</b> representation, while PFS maps patch-wise representations into an <b>artifact-dominant</b> forensic space.<br>
        <b>Right:</b> Under a label-inversion stress test (real cats vs. generated dogs &rarr; real dogs vs. generated cats), global classifiers drop sharply, while PFS stays stable by projecting patches into an artifact-dominant space.
      </div>
    </template>
  </FigureSection>
</template>
