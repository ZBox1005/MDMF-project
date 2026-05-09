<script setup>
import FigureSection from './FigureSection.vue'
</script>

<template>
  <FigureSection
    title="Framework"
    src="resources/framework.png"
    alt="MDMF framework overview"
  >
    <template #caption>
      <b>Patch Forensic Signature + MMD two-sample test.</b><br>
      A frozen DINOv2 ViT-L/14 produces patch tokens, while a learnable projection &phi;<sub>&theta;</sub>
      reparameterizes them into the forensic latent space (PFS). MDMF then measures MMD between the
      test image's PFS set and a real-image reference.
    </template>
  </FigureSection>
</template>
